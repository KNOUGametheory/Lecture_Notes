---
layout: default
title: 전개형 게임의 응용
parent: 게임이론
nav_order: 7
---

# 전개형 게임의 응용
d
<!-- 1.  선점 효과 복점 모형

2.  선점 효과의 측정

3.  입지와 가격 결정 -->

## 1.  선점 효과 복점 모형

### 학습목표

-   다음 질문에 대해 답을 할 수 있다.

    -   선도자와 추종자를 구분하는 기준은 무엇일까?

    -   선점 효과를 반영하기 위해어떤 모형에 어떤 가정을 추가/완화해야 할까?

    -   선점했을 때 차이는 어느 정도일까?

-   다음 문제를 생각해보자.

    -   과점 시장에서 선도 효과는 어떻게 반영될까?

-   ★ 핵심만 쏙쏙!

    {: .note}
	> **선점 효과는 최적 대응으로 고정하여 반영!**

### 선점 효과를 반영한 복점 모형

-   선점 효과를 고려하지 않은 모형: 쿠르노 복점 모형

    -   두 기업이 제품을 공급하는 과점인 복점에서 생산량으로 경쟁하는 상황을 모형화

    -   경쟁의 결과 및 영향, 담합의 안정성 등 설명 가능

-   쿠르노 복점 모형의 가정

    -   시장의 역수요함수 (단, $$a > 0$$는 시장 규모)

        $$P = a - Q$$ 

    -   시장의 공급량 

        $$Q = q_{1} + q_{2}$$

    -   기업 $$i$$는 이윤 $$\pi_{i}$$ 극대화를 위해 공급량 $$q_{i}$$를 결정

-   선점 효과(First-mover’s Advantage)

    -   쿠르노 복점 모형에서는 두 기업이 생산량을 동시에 결정

    -   현실적으로 두 기업의 생산량 결정 시점에 차이 존재 가능

    -   두 기업의 교섭력(bargaining power) 차이로 인해 생산량 결정에 대한 우선순위에 차이가 존재 가능

-   선도자와 추종자

    -   선도자(leader): 먼저 생산량 결정 또는 더 큰 교섭력

    -   추종자(follower): 나중에 생산량 결정 또는 더 작은 교섭력

-   선점 효과를 반영한 모형:

    스타켈버그(Stackelberg, 1934) 복점 모형

    -   쿠르노 복점 모형의 가정에 생산량 결정 순서를 반영

    -   선도자(기업 1)가 생산량을 먼저 결정

        추종자(기업 2)는 선도자의 생산량 결정에 최적으로 대응

    -   선도자와 추종자의 생산량의 합으로 시장 생산량 결정

    -   시장의 역수요함수 $$P = a - Q$$ (단, $$a > 0$$는 시장 규모)에 따라
        시장 청산 가격(market-clearing price) 및 이윤 결정

-   스타켈버그(Stackelberg, 1934) 복점 모형의 게임나무

    -   연속적인 생산량을 부채꼴 모양으로 표현

        ![표](/images/Lec_7_1_1_1.png)

    -   게임의 진행 순서

        -   기업 1(선도자)이 생산량 $$q_{1}$$ 결정

        -   기업 1의 생산량 $$q_{2}$$ 관찰 후 기업 2(추종자)가 생산량 $$q_{2}$$ 결정

        -   시장 생산량 $$Q = q_{1} + q_{2}$$에 따라 시장 청산 가격과 각 기업의 이윤 결정


### 선점 효과를 반영한 복점 모형의 균형

