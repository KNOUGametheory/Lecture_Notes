---
layout: default
title: 집합과 명제
parent: 게임이론을 위한 수학
nav_order: 1
---


# 집합과 명제

## 집합의 개념과 연산
- 핵심만 쏙쏙! 

    {: .note}
	> '집합'은 지피지기와 피아식별!

### 집합과 원소
- 집합(set): 순서를 고려하지 않은 서로 다른 개체의 모임

  - $$a \in A$$: 집합 $$A$$에 속한(in, $$\in$$) 개체(원소, element) $$𝑎$$
  
  - $$a \notin A$$: 집합 $$A$$에 속하지 않은(not in, $$\notin$$) 개체 $$b$$

- 집합을 가장 먼저 학습하는 이유는?

  - 집합을 기반으로 ‘함수’, ‘관계’, ‘그래프’ 등 수학 개념 설명
  
  - 게임이론에서도 ‘경기자 집합’, ‘전략 집합’, ‘정보 집합’ 등 다양한 집합을 활용하여 게임을 정의

### 집합의 표기
- 원소나열법(roster method, by enumeration)

  - 집합에 속한 (표현가능한) 모든 원소(구성원)을 나열
  
  - 집합은 대문자, 원소는 중괄호($$\{ \}$$, brace)안의 소문자
  
- 원소나열법 예시

  - 모음(vowel)인 영어 알파벳의 집합 $$𝑉 = \{𝑎,  𝑒,  𝑖,  𝑜,  𝑢\} $$
  
  - 100보다 작은 짝수의 집합 $$ 𝐸 = \{ 2,  4,  6, \cdots , 98\} $$
  
  - ‘가위바위보’ 게임 참가자 1의 전략 $$ 𝑆_{1} = \{가위, 바위, 보\} $$

- 조건제시법(set builder notation, by description)

  - 집합을 구성하는 ‘명확한’ 조건을 문장 또는 식으로 제시
  
  - 일반적으로 모든 원소를 나열하는 것 자체에 한계가 존재
  
  - 속성 $$𝑃$$를 가진 모든 $$𝑥$$의 집합 $$\{𝑥 \vert 𝑥 \text{는 속성} 𝑃 \text{를 가진다}\}$$
  
- 조건제시법 예시

  - $$ 𝑂 = \{𝑥 \vert 𝑥 \text{는 20보다 작은 홀수인 양의 정수} \} $$
  
  - $$ 𝑂 = \{𝑥 \in \mathbb{Z}^{+} \vert 𝑥 \text{는 홀수 and } 𝑥 < 20 \} $$

### 집합의 종류와 집합 사이의 관계

- 공집합(empty set, null set) $$\emptyset$$ 또는 $$\{ \text{    } \}$$

  - 어떤 개체(원소)도 속하지 않은 집합 
  
  - 집합을 구성하는 ‘조건’을 만족하는 개체(원소)가 없기 때문
    - cf. 전체 집합  $$𝑈$$(universe): 모든 원소를 포함하는 집합

- 공집합을 포함하는 집합 $$\{\emptyset\}$$

  - 공집합을 포함하는 집합 $$\{\emptyset\}$$은 공집합일까?
  
  - $$\rightarrow$$ **NO!** 하나의 개체를 원소로 가진 단일 원소 집합!
  
  - cf. 빈 폴더와 빈 폴더를 포함하는 폴더

- 집합의 크기(cardinality) $$ \vert 𝐴 \vert $$

  - 집합에 속한 서로 다른 개체(원소)의 개수
  
  - 유한집합(finite set)과 무한집합(infinite set)을 정의
  
  - cf. 가산성(countable, denumerable)

- 무한집합의 크기는 비교할 수 없을까?
  - 자연수 $$\mathbb{N}$$, 정수 $$\mathbb{Z}$$, 유리수 $$\mathbb{Q}$$

    - $$\rightarrow$$ $$ \vert \mathbb{N} \vert = \vert \mathbb{Z} \vert = \vert \mathbb{Q} \vert $$ (why? how?)
	
  - 모든 수 집합의 크기는 같다? **NO!**
  
  - $$ \vert \mathbb{Q} \vert < \vert \mathbb{R} \vert $$ (cf. 실수 $$ \mathbb{R} $$; $$\because$$ 대각화 논법, 대각선 논법)

