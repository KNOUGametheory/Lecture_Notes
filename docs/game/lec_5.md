---
layout: default
title: 혼합전략
parent: 게임이론
nav_order: 5
---

# 혼합전략


<!-- 1.  혼합전략의 개념

2.  혼합전략 내쉬균형

3.  혼합전략 내쉬균형의 적용 -->

## 1.  혼합전략의 개념

### 학습목표

-   다음 질문에 대해 답을 할 수 있다.

    -   순수전략 내쉬균형은 항상 존재할까?

    -   혼합전략에서 어떤 전략이 선택될지 알 수 있을까?

    -   합리화전략과 혼합전략 사이의 관계는 무엇일까?

-   다음 문제를 생각해보자.

    -   순수전략 내쉬균형이 존재하지 않는 게임의 특징은?

    -   혼합전략을 적용하면 보수는 어떻게 결정될까?

-   ★ 핵심만 쏙쏙!

    {: .note}
	> **순수전략에 선택될 확률을 부여하면 혼합전략!**

### 순수전략 균형이 존재하지 않는 게임

-   홀짝 게임(Matching Pennies)

    -   경기자: 각각 여러 개의 동전을 가진 두 경기자

    -   전략 집합: \{홀, 짝\}

    -   보수표

    ![표](/images/Lec_5_1_1_1.png)

    -   우월전략, 열등전략 모두 없음

    -   네 가지 전략 조합에서 전략을 바꿀 유인이 있는지 판단

-   전략 조합 1: (홀, 홀)

    -   경기자 1의 입장: 전략을 바꿀 유인 있음(홀 $$\rightarrow$$ 짝)

        $$u_{1}$$(홀,<span style="color:#FF0000">홀</span>) $$= - 1 < u_{1}$$(짝,<span style="color:#FF0000">홀</span>) $$= 1$$

    -   경기자 2의 입장: 전략을 바꿀 유인 없음

        $$u_{2}$$(<span style="color:#FF0000">홀</span>,홀) $$= 1 \geq u_{2}$$(<span style="color:#FF0000">홀</span>,짝) $$= - 1$$

    ![표](/images/Lec_5_1_1_1.png)

-   전략 조합 2: (홀, 짝)

    -   경기자 1의 입장: 전략을 바꿀 유인 없음

        $$u_{1}$$(홀,<span style="color:#105AD2">짝</span>) $$= 1 \geq u_{1}$$(짝,<span style="color:#105AD2">짝</span>) $$= - 1$$

    -   경기자 2의 입장: 전략을 바꿀 유인 있음(짝 $$\rightarrow$$ 홀)

        $$u_{2}$$(<span style="color:#FF0000">홀</span>,짝) $$= - 1 < u_{2}$$(<span style="color:#FF0000">홀</span>,홀) $$= 1$$

    ![표](/images/Lec_5_1_1_1.png)

-   전략 조합 3: (짝, 홀)

    -   경기자 1의 입장: 전략을 바꿀 유인 없음

        $$u_{1}$$(짝,<span style="color:#FF0000">홀</span>) $$= 1 \geq u_{1}$$(홀,<span style="color:#FF0000">홀</span>) $$= - 1$$

    -   경기자 2의 입장: 전략을 바꿀 유인 있음(홀 $$\rightarrow$$ 짝)

        $$u_{2}$$(<span style="color:#105AD2">짝</span>,홀) $$= - 1 < u_{2}$$(<span style="color:#105AD2">짝</span>,짝) $$= 1$$

    ![표](/images/Lec_5_1_1_1.png)

-   전략 조합 4: (짝, 짝)

    -   경기자 1의 입장: 전략을 바꿀 유인 있음(짝 $$\rightarrow$$ 홀)

        $$u_{1}$$(짝,<span style="color:#105AD2">짝</span>) $$= - 1 < u_{1}$$(홀,<span style="color:#105AD2">짝</span>) $$= 1$$

    -   경기자 2의 입장: 전략을 바꿀 유인 없음

        $$u_{2}$$(<span style="color:#105AD2">짝</span>,짝) $$= 1 \geq u_{2}$$(<span style="color:#105AD2">짝</span>,홀) $$= - 1$$

    ![표](/images/Lec_5_1_1_1.png)