-   모형의 풀이

    -   역진귀납법을 적용하여 게임 순서의 역순으로 풀이

    -   기업 2의 이윤 (여기에서, $$c$$는 생산의 평균 비용이자 한계 비용)

        $$\pi_{2} = Pq_{2} - cq_{2} = (P - c)q_{2}$$

    -   시장의 수요 함수($$P = a - Q$$)를 $$\pi_{2}$$에 대입

        $$
        \begin{align}
        \pi_{2} & = \left\lbrack (a - Q) - c \right\rbrack q_{2} \\
        & = \left\lbrack \left( a - \left( q_{1} + q_{2} \right) - c \right) \right\rbrack q_{2} \\
        & = \left\lbrack a - c - q_{1} - q_{2} \right\rbrack q_{2}
        \end{align}
        $$

    -   $$\pi_{2}$$을 최대화하는 생산량 $$q_{2}$$를 결정

        -   일계조건(First-order condition)
            $$\left. \ \frac{\partial\pi_{2}}{\partial q_{2}} \right\vert_{q_2 = \widetilde{q_2}} = 0$$

            $$
            \begin{align}
            \frac{\partial\pi_{2}}{\partial q_{2}} & = - q_{2} + \left\lbrack a - c - q_{1} - q_{2} \right\rbrack \\
            & = a - c - q_{1} - 2q_{2} \\
            \left. \ \frac{\partial\pi_{2}}{\partial q_{2}} \right\vert_{q_2 = \widetilde{q_2}} & = 0 \\
            \rightarrow \widetilde{q_{2}} & = \frac{a - c - q_{1}}{2}
            \end{align}
            $$

            기업 1의 생산량에 대한 기업 2의 최적 대응

        -   이계조건(Second-order condition)
            $$\left. \ \frac{\partial^{2}\pi_{2}}{\partial q_{2}^{2}} \right\vert_{q_2 = \widetilde{q_2}} \leq 0$$

            $$
            \begin{align}
            \frac{\partial^{2}\pi_{2}}{\partial q_{2}^{2}} & = \frac{\partial}{\partial q_{2}}\left( \frac{\partial\pi_{2}}{\partial q_{2}} \right) \\
            & = \frac{\partial}{\partial q_{2}}\left( a - c - q_{1} - 2q_{2} \right) \\
            & = - 2 \leq 0
            \end{align}
            $$

    -   기업 1의 이윤 (여기에서, $$c$$는 생산의 평균 비용이자 한계 비용)

        $$\pi_{1} = Pq_{1} - cq_{1} = (P - c)q_{1}$$

    -   시장의 수요 함수($$P = a - Q$$)를 $$\pi_{1}$$에 대입

        $$
        \begin{align}
        \pi_{1} & = \left\lbrack (a - Q) - c \right\rbrack q_{1} \\
        & = \left\lbrack \left( a - \left( q_{1} + q_{2} \right) - c \right) \right\rbrack q_{1} \\
        & = \left\lbrack a - c - q_{1} - q_{2} \right\rbrack q_{1}
        \end{align}
        $$

    -   $$\pi_{1}$$에 기업 2의 최적 대응($$\widetilde{q_{2}} = \frac{a - c - q_{1}}{2}$$)을 대입

        $$\widetilde{\pi_{1}} = \left\lbrack a - c - q_{1} - \left( \frac{a - c - q_{1}}{2} \right) \right\rbrack q_{1} = \left( \frac{a - c - q_{1}}{2} \right)q_{1}$$

    -   기업 2의 최적 대응을 반영한 상태에서 계산한 기업 1의 이윤 $$\widetilde{\pi_{1}}$$을 최대화하는 생산량 $$q_{1}$$을 결정

        -   일계조건(First-order condition)
            $$\left. \ \frac{\partial\widetilde{\pi_{1}}}{\partial q_{1}} \right\vert_{q_1 = \widehat{q_1}} = 0$$

            $$
            \begin{align}
            \frac{\partial\widetilde{\pi_{1}}}{\partial q_{1}} & = - \frac{q_{1}}{2} + \frac{a - c - q_{1}}{2} \\
            & = \frac{a - c}{2} - q_{1} \\
            \left. \ \frac{\partial\widetilde{\pi_{1}}}{\partial q_{1}} \right\vert_{q_1 = \widehat{q_1}} & = 0 \\
            \rightarrow \widehat{q_{1}} & = \frac{a - c}{2}
            \end{align}
            $$

        -   이계조건(Second-order condition)
            $$\left. \ \frac{\partial^{2}\widetilde{\pi_{1}}}{\partial q_{1}^{2}} \right\vert_{q_1 = \widehat{q_1}} \leq 0$$

            $$
            \begin{align}
            \frac{\partial^{2}\widetilde{\pi_{1}}}{\partial q_{1}^{2}} & = \frac{\partial}{\partial q_{1}}\left( \frac{\partial\widetilde{\pi_{1}}}{\partial q_{1}} \right) \\
            & = \frac{\partial}{\partial q_{1}}\left( \frac{a - c}{2} - q_{1} \right) \\
            & = - 1 \leq 0
            \end{align}
            $$

-   모형의 균형

    -   균형 생산량

        -   기업 1의 균형 생산량

            $$\widehat{q_{1}} = \frac{a - c}{2} = \frac{1}{2}(a - c)$$

        -   기업 2의 균형 생산량

            $$\widehat{q_{2}} = \frac{a - c}{4} = \frac{1}{4}(a - c)$$

            (기업 2의 최적 대응
            $$\widetilde{q_{2}} = \frac{a - c - q_{1}}{2}$$에
            $$q_{1} = \frac{a - c}{2}$$을 대입)

        -   시장의 균형 생산량

            $$\widehat{Q} = \widehat{q_{1}} + \widehat{q_{2}} = \frac{3}{4}(a - c)$$

    -   균형 가격

        $$\widehat{P} = a - \widehat{Q} = a - \frac{3}{4}(a - c) = \frac{a + 3c}{4}$$

    -   균형 이윤

        -   기업 1의 균형 이윤

            $$\widehat{\pi_{1}} = \left( \widehat{P} - c \right)\widehat{q_{1}} = \left\lbrack \left( \frac{a + 3c}{4} \right) - c \right\rbrack\left\lbrack \frac{1}{2}(a - c) \right\rbrack = \frac{1}{8}(a - c)^{2}$$

        -   기업 2의 균형 이윤

            $$\widehat{\pi_{2}} = \left( \widehat{P} - c \right)\widehat{q_{2}} = \left\lbrack \left( \frac{a + 3c}{4} \right) - c \right\rbrack\left\lbrack \frac{1}{4}(a - c) \right\rbrack = \frac{1}{16}(a - c)^{2}$$



