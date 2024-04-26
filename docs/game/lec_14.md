---
layout: default
title: 진화 게임
parent: 게임이론
nav_order: 14
---


# 진화 게임

<!-- ## 학습개요

진화 게임의 특성과 사회 과학에서의 활용을 학습한다. -->


<!-- ## 주요 용어

진화, 진화 게임, 진화적으로 안정적인 전략, 복제자 동학 -->

## 1. 진화와 게임이론

### 학습 목표

- 진화의 특성을 설명할 수 있다.

- 진화 게임의 특성을 설명할 수 있다.

### 진화

-   진화(evolution): 다음의 세 가지 조건이 있으면 진화가 일어남

    -   변이(variation): 개체군의 개체에서 속성(traits)의 변화가 나타나야 함

    -   선별(selection): 변이된 속성에 대한 결과가 있어야 함

    -   복제(replication, heritability, retention): 세대 간 또는 세대 내에 이전(transmission)되어야 함

    -   $$\rightarrow$$ 변이된 속성의 상대적 이득 $$\rightarrow$$ 생존 또는 재생산의 장점 $$\rightarrow$$ 개체군에서의 확산

-   적합도(fitness)

    -   만약 어떤 속성 또는 행위로 필요로 하는 자원을 더 확보할 수 있다면, 
	
	-   또는 그 결과로 더 큰 이득을 얻을 수 있다면,

    -   그 속성 또는 행위가 집단에서 더 잘 이전될 것 
	
	-   $$\rightarrow$$ 높은 적합도

    -   죄수의 딜레마 게임

        -   협력: $$b-c < b$$ : 배신

        -   배신이 더 높은 적합도

### 진화 게임