-   홀짝 게임의 균형

    -   네 가지 전략 조합 모두에서 적어도 한 경기자는 전략을 바꿀 유인이 있음

    -   순수전략 내쉬균형 없음

    ![표](/images/Lec_5_1_1_1.png)

### 순수전략을 선택할 확률을 도입

-   혼합전략(mixed strategy)

    -   선택할 가능성이 있는 순수전략(합리화전략)을 어떤 확률분포에 따라 무작위로 추출 또는 선택

        ※ 무작위 전략(randomized strategy)

    -   혼합전략을 활용할 때 어떤 전략이 선택될지는 사전적(ex-ante, prior)으로는 알 수 없음

    -   확률분포에 따라 무작위로 추출 또는 선택하기 때문에 어떤 순수전략이 선택될 경향성만 추정이 가능

-   혼합전략 예시 1

    -   홀짝 게임에서 '홀' 또는 '짝'을 선택할 확률분포를 정의

        $$\rightarrow$$ 주사위를 던져서 홀수가 나오면 '홀', 짝수가 나오면 '짝'

    -   주사위를 던질 때 표본공간
        $$S = \left\{ 1,\ 2,\ 3,\ 4,\ 5,\ 6 \right\}$$

        홀수 $$O = \left\{ 1,\ 3,\ 5 \right\}$$, 홀수가 나올 확률 $$\Pr\left\{ O \right\} = \frac{n(O)}{n(S)} = \frac{3}{6} = \frac{1}{2}$$

        짝수 $$E = \left\{ 2,\ 4,\ 6 \right\}$$, 짝수가 나올 확률 $$\Pr\left\{ E \right\} = \frac{n(E)}{n(S)} = \frac{3}{6} = \frac{1}{2}$$

    -   '홀'을 선택할 확률 $$\frac{1}{2}$$, '짝'을 선택할 확률 $$\frac{1}{2}$$

-   혼합전략 예시 2

    -   홀짝 게임에서 '홀' 또는 '짝'을 선택할 확률분포를 정의

        $$\rightarrow$$ 주사위를 던져서 '6의 약수'가 나오면 '홀', '6의 약수가 아닌 수'가 나오면 '짝'

    -   주사위를 던질 때 표본공간
        $$S = \left\{ 1,\ 2,\ 3,\ 4,\ 5,\ 6 \right\}$$

        6의 약수 $$A = \left\{ 1,\ 2,\ 3,\ 6 \right\} \rightarrow \Pr\left\{ A \right\} = \frac{n(A)}{n(S)} = \frac{4}{6} = \frac{2}{3}$$

        6의 약수가 아닌 수 $$B = \overline{A} = \left\{ 4,\ 5 \right\} \rightarrow \Pr\left\{ B \right\} = \frac{n(B)}{n(S)} = \frac{2}{6} = \frac{1}{3}$$

    -   '홀'을 선택할 확률 $$\frac{2}{3}$$, '짝'을 선택할 확률 $$\frac{1}{3}$$

### 혼합전략과 합리화전략

-   최적 대응(Best Response)

    -   경기자 $$i$$를 제외한 다른 경기자 $$- i$$의 전략이 주어졌을 때,
        경기자 $$i$$의 다른 모든 전략보다 '크거나 같은' 보수를 주는 전략

    -   경기자 $$i$$의 전략 $$\widehat{\sigma_{i}}$$는 다른 경기자 $$- i$$의
        전략(조합) $$\sigma_{- i}$$에 대한 최적대응 if
        $$u_{i}\left( \widehat{\sigma_{i}},\ \sigma_{- i} \right) \geq u_{i}\left( \sigma_{i},\ \sigma_{- i} \right)$$
        $$\forall\sigma_{i} \in S_{i}$$를 만족시키는 $$\sigma_{- i}$$가 존재

        예) 홀짝 게임에서 경기자 1의 최적 대응

        경기자 2가 '홀'을 선택? $$u_{1}$$(짝,<span style="color:#FF0000">홀</span>) $$= 1 \geq u_{1}$$(홀,<span style="color:#FF0000">홀</span>) $$= - 1$$

        경기자 2가 '짝'을 선택? $$u_{1}$$(홀,<span style="color:#105AD2">짝</span>) $$= 1 \geq u_{1}$$(짝,<span style="color:#105AD2">짝</span>) $$= - 1$$

