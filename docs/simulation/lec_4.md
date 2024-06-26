---
layout: default
title: 넷로고로 이해하는 분리 현상
parent: 넷로고와 파이선을 활용한 게임이론 시뮬레이션
nav_order: 4
---


# 넷로고로 이해하는 분리 현상

## 학습개요

분리 현상으로 넷로고 모형에서 반복 실험을 하는 방법과 결과를 해석하는 방법을 익힌다.

## 학습목표

1.  분리 현상이 무엇인지 설명할 수 있다.

2.  쉘링은 동질성에 대한 개인의 선호가 분리 현상의 원인일 수 있다고 생각했다. 이를 모형으로 확인한다.

3.  모형 분석 과정의 요령을 익힌다.

4.  모형 분석의 장단점을 이해한다.

## 주요 용어

분리 현상(segregation), 매개 변수, 숨은 가정, 차원성의 저주, 중립 모형, `BehaviorSpace`

## 분리 현상

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음 질문에 답을 해보자.
    > 	
    >     -   분리 현상과 쉘링의 아이디어는 무엇인가?
    >		
    >     -   분리 현상의 ODD 프로토콜을 어떻게 만들까?
    >
    > -   다음을 해보자.
    > 	
    >     -   분리 현상이 나타나는 무엇일까?
    > 	
    >     -   분리 현상을 줄여야 할까?
    > 	
    >     -   분리 현상을 줄이려면 무엇을 해야할까?