### 요약

-   선도자와 추종자를 구분하는 기준은 무엇일까?

    -   생산량을 결정하는 순서, 기업간 교섭력 차이 등

-   선점 효과를 반영하기 위해 어떤 모형에 어떤 가정을 추가/완화해야 할까?

    -   쿠르노 모형에서 생산량 동시 결정 가정을 완화

-   선점했을 때 차이는 어느 정도일까?

    -   선점하게 되면 균형 생산량 2배, 균형 이윤도 2배

## 2.  선점 효과의 측정


### 학습목표

-   다음 질문에 대해 답을 할 수 있다.

    -   스타켈버그 균형은 부분게임완전균형일까?

    -   선도 생산량이 동시 생산량보다 더 많을까?

    -   선도자와 추종자를 선택하는 게임에서 균형은?

-   다음 문제를 생각해보자.

    -   두 기업 모두 선도자이길 선택한다면 어떤 결과가 있을까? 왜 그런 결과로 귀결될까?

-   ★ 핵심만 쏙쏙!

    {: .note}
	> **'선도자' 전략을 선택하기 위해 선점 효과 측정이 필요!**

### 선점 효과를 반영한 모형의 균형

-   스타켈버그 모형의 균형

    -   균형 생산량

        -   기업 1의 균형 생산량

            $$\widehat{q_{1}} = \frac{a - c}{2} = \frac{1}{2}(a - c)$$

        -   기업 2의 균형 생산량

            $$\widehat{q_{2}} = \frac{a - c}{4} = \frac{1}{4}(a - c)$$

    -   부분게임완전내쉬균형? <span style="color:#FF0000">YES!</span>

        -   기업 1의 생산량에 따른 기업 2의 최적 대응을 고려

        -   기업 2는 최적 대응을 따르면 생산량 변경할 유인 없음!

        -   다시 한번 기업 1의 최적 생산량을 구했으므로 균형!

    -   다른 균형은 없을까?

    -   기업 2의 최적 대응($$\widetilde{q_{2}} = \frac{a - c - q_{1}}{2}$$)을 만족시키는 모든 생산량의 조합은 내쉬균형에 해당

        -   기업 1의 생산량 

            $$q_{1} = \frac{2}{3}(a - c)$$

        -   기업 2의 생산량

            $$q_{2} = \frac{a - c - \frac{2}{3}(a - c)\ }{2} = \frac{1}{6}(a - c)$$


### 선점 효과와 동시 결정의 비교

-   스타켈버그 복점 모형의 균형

    -   각 기업의 스타켈버그 균형 생산량

        -   기업 1의 스타켈버그 균형 생산량

            $$\widehat{q_{1}} = \frac{1}{2}(a - c)$$

        -   기업 2의 스타켈버그 균형 생산량

            $$\widehat{q_{2}} = \frac{1}{4}(a - c)$$

    -   각 기업의 스타켈버그 균형 이윤

        -   기업 1의 스타켈버그 균형 이윤

            $$\widehat{\pi_{1}} = \frac{1}{8}(a - c)^{2}$$

        -   기업 2의 스타켈버그 균형 이윤

            $$\widehat{\pi_{2}} = \frac{1}{16}(a - c)^{2}$$

-   쿠르노 복점 모형의 균형

    -   각 기업의 쿠르노 균형 생산량

        -   기업 1의 쿠르노 균형 생산량

            $$q_{1}^{*} = \frac{1}{3}(a - c)$$

        -   기업 2의 쿠르노 균형 생산량

            $$q_{2}^{*} = \frac{1}{3}(a - c)$$

    -   각 기업의 쿠르노 균형 이윤

        -   기업 1의 쿠르노 균형 이윤

            $$\pi_{1}^{*} = \frac{1}{9}(a - c)^{2}$$

        -   기업 2의 쿠르노 균형 이윤

            $$\pi_{2}^{*} = \frac{1}{9}(a - c)^{2}$$

-   균형 생산량 비교

    -   (추종자의 균형 생산량) $$<$$ (동시 결정 균형 생산량) $$<$$ (선도자의
        균형 생산량)

    -   $$\widehat{q_{2}} = \frac{1}{4}(a - c) < q^{*} = \frac{1}{3}(a - c) < \widehat{q_{1}} = \frac{1}{2}(a - c)$$

    -   동시 결정 $$\rightarrow$$ 선도자가 되었을 때 생산량의 증가

        $$\widehat{q_{1}} - q^{*} = \frac{1}{2}(a - c) - \frac{1}{3}(a - c) = \frac{1}{6}(a - c)$$

    -   동시 결정 $$\rightarrow$$ 추종자가 되었을 때 생산량의 감소

        $$q^{*} - \widehat{q_{2}} = \frac{1}{3}(a - c) - \frac{1}{4}(a - c) = \frac{1}{12}(a - c)$$