-   합리화전략(Rationalizable Strategy)

    -   경기자가 서로 '합리적으로 행동할 것이다'라고 가정

    -   다른 경기자의 선택에 최적 대응을 선택하는 것이 합리적!

    -   경기자 $$i$$의 입장에서 '합리적'으로 판단할 때, 절대로 선택되지 않을 전략을 제외하고 남은 전략의 집합

    -   혼합전략은 합리화전략의 혼합

        $$\rightarrow$$ 혼합전략은 합리화전략의 볼록결합(convex combination)

### 요약

-   순수전략 내쉬균형은 항상 존재할까?

    -   경기자에게 분배되는 보수의 합이 일정하면 그 게임은 순수전략 내쉬균형이 존재하지 않음

-   혼합전략에서 어떤 전략이 선택될지 알 수 있을까?

    -   사전적으로는 알 수 없으며, 경향성 추정만 가능

-   합리화전략과 혼합전략 사이의 관계는 무엇일까?

    -   혼합전략은 합리화전략의 볼록결합

## 2.  혼합전략 내쉬균형

### 학습목표

-   다음 질문에 대해 답을 할 수 있다.

    -   혼합전략의 확률분포는 어떻게 정의될까?

    -   혼합전략의 기대보수는 어떻게 계산해야 할까?

    -   홀짝 게임의 혼합전략 내쉬균형은 무엇일까?

-   다음 문제를 생각해보자.

    -   혼합전략 내쉬균형은 항상 존재할까?

    -   기대보수 이외의 다른 기준은 없을까?

-   ★ 핵심만 쏙쏙!

    {: .note}
	> **혼합전략 내쉬균형은 선택할 확률이 바뀌지 않는 확률분포**

### 확률분포와 기대보수

-   홀짝 게임(Matching Pennies)

    -   경기자: 각각 여러 개의 동전을 가진 두 경기자

    -   전략 집합: \{홀, 짝\}

    -   보수표

    ![표](/images/Lec_5_1_1_1.png)

-   홀짝 게임에서 경기자 1의 확률분포

    -   $$p$$: 경기자 1이 '홀'을 선택할 확률

    -   $$1 - p$$: 경기자 1이 '짝'을 선택할 확률

-   홀짝 게임에서 경기자 1의 혼합전략

    -   $$p = 0$$: 경기자 1이 확정적으로 '짝'을 선택

    -   $$p = \frac{1}{3}$$: {홀, 짝, 짝} 주머니에서 임의로 제비를 뽑아
        선택

    -   $$p = \frac{2}{3}$$: {홀, 홀, 짝} 주머니에서 임의로 제비를 뽑아
        선택

    -   $$p = 1$$: 경기자 1이 확정적으로 '홀'을 선택

-   경기자 1의 확률분포를 고려한 경기자 2의 기대보수

    -   경기자 2가 '홀'을 선택하면?

        $$
        \begin{align}
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack & = p \times u_{2}(\text{홀},\text{홀}) + (1 - p) \times u_{2}(\text{짝},\text{홀}) \\
        & = p \times (1) + (1 - p) \times ( - 1) = 2p - 1
        \end{align}
        $$

    -   경기자 2가 '짝'을 선택하면?

        $$
        \begin{align}        
        E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack & = p \times u_{2}(\text{홀},\text{짝}) + (1 - p) \times u_{2}(\text{짝},\text{짝}) \\
        & = p \times ( - 1) + (1 - p) \times (1) = 1 - 2p
        \end{align}
        $$

### 기대보수에 따른 대응곡선

-   경기자 2의 기대보수를 고려한 최적 대응

    -   경기자 1의 확률분포: 

        $$Pr\ \left\{ \text{홀} \right\} = p$$,
        $$Pr\ \left\{ \text{짝} \right\} = 1 - p$$

    -   경기자 2의 기대보수

        $$E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack = 2p - 1$$,
        $$E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack = 1 - 2p$$

    -   경기자 2의 확률분포: 

        $$Pr\ \left\{ \text{홀} \right\} = q$$,
        $$Pr\ \left\{ \text{짝} \right\} = 1 - q$$

    -   $$
        \begin{align} 
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack > E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack
        & \Leftrightarrow p > \frac{1}{2} \rightarrow q = 1 \\
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack = E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack
        & \Leftrightarrow p = \frac{1}{2} \rightarrow any \,\, q \in \lbrack 0,\ 1\rbrack \\
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack < E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack
        & \Leftrightarrow p < \frac{1}{2} \rightarrow q = 0
        \end{align}
        $$

