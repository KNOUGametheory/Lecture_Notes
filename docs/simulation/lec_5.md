---
layout: default
title: 넷로고로 이해하는 협력
parent: simulation
nav_order: 5
---


# 넷로고로 이해하는 협력

## 학습개요

넷로고 모형에서 협력의 진화를 다각도로 검토하는 방법을 익힌다.

## 학습목표

1.  협력의 진화를 설명할 수 있다.

2.  죄수의 딜레마 게임에 대한 ODD 프로토콜을 작성할 수있다.

3.  모형을 실행하며 모형의 변화 방향을 찾을 수 있다.

## 주요 용어

협력, 친족 선택, 직접 상호성, 간접 상호성, 네트워크 상호성, 집단 선택,
죄수의 딜레마 게임, TFT 전략

## 협력의 진화

-   협력(cooperation)

    -   다른 개체와 함께 행동하는 것

-   인간: 비혈연관계의 대규모 협력

    -   비혈연관계의 소규모: 생태계에서 개별 개체의 공생 관계 등

    -   혈연관계의 소규모: 군집생활을 하는 유인원 등

    -   혈연관계의 대규모: 개미군 등

-   협력하는 집단은 협력을 하지 않는 집단에 비해 유리할 수 있음. 하지만,
    협력이 당연할까?

    -   조별과제를 기피하는 것을 생각해보자

-   죄수의 딜레마 게임

    -   상호 배신이 유일한 내쉬 균형

-   협력의 유지를 설명 [@Nowak:2011aa Chs. 1--5]

    -   친족 선택(kin selection)

        -   Hamilton' Rule: $rb > c$ $\rightarrow$
            $\dfrac{b}{c} > \dfrac{1}{r}$ [@Hamilton:1964aa]

            -   $r$: 관련성의 계수(coefficient of relatedness)

            -   $c$: 비용

            -   $b$: 이득

            -   $\rightarrow$ 비용과 이득의 비율이 중요

        -   포괄적 적합도(inclusive fintness)

            -   자손의 번식 또는

            -   동일한 유전자를 갖고 있는 친척의 번식

        -   제한점: 매우 작고 정태적인 개체군이어야 함

    -   직접 상호성(direct reciprocity)

        -   죄수의 딜레마 게임 $\rightarrow$ 반복: 직접적인 관계에서의
            기억

            -   $wb > c$ $\rightarrow$ $\dfrac{b}{c} > \dfrac{1}{w}$:
                반복의 가능성이 높을 수록 협력의 가능성이 높음

        -   Tit-for-Tat 전략

            -   협력으로 시작

            -   협력에 대해서는 그 다음 게임에 협력

            -   배신에 대해서는 그 다음 게임에 배신

        -   제한점: 같은 경기자를 반복적으로 만나야 함

    -   간접 상호성(indirect reciprocity)

        -   평판(reputation)

        -   $qb > c$ $\rightarrow$ $\dfrac{b}{c} > \dfrac{1}{q}$: 평판을
            알고 있을 확률 $q$ 가 충분히 커야 함

        -   $\rightarrow$ 간접적인 관계에서의 기억

            > "For direct reciprocity you need a face, for indirect
            > reciprocity you need a name (David Haig).\"

        -   평판의 다른 효과 $\rightarrow$ 부정적 평판을 가진 주체에
            대한 처벌

            -   처벌: 자신의 비용을 들여 상대방의 편익을 감소시키거나
                비용을 증가시키는 행위

            -   처벌을 함으로써 (처벌의 비용보다 더 큰) 이득이 발생하지
                않는다면, 경제적 합리성에 위배

        -   언어, 지적 능력 등이 함께 발달해야 함

    -   네트워크 상호성(network reciprocity)

        -   지리적 근접성: 완전히 뒤섞이지 않고, 특정 개체와 더 자주
            접한다면

        -   $\rightarrow$ 일반화하여 생각하면 네트워크에서의 거리가
            가깝다면

        -   $k$: 이웃의 평균 수

            -   $\dfrac{b}{c} > k$

        -   협력자 군집에서 협력이 융성할 수 있음

    -   집단 선택(group selection)

        -   또는 다층 선택(multilevel selection)

        -   집단 내 비 협력 $\rightarrow$ 개체에게는 비 협력이 유리,
            집단 간 경쟁에는 불리

        -   집단 내 협력 $\rightarrow$ 개체에게는 협력이 불리, 집단 간
            경쟁에는 유리

        -   개체의 집단 간 이동성이 낮고, 집단 간 경쟁이 일정 수준
            이상으로 강해야 함

            -   $\dfrac{b}{c} > \dfrac{m+n}{m}$

            -   집단의 최대 크기 $n$, 집단의 수 $m$

## 죄수의 딜레마 게임