-   진화 게임(evolutionary game theory)

    -   전략을 개체의 어떤 속성이나 행위로, 보수를 적합도로 $$\rightarrow$$ 개체 간의 상호 작용에 따라 보수, 즉 적합도가 결정된다면 $$\rightarrow$$ 게임이론을 적용할 수 있음 [[1]](#1)

    -   전략 선택이 아니라 $$\rightarrow$$ 특정 속성 또는 행위(전략)의 상대적 우위

        -   정태적: 진화적으로 안정적인 전략

        -   동태적: 복제자 동학

-   사회과학에서의 응용

    -   속성의 이전

        -   생명체: 유전자(gene)

        -   사회: 학습 또는 모방(imitation) [[2]](#2)[[3]](#3)[[4]](#4)[[5]](#5)

    -   어떤 속성 또는 행위의 확산이나 감소를 설명하기 좋음

    -   학습 또는 모방: 유전자보다 잘못 복제될 가능성 높음 $$\rightarrow$$ 우리는 일단 이 문제를 다루지 않음

## 2. 진화적으로 안정적인 전략

### 학습 목표

- 진화적으로 안정적인 전략의 조건을 설명할 수 있다.


### 진화적으로 안정적인 전략

-   보수가 대칭인 게임 $$G$$ [[6]](#6)

    -   유한 전략 집합 $$S  = \{ s_{1}, \ldots, s_{n}\}$$

    -   대칭적인 보수 $$u_{1}(s_{j}, s_{i}) = u_{2}(s_{i}, s_{j})$$

-   진화 게임: 순수 전략

    -   게임 $$G$$를 하는 개체(individual)가 있는 개체군(population)

    -   개체가 순수 전략 $$\tau = s_{i}$$를 구사한다면, 개체는 $$i$$ 유형(type)이라고 할 수 있음

    -   개체군 전체에서 전략 $$s_{n}$$이 확률 $$p_{n}$$으로 구사된다면
	
	    -   개체군의 상태 $$\sigma = \sum p_{i} s_{i}$$
		
		-   단, $$p_{i} \geq 0,\sum p_{i}=1$$

    -   한 개체가 개체군 $$\sigma$$ 중 다른 개체와 무작위로 게임을 한다면, 그 때의 기대 보수

        $$
		u_{1}(s_{i}, \sigma) = \sum_{j=1}^{n} u_{1}(s_{i}, s_{j})p_{j}
        $$

    -   개체군의 상태 $$\sigma_{1} = \sum p_{1i}s_{i}$$, $$\sigma_{2} = \sum p_{2i}s_{i}$$ 이고, $$0<\epsilon<1$$ 이라면,

        $$
		(1-\epsilon)\sigma_{1} + \epsilon \sigma_{2} = \sum \left( (1-\epsilon)p_{1i} + \epsilon p_{2i} \right)s_{i}
        $$

-   진화게임: 혼합 전략

    -   개체는 혼합 전략 $$\tau = \sum q_{i}s_{i}$$를 구사(단, $$q_{i} \geq 0,\sum q_{i}=1$$)

    -   무작위로 상대와 매칭될 때, 기대 보수

        $$
		u_{1} (\tau, \sigma) = \sum_{i=1}^{n} q_{i} u_{1} (s_{i},\sigma) = \sum_{i, j =1}^{n} q_{i} u_{1} (s_{i},s_{j})p_{j}
        $$

        -   $$\rightarrow$$ $$u_{1} ( \tau, (1-\epsilon) \sigma_{1} + \epsilon \sigma_{2}) = (1-\epsilon) u_{1}(\tau,\sigma_{1})+\epsilon u_{1}(\tau,\sigma_{2})$$

    -   $$\epsilon$$을 $$\tau$$ 유형이 개체군에서 차지하는 비중으로 가정하면, 개체군의 상태를 다음과 같이 쓸 수 있음 
	
	    -   $$\rightarrow$$ $$(1-\epsilon) \sigma + \epsilon \tau$$ (단, $$0 < \epsilon < 1$$)

-   개체군의 상태 $$\sigma$$ 가 진화적으로 안정적(evolutionarliy stable)이라는 의미는 

       $$ 
	   u_{1} (\sigma, (1-\epsilon)\sigma + \epsilon \tau) > u_{1} (\tau, (1-\epsilon) \sigma + \epsilon \tau)
	   $$

    -   단, $$\tau \neq \sigma$$, $$\epsilon_{0} > 0$$, $$0 < \epsilon < \epsilon_{0}$$

-   위 식의 의미는

    -   어떤 개체군에 유형 $$\sigma$$ 가 있을 때, 소수의 다른 유형의 개체 $$\tau$$가 개체군에 침입하더라도

    -   유형 $$\sigma$$가 개체군의 다른 개체와 무작위로 게임을 할 때, 
	
	-   유형 $$\sigma$$의 개체가 유형 $$\tau$$의 개체보다 더 높은 기대 보수를 갖고 있음을 의미

    -   따라서, 침입자 또는 돌연변이라고 할 수 있는 개체 $$\tau$$는 사라질 것

-   진화적으로 안정적인 전략(ESS: Evolutionarily Stable Strategies)의 조건

    {: .theorem}
    > A population state $$\sigma$$ is evolutionarily stable if and only if for all $$\tau \neq \sigma$$
    > 
    > 1.  
	>    $$
	>    u_{1} (\sigma, \sigma) \geq u_{1} (\tau, \sigma)
	>    $$
    > 
    > 2.  If $$u_{1}(\tau, \sigma) = u_{1}(\sigma, \sigma)$$, then $$u_{1}(\sigma, \tau) > u_{1}(\tau, \tau)$$

    -   첫 번째 조건은 진화 게임에서 시행되는 두 경기자의 대칭 보수 게임에서 $$(\sigma, \sigma)$$가 혼합 전략 내쉬 균형임을 의미 
	
	    -   $$\rightarrow$$ $$\sigma$$에 대한 최적 대응은 $$\sigma$$

    -   두 번째 조건은 만약 $$\sigma$$에 대한 최적 대응 $$\tau$$가 있을 때, $$\tau$$에 대한 최적 대응이 $$\tau$$가 되어서는 안되고, $$\sigma$$이어야 함을 의미

        -   앞의 조건만 만족하는 경우 $$\tau$$ 가 생존

        -   $$\tau$$가 소멸하기 위해서는 $$\tau$$보다 $$\sigma$$가 더 높은 보수를 얻어야 하기 때문

-   진화적으로 안정적인 전략의 속성

    -   만약 전략 $$S$$가 진화적으로 안정적이라면, $$(S, S)$$는 내쉬 균형

        -   역은 성립하지 않음. 즉, $$(S, S)$$가 내쉬 균형이지만, 진화적으로 안정적이지 않을 수 있음

    -   만약 $$(S,S)$$가 어떤 게임의 고유한 최적 대응이라면(a strict Nash equilibrium), 
	
	    -   이 게임에 대응하는 진화 게임에서 $$S$$는 진화적으로 안정적

### 두 개의 전략이 있을 때 진화적 안정성

-   순수 전략의 경우 [[7]](#7)

       |          |       | $$P_{2}$$  |          |
	   |          |       | $$S$$      | $$T$$    |
       | $$P_{1}$$| $$S$$ | $$a, a$$   | $$b, c$$ |
       |          | $$T$$ | $$c, b$$   | $$d, d$$ |


    -   개체군에서 $$1-x$$의 비율로 $$S$$를, $$x$$의 비율로 $$T$$를 따른다고 할 때(단, $$ 0 < x < 1 $$),

        -   $$S$$ 전략을 따르는 개체는 $$1-x$$의 확률로 $$S$$를 따르는 개체를, $$x$$의 확률로 $$T$$를 만나게 되므로, 
		
		    -    기대 보수는 $$(1-x)a+xb$$

        -   $$T$$ 전략을 따르는 개체는 $$1-x$$의 확률로 $$S$$를 따르는 개체를, $$x$$의 확률로 $$T$$를 만나게 되므로, 
		
		    -    기대 보수는 $$(1-x)c+xd$$

        -   $$S$$가 진화적으로 안정적이기 위해서는 $$(1-x)a+xb > (1-x)c+xd$$

            1.  $$x>0$$이지만 충분히 작은 수라면, $$a>c$$

            2.  $$a=c$$ 이고 $$b>d$$

        -   $$a > c$$ 만족 $$\rightarrow$$ $$S$$는 내쉬 균형, 하지만, 진화적으로 안정적이지는 알 수 없음 $$\rightarrow$$ 두 번째 조건이 필요

-   혼합 전략의 경우

    -   경기자 1이 $$p$$의 확률로 $$S$$를 $$1-p$$의 확률로 $$T$$를, 경기자 2가 $$q$$의 확률로 $$S$$를 $$1-q$$의 확률로 $$T$$를 구사한다면,

    -   경기자 1의 기대 보수 $$V(p, q) = pqa + p(1-q)b + (1-p)qc + (1-p)(1-q)d$$

    -   앞에서의 논리대로 정리해보면, $$p$$가 진화적으로 안정적인 혼합 전략이 되기 위해서는 
	
        $$
		(1-x) V(p, p) + x V(p, q) > (1-x) V(q, p) + x V(q, q)
        $$

-   일반화하면, $$a \neq c$$, $$b \neq d$$ 인 다음의 보수 구조에서 [[8]](#8)

       |          |            | $$P_{2}$$  |            |
	   |          |            | $$s_{1}$$  | $$s_{2}$$  |
       | $$P_{1}$$| $$s_{1}$$  | $$a, a$$   | $$b, c$$   |
       |          | $$s_{2}$$  | $$c, b$$   | $$d, d$$   |

    1.  $$a > c$$, $$d < b$$

        -   전략 $$s_{1}$$은 전략 $$s_{2}$$에 대해 강 우월 전략

        -   유일한 내쉬 균형 $$(s_{1}, s_{1})$$

        -   개체군에서 $$s_{1}$$이 진화적으로 안정적

    2.  $$a < c$$, $$d > b$$

        -   전략 $$s_{2}$$은 전략 $$s_{1}$$에 대해 강 우월 전략

        -   유일한 내쉬 균형 $$(s_{2}, s_{2})$$

        -   개체군에서 $$s_{2}$$가 진화적으로 안정적

    3.  $$a > c$$, $$d > b$$

        -   세 개의 내쉬 균형 $$(s_{1}, s_{1}), (s_{2}, s_{2}), (\sigma, \sigma)$$

            $$
			\sigma = ps_{1} + (1-p) s_{2}
            $$

            $$
			p = \dfrac{d-b}{(a-c) + (d-b)}
			$$

            $$
			1-p = \dfrac{a-c}{(a-c)+(d-b)}
			$$

        -   진화적으로 안정적: $$(s_{1}, s_{1}), (s_{2}, s_{2})$$

        -   진화적으로 안정적이지 않음: $$(\sigma, \sigma)$$

    4.  $$a < c$$, $$d < b$$

        -   세 개의 내쉬 균형 $$(s_{1}, s_{2}), (s_{2}, s_{1}), (\sigma, \sigma)$$

        -   진화적으로 안정적: $$(\sigma, \sigma)$$

## 3. 복제자 동학

### 학습 목표

- 복제자 동학의 개념을 설명할 수 있다.

### 복제자 동학

-   이산적인 경우 [[9]](#9)

    -   환경
	
	    - 개체군의 크기 $$N$$
		- 순수 전략 $$s_{1}$$을 구사하는 개체의 빈도(frequency) $$p$$
		- 순수 전략 $$s_{2}$$를 구사하는 개체의 빈도 $$1-p$$
		- 전략 $$s_{1}$$, $$s_{2}$$의 적합도 $$V(s_{1})$$, $$V(s_{2})$$

    -   현재 기에 $$s_{1}$$ 전략을 구사하는 유형의 개체 수는 다음과 같이 표현할 수 있음 
	
        $$ 
		p N V(s_{1})
		$$

    -   만약 모든 개체의 재생산률이 $$z$$로 동일하다면, 다음 기에서 $$s_{1}$$ 전략을 구사하는 유형의 개체 수의 빈도 $$p^{'}$$는 다음과 같이 표현할 수 있음 
	
        $$ 
		p^{'} = \dfrac{p N V(s_{1})z}{p N V(s_{1})z + (1-p) N V(s_{2})z }
		$$

    -   $$Nz$$를 정리하면, 위 식을 다음과 같이 고쳐 쓸 수 있음 
	
        $$ 
		p^{'} = p \dfrac{V(s_{1})}{pV(s_{1}) + (1-p)V(s_{2})}
		$$

    -   개체군에서의 평균 적합도 $$\overline{w} = pV(s_{1}) + (1-p)V(s_{2})$$
	
	    - $$i$$ 전략에 대해 일반화 하면 $$ p_{i}^{'} = p_{i} \dfrac{V(i)}{\overline{w}}$$

    -   $$i$$ 전략의 빈도 변화 $$\rightarrow$$ 이산적일 때의 복제자 동학 
	
        $$
		\Delta p_{i} = p_{i}^{'} - p_{i} = p_{i} \left( \dfrac{V(i)}{\overline{w}} - 1 \right)
		$$

    -   $$\rightarrow$$ 평균 적합도 $$\overline{w}$$ 보다 높은 $$V(i)$$는 개체군에서의 빈도를 높이고, 반대의 경우 낮춤

-   연속적인 경우, 개체군의 상태 $$\sigma$$ 가 시간 $$t$$에 따라 변한다면 [[10]](#10)

    -   $$\sigma(t) = \sum p_{i}(t) s_{i}$$

    -   각 개체가 전략 1과 전략 2 중 하나를 사용하고 있을 때(즉, 순수 전략) 게임을 한 후, 경기자가 자신의 전략을 수정할 수 있다고 생각해보자

    -   집단 내 구성원 중 다른 하나를 무작위로 골라 비교하여 자신의 전략과 다르고, 자신보다 높은 보수를 얻었다면 그 개체의 전략을 자신의 전략으로 삼는다고 하자

-   가정

    -   $$u_{1}(s_{i}, \sigma) > u_{1}(\sigma, \sigma)$$라면, $$s_{i}$$의 적합도가 높으므로 $$\rightarrow$$ $$p_{i}(t)$$ 는 증가할 것

    -   $$u_{1}(s_{i}, \sigma) < u_{1}(\sigma, \sigma)$$라면, $$s_{i}$$의 적합도가 낮으므로 $$\rightarrow$$ $$p_{i}(t)$$ 는 감소할 것

    -   즉 $$p_{i}$$의 변화는 $$u_{1}(s_{i}, \sigma) - u_{1}(\sigma, \sigma)$$에 비례할 것 $$\rightarrow$$ 비례 상수를 1로 하자

-   연속적인 복제자 동학은 $$\dot{p}_{i} = \left( u_{1}(s_{i}, \sigma) - u_{1}(\sigma, \sigma) \right)p_{i}, i=1,\ldots,n$$

### 죄수의 딜레마 게임

-   죄수의 딜레마 게임, 단, $$a, b, c > 0, b > c$$ [[11]](#11)

       |          |       | $$P_{2}$$     |          |
	   |          |       | $$C$$         | $$D$$    |
       | $$P_{1}$$| $$C$$ | $$b-c, b-c$$  | $$-c, b$$ |
       |          | $$D$$ | $$b, -c$$     | $$0, 0$$ |


-   두 개의 순수 전략: 항상 협력($$ALLC$$), 항상 배반($$ALLD$$)

-   협력자의 비율 $$p$$, 배반자의 비율 $$1-p$$

-   기대 보수

	$$
    \begin{align}
	   V(ALLC) & = p(b-c) + (1-p)(-c) = pb-c \\
	   V(ALLD) & = pb + (1-p)(0) = pb          
    \end{align}
    $$

-   모두 $$ALLC$$ 를 하는 경우, 즉 $$p=1$$

    -   $$\rightarrow$$ 진화적으로 안정적이지 않음

    -   $$V(ALLD) = pb > pb -c = V(ALLC)$$ 이므로, $$ALLD$$ 전략을 구사하는 침입자의 확산을 막을 수 없음

-   만약 협력이 사라지지 않으려면 어떤 변화가 있어야 할까?

    -   $$\rightarrow$$ 협력의 진화 [[12]](#12)

    -   친족 선택(kin selection), 직접 상호성(direct reciprocity), 간접 상호성(indirect reciprocity), 네트워크 상호성(network reciprocity), 집단 선택(Group selection)

-   친족 선택

    -   같은 유형을 만날 확률 $$r$$ 도입
	
	$$
    \begin{align}
      Pr(ALLC|ALLC) & = r + (1-r) p \\	  
      Pr(ALLD|ALLD) & = r + (1-r)(1-p)          
    \end{align}
    $$

    -   기대 보수 
	
    $$
    \begin{align}
       V(ALLC) & = [r + (1-r) p](b-c) + (1-r)(1-p)(-c)  \\
	   & = r(1-p)b+pb-c \\
	   V(ALLD) & = (1-r)pb + [r + (1-r)(1-p)](0) \\
	   & = (1-r)pb                     
    \end{align}
    $$

    -   $$ALLC$$가 균형이 될 수 있는 조건 
	
    $$
	\begin{align}
        V(ALLC) & > V(ALLD) \\
	r(1-p)b+pb-c & > (1-r)pb \\
	   rb - c & > 0 \\
       rb > c
    \end{align}
    $$

    -   $$r$$이 충분히 커서 협력의 비용을 상쇄할 수 있어야 함

    -   $$r$$: 관련성의 계수(coefficient of relatedness) 

        -   $$\rightarrow$$ 포괄 적합도(inclusive fitness): 진화적 적합도는 속성을 공유하고 있는 미래 세대의 총 수와 관련되어 있음

        -   "we expect to find that no one is prepared to sacrifice his life for any single person but that everyone will sacrifice it when he can thereby save more than two brothers, or four half-brothers, or eight first cousins\" <a id="13">[13]</a> 

    -   우리의 경우, 혈연 관계에 국한되지는 않음 $$\rightarrow$$ 지리적 특성, 사회 관계 등 다양하게 해석 가능

-   직접 상호성

    -   게임이 반복된다고 가정

        -   그 다음 게임을 할 확률 $$w$$

        -   두 번째 게임을 할 확률 $$w$$, 세 번째 게임을 할 확률 $$w \times w = w^{2}$$, $$\ldots$$

    -   한 가지 전략을 추가: Tit-for-Tat(TFT)

        -   항상 협력으로 시작

        -   상대가 협력하면 다음 기에 협력

        -   상대가 배신하면 다음 기에 배신

    -   기대 보수

        $$
		\begin{align}
		V(ALLC|ALLC) & = (b-c) + (b-c) w + (b-c) w^{2} + \ldots = \dfrac{b-c}{1-w} \\
		V(ALLC|ALLD) & = (-c) + (-c) w + (-c) w^{2} + \ldots = \dfrac{-c}{1-w} \\
		V(ALLD|ALLC) & = (b) + (b) w + (b) w^{2} + \ldots = \dfrac{b}{1-w} \\
		V(ALLD|ALLD) & = 0 \\
		V(TFT|TFT) & = (b-c) + (b-c) w + (b-c) w^{2} + \ldots = \dfrac{b-c}{1-w} \\
		V(ALLD|TFT) & = (b) + (0) w + (0) w^{2} + \ldots = b 
		\end{align}
		$$

    -   다음 조건을 만족 할 때, TFT는 진화적으로 안정적일 수 있음
	
	    $$
        \begin{align}
                V(TFT|TFT) & > V(ALLD|TFT) \\
                \dfrac{b-c}{1-w} & > b \\
                wb & > c  
        \end{align}
        $$

        -   $$w$$가 충분히 커서, 협력자가 일회성으로 입는 손해를 상쇄할 수
            있어야 함

        -   $$\rightarrow$$ 충분히 많은 수의 게임이 반복되어야 함을 의미

    -   ALLD 는 TFT에 대해 진화적으로 안정적인가?
	
	    $$
		\begin{align}
		V(TFT|ALLD) & = (-c) + (0) w + (0) w^{2} + \ldots = -c \\
		V(TFT|ALLD) & < V(ALLD|ALLD)
		\end{align}
		$$ 

        -   ALLD 는 TFT에 대해 진화적으로 안정적

    -   이 게임의 균형은?

        -   시뮬레이션을 통해 찾아볼 수 있음

## 정리하기

1.  변이, 선별, 복제가 있을 때, 진화가 일어난다.

2.  진화 게임으로 어떤 속성 또는 행위의 확산이나 감소를 설명할 수 있다.

3.  진화적으로 안정적인 전략으로 정태적으로 돌연변이 전략이 침입하지 못하는 조건을 확인할 수 있다.

4.  복제자 동학으로 동태적으로 적합도가 높은 전략을 확인할 수 있다.

### 참고문헌
<a id="1">[1]</a>
[John Maynard Smith and George R. Price (1973). "The Logic of Animal Conflict," *Nature,* 246. 15-18.](https://doi.org/10.1038/246015a0){:target="_blank"}

<a id="2">[2]</a>
[Alberto Bisin and Thierry Verdier (2022). "Advances in the Economic Theory of Cultural Transmission," *NBER Working Papers*, 30466.](https://www.nber.org/system/files/working_papers/w30466/w30466.pdf){:target="_blank"} 

<a id="3">[3]</a>
[Robert Boyd and Peter J. Richerson (1985). *Culture and the Evolutionary Process,* University of Chicago Press.](https://press.uchicago.edu/ucp/books/book/chicago/C/bo5970597.html){:target="_blank"}

<a id="4">[4]</a>
[Richard McElreath and Robert Boyd (2007). *Mathematical models of social evolution : a guide for the perplexed,* Universtiy of Chicago Press.](https://press.uchicago.edu/ucp/books/book/chicago/M/bo4343149.html){:target="_blank"}

<a id="5">[5]</a>
[Alex Mesoudi (2011). *Cultural Evolution: How Darwinian Theory Can Explain Human Culture and Synthesize the Social Sciences,* University of Chicago Press.](https://press.uchicago.edu/ucp/books/book/chicago/C/bo8787504.html){:target="_blank"}

<a id="6">[6]</a>
[Stephen Schecter and Herbert Gintis (2016). *Game Theory in Action: An Introduction to Classical and Evolutionary Models,* Ch. 8, Princeton University Press](https://press.princeton.edu/books/hardcover/9780691167640/game-theory-in-action){:target="_blank"}

<a id="7">[7]</a>
[David Easley and Jon Kleinberg (2010). *Networks, Crowds, and Markets: Reasoning about a Highly Connected World*, Ch. 7, Cambridge University Press.](https://www.cambridge.org/core/books/networks-crowds-and-markets/A70C7855A3003FE1079C25F8397AF641){:target="_blank"}

<a id="8">[8]</a>
Schecter and Gintis (2016). Ch. 8.

<a id="9">[9]</a>
[Paul E. Smaldino (2023). *Modeling Social Behavior: mathematial and agent-based models of social dynamics of cultural evolution,* Ch. 6, Princeton University Press.](https://press.princeton.edu/books/paperback/9780691224145/modeling-social-behavior){:target="_blank"}

<a id="10">[10]</a>
Schecter and Gintis (2016). Ch. 10.

<a id="11">[11]</a>
Smaldino (2023). Ch. 6.

<a id="12">[12]</a>
[Martin A. Nowak (2006). "Five Rules for the Evolution of Cooperation," *Science*, 314. 1560-1563.](https://doi.org/10.1126/science.1133755){:target="_blank"}

<a id="13">[13]</a> 
[William D. Hamilton (1964). "The genetical evolution of social behaviour," *Journal of Theoretical Biology*, 7(1), p. 16.](https://doi.org/10.1016/0022-5193(64)90038-4){:target="_blank"}