-   경기자 2의 대응곡선

    -   $$
        \begin{align}  
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack > E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack
        & \Leftrightarrow p > \frac{1}{2} \rightarrow q = 1 \\
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack = E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack
        & \Leftrightarrow p = \frac{1}{2} \rightarrow any \,\, q \in \lbrack 0,\ 1\rbrack \\
        E\left\lbrack u_{2}( \cdot ,\text{홀}) \right\rbrack < E\left\lbrack u_{2}( \cdot ,\text{짝}) \right\rbrack
        & \Leftrightarrow p < \frac{1}{2} \rightarrow q = 0
        \end{align}
        $$  

    ![표](/images/Lec_5_2_2_1.png)

-   경기자 1의 기대보수를 고려한 최적 대응

    -   경기자 2의 확률분포: 

        $$Pr\ \left\{ \text{홀} \right\} = q$$,
        $$Pr\ \left\{ \text{짝} \right\} = 1 - q$$

    -   경기자 1의 기대보수

        $$E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack = 1 - 2q$$,
        $$E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack = 2q - 1$$

    -   경기자 1의 확률분포: 

        $$Pr\ \left\{ \text{홀} \right\} = p$$,
        $$Pr\ \left\{ \text{짝} \right\} = 1 - p$$

    -   $$
        \begin{align} 
        E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack > E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack
        & \Leftrightarrow q < \frac{1}{2} \rightarrow p = 1 \\
        E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack = E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack
        & \Leftrightarrow q = \frac{1}{2} \rightarrow any \,\, p \in \lbrack 0,\ 1\rbrack \\
        E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack < E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack
        & \Leftrightarrow q > \frac{1}{2} \rightarrow p = 0
        \end{align}
        $$

-   경기자 1의 대응 곡선

    -   $$
        \begin{align} 
        E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack > E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack
        & \Leftrightarrow q < \frac{1}{2} \rightarrow p = 1 \\
        E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack = E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack
        & \Leftrightarrow q = \frac{1}{2} \rightarrow any \,\, p \in \lbrack 0,\ 1\rbrack \\
        E\left\lbrack u_{1}(\text{홀},  \cdot ) \right\rbrack < E\left\lbrack u_{1}(\text{짝},  \cdot ) \right\rbrack
        & \Leftrightarrow q > \frac{1}{2} \rightarrow p = 0
        \end{align}
        $$

    ![표](/images/Lec_5_2_2_2.png)

### 대응곡선과 혼합전략 내쉬균형

-   혼합전략 내쉬균형(Mixed Strategy Nash Equilibrium)

    -   두 경기자 모두에게 최적 대응인 $$p^{*}$$와 $$q^{*}$$를 결정

    -   두 대응곡선이 교차하는 점이 혼합전략 내쉬균형

    ![표](/images/Lec_5_2_3_1.png)

-   홀짝 게임의 혼합전략 내쉬균형

    -   경기자 1: '홀' 선택 확률 $$p^{*} = \frac{1}{2}$$, '짝' 선택 확률
        $$1 - p^{*} = \frac{1}{2}$$

    -   경기자 2: '홀' 선택 확률 $$q^{*} = \frac{1}{2}$$, '짝' 선택 확률
        $$1 - q^{*} = \frac{1}{2}$$

    ![표](/images/Lec_5_2_3_1.png)

-   홀짝 게임의 혼합전략 내쉬균형 해석

    -   경기자 1: '홀' 선택 확률 $$p^{*} = \frac{1}{2}$$, '짝' 선택 확률
        $$1 - p^{*} = \frac{1}{2}$$

        {홀, 짝} 제비가 같은 비율로 섞인 주머니에서 무작위로 하나의 제비를 추출하여 제비에 적힌 대로 실행

    -   경기자 2: '홀' 선택 확률 $$q^{*} = \frac{1}{2}$$, '짝' 선택 확률
        $$1 - q^{*} = \frac{1}{2}$$

        '제대로 만들어진' 동전을 던져서 '앞면'이 나오면 '홀', '뒷면'이 나오면 '짝'을 선택

    -   순수전략의 조합 (홀, 홀); (홀, 짝); (짝, 홀); (짝, 짝)이 각각 $$\frac{1}{4}$$의 확률로 실현될 것!

    -   네 가지 순수전략의 조합 중에서 무엇이 실현될지는 사전적으로 알 수 없음

    -   혼합전략 내쉬균형에서, 선택가능한 전략 조합은 같은 수준의 기대보수(홀짝 게임에서는 '0')를 제공

