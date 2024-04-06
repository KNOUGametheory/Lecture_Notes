---
layout: default
title: SIR 모형으로 연구하기
parent: 넷로고와 파이선을 활용한 게임이론 시뮬레이션
nav_order: 7
---


# SIR 모형으로 연구하기

## 학습개요

SIR 모형을 파이선으로 구현한다.

## 학습목표

1.  파이선을 활용해 그래프를 그릴 수 있다.

2.  파이선의 반복 구문을 이해한다.

3.  이미 만들어진 파이선 모형을 읽을 수 있다.

## 주요 용어

`lambda` 함수, `list`, `array`, `fig`, `ax`, `plt.show()`, `for  in `

## SIR 모형

### SIR 모형의 특징

-   국가수리과학연구소, 코로나19 확산 예측

    -   <https://www.nims.re.kr/research/pageView/741>

-   Thomas J. Sargent and John Stachurski, "Modeling COVID 19,\"
    *Intermediate Quantitative Economics with Python*.

    -   <https://python.quantecon.org/sir_model.html>

    -   [@Atkeson:2020ac]

-   4 단계: susceptible (S) $$\rightarrow$$ exposed (E) $$\rightarrow$$
    infected (I) $$\rightarrow$$ removed (R) $$$$\begin{aligned}
        \dot{s}(t)  & = \dfrac{dS}{dt}  = -\beta(t) s(t) i(t) \\
        \dot{e}(t)  & =  \dfrac{de}{dt} = \beta(t) s(t) i(t) - \sigma e(t)  \\  
        \dot{i}(t) & = \dfrac{di}{dt} = \sigma e(t) - \gamma i(t) 
        
    \end{aligned}$$$$

    -   $$\beta(t)$$: 감염병의 전파율

    -   $$\sigma$$: 감염율

    -   $$\gamma$$: 회복율

    -   사망률 $$r = 1- s - e- i$$

    -   누적 감염 $$c = i + r$$

-   벡터로 표현하면 $$$$\begin{aligned}
        \dot{x} & = F(x, t), \quad x \coloneqq (s, e, i) \\
        
    \end{aligned}$$$$

-   주요 파라미터: 결과 재현을 위해, 우선 미국과 일치시키자

    -   $$\sigma = 1/5.2$$: 평균 잠복기 5.2 일

    -   $$\gamma = 1/18$$: 평균 지속기 18일

    -   $$\beta(t) \coloneqq R(t) \gamma$$: $$R(t)$$ $$t$$ 기의 실질 감염재생산 지수 $$\rightarrow$$ $$R(0)$$: 상수

    -   이상의 값은 역학 연구의 결과에 따라 변경 가능

    -   다른 변수 $$\rightarrow$$ 역시 조건에 따라 변경 가능

        -   인구 `pop_size`: 3억 3천만명

        -   기간 `t_length`: 550일

### SIR 모형의 설정

-   새파일 열고, 저장

-   파이선 패키지 설정

                import matplotlib.pyplot as plt
                import numpy as np
                from numpy import exp
                from scipy.integrate import odeint

    -   `matplotlib.pyplot`: `matplotlib` 패키지에서 `Matlab`과 유사한 설정을 가능하게 하는 하위 모듈

        -   <https://matplotlib.org/stable/api/pyplot_summary.html>

    -   `from 패키지(모듈)이름` `import 모듈이름(함수)`:

        -   장점

            -   `np.exp` 가 아니라, `exp`를 바로 쓸 수 있음

            -   다른 패키지에 같은 이름의 함수를 사용하다 생길 수 있는 문제를 막을 수 있음

        -   단점

            -   코드가 길어지고, 주석이 없는 경우, 출처를 알 수 없을 때 있음

        -   <https://docs.python.org/3/reference/import.html>

    -   `exp`: 지수(exponential) 계산을 위해 필요,
        <https://numpy.org/doc/stable/reference/generated/numpy.exp.html>

    -   `odient`: 미분 방정식(differential equation)을 풀기 위해 필요,
        <https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.odeint.html>

-   계산 모형 설정

            def F(x, t, R0):
                    s, e, i = x
                    
                    beta = R0(t) * gamma if callable(R0) else R0 * gamma
                    ne = beta * s * i
                    
                    ds = - ne
                    de = ne - sigma * e
                    di = sigma * e - gamma * i

                    return ds, de, di

    -   `callable()`: 내장 함수. 괄호 안의 오브젝트가 호출 가능하다면 `True`, 그렇지 않다면 `False`

        -   우리의 경우, $$R0$$가 $$t$$에 대한 함수라면 $$\rightarrow$$ 지금은 상수이지만, 뒤에서 함수로 다룰 예정

