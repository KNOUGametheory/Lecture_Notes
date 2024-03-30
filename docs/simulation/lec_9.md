---
layout: default
title: 파이선으로 이해하는 협력
parent: simulation
nav_order: 9
has_children: false
permalink: /docs/simulation/
---

# 파이선으로 이해하는 협력

## 학습개요

죄수의 딜레마 게임에서, 여러 전략의 경쟁을 파이선으로 구현한다.

## 학습목표 

1.  필요에 따라 클래스를 만들 수 있다.

2.  죄수의 딜레마 게임을 파이선으로 만들 수 있다.

3.  죄수의 딜레마 게임에서 다양한 전략의 경쟁을 파이선으로 만들 수 있다.

## 주요 용어 

`*`와 `**`의 용례, `numpy.random.seed`, `pandas`

## 필요한 환경 만들기

-   TFT 전략과 다른 전략의 경쟁 [@Downey:2012aa]

    -   구현 대상: 전략, 보수의 비교, 학습 등

    -   <https://colab.research.google.com/github/AllenDowney/ThinkComplexity2/blob/master/notebooks/chap12.ipynb>

-   사용하려는 파일 가져오기, (그림) 파일 저장 $\rightarrow$ 이전과 같음

-   `Simulation` 클래스 만들기

    -   경기자의 공간 설정

                    class Simulation:
                        
                        def __init__(self, fit_land, agents):
                            self.fit_land = fit_land
                            self.agents = np.asarray(agents)
                            self.instruments = []

    -   `instrument` 설정과 그래프 그리기 $\rightarrow$ 이후에 나옴

                        def add_instrument(self, instrument):
                            self.instruments.append(instrument)
                            
                        def plot(self, index, *args, **kwargs):
                            self.instruments[index].plot(*args, **kwargs)

        -   `*args`: non Keyword Arguments, 여러 개의 변수를 함수로
            넘겨주어야 하는 데 몇 개를 넘겨야할 지 모를 때, 해당 변수를
            튜플로 처리

        -   `**kwargs`: Keyword Arguments, 키워드를 특정 값으로 함수에
            넘겨줄 때, 각각 키와 값으로 가져오는 딕셔너리로 처리

    -   1번 시행: 초기화 -- 게임 -- 적합도 계산 -- 적합도가 낮은 경우,
        전략 수정$\rightarrow$ 몇 번 시행?

                        def run(self, num_steps=500):
                            self.update_instruments()
                            
                            for _ in range(num_steps):
                                self.step()
                            
                        def step(self):
                            n = len(self.agents)
                            fits = self.get_fitnesses()
                            
                            index_dead = self.choose_dead(fits)
                            num_dead = len(index_dead)
                            
                            replacements = self.choose_replacements(num_dead, fits)
                            self.agents[index_dead] = replacements
                    
                            self.update_instruments()

        -   `range`:

    -   1번의 시행에서 필요한 함수를 정의: `instrument` 업데이트, 적합도
        계산, 적합도 비교, 전략 변경 등

                        def update_instruments(self):
                            for instrument in self.instruments:
                                instrument.update(self)
                                
                        def get_locs(self):
                            return [tuple(agent.loc) for agent in self.agents]
                        
                        def get_fitnesses(self):
                            fits = [agent.fitness for agent in self.agents]
                            return np.array(fits)
                        
                        def choose_dead(self, ps):
                            n = len(self.agents)
                            is_dead = np.random.random(n) < 0.1
                            index_dead = np.nonzero(is_dead)[0]
                            return index_dead
                            
                        def choose_replacements(self, n, weights):
                            agents = np.random.choice(self.agents, size=n, replace=True)
                            replacements = [agent.copy() for agent in agents]
                            return replacements

-   `Instrument` 클래스 만들기

                class Instrument:
                def __init__(self):
                    self.metrics = []
                    
                def update(self, sim):
                    pass
                    
                def plot(self, **options):
                    plt.plot(self.metrics, **options)

    -   각 단계에서의 현재 값 계산

    -   `pass`: 아무것도 실행하지 않고자 할 때

    -   `**`: 딕셔너리로 풀어줌(unpacking). `*`는 인수로 풀어줌. 예를
        들어,

                    def sum(a, b, c, d):
                       return a + b + c + d

                    values1 = (1, 2)
                    values2 = { 'c': 10, 'd': 15 }
                    
                    s = sum(*values1, *values1)
                    s = sum(*values1, **values2) 