-   Overview [@Smaldino:2023aa Ch. 6]

    -   목적과 패턴

        -   다음과 같은 보수 구조의 죄수의 딜레마 게임에서 협력이 유지될
            조건은 무엇인가?

            :::: center
            ::: game
            22\[$P_{1}$\]\[$P_{2}$\] $C$ $D$\
            $C$ $b-c, b-c$ $-c, b$\
            $D$ $b, -c$ $0, 0$
            :::

            \
            ::::

        -   게임을 한 후 이웃한 다른 경기자와 비교하여 더 높은 보수를
            받는 전략을 학습

    -   독립체, 상태 변수, 척도

        -   경기자: 이동이 가능 $\rightarrow$ `turtles`

        -   전략: 경기자가 갖고 있는 속성 $\rightarrow$ `strategy`

            -   협력, 배신

            -   두 개의 전략이 있으므로 두 개의 색으로 구분할 수 있도록
                하자

        -   보수: 게임의 결과에 따라 결정 $\rightarrow$ `payoff`

        -   척도

            -   공간: 일단 추상적 공간으로

            -   시간: 경기자의 게임 시행과 학습을 한 단위로

    -   전체 과정과 스케쥴

        -   경기자의 전략이 협력 또는 배신 중 어느 하나로 수렴하면 멈춤

        -   게임 시행 $\rightarrow$ 하위 모형 `play-game`을 실행

            -   근접한 이웃과 게임

            -   우리는 게임의 보수를 알고 있으므로 경기자의 속성(전략)에
                따라 게임의 기대 보수를 계산할 수 있음

            -   $V(C) = n_{c}(b-c)-n_{D}c$

            -   $V(D) = n_{c}b$

            -   $n_{c}, n_{d}$: 각각 상대 경기자 중 협력자, 배신자의 수

        -   모든 경기자는 전략을 업데이트 $\rightarrow$ 하위 모형
            `evolve` 를 실행

            -   게임을 한 이웃과 비교해 보수가 가장 높은 전략을 모방

        -   경기자의 전략 변경에 맞춰 경기자의 색을 변경 $\rightarrow$
            하위 모형 `recolor`를 실행

-   Design Concepts

    -   관심 변수

        -   협력자의 최초 비중

        -   비용과 이득의 비율 $\dfrac{c}{b}$

        -   협력자의 최종 비중

    -   창발

        -   경기자의 전략 학습으로 시스템 전체에서 전략의 수렴이
            나타나는가?

    -   적응

        -   다른 경기자의 보수 변화에 대해 어떻게 반응하는가?

    -   목표

        -   이웃과 비교하여 보수를 높이는 것

    -   지각

        -   상대 경기자의 전략과 보수

    -   확률 과정

        -   모형 초기화

    -   관찰

        -   협력자의 분포

-   Details

    -   최초 설정

        -   공간: 31 $\times$ 31, Torus $\rightarrow$ 게임 후 학습
            과정이 있으므로

        -   협력자의 비율 $\rightarrow$ `init-coop-freq`

        -   보수 비율 $\rightarrow$ `payoff-benefit`, `payoff-cost`

    -   입력 자료

        -   기본 모형에서는 필요하지 않음

    -   하위 모형

        -   `play-game`

            -   매 게임마다 보수를 0으로 초기화할 지, 아니면 누적할 지
                $\rightarrow$ 일단, 초기화

            -   어떤 이웃과 게임할 지 $\rightarrow$ `neighbors4`:
                경기자를 중심에 둔 주변 4개의 셀(동서남북)로 가정

            -   이웃 중 협력자와 배신자의 수를 알아야 함 $\rightarrow$
                `let neighbors-C`, `count`, `with`

            -   게임 시행 후 보수 결정 $\rightarrow$ `set payoff`

        -   `evolve`

            -   경기자의 이웃 중 높은 보수를 파악 $\rightarrow$ 이웃의
                범위는? 게임 대상과 일치

            -   `best-neighbor`: 가장 높은 보수를 가진 이웃

            -   자신의 보수와 가장 높은 보수를 가진 이웃의 보수를 비교

            -   예제 코드: 순차적으로 전략을 학습하므로, 가장 높은
                보수를 가진 이웃의 전략을 학습한다는 보장이 없음

        -   `recolor`

            -   전략에 따라 경기자의 색을 구분

            -   초기 설정에 포함되지 않을까?

-   <https://github.com/psmaldino/modsoc/tree/main/ch06_cooperation>
    $\rightarrow$ $PD_simple.nlogo$

-   최초 협력자 $0.5$, $b=1$ 고정, $c$ 비율만 조정

    -   $c = 0.1, 0.9$ 의 결과를 비교해보자

    -   $c = 0.2, 0.3, 0.4, 0.5, 0.6$ 을 비교해보자

    -   $c = 0.25$를 해보자 $\rightarrow$ 극적인 변화가 있음

    -   $0.25 < c < 0.5$에서 협력이 완전히 사라지지 않음