-   초기값 설정

            """
            초기값 설정
            """
            
            i_0 = 1e-7
            e_0 = 4 * i_0
            s_0 = 1 - i_0 - e_0
            
            x_0 = s_0, e_0, i_0 
            
            gamma = 1 / 18 # 지속기 18일
            sigma = 1 / 5.2 # 잠복기 5.2일

    -   주석 처리

        -   문단 단위: 세 개의 인용 부호`"""` ,`'''`로 시작, 같은 세 개의 인용 부호로 끝

        -   한 줄: `#`

    -   초기값 확인

                    list (x_0)

-   시간에 따른 주요 변수의 변화 $$\rightarrow$$ 미분 방정식

            def solve_path(R0, t_vec, x_init=x_0):
                G = lambda x, t: F(x, t, R0)
                
                s_path, e_path, i_path = odeint(G, x_init, t_vec).transpose()
                
                c_path = 1 - s_path - e_path
            
                return i_path, c_path

    -   `lambda 함수이름: 돌려줄값`

        -   `lambda` 함수: 익명 함수(anonymous function), 다른 함수를 불러와서 사용, 변수 지정도 가능 
		
		-   $$\rightarrow$$ 다양하게 사용 가능하니, 사용법을 익혀두면 좋음

    -   `transpose`: 전치 행렬을 생각할 것

-   시간 지정

            t_length = 550
            grid_size = 1000
            t_vec = np.linspace(0, t_length, grid_size)

    -   `linspace(시작값,최종값,균등간격)`: `numpy` 내장 범용 함수(universal functions) 중 하나

        -   자주 활용할 수 있는 내장 범용 함수를 익혀 둘 것: `mean`, `std`, `max`, `reshape`, `vectorize` 등

        -   범용 함수 목록: <https://numpy.org/doc/stable/reference/ufuncs.html>

## 실질 감염재생산 지수: 상수

-   실질 감염재생산 지수의 효과 확인: 실질 감염재생산 지수의 크기를 키워가면서

            R0_vals = np.linspace(1.6, 3.0, 6)
            labels = [f'$$R0 = {r:.2f}$$' for r in R0_vals]
            i_paths, c_paths = [], []

    -   실질 감염재생산지수(effective reproduction number)

        -   한 명의 감염자가 평균적으로 감염시킬 수 있는 2차 감염자의 수

        -   1보다 크면 최소 한 사람 이상 추가적으로 감염될 수 있다는 뜻이므로

        -   클 수록 인구 집단 내에서 확산될 가능성이 높아짐

    -   `np.linspace(1.6, 3.0, 6)` : 1.6부터 3.0까지 6 균등

    -   `labels = [구문]`: 그래프 축, 범례 등에 사용

    -   `f'구문'`: `''` 안의 내용을 문자열로 지정해줌(f-strings: Formatted string literals)

    -   `:.2f`: 소수점 둘째 자리까지

    -   `for 변수이름 in 범위`: `for` 반복문(loop) $$\rightarrow$$ 우리의 경우 `R0_vals`에서 `r`이 반복

    -   `[]`: 비어 있는 목록(empty lists)을 만듬

        -   `list (i_paths)`: `[]` 가 나오는 것이 정상 $$\rightarrow$$ 비어 있는 목록이므로

        -   목록(list): 파이선에서 항목을 순서 지어 모을 때(an ordered collection of items) 사용

-   실질 감염재생산 지수에 따라 계산

            for r in R0_vals:
                i_path, c_path = solve_path(r, t_vec)
                i_paths.append(i_path)
                c_paths.append(c_path)

    -   `목록이름.append`: 호출한 목록의 마지막에 목록을 추가함

    -   `list (i_paths)`: 계산된 값의 긴 목록이 나올 것

        -   `array`: 다차원 배열 객체 $$\rightarrow$$ 행렬 연산과 비슷한 계산을 할 수 있음

        -   <https://numpy.org/doc/stable/user/absolute_beginners.html#whats-the-difference-between-a-python-list-and-a-numpy-array>

-   그래프 설정

            def plot_paths(paths, labels, times=t_vec):
            
                fig, ax = plt.subplots()
            
                for path, label in zip(paths, labels):
                    ax.plot(times, path, label=label)
            
                ax.legend(loc='upper left')
            
                plt.show()

    -   `fig`: 그림 객체를 생성 $$\rightarrow$$ 그림의 틀

    -   `ax`: 그래프를 그릴 수 있는 캔버스

    -   `subplots`: 메소드를 사용해, 여러 개의 그래프를 그릴 수 있음

        -   `fig, axes = plt.subplots(2, 3)` 를 해볼 것

    -   `zip`: 성분을 차례로 순서쌍 형식으로 반환시킴

        -   <https://docs.python.org/3/library/functions.html#zip>

    -   `legend`: 범례, `loc`: 위치

    -   `plt.show()`: 메소드를 이용해 그림을 볼 수 있음