-   `MeanFitness` 클래스 만들기: 평균 적합도 계산

                class MeanFitness(Instrument):
                    label = 'Mean fitness'
                    
                    def update(self, sim):
                        mean = np.nanmean(sim.get_fitnesses())
                        self.metrics.append(mean)

    -   `nanmean`: NaN을 무시하고 산술 평균을 계산

        -   <https://numpy.org/doc/stable/reference/generated/numpy.nanmean.html>

## 전략의 경쟁

-   경기자 `Agent` 클래스 만들기: 경기자 속성 $=$ 전략, 복제, 변이; 상대
    경기자의 이전 선택에 따라 나의 다음 선택을 결정

            class Agent:
                
                keys = [(None, None),
                        (None, 'C'),
                        (None, 'D'),
                        ('C', 'C'),
                        ('C', 'D'),
                        ('D', 'C'),
                        ('D', 'D')]
                
                def __init__(self, values, fitness=np.nan):
                    self.values = values
                    self.responses = dict(zip(self.keys, values))
                    self.fitness = fitness
                    
                def reset(self):
                    self.hist = [None, None]
                    self.score = 0
                    
                def past_responses(self, num=2):
                    return tuple(self.hist[-num:])
                
                def respond(self, other):
                    key = other.past_responses()
                    resp = self.responses[key]
                    return resp
                    
                def append(self, resp, pay):
                    self.hist.append(resp)
                    self.score += pay
                    
                def copy(self, prob_mutate=0.05):
                    if np.random.random() > prob_mutate:
                        values = self.values
                    else:
                        values = self.mutate()
                    return Agent(values, self.fitness)
                
                def mutate(self):
                    values = list(self.values)
                    index = np.random.choice(len(values))
                    values[index] = 'C' if values[index] == 'D' else 'D'
                    return values

-   경기자 타입(전략)을 유전형(genotype)처럼 간주

            all_c = Agent('CCCCCCC')
            all_c.responses
            
            all_d = Agent('DDDDDDD')
            all_d.responses

            tft = Agent('CCDCDCD')
            tft.responses

-   돌연변이 설정

            np.random.seed(17)
                for i in range(10):
                print(all_d.copy().values)

-   1,000개의 셀을 복제 한 후, 이 중 돌연변이의 수를 계산

            np.sum([all_d.copy().values != all_d.values for i in range(1000)])    

-   `Tournament` 클래스 만들기: 경쟁 규칙을 만들기

            class Tournament:
            
            payoffs = {('C', 'C'): (3, 3),
                       ('C', 'D'): (0, 5),
                       ('D', 'C'): (5, 0),
                       ('D', 'D'): (1, 1)}
            
            num_rounds = 6

            def play(self, agent1, agent2):
                agent1.reset()
                agent2.reset()
                
                for i in range(self.num_rounds):
                    resp1 = agent1.respond(agent2)
                    resp2 = agent2.respond(agent1)

                    pay1, pay2 = self.payoffs[resp1, resp2]
                    
                    agent1.append(resp1, pay1)
                    agent2.append(resp2, pay2)
                    
                return agent1.score, agent2.score
                        
            def melee(self, agents, randomize=True):
                if randomize:
                    agents = np.random.permutation(agents)
                    
                n = len(agents)
                i_row = np.arange(n)
                j_row = (i_row + 1) % n
                
                totals = np.zeros(n)
                
                for i, j in zip(i_row, j_row):
                    agent1, agent2 = agents[i], agents[j]
                    score1, score2 = self.play(agent1, agent2)
                    totals[i] += score1
                    totals[j] += score2
                    
                for i in i_row:
                    agents[i].fitness = totals[i] / self.num_rounds / 2

    -   `num_rounds`: 몇 개의 하위 게임 $\rightarrow$ 현재 6개

    -   우리가 만드는 것은 반복 죄수의 딜레마 게임

    -   `play`

        -   `reset`: 첫 번째 하위 게임을 시작하기 전, 기록을 초기화

        -   `respond`: 주어진 상대방의 반응에 대해 경기자가 반응하도록
            경기자를 호출

        -   `append`: 우리의 경우, 선택과 이에 대한 보수(점수)를 저장

    -   `melee`

        -   경기자 목록(list)을 만듬: 누가 누구를 상대할 것인가?

        -   `randomize`: 무작위 색인

        -   `permutation`: sequence를 치환시킴

            -   <https://numpy.org/doc/stable/reference/random/generated/numpy.random.permutation.html>

        -   `i_row`, `j_row`: 짝 짓기 색인

        -   `arange`: 주어진 값에서 균등 배치

            -   <https://numpy.org/doc/stable/reference/generated/numpy.arange.html#numpy-arange>

        -   `totals`: 총 보수(점수)

        -   `fitness`: 상대방 별, 하위 게임 별, 평균 적합도(획득 점수의
            평균 )를 저장