### 요약

-   혼합전략의 확률분포는 어떻게 정의될까?

    -   각각의 순수전략(합리화전략)을 선택할 확률

    -   확률분포를 정의하는 것이 경기자의 전략 집합

-   혼합전략의 기대보수는 어떻게 계산해야 할까?

    -   상대의 확률분포를 기준으로 보수의 기댓값 계산

-   홀짝 게임의 혼합전략 내쉬균형은 무엇일까?

    -   '홀'과 '짝'을 각각 $$\frac{1}{2}$$의 확률로 무작위하게 선택

## 3.  혼합전략 내쉬균형의 적용

### 학습목표

-   다음 질문에 대해 답을 할 수 있다.

    -   가위바위보 게임은 순수전략 내쉬균형이 존재할까?

    -   가위바위보 게임의 혼합전략 내쉬균형은 무엇일까?

    -   가위바위 게임의 혼합전략 내쉬균형은 어떻게 구현할까?

-   다음 문제를 생각해보자.

    -   혼합전략으로 설명될 수 있는 상황은 무엇일까?

    -   현실 상황에서 혼합전략 내쉬균형의 의미는?

-   ★ 핵심만 쏙쏙!

    {: .note}
	> **혼합전략 내쉬균형은 기대보수를 같게 하는 확률분포**

### 가위바위보 게임의 순수전략 균형

-   가위바위보 게임(Rock-Paper-Scissors Game)

    -   경기자: 두 경기자(경기자 1, 경기자 2)

    -   전략 집합: \{가위, 바위, 보\}

    -   보수표

    ![표](/images/Lec_5_3_1_1.png)