- 집합의 상동(equivalence) $$𝐴=𝐵$$

  - 집합 $$𝐴$$가 집합 $$𝐵$$의 부분집합($$ 𝐴 \subseteq 𝐵$$)이면서 동시에 집합 $$𝐵$$가 집합 $$𝐴$$의 부분집합($$ 𝐵 \subseteq 𝐴$$)
  
  - 두 집합의 원소가 모두 같음을 보이는 데 한계가 존재

- 진부분집합(proper subset) $$A \subsetneq B$$

  - 집합 $$𝐴$$가 집합 $$𝐵$$의 부분집합($$A \subseteq B$$)이면서 동시에 집합 $$𝐴$$와 집합 $$𝐵$$가 상등이 아닐 때($$𝐴 \neq 𝐵$$)
  
  - cf. 일상생활의 부분집합 관계는 대부분 진부분집합

- 멱집합(powerset)

  - $$\mathcal{p}(S)$$ : 집합 $$𝑆$$의 모든 부분집합을 원소로 가진 집합
  
  - $$𝐵 = \{0,  1\}$$
    
	- $$\rightarrow \mathcal{𝒫}(𝐵) = \{\emptyset, \{0\}, \{1\}, \{0, 1\} \} $$ 
	
	- $$\emptyset \rightarrow \mathcal{𝒫}(\emptyset) = \{\emptyset\}; \{\emptyset\} \rightarrow \mathcal{𝒫}(\{\emptyset\}) = \{ \emptyset,  \{\emptyset\} \} $$
  
  - 유한집합의 부분집합의 개수는?

    - 유한집합 $$𝑆$$ 의 멱집합 $$\mathcal{𝒫}(𝑆)$$의 크기
	- $$\vert S \vert = 𝑛 \rightarrow \vert \mathcal{𝒫}(𝑆) \vert = 2^{𝑛} $$ (why? how?)

### 집합의 연산
- 합집합(union) $$A \cup B $$

  -  집합 $$𝐴$$와 집합 $$𝐵$$ 중 적어도 하나에 포함된 개체(원소)의 집합
  
  -  $$𝐴 \cup 𝐵 = \{𝑥 \vert 𝑥 \in 𝐴 \text{ 또는 } 𝑥 \in 𝐵 \} = \{ 𝑥 \vert 𝑥 \in 𝐴 \vee x \in 𝐵 \} $$

	 ![Venn Diamgram of Union Sets](/images/Lec_1_Union_set_VD.png)

	 | $$A$$ | $$B$$  | $$A \vee B $$ |
	 | True  | True   | True          |
	 | True  | False  | True          |
	 | False | True   | True          |
	 | False | False  | False         | 

- 교집합(intersection) $$ 𝐴 \cap 𝐵 $$
  
  -  집합 $$𝐴$$와 집합 $$𝐵$$ 모두에 포함된 개체(원소)의 집합
  
  - $$ 𝐴 \capt 𝐵 = \{𝑥 \vert 𝑥 \in 𝐴 \text{ 그리고 } 𝑥 \in 𝐵\ } = \{𝑥 \vert 𝑥 \in 𝐴 \wedge 𝑥 \in 𝐵 \} $$
  
  - cf. 집합 $$𝐴$$와 집합 $$𝐵$$는 서로소(disjoint) if $$𝐴 \cap 𝐵 = \emptyset $$

	 ![Venn Diamgram of Intersection Sets](/images/Lec_1_Intersection_set_VD.png)

	 | $$A$$ | $$B$$  | $$A \wedge B $$ |
	 | True  | True   | True            |
	 | True  | False  | False           | 
	 | False | True   | False           | 
	 | False | False  | False           | 

- 차집합(difference) $$𝐴−𝐵$$ 또는 $$𝐴∖𝐵$$

  - 집합 𝐴의 원소 중 집합 𝐵에 포함되지 않은 원소의 집합
  
   $$
   𝐴 − 𝐵 = \{𝑥 \vert 𝑥 \in 𝐴 \text{ 그리고 } 𝑥 \notin  𝐵 \} = \{𝑥 \vert 𝑥 \in 𝐴 \wedge 𝑥 \notin 𝐵 \} 
   $$ 	
   
   $$
   𝐴−𝐵 = 𝐴 − ( 𝐴 \cap B )
   $$

   ![Venn Diamgram of Difference Sets](/images/Lec_1_difference_set_VD_1.png)

   ![Venn Diamgram of Difference Sets](/images/Lec_1_difference_set_VD_2.png)



## 명제와 논리

## 증명의 기초