-   균형 이윤 비교

    -   (추종자의 균형 이윤) $$<$$ (동시 결정 균형 이윤) $$<$$ (선도자의 균형
        이윤)

    -   $$\widehat{\pi_{2}} = \frac{1}{16}(a - c)^{2} < \pi^{*} = \frac{1}{9}(a - c)^{2} < \widehat{\pi_{1}} = \frac{1}{8}(a - c)^{2}$$

    -   동시 결정 $$\rightarrow$$ 선도자가 되었을 때 균형 이윤의 증가

        $$\widehat{\pi_{1}} - \pi^{*} = \frac{1}{8}(a - c)^{2} - \frac{1}{9}(a - c)^{2} = \frac{1}{72}(a - c)^{2}$$

    -   동시 결정 $$\rightarrow$$ 추종자가 되었을 때 균형 이윤의 감소

        $$\pi^{*} - \widehat{\pi_{2}} = \frac{1}{9}(a - c)^{2} - \frac{1}{16}(a - c)^{2} = \frac{7}{144}(a - c)$$

### 선도자-추종자가 불분명한 모형

-   선도자-추종자를 결정하는 게임

    -   경기자: 경쟁관계에 있는 두 기업

    -   전략 집합: \{선도, 추종\}

    -   보수표

        ![표](/images/Lec_7_2_3_1.png)

-   선도자-추종자를 결정하는 게임의 순수전략 균형

    -   동시 선택 정규형 게임으로 간주할 때 내쉬균형

        (선도, 추종); (추종; 선도) 두 개의 순수전략 내쉬균형이 존재

        ![표](/images/Lec_7_2_3_2.png)

-   선도자-추종자를 결정하는 게임의 혼합전략 균형

    -   기업 1의 확률분포: 

        $$\Pr\left\{ \text{선도} \right\} = p$$,
        $$\Pr\left\{ \text{추종} \right\} = 1 - p$$

    -   기업 2의 기대보수

        -   기업 2가 '선도'를 선택:

            $$p \times (0) + (1 - p) \times \frac{(a - c)^{2}}{8} = \frac{(a - c)^{2}}{8} - p \times \frac{(a - c)^{2}}{8}$$

        -   기업 2가 '추종'을 선택:

            $$p \times \frac{(a - c)^{2}}{16} + (1 - p) \times \frac{(a - c)^{2}}{9} = \frac{(a - c)^{2}}{9} - p \times \frac{7(a - c)^{2}}{144}$$

    -   기업 2의 기대보수가 같아지는 확률 계산

        $$
        \begin{align}
        \frac{(a - c)^{2}}{8} - p \times \frac{(a - c)^{2}}{8} & = \frac{(a - c)^{2}}{9} - p \times \frac{7(a - c)^{2}}{144} \\
        \rightarrow \frac{(a - c)^{2}}{72} & = p \times \frac{11(a - c)^{2}}{144} \\
        \rightarrow p^{*} & = \frac{2}{11}
        \end{align}
        $$

-   선도자-추종자를 결정하는 게임의 혼합전략 균형

    -   기업 1의 혼합전략

        $$\left( p^{*},\ 1 - p^{*} \right) = \left( \frac{2}{11},\frac{9}{11} \right)$$

    -   기업 2의 혼합전략

        $$\left( q^{*},\ 1 - q^{*} \right) = \left( \frac{2}{11},\frac{9}{11} \right)$$

    -   사후적으로 각 순수전략 균형이 발생할 확률

        $$
        \begin{align}
        \Pr\left\{ \text{(선도, 선도)} \right\} & = \frac{2}{11} \times \frac{2}{11} = \frac{4}{121} \\
        \Pr\left\{ \text{(선도, 추종)} \right\} & = \Pr\left\{ \text{(추종, 선도)} \right\} = \frac{2}{11} \times \frac{9}{11} = \frac{18}{121}  \\
        \Pr\left\{ \text{(추종, 추종)} \right\} & = \frac{9}{11} \times \frac{9}{11} = \frac{81}{121}
        \end{align}
        $$

### 요약

-   스타켈버그 균형은 부분게임완전균형일까?

    -   부분게임에서 생산량을 변경할 유인이 없음

    -   추종자의 최적 대응에 해당하는 생산량은 모두 균형

-   선도 생산량이 동시 생산량보다 더 많을까? <span style="color:#FF0000">YES!</span>

    -   추종 생산량 감소량이 선도 생산량 증가량보다 큼

-   선도자와 추종자를 선택하는 게임에서 균형은?

    -   (선도, 추종); (추종, 선도); 혼합전략
        $$\left( \frac{2}{11},\frac{9}{11} \right)$$


## 3.  입지와 가격 결정

### 학습목표