-   가위바위보 게임(Rock-Paper-Scissors Game)

    -   우월전략, 열등전략 모두 없음

    -   9가지 전략조합이 균형이 될 수 있는지 판단 필요

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 1: (가위, 가위)

    -   경기자 1: $$u_{1}$$(가위,<span style="color:#FF0000">가위</span>) $$= 0 < u_{1}$$(바위,<span style="color:#FF0000">가위</span>) $$= 1$$

    -   경기자 2: $$u_{2}$$(<span style="color:#FF0000">가위</span>,가위) $$= 0 < u_{2}$$(<span style="color:#FF0000">가위</span>,바위) $$= 1$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 2: (가위, 바위)

    -   경기자 1: $$u_{1}$$(가위,<span style="color:#659952">바위</span>) $$= - 1 < u_{1}$$(바위,<span style="color:#659952">바위</span>) $$= 0$$

    -   경기자 2: $$u_{2}$$(<span style="color:#FF0000">가위</span>,바위) $$= 1 \geq u_{2}$$(<span style="color:#FF0000">가위</span>,가위) $$= 0$$

        $$\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,u_{2}$$(<span style="color:#FF0000">가위</span>,바위) $$= 1 \geq u_{2}$$(<span style="color:#FF0000">가위</span>,보) $$= - 1$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 3: (가위, 보)

    -   경기자 1: $$u_{1}$$(가위,<span style="color:#105AD2">보</span>) $$= 1 \geq u_{1}$$(바위,<span style="color:#105AD2">보</span>) $$= - 1$$

        $$\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,u_{1}$$(가위,<span style="color:#105AD2">보</span>) $$= 1 \geq u_{1}$$(보,<span style="color:#105AD2">보</span>) $$= 0$$

    -   경기자 2: $$u_{2}$$(<span style="color:#FF0000">가위</span>,보) $$= - 1 < u_{2}$$(<span style="color:#FF0000">가위</span>,바위) $$= 1$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 4: (바위, 가위)

    -   경기자 1: $$u_{1}$$(바위,<span style="color:#FF0000">가위</span>) $$= 1 \geq u_{1}$$(가위,<span style="color:#FF0000">가위</span>) $$= 0$$

        $$\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,u_{1}$$(바위,<span style="color:#FF0000">가위</span>) $$= 1 \geq u_{1}$$(보,<span style="color:#FF0000">가위</span>) $$= - 1$$

    -   경기자 2: $$u_{2}$$(<span style="color:#659952">바위</span>,가위) $$= - 1 < u_{2}$$(<span style="color:#659952">바위</span>,바위) $$= 0$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 5: (바위, 바위)

    -   경기자 1: $$u_{1}$$(바위,<span style="color:#659952">바위</span>) $$= 0 < u_{1}$$(보,<span style="color:#659952">바위</span>) $$= 1$$

    -   경기자 2: $$u_{2}$$(<span style="color:#659952">바위</span>,바위) $$= 0 < u_{2}$$(<span style="color:#659952">바위</span>,보) $$= 1$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 6: (바위, 보)

    -   경기자 1: $$u_{1}$$(바위,<span style="color:#105AD2">보</span>) $$= - 1 < u_{1}$$(가위,<span style="color:#105AD2">보</span>) $$= 1$$

    -   경기자 2: $$u_{2}$$(<span style="color:#659952">바위</span>,보) $$= 1 \geq u_{2}$$(<span style="color:#659952">바위</span>,가위) $$= - 1$$

        $$\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,u_{2}$$(<span style="color:#659952">바위</span>,보) $$= 1 \geq u_{2}$$(<span style="color:#659952">바위</span>,바위) $$= 0$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 7: (보, 가위)

    -   경기자 1: $$u_{1}$$(보,<span style="color:#FF0000">가위</span>) $$= - 1 < u_{1}$$(가위,<span style="color:#FF0000">가위</span>) $$= 0$$

    -   경기자 2: $$u_{2}$$(<span style="color:#105AD2">보</span>,가위) $$= 1 \geq u_{2}$$(<span style="color:#105AD2">보</span>,바위) $$= - 1$$

        $$\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,u_{2}$$(<span style="color:#105AD2">보</span>,가위) $$= 1 \geq u_{2}$$(<span style="color:#105AD2">보</span>,보) $$= 0$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 8: (보, 바위)

    -   경기자 1: $$u_{1}$$(보,<span style="color:#659952">바위</span>) $$= 1 \geq u_{1}$$(가위,<span style="color:#659952">바위</span>) $$= - 1$$

        $$\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,u_{1}$$(보,<span style="color:#659952">바위</span>) $$= 1 \geq u_{1}$$(바위,<span style="color:#659952">바위</span>) $$= 0$$

    -   경기자 2: $$u_{2}$$(<span style="color:#105AD2">보</span>,바위) $$= - 1 < u_{2}$$(<span style="color:#105AD2">보</span>,가위) $$= 1$$

    ![표](/images/Lec_5_3_1_1.png)

-   전략조합 9: (보, 보)

    -   경기자 1: $$u_{1}$$(보,<span style="color:#105AD2">보</span>) $$= 0 < u_{1}$$(가위,<span style="color:#105AD2">보</span>) $$= 1$$

    -   경기자 2: $$u_{2}$$(<span style="color:#105AD2">보</span>,보) $$= 0 < u_{2}$$(<span style="color:#105AD2">보</span>,가위) $$= 1$$

    ![표](/images/Lec_5_3_1_1.png)

-   가위바위보 게임

    -   순수전략 내쉬균형 없음

    -   약열등전략의 단계적 소거로 제외되는 전략 없음

    ![표](/images/Lec_5_3_1_1.png)

### 가위바위보 게임의 혼합전략 균형

-   가위바위보 게임에서 경기자 1의 확률분포

    -   $$p$$: 경기자 1이 '가위'를 선택할 확률

    -   $$q$$: 경기자 1이 '바위'를 선택할 확률

    -   $$1 - p - q$$: 경기자 1이 '보'를 선택할 확률

-   가위바위보 게임에서 경기자 1의 혼합전략

    -   $$p = 1,\ q = 0$$ : 경기자 1이 확정적으로 '가위'를 선택

    -   $$p = \frac{1}{3},\ q = \frac{1}{3}$$ : {가위, 바위, 보}에서
        제비를 뽑아 선택

    -   $$p = \frac{2}{3},\ q = \frac{1}{3}$$: {가위, 가위, 바위}에서
        제비를 뽑아 선택

    -   $$p = 0,q = 0$$: 경기자 1이 확정적으로 '보'를 선택


