---
layout: default
title: 행위자 기반 모형
parent: 넷로고와 파이선을 활용한 게임이론 시뮬레이션
nav_order: 1
---


# 행위자 기반 모형

## 학습개요

행위자 기반 모형의 특징과 활용 범위를 학습한다.

## 학습목표

1.  모형이 무엇인지 이해한다.

2.  행위자 기반 모형의 특징과 장단점을 설명할 수 있다.

## 주요 용어

모형, 행위자, 적응적 행동, 창발, 타당성

## 모형의 이해

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음 질문에 답을 해보자.
    > 	
    >     -   모형은 무엇인가?
    >		
    >     -   모형은 어떤 과정으로 개발되는가?
    >	
    >     -   모형의 장점은 무엇인가?
    >
    > -   다음을 해보자.
    > 	
    >     -   자신의 연구 분야에서 대표적인 모형을 설명해보자.	

-   행위자 기반 모형 [[1]](#1)

    > "Agent-based models consist not of real people but of computational objects that interact according to rules.\"

-   모형 [[2]](#2)

    > "A model is a purposeful representation of some real system.\"

-   모형의 목적: 다음 세 가지 각각 또는 중첩

    -   사물이 어떻게 작동하는 지 이해

    -   관찰된 패턴을 설명

    -   변화에 시스템의 변화가 어떻게 반응하는 지 예측

-   모형의 종류

    -   실제 사물(real objects):

    -   언어적 설명(verbal language): 다윈의 진화론

    -   그림(pen-and-paper objects with diagrams)

    -   대수(numerics)

    -   수식(algebra or arithmetics)

-   모형은 현실을 모두 반영해야 하는가?

    -   사용 목적 $$\rightarrow$$ 필터로 작동

    -   즉, 질문에 답하는 데 상관이 없거나 중요성이 충분하지 않은 현실의
        특징은 제외시켜야 함

    -   보르헤스, 『과학의 엄밀성에 대하여』(Jorge Luis Borges, *On
        Exactitude in Science*)

        > "제국의 지도학은 너무 완벽해 한 지역의 지방이 도시 하나의 크기였고, 제국의 지도는 한 지방의 크기에 달했다. 하지만 이 터무니없는 지도에도 만족 못한 지도제작 길드는 정확히 제국의 크기만 한 제국전도를 만들었는데, 그 안의 모든 세부는 현실의 지점에 대응했다. 지도학에 별 관심이 없었던 후세대는 이 방대한 지도가 쓸모없음을 깨닫고, 불손하게 그것을 태양과 겨울의 혹독함에 내맡겨버렸다. 서부의 사막에는 지금도 누더기가 된 그 지도가 남아 있어, 동물과 거지들이 그 안에 살고 있다. 온 나라에 지리학 분과의 다른 유물은 남아 있지 않다.\"

-   모형 개발 [[3]](#3)

    -   질문을 형식화(formalization)

        -   기초적인 아이디어가 필요

            -   시스템이 어떻게 작동하는가에 대한 경험적 지식, 직관 등

            -   상상(imagination)

            -   이상화(idealization)

            -   유사성

    -   핵심적인 과정과 구조에 대한 가설 수집

        -   관심있는 문제에서 핵심적인 과정과 구조를 찾는 과정

        -   영향력이 가장 큰 요소는 무엇인가?

        -   각각의 요소는 독립적인가? 상호 영향을 미치는가?

        -   다른 요소로부터 영향을 받는가?

        -   $$\rightarrow$$ 다이어그램, 흐름도, 캐리커쳐 등으로 그려볼 수도 있음

        -   말도 안될 정도로 단순한 모형일 수록 다루기 쉽고 생산적

            -   점진적으로 발전시켜 나갈 것

            -   최소한의 요소만 두고

            -   그 외는 wish list 로 $$\rightarrow$$ 이후에 중요도를 다시 평가

    -   모형 구조 선택

        -   척도(scale), 속성(entities), 상태 변수(state variables), 매개 변수(parameters), 과정(processes) 등의 결정

    -   모형 실행

        -   모형의 내부 논리 구조에 따라 모형의 작동 시킴

        -   작동을 안할 수 있음: 가설 오류 아니면 코딩 실수 때문일 수도

        -   예상보다 시간이 오래 걸릴 수도 있음

    -   모형 분석

        -   모형이 실재의 세계를 얼마나 잘 반영하고 있는 지 평가할
            기준이 필요

            -   기준은 실재 시스템을 식별하고 특징 지울 수 있는 패턴이나 규칙성에 기반해야 함

        -   우리는 모형으로부터 어떤 결론을 도출할 수 있는가?

    -   그리고 모형에 대한 평가 이후 모형을 수정 $$\rightarrow$$ 재평가 $$\rightarrow$$ 재수정 $$\cdots$$

        -   모형이 완벽하다면, 논리적으로 일관, 증거와 일치, 예측이 성공

    -   모형으로 의사소통하기

        -   그 종류는 다양

        -   좁게는 논문으로 발표

        -   넓게는 대중 등에게 지식을 전달

-   모형의 장점 [[4]](#4)

    -   적확성(Precision)

        -   언어를 사용한 모형(verbal models): 중요. 모호함이나 해석의 여지가 있음. 하지만, 아이디어나 가정에 대한 설명 등은 글로 할 수 밖에 없으며, 모호함은 유연성을 주기도 함

        -   형식 모형(formal models): 수학을 사용. 관계나 과정을 정확하고 모호하지 않게 설명 $$\rightarrow$$ 모형을 현실에 대응시키는 문제는 남아 있지만, 우리는 이를 고려하지 않음

    -   추적 가능(Tractability)

        -   현실적으로 시간, 자원, 인과성, 윤리 등 연구의 제약이 많음

        -   모형을 사용하여 결론에 도달하는 논리적 과정을 추적할 수 있음

        -   자원과 윤리적 제약 등으로 실험해보기 어려운 반사실적 추론(counterfactual inference)을 해볼 수 있음

    -   통찰(Insight)

        -   복잡한 체계를 이해할 수 있는 단순 명료한 시각을 제공

## 행위자 기반 모형

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음 질문에 답을 해보자.
    > 	
    >     -   행위자 기반 모형은 무엇인가?
    >		
    >     -   행위자 기반 모형의 특징은 무엇인가?
    >	
    >     -   행위자 기반 모형의 장단점은 무엇인가?
    >
    > -   다음을 해보자.
    > 	
    >     -   행위자 기반 모형으로 설명하기 좋은 사회 현상을 찾아보자.
    > 	
    >     -   행위자 기반 모형으로 설명할 필요가 없는 사회 현상을 찾아보자.		

-   행위자 기반 모형의 정의의 재검토

    > "Agent-based models consist not of real people but of computational objects that interact according to rules.\"

    -   행위자

        -   어떤 목적을 갖고 있는 의사 결정 주체

            -   self-interested and rational economic agent.

        -   조직, 인간, 제도 등 다양하게 해석 가능

    -   계산 가능

        -   행위자의 행동 속성 및 관련된 특성을 계산할 수 있도록 함

-   행위자 기반 모형의 예

    -   감염병의 전파

        -   인구의 일정 부분이 감염병에 노출됨

        -   노출된 일부가 감염됨

        -   감염자 중 일부는 회복하지 못하거나 나머지는 회복하고 면역을 가질 것

        -   감염자 중 일부는 전파시킴

    -   $$\rightarrow$$ SIR (Susceptible - Infected - Recovered or immune)
        모형 
		
		$$
		\begin{align}
        \dfrac{dS}{dt} & = -\beta S I \\
        \dfrac{dI}{dt} & = \beta S I - \gamma I \\          
        \dfrac{dR}{dt} & =\gamma I \\
        \end{align}
		$$

        -   $$\beta$$: 감염병의 전파율

        -   $$\gamma$$: 감염병의 회복율

        -   각 식은 시간의 변화에 따라 감염될 수 있는 사람, 감염된 사람, 회복된 사람의 상대적 수를 표현

    -   단순한 모형 <!-- [[5]](#5) -->

        -   <https://github.com/psmaldino/modsoc/tree/main/ch04_contagion>{:target="_blank"}

    -   정교한 모형 <!-- [[6]](#6) -->

        -   <https://doi.org/10.1016/j.imu.2020.100403>{:target="_blank"}

-   행위자 기반 모형의 특징

    -   계산 가능성의 확장

        -   고유성/이질성 부여 가능

        -   행위자의 크기, 위치, 보유 자원, 과거 기록 등이 각기 다르게 함

    -   (국지적) 상호작용

        -   행위자는 다른 행위자와 상호작용하지만, 그들의 이웃하고만 상호작용

    -   행위 규칙

        -   모형의 목적에 따라 다양하게 결정 가능

-   장점

    -   적응적 행동(adaptive behaviors)

        -   행위자는 그 자신, 다른 행위자 그리고 환경의 현재 상태에 행동을 적응

    -   창발(emergence)

        -   시스템의 개별 구성 요소가 상호 작용 및 환경에 반응하면서 시스템 동학을 만듬

    -   분석 층위를 넘나듬

        -   시스템의 개체로 인해 시스템 차원의 사건이 발생

        -   시스템 차원의 사건으로 인해 개체도 영향을 받음

-   단점

    -   체계적인 연구 방법론을 구성하는 중

        -   연구자마다 행위자 기반 모형의 정의가 다르고,

        -   사용하는 프로그래밍 언어도 다름

        -   하지만, 공통의 기반을 만들어 가는 중

            -   ODD

    -   창발성을 설명하는 문제

        -   창발의 이유를 정확히 설명할 수 없음

        -   방정식 체계의 해로 창발을 설명할 수 있다면 행위자 기반 모형은 불필요

        -   따라서 행위자 기반 모형으로 창발을 설명하는 것은 물건을 더듬 더듬 만지는 것과 비슷한 작업

    -   모형을 현실에 적용하는 문제

        -   모형의 예측력이 현실에서도 작동할 수 있다고 선험적으로 말할 수 있는 근거는?

## 정리하기

1.  모형은 연구 목적에 따라 현실을 대표한 것이다.

2.  우리는 모형으로 작동 방식을 이해, 관찰된 패턴을 설명, 변화를 예측하려고 한다.

3.  모형으로 연구하기 위해, 최대한 단순하게 만들어 시작하고, 수정과 평가, 재수정과 재평가를 반복하는 것이 좋다.

4.  모형은 모호하지 않으며, 논리적 과정을 추적할 수 있도록 하고, 통찰력을 제공한다.

5.  행위자 기반 모형은 행동 규칙을 따르는 행위자의 상호 작용을 계산한다.

6.  행위자 기반 모형은 연구 목적에 따라 계산 가능성을 확장시키고, (국지적) 상호 작용을 반영하며, 행위 규칙을 설정할 수 있다.

7.  행위자 기반 모형은 적응적 행동, 창발을 설명하는 데 장점이 있고, 개체와 시스템 간의 상호 영향을 확인하기 좋다.

8.  행위자 기반 모형은 다양성이 너무 높다는 단점이 있고, 창발을 어떻게 설명할 지, 그리고 모형의 결과를 현실에 어떻게 적용할 지에서 많은 추가적인 연구가 필요하다.

### 참고자료

- [권오규, 김영진, 백승기, 정형채, 2022, 행위자 기반 모형의 이해와 활용, 물리학과 첨단 기술, 7-8.](https://webzine.kps.or.kr/?p=5_view&idx=16729){:target="_blank"}

- [조남운, 2016, 경제학에서의 행위자 기반 모형: 소개와 전망.](/references/Cho2016kk.pdf){:target="_blank"}

- [Bill Rand, "Agent-Based Modeling: An Initial Exploration," Complexity Explorer](https://youtu.be/Z8Wf1vF_xgQ){:target="_blank"}


### 참고문헌

<a id="1">[1]</a>
Scott E. Page (2008). "Agent-Based Models" in Steven N. Durlauf and Lawrence E. Blume eds. *The New Palgrave Dictionary of Economics.* Palgrave Macmillan.

<a id="2">[2]</a>
A. M. Starfield and Karl A. Smith and A. L. Bleoloch (1990). *How to model it: Problem solving for the computer age.* McGraw-Hill.

<a id="3">[3]</a>
[Steven F. Railsback and Volker Grimm (2019). *Agent-Based and Individual-Based Modeling: A Practical Introduction,* Second edition, pp. 7--10. Princeton University Press.](https://press.princeton.edu/books/hardcover/9780691190822/agent-based-and-individual-based-modeling){:target="_blank"}

<a id="4">[4]</a>
[Paul E. Smaldino (2023). *Modeling Social Behavior: mathematial and agent-based models of social dynamics of cultural evolution,* Princeton University Press.](https://press.princeton.edu/books/paperback/9780691224145/modeling-social-behavior){:target="_blank"}

<!-- <a id="5">[5]</a>
Smaldino (2023). Ch. 4.

<a id="6">[6]</a>
[@Gharakhanlou:2020aa]

(https://doi.org/10.1016/j.imu.2020.100403) -->