-   다음 질문에 대해 답을 할 수 있다.

    -   입지와 가격 결정 게임은 어떤 모형에서 확장될까?

    -   소비자는 어떤 비용을 지불하고 제품을 구입할까?

    -   부분게임완전균형의 입지와 가격은 무엇일까?

-   다음 문제를 생각해보자.

    -   두 상점의 효율성 차이가 있다면?

    -   상품의 가치가 상수가 아니라 변수라면?

-   ★ 핵심만 쏙쏙!

    {: .note}
	> **소비자는 효용이 더 큰 상점을 방문하여 상품을 구매**

### 입지와 가격을 동시에 결정하는 모형 개요

-   호텔링 모형을 확장

    -   단위 길이(e.g., 1km) 직선 거리로 형성된 도시

        $$\rightarrow$$ 도시의 왼쪽 경계는 ‘0’, 도시의 오른쪽 경계는 ‘1’

    -   두 상점이 경쟁하기 위한 입지(위치)를 선정한 후 위치를 기준으로 상품에 대한 가격을 결정하는 문제

    -   역진귀납법을 적용하여 게임을 풀이

        -   상점의 위치가 고정된 상태에서 가격(최적 대응)을 결정

        -   가격의 최적 대응을 반영한 후 상점의 입지를 결정

-   상점의 위치와 관련된 가정

    -   상점 1의 위치 $$a \in \lbrack 0,\ 1\rbrack$$, 상점 2의 위치
        $$1 - b \in \lbrack 0,\ 1\rbrack$$

    -   상점 1의 위치가 상점 2의 위치보다 왼쪽

        $$0 \leq a \leq 1 - b \leq 1 \rightarrow 1 - a - b \geq 0$$

    -   상점 $$i$$의 위치가 결정된 이후 같은 상품에 대하여 상점 $$i$$의 단위 판매가격 $$P_{i}$$를 결정

-   소비자의 구매의사결정에 관한 가정

    -   소비자는 '0'과 '1' 사이 직선 도시에 균등분포에 따라 거주

    -   모든 소비자는 상품의 가치를 $$v$$로 평가

    -   각 소비자는 효용이 더 큰 상점을 방문하여 상품을 구입

        -   소비자의 효용

            $$u_{c}\left( x,P_{i};\ y_{i} \right) = v - \left( P_{i} + t\left( x - y_{i} \right)^{2} \right)$$

        -   소비자의 효용은 '0'보다 충분히 큼

            $$u_{c}\left( x,P_{i};\ y_{i} \right) \gg 0 \Leftrightarrow v \gg P_{i} + t\left( x_{i} - y_{i} \right)^{2}$$

            $$\rightarrow$$ 소비자는 어느 상점에서든 상품을 구입하는 게 유리

### 위치를 고정한 상태에서 가격 결정

-   두 상점이 무차별한 소비자의 위치

    -   상점 1의 위치 $$a \in \lbrack 0,\ 1\rbrack$$, 상점 2의 위치
        $$1 - b \in \lbrack 0,\ 1\rbrack$$

    -   위치 $$x$$에 거주하는 소비자가 상점 $$i$$에서 상품을 구매한 효용

        -   상점 1에서 상품을 구입한 소비자의 효용

            $$u_{c}\left( x,\ P_{1};y_{1} = a \right) = v - \left( P_{1} + t(x - a)^{2} \right)$$

        -   상점 2에서 상품을 구입한 소비자의 효용

            $$u_{c}\left( x,\ P_{2};y_{2} = 1 - b \right) = v - \left( P_{2} + t\left( x - (1 - b) \right)^{2} \right)$$

    -   '중위투표자정리'를 확장 $$\rightarrow$$ 무차별한 소비자의 위치 결정

    -   무차별한 소비자:

        $$
        \begin{align}
        u_{c}\left( x,\ P_{1};y_{1} = a \right) & = u_{c}\left( x,\ P_{2};y_{2} = 1 - b \right) \\

        v - \left( P_{1} + t(x - a)^{2} \right) & = v - \left( P_{2} + t\left( x - (1 - b) \right)^{2} \right) \\

        P_{1} + t(x - a)^{2} & = P_{2} + t\left( x - (1 - b) \right)^{2} \\

        t\left\{ (x - a)^{2} - \left( x - (1 - b) \right)^{2} \right\} & = P_{2} - P_{1} \\

        t(1 - a - b)\left\{ 2x - (1 + a - b) \right\} & = P_{2} - P_{1}
        \end{align}
        $$

    -   무차별한 소비자의 위치 $$\widetilde{x}$$

        $$
        \begin{align}
        & t(1 - a - b)\left\{ 2x - (1 + a - b) \right\} = P_{2} - P_{1} \\

        & 2x - (1 + a - b) = \frac{P_{2} - P_{1}}{t(1 - a - b)} \\

        & 2x = 1 + a - b + \frac{P_{2} - P_{1}}{t(1 - a - b)} \\

        & \widetilde{x} = \frac{1 + a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)} = a + \frac{1 - a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)}
        \end{align}
        $$