-   경기자 1의 확률분포를 고려한 경기자 2의 기대보수

    -   경기자 2가 '가위'를 선택하면?

        $$
        \begin{align}
        E\left\lbrack u_{2}( \cdot , \text{가위}) \right\rbrack & = p \times u_{2}(\text{가위},\text{가위}) \\
        & + q \times u_{2}(\text{바위}, \text{가위}) \\
        & + (1 - p - q) \times u_{2}(\text{보},\text{가위}) \\
        & = p \times (0) + q \times ( - 1) + (1 - p - q) \times (1) \\ 
        & = - p - 2q + 1
        \end{align}
        $$

    -   경기자 2가 '바위'를 선택하면?

        $$
        \begin{align}
        E\left\lbrack u_{2}( \cdot , \text{바위}) \right\rbrack & = p \times u_{2}(\text{가위},\text{바위}) \\
        & + q \times u_{2}(\text{바위}, \text{바위}) \\
        & + (1 - p - q) \times u_{2}(\text{보},\text{바위}) \\
        & = p \times (1) + q \times (0) + (1 - p - q) \times ( - 1) \\
        & = 2p + q - 1
        \end{align}
        $$

    -   경기자 2가 '보'를 선택하면?

        $$
        \begin{align}
        E\left\lbrack u_{2}( \cdot , \text{보}) \right\rbrack & = p \times u_{2}(\text{가위},\text{보}) \\
        & + q \times u_{2}(\text{바위}, \text{보}) \\
        & + (1 - p - q) \times u_{2}(\text{보},\text{보}) \\
        & = p \times ( - 1) + q \times (1) + (1 - p - q) \times (0) \\ 
        & = - p + q
        \end{align}
        $$

-   경기자 2의 기대보수를 같게 하는 경기자 1의 확률분포

    -   (경기자 2가 '가위'를 선택할 때 기대보수)\
        = (경기자 2가 '바위'를 선택할 때 기대보수)\
        = (경기자 2가 '보'를 선택할 때 기대보수)

$$- p - 2q + 1 = 2p + q - 1\ $$ 🡪 $$3p + 3q = 2$$

$$2p + q - 1 = - p + q$$ 🡪 $$3p = 1$$

$$\therefore p^{*} = \frac{1}{3},\ q^{*} = \frac{1}{3}$$

-   가위바위보 게임의 혼합전략 내쉬균형 해석

    -   경기자 1: '가위' 선택 확률 $$p^{*} = \frac{1}{3}$$,\
        '바위' 선택 확률 $$q^{*} = \frac{1}{3}$$,\
        '보' 선택 확률 $$1 - p^{*} - q^{*} = \frac{1}{3}$$\
        {가위, 바위, 보} 제비가 같은 비율로 섞인 주머니에서\
        무작위로 하나의 제비를 추출하여 제비에 적힌 대로 실행

    -   보수표가 대칭이므로, 경기자 2의 확률도 동일

-   가위바위보 게임의 혼합전략 내쉬균형 해석

    -   순수전략의 조합\
        (가위, 가위); (가위, 바위); (가위, 보);\
        (바위, 가위); (바위, 바위); (바위, 보);\
        (보, 가위); (보, 바위); (보, 보)가 각각 $$\frac{1}{9}$$ 확률로 실현

    -   9가지 순수전략의 조합 중에서 무엇이 실현될지는 사전적으로 알 수 없음

    -   혼합전략 내쉬균형에서, 선택가능한 전략 조합은 같은 수준의 기대보수(가위바위보 게임에서는 '0')를 제공

### 요약

-   가위바위보 게임은 순수전략 내쉬균형이 존재할까?

    -   순수전략 내쉬균형이 존재하지 않음

    -   모든 순수전략 조합에서 전략을 바꿀 유인이 존재

-   가위바위보 게임의 혼합전략 내쉬균형은 무엇일까?

    -   '가위', '바위', '보'을 각각 $$\frac{1}{3}$$ 확률로 무작위 선택

-   가위바위보 게임의 혼합전략 내쉬균형은 어떻게 구현할까?

    -   같은 비율로 섞인 제비, 삼등분 주사위 등


## 정리하기

-   순수전략 내쉬균형이 존재하지 않는 게임도 존재

-   혼합전략은 합리화전략(순수전략)이 선택될 확률의 분포를 부여한 전략

-   혼합전략 내쉬균형을 따르면, 사전적으로 계산되는 경기자의 기대보수는 같은 수준에서 결정