-   그래프를 그림

            plot_paths(i_paths, labels)
            
            plot_paths(c_paths, labels) 

    -   Jupyter Notebook이나 Ipython 쉘에서는 필요없지만, 그림이 안 보이면 다음 구문을 시작에 선언할 것: `%matplotlib inline`

-   실질 감염재생산 지수가 낮을 수록

    -   감염율이 늦게 최고 값을 기록, 그 값도 낮음

    -   누적도 마찬가지

## 실질 감염재생산 지수: 함수

-   정책적 대응

    -   거리두기 등 $$\rightarrow$$ 실질 감염재생산 지수를 변화시킬수 있다면 $$\rightarrow$$ 그 효과는?

-   실질 감염재생산 지수를 함수로 바꿈

            def R0_mitigating(t, r0=3, eta=1, r_bar=1.6):
               R0 = r0 * exp(- eta * t) + (1 - exp(- eta * t)) * r_bar
               return R0

    -   $$r0=3$$ 부터 1.6까지 $$\rightarrow$$ 거리 두기의 결과로 해석

    -   `eta`: 속도를 조정 $$\rightarrow$$ 정책의 실제 집행 정도

-   `eta`를 변화시킴

            eta_vals = 1/5, 1/10, 1/20, 1/50, 1/100
            labels = [fr'$$\eta = {eta:.2f}$$' for eta in eta_vals]

    -   여러 개의 값을 나열하여 입력할 수도 있음

-   `eta` 변화에 따른 실질 감염재생산 지수의 변화를 확인

            fig, ax = plt.subplots()

            for eta, label in zip(eta_vals, labels):
                ax.plot(t_vec, R0_mitigating(t_vec, eta=eta), label=label)
            
            ax.legend()
            plt.show()  

    -   `eta`가 클 수록, 감염 재생산 지수가 빠르게 하락

-   감염율을 계산

            i_paths, c_paths = [], []
            
            for eta in eta_vals:
                R0 = lambda t: R0_mitigating(t, eta=eta)
                i_path, c_path = solve_path(R0, t_vec)
                i_paths.append(i_path)
                c_paths.append(c_path)

    -   `lambda` 함수 사용을 확인할 것

-   그래프

            plot_paths(i_paths, labels)
            plot_paths(c_paths, labels)

    -   `eta`가 클 수록

        -   감염율이 늦게 최고 값을 기록, 그 값도 낮음

        -   누적도 마찬가지

-   인구를 도입

            pop_size = 3.3e8
            
            i_0 = 25_000 / pop_size
            e_0 = 75_000 / pop_size
            s_0 = 1 - i_0 - e_0
            x_0 = s_0, e_0, i_0 

    -   `_`: 자리수 표현

-   2 개의 시나리오 비교

            R0_paths = (lambda t: 0.5 if t < 30 else 2,
                    lambda t: 0.5 if t < 120 else 2)

            labels = [f'scenario {i}' for i in (1, 2)]
            
            i_paths, c_paths = [], []
            
            for R0 in R0_paths:
                i_path, c_path = solve_path(R0, t_vec, x_init=x_0)
                i_paths.append(i_path)
                c_paths.append(c_path)  

    -   30일간 $$R_t = 0.5$$, 이후 17개월 간 $$R_{t} = 2$$

    -   120일간 $$R_t = 0.5$$, 이후 14개월 간 $$R_{t} = 2$$

-   그래프

            plot_paths(i_paths, labels)

-   사망률 `nu` 도입

            nu = 0.01   
            
            paths = [path * nu * pop_size for path in c_paths] # 누적사망
            plot_paths(paths, labels)
            
            paths = [path * nu * gamma * pop_size for path in i_paths] #일일사망
            plot_paths(paths, labels)

    -   실질 감염재생산 지수를 같은 수준으로 상대적으로 더 길게 유지할 수록

        -   감염과 누적 사망의 최고점을 늦출 수 있음

## 정리하기

1.  익명 함수(`lambda` 함수)를 다른 함수를 불러 올 때, 변수를 지정할 때 사용할 수 있다. 이외의 사용 방법을 익히면 좋다.

2.  `numpy`의 범용 함수는 평균, 최대값 등을 계산하는 데 유용하게 사용할 수 있다. 다양한 사용 방법을 익히면 좋다.

3.  그래프를 그리기 위해 `matplotlib.pyplot` 패키지를 사용하는 것이 편리하다.

4.  `for` 반복 구문은 여러 변수를 정해진 규칙에 따라 처리할 수 있다.