-   두 상점의 수요를 계산

    -   $$x \in \left\lbrack 0,\widetilde{x} \right)$$에 거주하는 소비자는
        상점 1에서 상품을 구입

        상점 1의 수요

        $$
        \begin{align}
        \widetilde{x} = a + \frac{1 - a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)}
        \end{align}
        $$

    -   $$x \in \left( \widetilde{x},\ 1 \right\rbrack$$에 거주하는
        소비자는 상점 2에서 상품을 구입

        상점 2의 수요

        $$
        \begin{align}
        1 - \widetilde{x} & = 1 - \left\lbrack a + \frac{1 - a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)} \right\rbrack \\
        & = 1 - a - \frac{1 - a - b}{2} - \frac{P_{2} - P_{1}}{2t(1 - a - b)} \\
        & = b + \frac{1 - a - b}{2} + \frac{P_{1} - P_{2}}{2t(1 - a - b)}
        \end{align}
        $$

-   두 상점의 이윤을 계산

    -   상점 1의 이윤

        $$
        \begin{align}
        \pi_{1}\left( P_{1},\ P_{2} \right) & = \left( P_{1} - c \right)\widetilde{x} \\
        & = \left( P_{1} - c \right)\left\lbrack a + \frac{1 - a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)} \right\rbrack
        \end{align}
        $$

    -   상점 2의 이윤

        $$
        \begin{align}
        \pi_{2}\left( P_{1},\ P_{2} \right) & = \left( P_{2} - c \right)\left( 1 - \widetilde{x} \right) \\
        & = \left( P_{2} - c \right)\left\lbrack b + \frac{1 - a - b}{2} + \frac{P_{1} - P_{2}}{2t(1 - a - b)} \right\rbrack
        \end{align}
        $$

-   각 상점의 이윤을 최대화하는 가격 결정

    -   상점 1의 이윤 $$\pi_{1}$$을 가격 $$P_{1}$$으로 편미분 후 일계조건

        $$
        \begin{align}
        \frac{\partial}{\partial P_{1}}\pi_{1}\left( P_{1},\ P_{2} \right) & = \frac{\partial}{\partial P_{1}}\left( P_{1} - c \right)\left\lbrack a + \frac{1 - a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)} \right\rbrack \\
        & = \left\lbrack a + \frac{1 - a - b}{2} + \frac{P_{2} - P_{1}}{2t(1 - a - b)} \right\rbrack + \left( P_{1} - c \right)\left( \frac{- 1}{2t(1 - a - b)} \right) \\
        & = a + \frac{1 - a - b}{2} + \frac{P_{2} - 2P_{1} + c}{2t(1 - a - b)} \\
        \frac{\partial}{\partial P_{1}}\pi_{1}\left( P_{1},\ P_{2} \right) & = 0 \\
        \rightarrow \widehat{P_{1}} & = \frac{1}{2}\left\lbrack P_{2} + c + t(1 - a - b)(1 + a - b) \right\rbrack
        \end{align}
        $$

    -   상점 2의 이윤 $$\pi_{2}$$를 가격 $$P_{2}$$으로 편미분 후 일계조건

        $$
        \begin{align}
        \frac{\partial}{\partial P_{2}}\pi_{2}\left( P_{1},\ P_{2} \right) & = \frac{\partial}{\partial P_{2}}\left( P_{2} - c \right)\left\lbrack b + \frac{1 - a - b}{2} + \frac{P_{1} - P_{2}}{2t(1 - a - b)} \right\rbrack \\
        & = \left\lbrack b + \frac{1 - a - b}{2} + \frac{P_{1} - P_{2}}{2t(1 - a - b)} \right\rbrack + \left( P_{2} - c \right)\left( \frac{- 1}{2t(1 - a - b)} \right) \\
        & = b + \frac{1 - a - b}{2} + \frac{P_{1} - 2P_{2} + c}{2t(1 - a - b)} \\
        \frac{\partial}{\partial P_{2}}\pi_{2}\left( P_{1},\ P_{2} \right) & = 0 \\
        \rightarrow \widehat{P_{2}} & = \frac{1}{2}\left\lbrack P_{1} + c + t(1 - a - b)(1 - a + b) \right\rbrack
        \end{align}
        $$

    -   상점 1과 상점 2의 최적 대응을 연립하여 균형 가격 결정

        -   상점 1의 최적 대응

            $$\widehat{P_{1}} = \frac{1}{2}\left\lbrack P_{2} + c + t(1 - a - b)(1 + a - b) \right\rbrack$$

            상점 2의 최적 대응

            $$\widehat{P_{2}} = \frac{1}{2}\left\lbrack P_{1} + c + t(1 - a - b)(1 - a + b) \right\rbrack$$

    -   상점 1과 상점 2의 최적 대응을 연립하여 균형 가격 결정

        -   $$\widehat{P_{2}} \rightarrow \widehat{P_{1}}\left( P_{2} \right)$$에 대입 후 정리

            $$
            \begin{align}
            2P_{1} & = \frac{1}{2}\left\lbrack P_{1} + c + t(1 - a - b)(1 - a + b) \right\rbrack + c + t(1 - a - b)(1 + a - b) \\

            4P_{1} & = P_{1} + c + t(1 - a - b)(1 - a + b) + 2c + 2t(1 - a - b)(1 + a - b) \\

            3P_{1} & = 3c + t(1 - a - b)\left( 1 - a + b + 2(1 + a - b) \right)  \\

            3P_{1} & = 3c + t(1 - a - b)(3 + a - b) \\

            \therefore \widehat{P_{1}} &= c + t(1 - a - b)\left( 1 + \frac{a - b}{3} \right)
            \end{align}
            $$

        -   $$\widehat{P_{1}} \rightarrow \widehat{P_{2}}\left( P_{1} \right)$$에 대입 후 정리

            $$
            \begin{align}
            \widehat{P_{2}} & = \frac{1}{2}\left\lbrack P_{1} + c + t(1 - a - b)(1 - a + b) \right\rbrack \\
            & = \frac{1}{2}\left\lbrack c + t(1 - a - b)\left( 1 + \frac{a - b}{3} \right) + c + t(1 - a - b)(1 - a + b) \right\rbrack \\
            & = \frac{1}{2}\left\lbrack 2c + t(1 - a - b)\left( 2 - \frac{2(a - b)}{3} \right) \right\rbrack \\
            \therefore \widehat{P_{2}} & = c + t(1 - a - b)\left( 1 + \frac{b - a}{3} \right) 
            \end{align}
            $$