-   `Tournament` 클래스 시험하기

            tour = Tournament()
            tour.play(all_d, all_c)

            tour.play(all_d, tft)
            
            tour.play(tft, all_c)
            
            agents = [all_c, all_d, tft]
            agents
            
            tour.melee(agents)

    -   적합도 확인

                    for agent in agents:
                    print(agent.values, agent.fitness)

-   생존 확률: 한 회의 게임에서 획득한 점수로부터 생존 확률 계산

            def logistic(x, A=0, B=1, C=1, M=0, K=1, Q=1, nu=1):
                exponent = -B * (x - M)
                denom = C + Q * np.exp(exponent)
                return A + (K-A) / denom ** (1/nu)
            
            def prob_survive(scores):
                return logistic(scores, A=0.7, B=1.5, M=2.5, K=0.9)
            
            scores = np.linspace(0, 5)
            probs = prob_survive(scores)
            plt.plot(scores, probs)
            decorate(xlabel='Score', ylabel='Probability of survival')

    -   일반적인 로지스틱 함수 사용

        -   $A$: 하계(lower bound)

        -   $B$: 전환 정도

        -   $C$: 중요한 변수는 아님

        -   $M$: 전환 시점

        -   $K$: 상계(upper bound)

        -   $Q$: 전환 방향 (왼쪽 또는 오른쪽)

        -   $nu$: 전환 대칭성

    -   `prob_survive`: 점수에 따라 생존 확률 계산

-   `PDSimulation` 클래스 만들기 $\rightarrow$ 매 하위 게임에서 얻는
    점수와 생존 확률을 맵핑

            class PDSimulation(Simulation):
            
            def __init__(self, tournament, agents):
                self.tournament = tournament
                self.agents = np.asarray(agents)
                self.instruments = []
                
            def step(self):
                self.tournament.melee(self.agents)
                Simulation.step(self)
                
            def choose_dead(self, fits):
                ps = prob_survive(fits)
                n = len(self.agents)
                is_dead = np.random.random(n) < ps
                index_dead = np.nonzero(is_dead)[0]
                return index_dead

    -   `asarray`: 입력 값을 `array`로 바꿔줌

        -   <https://numpy.org/doc/stable/reference/generated/numpy.asarray.html>

    -   1번의 시행(`step`): 각 경기자의 적합도를 결정하는 `melee` 실행

-   최초 경기자 설정: 두 가지 방법

            def make_random_agents(n):
              agents = [Agent(np.random.choice(['C', 'D'], size=7)) 
                      for _ in range(n)]
              return agents
            
            def make_identical_agents(n, values):
              agents = [Agent(values) for _ in range(n)]
              return agents

    -   `make_random_agents`: 무작위로 속성 배정

    -   `make_identical_agents`: 동일한 속성