-   왜 그럴까?

    -   협력자의 이웃 경기자 중 협력자가 둘이라면, 이 협력자의 보수는
        $2(b-c)-2c = 2b-4c$

    -   배신자의 이웃 경기자 중 협력자가 하나라면, 이 배신자의 보수는
        $b$

    -   $2b-4c > b$ $\rightarrow$ $\dfrac{b}{4}>c$ 라면 협력이 확산됨

    -   협력자의 이웃 경기자 중 협력자가 넷이라면, 이 협력자의 보수는
        $4(b-c) = 4b-4c$

    -   협력자의 이웃 경기자 중 협력자가 둘이라면, 이 협력자의 보수는
        $2b$

    -   $4b-4c > 2b$ $\rightarrow$ $\dfrac{b}{2}>c$

-   $\rightarrow$ 협력 비용의 상대적 크기와 함께, 협력자의 군집은 협력의
    생존에 영향을 줄 수 있음

## 죄수의 딜레마 게임의 진화

-   기본 모형에서는 경기자의 위치, 즉 게임 상대가 고정되어 있었음
    $\rightarrow$ 게임 상대를 무작위로 바꾼다면

    -   <https://github.com/psmaldino/modsoc/tree/main/ch06_cooperation>
        $\rightarrow$ $PD_randomized.nlogo$

    -   `randomize-locations` 도입

-   게임의 반복, 항상 협력(ALLC), 항상 배신(ALLD), TFT 전략을 비교

    -   TFT: Tit for Tat

        -   항상 협력으로 시작

        -   상대가 협력하면 다음 기에 협력

        -   상대가 배신하면 다음 기에 배신

    -   게임을 $k$ 번 반복할 때의 경기자 1의 보수표

        :::: center
        ::: game
        33\[$P_{1}$\]\[$P_{2}$\] $ALLC$ $TFT$ $ALLD$\
        $ALLC$ $k(b-c)$ $k(b-c)$ $-kc$\
        $TFT$ $k(b-c)$ $k(b-c)$ $-c$\
        $ALLD$ $kb$ $b$ $0$\
        :::

        \
        ::::

    -   기대 보수

        -   $V(ALLC) = kn_{c}(b-c)-kn_{D}c$

        -   $V(TFT) = kn_{c}(b-c)-n_{D}c$

        -   $V(ALLD) = kn_{c}b$

-   <https://github.com/psmaldino/modsoc/tree/main/ch06_cooperation>
    $\rightarrow$ $PD_reciprocity.nlogo$

    -   `TFT?`

        -   `true` $\rightarrow$ TFT

        -   `false` $\rightarrow$ ALLC

        -   `recolor`에도 TFT 할당 필요

    -   반복 횟수: `num-iterations`

    -   보수 변화 $\rightarrow$ `play-game` 수정

    -   TFT가 작동하는지 확인 $\rightarrow$ $k=1$ 시행

-   최초 협력자 $0.5$, $b=1$, $c=0.25$, $randomization-prob=0$, $k=4$
    시행

    -   $\rightarrow$ 모두 TFT

-   직전의 조건에서 $randomization-prob=1$로

    -   $\rightarrow$ 모두 TFT

-   직전의 조건에서 $c=0.7$로

    -   $\rightarrow$ 모두 D

-   최초 협력자 $0.05$, $c=0.3$, $randomization-prob=0.1$ 로

    -   $\rightarrow$ 모두 TFT

    -   TFT의 강력한 힘 [@Axelrod:1984dz]

-   하지만, TFT 보다 보수가 더 큰 전략이 있음

    -   $<$ Generous TFT: 배신 전략을 경험하더라도 일정 확률로 그 다음
        게임에 협력

    -   $<$ win-stay, lose-shift: 직전 게임에서 상호 협력했다면
        $\rightarrow$ 다음 게임에도 협력 / 상호 배신했다면 $\rightarrow$
        일정 확률로 협력 / 상대만 협력했다면 $\rightarrow$ 배신 / 상대만
        배신했다면 $\rightarrow$ 배신

-   이외에도 다양한 변형이 가능

    -   행동 실험 또는 행동 게임과도 결합 [@Camerer:2003fk]

    -   문화적 차이 [@Henrich:2005aa]

-   보수 구조에 따라 다른 게임도 모형으로 만들 수 있음

    -   매-비둘기 게임, 사슴 사냥 게임, 공공재 게임 등

-   넷로고의 단점

    -   `Java`, `Scala` 언어로 프로그램되어 있음 $\rightarrow$ `Java`로
        바로 시뮬레이션 하는 것보다 느림

    -   `primitive`는 매우 유용하지만, `primitive` 외의 다른 무엇을
        반영하고자 하는 모형 설계에서는 제약이 될 수 있음

## 정리하기

1.  인간 협력은 비혈연관계에서의 대규모 협력이라는 특징을 갖고 있다.

2.  죄수의 딜레마 게임을 다양하게 변형하여 협력을 연구할 수 있다.

3.  방정식 체계를 시뮬레이션 모형으로 만들었을 때, 예상하지 못한 결과가
    나타날 수 있지만, 예상하지 못한 결과는 연구의 출발점이기도 하다.

4.  넷로고는 속도가 느리다는 점과 연구자의 의도를 모두 구현하는 데에는
    한계가 있다는 단점이 있다.