-   균형 가격을 반영한 상점의 이윤 결정

    -   상점 1의 이윤

        $$
        \begin{align}
        \pi_{1}\left( \widehat{P_{1}}, \widehat{P_{2}} \right) & = \left( \widehat{P_{1}} - c \right)\widetilde{x} \\
        & = \left( \widehat{P_{1}} - c \right)\left\lbrack a + \frac{1 - a - b}{2} + \frac{\widehat{P_{2}} - \widehat{P_{1}}}{2t(1 - a - b)} \right\rbrack \\
        & = t(1 - a - b)\left( 1 + \frac{a - b}{3} \right)\left\lbrack a + \frac{1 - a - b}{2} + \frac{b - a}{3} \right\rbrack \\
        & = t(1 - a - b)\left( 1 + \frac{a - b}{3} \right)\left\lbrack \frac{1}{2} + \frac{a - b}{6} \right\rbrack \\
        & = \frac{t}{2}(1 - a - b)\left( 1 + \frac{a - b}{3} \right)^{2}
        \end{align}
        $$

    -   상점 2의 이윤

        $$
        \begin{align}
        \pi_{2}\left( \widehat{P_{1}}, \widehat{P_{2}} \right) & = \left( \widehat{P_{2}} - c \right)\left( 1 - \widetilde{x} \right) \\
        & = \left( \widehat{P_{2}} - c \right)\left\lbrack b + \frac{1 - a - b}{2} + \frac{\widehat{P_{1}} - \widehat{P_{2}}}{2t(1 - a - b)} \right\rbrack \\
        & = t(1 - a - b)\left( 1 + \frac{b - a}{3} \right)\left\lbrack b + \frac{1 - a - b}{2} + \frac{a - b}{3} \right\rbrack \\
        & = t(1 - a - b)\left( 1 + \frac{b - a}{3} \right)\left\lbrack \frac{1}{2} + \frac{b - a}{6} \right\rbrack \\
        & = \frac{t}{2}(1 - a - b)\left( 1 + \frac{b - a}{3} \right)^{2}
        \end{align}
        $$

### 균형 가격을 반영한 상점의 입지 결정