-   분리 (Segregation) [[1]](#1)[[2]](#2) 

    -   개인은, 때로는 국가도, 인종, 민족, 종교 등에 따라 지리적으로 군집(clustering)하는 것이 확인됨

    -   현실: [The New York Times, "Mapping Segregation"](https://www.nytimes.com/interactive/2015/07/08/us/census-race-map.html){:target="_blank"}

    -   이유들

        1.  조직적 행동: 거주 허가를 받아야만 해당 지역에 살 수 있음

        2.  사회경제적 필터: 인종, 종교 등 사회경제적 조건에 따라 해당 지역의 거주 기회를 가질 수 있음

        3.  개인의 선호: 자신과 비슷한 특성을 가진 사람 주변에 살고 싶어할 수 있음

    -   세 번째 이유에 주목

-   Overview

    -   목적과 패턴

        -   왜 자신이 속한 집단의 성격에 따라 이웃과 살게 되는가?

            -   집단을 나누는 기준은 다양할 수 있음: 인종, 민족, 종교 등

            -   하지만, 최소 두 개의 집단이 필요: 행위자가 속한 집단과 이 행위자가 속하지 않은 다른 집단

        -   개인의 선호에 주목 $$\rightarrow$$ 자신과 다른 정도에 대한 관용(`similarity-threshold`)

    -   독립체, 상태 변수, 척도

        -   가구: 이동이 가능 $$\rightarrow$$ `turtles`

        -   집: 이동이 불가능 $$\rightarrow$$ `patches`

        -   관용: 정의와 측정 모두 어려움 $$\rightarrow$$ 하지만, 행복에
            영향을 준다고 가정

            -   가장 간단하게는 `boolean` 변수로 $$\rightarrow$$ `happy?`

            -   특정 관용 수준 이내라면 행복, 이 수준 이상이라면
                행복하지 않음 $$\rightarrow$$ 이사

        -   척도

            -   51 $$\times$$ 51: 도로 등 지형적 특징을 반영하지 않음

            -   `Torus` $$\rightarrow$$ 실린더라면 경계 근처에서 이사, 행복 등의 계산에서 문제가 있음

            -   시간: 가구의 이동 결정을 단위로

    -   전체 과정과 스케쥴

        -   모든 가구가 행복하다면 멈춤

        -   행복하지 않은 가구는 이사 $$\rightarrow$$ 하위 모형 `move-unhappy-turtles`를 실행

            -   가구의 (이사) 순서는 중요하지 않음

        -   모든 가구는 행복(`happy?`)을 업데이트 $$\rightarrow$$ 하위 모형 `update-turtles` 를 실행

        -   결과 값 업데이트 $$\rightarrow$$ 하위 모형 `update-globals`를 실행

-   Design Concepts

    -   관심 변수

        -   관용 기준, 분리 현상

    -   창발

        -   행위자의 이사 결정으로 시스템 전체에서 분리 현상이 나타나는가?

    -   적응

        -   다른 행위자의 이사 결정에 대해 어떻게 반응하는가?

    -   목표

        -   행복 $$\rightarrow$$ 행위자는 자신과 다른 집단의 이웃이 많으면 이사

    -   지각

        -   행위자의 이웃이 자신이 속한 집단인지 아닌지

    -   확률 과정

        -   모형 초기화

        -   이사 과정 $$\rightarrow$$ 우리는 이사의 구체적인 과정이 관심사는 아님

    -   관찰

        -   가구 분포, 가구의 행복

        -   이웃 중 같은 집단의 비율, 전체에서 행복하지 않은 가구의 비율

-   Details

    -   최초 설정

        -   전체 공간 중 행위자가 차지한 비율 $$\rightarrow$$ 밀집도 `density`

        -   두 집단의 비율 $$\rightarrow$$ 전체 행위자를 두 집단에 같은 확률로 무작위 배정

    -   입력 자료

        -   기본 모형에서는 필요하지 않음

    -   하위 모형

        -   `move-unhappy-turtles`

            -   이사 기준을 확인해야 함 $$\rightarrow$$ `not happy?`

            -   이사: 무작위로 선택된 셀의 중앙으로 이동 $$\rightarrow$$ `move-to one-of`

            -   비어있는 셀로 이사해야 함 $$\rightarrow$$ `not any? turtles-here`

        -   `update-turtles`

            -   행위자의 이웃 중 같은 집단의 비율을 파악 $$\rightarrow$$ 이웃의 범위는? 
			
			    -   행위자를 중심에 둔 주변 8개의 셀로 가정: 국지적 정보라는 의미

            -   `similar-nearby`: 이웃 중 같은 집단

            -   `total-nearby`: 총 이웃

            -   `prop-similar-neighbors`: 동질성
			
			    -   `similar-nearby` / `total-nearby` $$\rightarrow$$ 이웃이 없을 때는? 행복한 것으로

            -   `similar-threshold`: 관용 기준, 0 -- 1 $$\rightarrow$$ 모든 가구에 동등하게 적용

            -   `happy?`: 행복 여부, `prop-similar-neighbors` $$\geq$$
                `similar-threshold`

        -   `update-globals`

            -   `average-similarity`: 평균 동질성

            -   `unhappiness`: 평균 불행

## 모형으로 놀아보기

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음을 할 수 있다.
    > 	
    >     -   이미 만들어진 모형을 읽을 수 있다.
    >		
    >     -   변수를 변화시키는 요령을 알 수 있다.
    >		
    >     -   필요에 따라 이미 만들어진 모형을 수정할 수 있다.
    >
    > -   다음을 해보자.
    > 	
    >     -   관심가는 모형을 인터넷에서 찾아보자.
    > 	
    >     -   찾은 모형의 구조를 해석해보자.
    > 	
    >     -   찾은 모형으로 자신의 관심사를 연구하기 위해서는 무엇을 수정해야할 지 생각해보자.

-   다음 두 코드의 ODD 프로토콜 및 코드 자체를 서로 비교해보자.

    1.   [`segregation.nlogo`](https://github.com/psmaldino/modsoc/blob/main/ch03_schelling/segregation.nlogo){:target="_blank"} [[3]](#3)  

    2.   `Models Library` $$\rightarrow$$ `Sample Models` $$\rightarrow$$ `Social Science` $$\rightarrow$$ `Segregation`

         -   위 모형과 이사, 관용 기준, 동질성 계산 방법이 다소 다름

         -   하지만, ODD, 더 나아가 우리의 연구 주제에서 벗어나지는 않는 차이

-   변수를 변화시키며 결과를 관찰해보자

    -   일반적인 방법은, 극단적인 값에서 시작한 후, 전환점(tipping point)을 찾아보는 것

    -   어떤 변수를 변화시켰을 때 분명한 변화가 관찰된다면, 이 변수의 값을 고정하고, 다른 변수를 변화시켜봐야함

    -   만약 시점이 중요하다면, 한 기 씩(tick by tick) 실행해봐야할 수도 있음

-   변수를 변화시킴에 따라 시각적으로 결과의 차이를 바로 알 수 있는 도구가 있으면 좋음

    -   매개 변수, 초기 조건, 모형의 가정 등 결과에 영향을 줄 수 있는 요인에 대한 직관을 얻을 수 있음

    -   하지만, 현혹되어서도 안됨 $$\rightarrow$$ 강건한 분석이 필요

-   둘 중 어느 것으로 해보아도 되지만, [`segregation.nlogo`](https://github.com/psmaldino/modsoc/blob/main/ch03_schelling/segregation.nlogo){:target="_blank"} 로

    -   `density` 0.45, 0.90 그리고

    -   `similarity-threshold` 0.14, 0.26, 0.45 으로 바꿔가며 결과를 비교해보자.

-   `density` 와 `similarity-threshold` 를 바꿔보았을 때, 무엇을 확인할 수 있나?

    -   관용 기준이 아주 높지 않아도 거주 군집이 확인됨

-   $$\rightarrow$$ 선호가 강하지 않더라도 분리 현상이 강하게 나타날 수 있음을 시사

    -   선호의 강약은 어떻게 측정할 것인가?

    -   분리 현상의 강약은 어떻게 측정할 것인가?

        -   평균 동질성과 평균 불행이 필요했던 이유

        -   필요에 따라 관찰해야하는 결과 값을 직접 추가하고, 또 결과값을 추출할 수 있어야 함

## 실험: 변화와 반복 시행

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음 질문에 답을 해보자.
    > 	
    >     -   어떤 변수를 변화할 지, 반복 시행의 횟수를 몇 번으로 할 지 결정하는 기준은 무엇인가?
    >		
    >     -   `BehavioralSpace`를 어떻게 사용하는가?
    >		
    >     -   분리 모형의 함의는 무엇인가?
    >
    > -   다음을 해보자.
    > 	
    >     -   분리 현상에 대한 최근 연구를 찾아보자.
    > 	
    >     -   분리 현상을 개선하기 위한 실제 정책을 찾아보자.

-   행위자 기반 모형

    -   장점: 행위자 다양성, 현실과 유사한 체계

    -   단점: 확률 과정, 불확실성 $$\rightarrow$$ 동일한 초기 조건이라도 결과값이 다를 수 있음

-   동일한 조건으로 반복 시행이 필요

    -   반복 시행으로 얻은 결과값 $$\rightarrow$$ 통계 분석

-   몇 회의 반복 시행이 필요한가?

    -   정답은 없음("It depends.\")

    -   변수가 많을 수록 더 많은 반복 시행하는 것이 일반적, 확률 과정의 효과가 증폭될 수 있으므로

    -   보통은 어떤 패턴이 안정적으로 유지될 때까지

    -   만약 안정적 패턴이 나오지 않는다면 $$\rightarrow$$ 안정적 패턴이 나오는 변수를 찾아보기도

-   매개 변수(parameters)

    -   매개 변수 값은 기존의 실증 연구로부터 차용하기도 함

    -   아니면, 이론에 근거하기도 함
	
	    -   개별적인 선호가 영향을 줄 수 있다는 쉘링의 가정처럼

    -   모형의 결과가 매개 변수의 값에 따라 달라지는 경우가 많음 
	
	    -   $$\rightarrow$$ 매개 변수의 효과를 체계적으로 기록하는 것이 좋음

-   숨은 가정(hidden assumptions)

    -   지금 분리 모형의 경우

        -   개체군에 2개의 집단만 있음

        -   각 집단의 크기는 대략 비슷

        -   이웃을 근접한 8개의 `pateches`로만 정의

        -   이사 비용이 없음

        -   관용 기준에 따라 이사하거나 이사하지 않거나, 2개의 선택만 있음

        -   모든 행위자의 관용 기준은 동일함

        -   $$\rightarrow$$ 더 많은 가정이 숨어 있을 수 있음

        -   $$\rightarrow$$ 눈에 잘 안 띄는, 임의적이고 암묵적인 가정이 모형의 결과에 영향을 미칠 수도 있음

-   차원성의 저주(the curse of dimensionality)

    -   모든 가정의 영향을 검토하기는 어려움 $$\rightarrow$$ 가능성이 너무 많음

    -   만약 8개의 매개 변수, 5번의 반복 시행 조합, 1번의 반복 시행 조합에서 100회의 시뮬레이션이 있다면
	
	    -   총 시뮬레이션 횟수는 $$5^{8} \times 100 = 39,062,500$$ 회

    -   변수의 증가에 따라 시뮬레이션 횟수는 지수적으로 증가

    -   컴퓨터 성능의 향상과 가격의 하락으로 시뮬레이션 횟수는 증가 $$\rightarrow$$ 하지만, 여전히 너무 많은 횟수는 문제

    -   이 문제를 해결하기 위한 왕도는 없음 [[4]](#4)

-   중립 모형(neutral model or null model)

    -   핵심적인 가설을 무시하고 변수의 효과를 볼 수도 있음

    -   지금 분리 모형의 경우, 이웃의 속성과 행복과 무관하게, 행위자의 이사 결정이 무작위(randomly)로 이뤄진다면 어떤 결과가 나올까?

        -   $$\rightarrow$$ 이사 결정에 대해 새로운 코드를 짜야 함 $$+$$ 집단 구분의 영향을 없애야 함

    -   그러나, 중립 모형으로 어떤 변수가 결과에 큰 영향을 준다고 하더라도, 이는 상관 관계일 뿐이지, 그 자체로 인과 관계(causal relations)를 의미하지 않음

-   다시 모형으로 돌아와서

    -   밀집도와 관용 기준을 변화시키면서, 빠르게 균형에 도달하거나 아니면 균형에 도달하지 않는 경우도 확인했을 것 $$\rightarrow$$ 좀 더 강건한 결과를 확인해보자

    -   `density`: 0.1 부터 0.9 까지 0.1 씩 증가

    -   `similarity-threshold`: 0.05 부터 0.70 까지 0.05 씩 증가

    -   각 조합에 대해 100 `ticks` 동안 시뮬레이션 진행

    -   각 시뮬레이션을 100번 시행

    -   변수 값의 범위는 임의로 선택한 것 $$\rightarrow$$ 결정은 필요, 더 넓은 범위로 할 수도 있음. 이론에 의한 뒷받침되거나 또는 모형을
        계속 다루면서 쌓이는 경험을 따르거나

-   넷로고: 메뉴 중 `Tools` $$\rightarrow$$ `Behavior Space`

    -   우리 분리 모형의 경우, 이미 입력되어 있음

    -   새로 만들고자 한다면, `New` 를 누르고

    -   수정하고자 한다면, 대상 선택 후 `Edit`를 누르고

    -   `Experiment Name` 쓰고,

    -   변수 변화: 기본 구조 `["변수명" [시작값 증가값 최종값]]`

    -   `Repetitions`: 반복횟수

    -   조합을 순차적으로 시행하도록 체크

    -   결과값

    -   `Time limit`: 한 회의 시행 기간

-   `Run`을 누르면

    -   `Table output` 사용을 권고: 분석하기 위한 구조로 바꾸기 용이함

    -   `Update ..` 는 계산 시간을 늘리므로, 체크하지 않는 것을 권고

-   결과

    -   `similarity-threshold`를 가로축, `average-similarity`를 세로축으로 각각의 `density`에 대해 그래프를 그려보자

    -   `average-similarity`: 행위자와 같은 집단이 이웃에 있는 비율이 높을 수록 분리 현상이 강하다고 할 수 있음

    -   `similarity-threshold`가 높을 수록 분리가 더 잘 관찰됨

    -   `similarity-threshold` 보다 `average-similarity`가 항상 높음 
	
	    -   $$\rightarrow$$ 이웃에 대한 선호가 강하지 않더라도, 집단 전체에서는 분리 현상이 나타남을 시사

    -   낮은 `density`에서도 분리가 잘 관찰됨

-   수정

    -   이웃이 없는 경우 행복한 것으로 가정했음 $$\rightarrow$$ 하지만 외로우므로 행복이 0일 수도 있음

    -   그 결과는? 이전의 결과와 비교하면? $$\rightarrow$$ 직접 해보자

-   모형에 의한 설명에 만족할 수 있을까? $$\rightarrow$$ 후속 연구의 아이디어

    -   우리는 단지, 개인의 선호에 의해 분리 현상이 나타날 수 있음
	
	-   그리고 낮은 동질성 수준에서도 쉽게 나타날 수 있음을 설명

    -   분리는 제도나 경제적 제약 등으로도 나타날 수 있음

        -   $$\rightarrow$$ 하지만, 우리의 설명이 맞다면 소득 수준, 교육 수준이 동일하더라도, 개인의 작은 선호로도 분리가 나타날 것
		
		-   과연?

    -   모형 자체에 대한 가정도 검토해볼 수 있음

        -   이사의 비용을 고려하지 않음 $$\rightarrow$$ 사회적 관계 (가족, 친구, 직장 등)가 제약 조건이 될 수도 있음

## 정리하기

1.  개인, 때로는 국가도 인종, 민족, 종교 등에 따라 지리적으로 군집하는 것을 분리 현상이라고 한다.

2.  분리 현상의 이유는 다양하겠지만, 쉘링은 개인의 선호가 이유일 수 있음을 생각했다.

3.  원인이 되는 변수를 찾기 위해

    1.  극단적으로 변수 값을 바꿔볼 수 있다.

    2.  변화가 확인되면 영향을 주는 것으로 여겨지는 변수의 값은 고정하고, 다른 변수의 값을 변화시킨다.

    3.  한 기마다 시행할 수도 있다.

4.  변수 변화에 따른 결과의 변화를 시각적으로 확인할 필요도 있다.

5.  모형을 다루면서 어떤 변수를 변화 시킬지, 반복 시행의 횟수 등을 결정하기도 한다.

6.  매개 변수, 숨은 가정 등 변화할 수 있는 요소는 많지만, 다양성이 높아질 수록 계산량이 많아지는 문제가 있다.

7.  `BehaviorSpace`를 사용해 반복 시행을 할 수 있다.

8.  쉘링의 아이디어에 따른 분리 모형은 개별 행위자가 원하는 동질성 수준이 낮더라도 분리 현상이 나타날 수 있음을 보여준다.

9.  모형의 결과는 향후 연구 방향의 시작이기도 하다.

### 참고자료

- [Bill Rand, "Agent-Based Modeling: Schelling's Tipping Model," Complexity Explorer](https://youtu.be/9Hu-50BNVBc){:target="_blank"}

### 참고문헌

<a id="1">[1]</a>
[Thomas C. Schelling (1971). "Dynamic Models of Segreation." *Journal of Mathematical Sociology.* 1(3). 143--186.](https://doi.org/10.1080/0022250X.1971.9989794){:target="_blank"}


<a id="2">[2]</a>
[Thomas C. Schelling (2006). *Micromotives and Macrobehavior.* W.W. Norton & Company.](https://wwnorton.com/books/Micromotives-and-Macrobehavior/){:target="_blank"}

<a id="3">[3]</a>
[Paul E. Smaldino (2023). *Modeling Social Behavior: mathematial and agent-based models of social dynamics of cultural evolution,* Ch. 3, Princeton University Press.](https://press.princeton.edu/books/paperback/9780691224145/modeling-social-behavior){:target="_blank"}

<a id="4">[4]</a>
[Ligmann-Zielinska et. al. (2020). "'One Size Does Not Fit All': A Roadmap of Purpose-Driven Mixed-Method Pathways for Sensitivity Analysis of Agent-Based Models." *Journal of Artificial Societies and Social Simulation.* 23(1). 6.](https://doi.org/10.18564/jasss.4201){:target="_blank"}