-   전략에 따라 속성 만들기

            class Niceness(Instrument):
               label = 'Niceness'
                
               def update(self, sim):
                  responses = np.array([agent.values for agent in sim.agents])
                  metric = np.mean(responses == 'C')
                  self.metrics.append(metric)
                
           class Opening(Instrument):
               label = 'Opening'
                    
                def update(self, sim):
                    responses = np.array([agent.values[0] for agent in sim.agents])
                    metric = np.mean(responses == 'C')
                    self.metrics.append(metric)
                
            class Retaliating(Instrument):
                label = 'Retaliating'
                
                def update(self, sim):
                    after_d = np.array([agent.values[2::2] for agent in sim.agents])
                    after_c = np.array([agent.values[1::2] for agent in sim.agents])
                    metric = np.mean(after_d == 'D') - np.mean(after_c == 'D')
                    self.metrics.append(metric)
                
            class Forgiving(Instrument):
               label = 'Forgiving'
              
              def update(self, sim):
                after_dc = np.array([agent.values[5] for agent in sim.agents])
                after_cd = np.array([agent.values[4] for agent in sim.agents])
                metric = np.mean(after_dc == 'C') - np.mean(after_cd == 'C')
                self.metrics.append(metric)
                
            class Forgiving2(Instrument):
               label = 'Forgiving2'        
               def update(self, sim):
                    after_two = np.array([agent.values[3:] for agent in sim.agents])
                    metric = np.mean(np.any(after_two=='C', axis=1))
                    self.metrics.append(metric)        

    -   `Niceness`: 개체군에서 $C$ 유형의 평균적인 수

    -   `Opening`: 첫 하위 게임에서 협력하는 경기자의 비율

    -   `Retalitating`: 상대방의 배신 이후 배신하는 경기자의 비율,
        상대방의 협력 이후 배신하는 경기자의 비율 $\rightarrow$ 두 비율
        간의 차이

    -   `Forgiving`: 상대방의 DC 이후 협력하는 경기자의 비율, 상대방의
        CD 이후 협력하는 경기자의 수 $\rightarrow$ 둘의 차이

    -   `Forgiving2`: 상대방의 첫 두 게임에 대해 협력하는 경기자의 수

## 경쟁 결과 비교

-   배신자 100명으로 시작

            tour = Tournament()
            
            agents = make_identical_agents(100, list('DDDDDDD'))
            sim = PDSimulation(tour, agents)
            
            sim.add_instrument(MeanFitness())
            sim.add_instrument(Niceness())
            sim.add_instrument(Opening())
            sim.add_instrument(Retaliating())
            sim.add_instrument(Forgiving()) 

-   5,000회 시행

            np.random.seed(17)
            sim.run(5000)

    -   `RuntimeWarning`은 무시

-   결과(평균 적합도) 확인

            def plot_result(index, **options):
               sim.plot(index, **options)
               instrument = sim.instruments[index]
               print(np.mean(instrument.metrics[1000:]))
               decorate(xlabel='Time steps', 
                             ylabel=instrument.label)
                             
            plot_result(0, color='C0')
            savefig('figs/chap12-1')

    -   초기의 평균 적합도는 1 $\rightarrow$ 모두 배신 전략을 하고
        있으므로

    -   협력자로의 변이가 나타나면서 평균 적합도는 2.5 근방에서 진동

-   `Niceness`와 `Opening`, 두 개의 그래프 그려보기

            plt.figure(figsize=(8,4))
            plt.subplot(1,2,1)
            
            plot_result(1, color='C1')
            decorate(ylim=[0, 1.05])
            
            plt.subplot(1,2,2)
            plot_result(2, color='C2')
            decorate(ylim=[0, 1.05])
            
            savefig('figs/chap12-2')

    -   `Niceness`: 평균 협력자는 절반 이상 분포, 장기적으로 0.6을 상회

    -   `Opening`: 첫 게임의 협력자도 평균 협력자의 분포와 유사, 하지만,
        그 비중 변동은 심함

-   최종 단계에서 유형 분포

            for agent in sim.agents:
                print(agent.values)

-   가장 흔한 유형 확인하기

            from pandas import Series

            responses = [''.join(agent.values) for agent in sim.agents]
            Series(responses).value_counts()

    -   `Pandas`: 데이터 분석에 사용

        -   <https://pandas.pydata.org>

    -   `Series`: 연속적인 값의 일차원 배열과 자료 라벨(인덱스)의 배열로
        정리

        -   <https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.html>

## 정리하기

1.  `*`는 해당 값을 튜플로, `**`는 딕셔너리로 처리한다.

2.  구현하려는 모형의 전체 과정을 하나의 완결된 실행 단위로 쪼개어
    정리하고, 이를 `class`로 구현한다.

3.  데이터 분석을 위해 보통 `Pandas`를 사용한다.