-   상점의 이윤을 최대화하는 위치를 결정

    -   상점 1의 이윤
        $$\widehat{\pi_{1}} = \frac{t}{2}(1 - a - b)\left( 1 + \frac{a - b}{3} \right)^{2}$$을
        위치 $$a$$로 편미분

        -   $$
            \begin{align}
            \frac{\partial\widehat{\pi_{1}}}{\partial a} & = \frac{t}{2}\left\lbrack - \left( 1 + \frac{a - b}{3} \right)^{2} + (1 - a - b) \times \frac{2}{3}\left( 1 + \frac{a - b}{3} \right) \right\rbrack \\
            & = - \frac{t}{6}\left( 1 + \frac{a - b}{3} \right)\left\lbrack (3 + a - b) - 2(1 - a - b) \right\rbrack \\
            & = - \frac{t}{6}\left( 1 + \frac{a - b}{3} \right)(1 + 3a + b) \leq 0
            \end{align}
            $$

        -   $$\widehat{\pi_{1}}$$은 $$a$$에 대하여 감소 $$\rightarrow$$ $$a^{*} = 0$$일 때
            $$\widehat{\pi_{1}}$$이 최대

    -   상점 2의 이윤
        $$\widehat{\pi_{2}} = \frac{t}{2}(1 - a - b)\left( 1 + \frac{b - a}{3} \right)^{2}$$을
        위치 $$b$$로 편미분

        -   $$
            \begin{align}
            \frac{\partial\widehat{\pi_{2}}}{\partial b} & = \frac{t}{2}\left\lbrack - \left( 1 + \frac{b - a}{3} \right)^{2} + (1 - a - b) \times \frac{2}{3}\left( 1 + \frac{b - a}{3} \right) \right\rbrack \\
            & = - \frac{t}{6}\left( 1 + \frac{b - a}{3} \right)\left\lbrack (3 + b - a) - 2(1 - a - b) \right\rbrack \\
            & = - \frac{t}{6}\left( 1 + \frac{b - a}{3} \right)(1 + a + 3b) \leq 0
            \end{align}
            $$

        -   $$\widehat{\pi_{2}}$$은 $$b$$에 대하여 감소 $$\rightarrow$$
            $$b^{*} = 0\left( 1 - b^{*} = 1 \right)$$일 때
            $$\widehat{\pi_{2}}$$이 최대

    -   최적 입지 $$\left( a^{*},\ 1 - b^{*} \right) = (0,\ 1)$$

        -   상점 1의 최적 입지 

            $$a^{*} = 0$$ $$\rightarrow$$ 선형도시의 왼쪽 경계

        -   상점 2의 최적 입지

            $$1 - b^{*} = 1$$ $$\rightarrow$$ 선형도시의 오른쪽 경계

    -   최적 입지에서 균형 가격 

        $$P_{1}^{*} = P_{2}^{*} = c + t$$

    -   최적 입지에서 균형 수요

        $$x^{*} = 1 - x^{*} = \frac{1}{2}$$

    -   최적 입지에서 균형 이윤

        $$\pi_{1}^{*} = \pi_{2}^{*} = \frac{t}{2}$$

-   부분게임완전균형이 가장 '효율적인' 입지인가?

    -   부분게임완전균형에서의 입지:
        $$\left( a^{*},\ 1 - b^{*} \right) = (0,\ 1)$$

    -   부분게임완전균형에서 소비자가 부담하는 '교통비'

        $$\int_{0}^{\frac{1}{2}}{t(x - 0)^{2}dx} + \int_{\frac{1}{2}}^{1}{t(1 - x)^{2}dx} = \left. \ \frac{t}{3}x^{3} \right|_{0}^{\frac{1}{2}} + \left. \ \left( - \frac{t}{3}(1 - x)^{3} \right) \right|_{\frac{1}{2}}^{1} = \frac{t}{24} + \frac{t}{24} = \frac{t}{12}$$

    -   같은 가격, 대칭적 입지를 가정할 때 소비자가 부담하는 '교통비'

        $$2\int_{0}^{\frac{1}{2}}{t(x - a)^{2}dx} = \left. \ \frac{2t}{3}(x - a)^{3} \right|_{0}^{\frac{1}{2}} = \frac{2t}{3}\left( \left( \frac{1}{2} - a \right)^{3} - (0 - a)^{3} \right) = \frac{t}{12}\left( 12a^{2} - 6a + 1 \right)$$

    -   소비자가 부담하는 '교통비'을 최소화하는 입지와 그때 '교통비'

        -   $$
            \begin{align}
            \frac{d}{da}\left\lbrack \frac{t}{12}\left( 12a^{2} - 6a + 1 \right) \right\rbrack & = \frac{t}{12}(24a - 6) = 0 \\
            \rightarrow \widetilde{a} & = \frac{1}{4}, 1 - \widetilde{b} = \frac{3}{4}
            \end{align}
            $$

        -   $$\left( \widetilde{a} = \frac{1}{4},1 - \widetilde{b} = \frac{3}{4} \right)$$에서
            소비자 부담 교통비

            $$\frac{t}{12}\left( 12\left( \frac{1}{4} \right)^{2} - 6\left( \frac{1}{4} \right) + 1 \right) = \frac{t}{48}$$


### 요약

-   입지와 가격 결정 게임은 어떤 모형에서 확장될까?

    -   선형도시의 상점 입지를 결정하는 호텔링 모형

-   소비자는 어떤 비용을 지불하고 제품을 구입할까?

    -   상점까지의 거리의 제곱에 비례하는 일종의 ‘교통비’

    -   ‘교통비’와 상품 판매 가격의 합을 지불

-   부분게임완전균형의 입지와 가격은 무엇일까?

    -   선형도시의 양끝점, 원가와 ‘교통비’ 요율의 합

## 정리하기

-   선점 효과는 최적 대응을 반영 및 고정하여 계산

-   선도자, 추종자를 결정하는 전략을 파악하기 위해 선도 효과의 측정과 분석이 필요

-   입지와 가격을 결정하는 문제는 호텔링 모형을 확장하여 가격에 따른 소비자의 행동을 가정