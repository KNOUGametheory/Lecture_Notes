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
  
  -  $$𝐴 \cup 𝐵 = \{𝑥 \vert 𝑥 \in 𝐴 \text{ 또는 } 𝑥 \in 𝐵 \} = \{ 𝑥 \vert 𝑥 \in 𝐴 \lor x \in 𝐵 \} $$

	 ![Venn Diamgram of Union Sets](/images/Lec_1_Union_set_VD.png)

	 | $$a$$ | $$b$$  | $$a \lor b $$ |
	 | True  | True   | True          |
	 | True  | False  | True          |
	 | False | True   | True          |
	 | False | False  | False         | 

- 교집합(intersection) $$ 𝐴 \cap 𝐵 $$
  
  -  집합 $$𝐴$$와 집합 $$𝐵$$ 모두에 포함된 개체(원소)의 집합
  
   $$ 
   𝐴 \cap 𝐵 = \{𝑥 \vert 𝑥 \in 𝐴 \text{ 그리고 } 𝑥 \in 𝐵 \} = \{𝑥 \vert 𝑥 \in 𝐴 \land 𝑥 \in 𝐵 \} 
   $$
  
  - cf. 집합 $$𝐴$$와 집합 $$𝐵$$는 서로소(disjoint) if $$𝐴 \cap 𝐵 = \emptyset $$

	 ![Venn Diamgram of Intersection Sets](/images/Lec_1_Intersection_set_VD.png)

	 | $$a$$ | $$b$$  | $$a \land b $$ |
	 | True  | True   | True            |
	 | True  | False  | False           | 
	 | False | True   | False           | 
	 | False | False  | False           | 

- 차집합(difference) $$𝐴−𝐵$$ 또는 $$𝐴∖𝐵$$

  - 집합 𝐴의 원소 중 집합 𝐵에 포함되지 않은 원소의 집합
  
   $$
   𝐴 − 𝐵 = \{𝑥 \vert 𝑥 \in 𝐴 \text{ 그리고 } 𝑥 \notin  𝐵 \} = \{𝑥 \vert 𝑥 \in 𝐴 \land 𝑥 \notin 𝐵 \} 
   $$ 	
   
   $$
   𝐴−𝐵 = 𝐴 − ( 𝐴 \cap B )
   $$

   ![Venn Diamgram of Difference Sets](/images/Lec_1_difference_set_VD_1.png)

   ![Venn Diamgram of Difference Sets](/images/Lec_1_difference_set_VD_2.png)

- 여집합(complement) $$ 𝐴^{𝑐} $$ 또는 $$\overline{A}$$

  - 전체집합 $$𝑈$$의 원소이지만 집합 $$𝐴$$에는 속하지 않는 원소의 집합
  
  $$
  \overline{A} = \{𝑥 \vert 𝑥 \in 𝑈 \text{ 그리고 } 𝑥 \notin 𝐴 \} = \{𝑥 \vert 𝑥 \in 𝑈 \land 𝑥 \notin 𝐴 \} 
  $$
  
  $$
  𝐴−𝐵 = 𝐴 − (𝐴 \cap B) = 𝐴 \cap \overline{𝐵}
  $$
  
  ![Venn Diamgram of Complements Sets](/images/Lec_1_complement_set_VD.png)

	 | $$a$$ | $$\neg a$$  | 
	 | True  | False       | 
	 | False | True        | 

- 연산 법칙

  - 항등 법칙: $$ 𝐴 \cap 𝑈 = 𝐴, 𝐴 \cup \emptyset = 𝐴 $$
  
  - 지배 법칙: $$ 𝐴 \cup 𝑈 = 𝑈, 𝐴 \cap \emptyset = \emptyset $$
  
  - 멱등 법칙: $$ 𝐴 \cup 𝐴 = 𝐴, 𝐴 \cap 𝐴 = 𝐴 $$
  
  - 보원 법칙: $$ \overline{(\overline{A})} = A $$
  
  - 교환 법칙: $$ 𝐴 \cup 𝐵 = 𝐵 \cup 𝐴, 𝐴 \cap 𝐵 = 𝐵 \cap 𝐴 $$
  
  - 결합 법칙: $$ 𝐴 \cup ( 𝐵 \cup 𝐶 ) = ( 𝐴 \cup 𝐵 ) \cup 𝐶; 𝐴 \cap ( 𝐵 \cap 𝐶) = ( 𝐴 \cap 𝐵 ) \cap 𝐶 $$
  
  - 분배 법칙: 

    - $$ 𝐴 \cup ( 𝐵 \cap 𝐶 ) = ( 𝐴 \cup 𝐵) \cap ( 𝐴 \cup 𝐶) $$
	
	- $$ 𝐴 \cap ( 𝐵 \cup 𝐶 ) = ( 𝐴 \cap 𝐵) \cup ( 𝐴 \cap 𝐶) $$
  
  - 드 모르간(De Morgan)의 법칙 $$ \overline{A \cap B} = \overline{A} \cup \overline{B}, \overline{a \cup B} = \overline{A} \cap \overline{B} $$
  
  - 흡수 법칙: $$ 𝐴 \cup ( 𝐴 \cap 𝐵 ) = 𝐴, 𝐴 \cap ( 𝐴 \cup 𝐵 ) = 𝐴 $$
  
  - 보수 법칙: $$ 𝐴 \cup \overline{A} = 𝑈,  𝐴 \cap \overline {A} = \emptyset $$

### 응용해 봅시다!

  - ‘가위바위보’ 게임을 집합으로 정의해보면?
  
  - 경기자(player) 집합 $$ 𝐼 = \{ 1, 2 \} $$
  
  - 경기자 $$ 𝑖 \in 𝐼$$ 의 전략 집합 $$ 𝑆_{𝑖} = \{ \text{가위}, \text{바위}, \text{보} \} $$
  
  - 전략 프로파일 $$ (𝑠_{1}, 𝑠_{2})$$에 따른 경기자의 보수 $$ u_{i} (𝑠_{1}, 𝑠_{2} ) $$

       |          |       | $$P_{2}$$    |             |             | 
	   |          |       | 가위          | 바위         |     보       | 
	   | $$P_{1}$$| 가위   | $$(0, 0)$$   | $$(-1, 1)$$ | $$(1, -1)$$  | 
	   |          | 바위   | $$(1, -1)$$  | $$(0, 0)$$  | $$(-1, 1)$$  | 
	   |          | 보    | $$(-1, 1)$$  | $$(1, -1)$$  | $$(0, 0)$$  | 


## 명제와 논리
- 핵심만 쏙쏙! 

    {: .note}
	> '명제'는? 집합으로 분류된 '피아'의 관계!

### 명제의 정의

- 명제(proposition) $$𝑝$$

  - 참(True)/거짓(False) 중 하나의 진리값을 갖는(진리값을 명확하게 구별할 수 있는) 문장 또는 식
  
  - cf. 명제 $$𝑝$$의 부정: $$\neg 𝑝$$ 또는 “not $$p$$”

- 명제를 학습하는 이유는?

  - 수학적 진술의 명확화, 논리적 추론이 가능
  
  - 대상 또는 진술 사이의 관계를 검증

- 조건명제 또는 명제함수 $$𝑝(𝑥)$$

  - 변수의 값에 따라 명제의 참(True)/거짓(False)이 판별
  
  - 어떤 전체집합 $$𝑈$$ (또는 정의역 $$\mathcal{D}$$)의 임의의 원소 $$x \in U $$를 대입하면 명제가 되는 관계식 

- 진리집합(truth set)

  - 명제함수 $$𝑝(𝑥)$$에 대하여, 명제함수를 ‘참(True)’으로 만드는 전체집합 $$𝑈$$에 속한 원소 $$𝑥$$의 집합
  
  - 진리집합 $$ 𝑃 = \{ 𝑥 \in 𝑈 \vert 𝑝(𝑥) \text{는 "참(True)"} \} $$
  
### 명제의 연산

- 논리합(disjunction)

  - 두 명제 $$𝑝$$와 $$𝑞$$가 모두 ‘거짓’일 때만 ‘거짓'

    - 다른 경우에는 진리값이 ‘참’인 관계
  
  - 논리합의 표현: $$ 𝑝 \lor 𝑞$$ 또는 “𝑝 or 𝑞”

	| $$p$$ | $$q$$  | $$p \lor q $$ |
	| T     | T      | T             |
	| T     | F      | T             |
	| F     | T      | T             |
	| F     | F      | F             |
  
-  논리곱(conjunction)

  - 두 명제 $$𝑝$$와 $$𝑞$$가 모두 ‘참’일 때만 ‘참'

    -  다른 경우에는 진리값이 ‘거짓’인 관계

  - 논리합의 표현: $$𝑝 \land 𝑞$$ 또는 “𝑝 and 𝑞”

    | $$p$$ | $$q$$  | $$p \land q $$ |
	| T     | T      | T               |
	| T     | F      | F               |
	| F     | T      | F               |
	| F     | F      | F               |

- 배타적(exclusive) 논리합

  - 두 명제 $$𝑝$$와 $$𝑞$$ 중 어느 하나만 ‘참’일 때 ‘참'

    - $$𝑝$$와 $$𝑞$$가 모두 ‘거짓‘일 때 ‘거짓’
	
	- $$𝑝$$와 $$𝑞$$가 모두 ‘참‘일 때 ‘거짓’인 관계

  - 배타적 논리합의 표현: $$𝑝 \oplus 𝑞$$ 또는 “𝑝 xor 𝑞”

- 논리합과 배타적 논리합의 비교

  - (포괄적) 논리합은 모두 ‘참‘이어도 ‘참’
  
  - 배타적 논리합은 모두 ‘참‘일 때 ‘거짓’

    | $$p$$ | $$q$$  | $$p \oplus q $$ |
	| T     | T      | F               |
	| T     | F      | F               |
	| F     | T      | F               |
	| F     | F      | F               |


### 조건문과 필요조건, 충분조건

- 조건문 $$ 𝑝 \rightarrow 𝑞 $$

  - 가정 또는 전제 $$𝑝$$가 ‘참’이라는(성립한다는) 조건에서 결론 또는 결과 $$𝑞$$가 ‘참‘이라고 주장할 때 활용
  
  - 가정 $$𝑝$$가 ‘참’이고 결론 $$𝑞$$가 ‘거짓‘일 때 $$ 𝑝 \rightarrow 𝑞$$ 는 ‘거짓’
  
  - $$ p \rightarrow q $$의 표현: “$$𝑝$$이면 $$𝑞$$이다.”, “IF $$𝑝$$, THEN $$𝑞$$”, “$$𝑝$$ implies $$𝑞$$”
  
  - cf. 가정 $$𝑝$$가 ‘거짓’이고, 결론 $$𝑞$$가 ‘거짓‘일 때 $$𝑝 \rightarrow 𝑞$$는 ‘참’(why?)

    | $$p$$ | $$q$$  | $$p \rightarrow q $$ |
	| T     | T      | T                    |
	| T     | F      | F                    |
	| F     | T      | T                    |
	| F     | F      | T                    |

- 필요조건, 충분조건, 필요충분조건

  - 조건문 $$𝑝 \rightarrow 𝑞$$의 진리값이 ‘참(True)’일 때만 성립
  
  - 충분조건(sufficient condition) $$𝑝 \rightarrow 𝑞$$가 ‘참‘일 때, 가정 $$𝑝$$
  
  - 필요조건(necessary condition) $$𝑝 \rightarrow 𝑞$$가 ‘거짓‘일 때, 결론 $$𝑞$$
  
  - 필요충분조건(necessary and sufficient condition) 필요조건이면서 동시에 충분조건!

- 조건문의 역, 이, 대우

  - 조건문 $$𝑝 \rightarrow 𝑞$$ 
    
	- “비가 오면, 김치전을 먹는다”
  - 역(converse) $$q \rightarrow p$$

    - “김치전을 먹으면, 비가 온다“
  - 이(inverse) $$\neg 𝑝 \rightarrow \neg 𝑞$$ 

	- “비가 오지 않으면, 김치전을 먹지 않는다”

  - 대우(contraposition) $$\neg q \rightarrow \neg p$$

    - “김치전을 먹지 않으면, 비가 오지 않는다”

### 논리적 동치
- 드 모르간의 법칙: 명제의 부정으로 논리를 단순화

  - $$\neg (p \land q) \equiv \neg p \lor \neg q $$

    | $$p$$ | $$q$$  | $$p \land q$$ | $$ \neg (p \land q) $$ | $$ \neg p$$ | $$ \neg q$$ | $$\neg p \lor \neg q$$ |
	| T     | T      | T              | F                       | F           | F           | F                      |
	| T     | F      | F              | T                       | F           | T           | T                      |
	| F     | T      | F              | T                       | T           | F           | T                      |
	| F     | F      | F              | T                       | T           | T           | T                      |


  - $$\neg (p \lor q) \equiv \neg p \land \neg q $$

    | $$p$$ | $$q$$  | $$p \lor q$$ | $$ \neg (p \lor q) $$     | $$ \neg p$$ | $$ \neg q$$ | $$\neg p \land \neg q$$ |
	| T     | T      | T              | F                       | F           | F           | F                        |
	| T     | F      | T              | F                       | F           | T           | F                        |
	| F     | T      | T              | F                       | T           | F           | F                        |
	| F     | F      | F              | T                       | T           | T           | T                        |


- 조건문 $$𝑝 \rightarrow 𝑞$$ 의 동치: $$\neg p \lor q $$

  - 조건문 $$𝑝 \rightarrow 𝑞$$ 는 가정 $$𝑝$$가 ‘참(True)’이고 결론 $$𝑞$$가 ‘거짓(False)’일 때만 ‘거짓(False)’
  
  - “비가 오면, 김치전을 먹는다” $$\equiv$$ “비가 오지 않거나 김치전을 먹는다”

    | $$p$$ | $$q$$  | $$p \rightarrow q$$ | $$ \neg p$$ | $$ q$$ | $$\neg p \lor q$$ |
	| T     | T      | T                   | F           | T      | T                 |
	| T     | F      | F                   | F           | F      | F                 |
	| F     | T      | T                   | T           | T      | T                 |
	| F     | F      | T                   | T           | F      | T                 |
	
- 새로운 논리적 동치 만들기
    $$
    \begin{align}
	\neg (p \rightarrow q) & \equiv p \land \neg q \\
    \neg (p \rightarrow q) & \equiv \neg (\neg p \lor q) \quad \text{(조건문의 동치)} \\
                           & \equiv \neg (\neg p) \land \neg q \\
                           & \equiv p \land \neg q \quad \text{(드 모르간의 법칙, 이중 부정)} \\
    \end{align}
    $$
	
    $$
	\begin{align}
    \neg(p \lor (\neg p \land q)) & \equiv \neg p \land \neg q \\
	\neg(p \lor (\neg p \land q)) & \equiv \neg p \land \neg (\neg p \land q) \\
	                               & \equiv \neg p \land (\neg (\neg p) \lor \neg q) \quad \text{(드 모르간의 법칙)} \\
								   & \equiv \neg p \land (p \lor \neg q) \\
								   & \equiv (\neg p \land p) \lor (\neg p \land \neg q) \quad \text{(분배 법칙)} \\
								   & \equiv F \lor (\neg p \land \neg q) \\
								   & \equiv \neg p \land \neg q \quad \text{(부정법칙, 항등법칙)}\\ 
	\end{align}
	$$ 	

### 한정 기호

- 전칭 한정기호(universal quantifier) $$\forall$$

  - 어떤 변수가 취할 수 있는 모든 값에 대하여 주어진 명제가 ‘참(True)’이라고 주장할 때 활용
  
  - $$\forall x p(x)$$: 정의역에 속한 모든 $$𝑥$$의 값에 대하여 $$𝑃(𝑥)$$ “모든 $$𝑥$$에 대하여 $$𝑃(𝑥)$$” 또는 “임의의 $$𝑥$$에 대하여 $$𝑃(𝑥)$$”
  
  - $$𝑃(𝑥):𝑥+2 > 𝑥$$, 정의역이 실수 전체일 때($$\mathcal{D} = \mathbb{R}$$), $$\forall x p(x) = T$$ 또는 $$\forall x \in \mathbb{R}$$, $$𝑃(𝑥):(𝑥+2)−𝑥 = 2 > 0 \rightarrow T$$
  
  - cf. 반례(counter example): $$𝑃(𝑥)=𝐹$$로 만드는 정의역 원소 $$𝑥 \in \mathcal{D}$$

- 존재 한정기호(existential quantifier) $$\exists$$

  - 어떤 특성을 갖는 원소가 존재한다고 주장할 때 활용
  
  - $$\exists x Q(x)$$: 정의역에 속하는 적어도 하나의 $$𝑥$$에 대하여 $$𝑄(𝑥)$$ “어떤 $$𝑥$$에 대하여 $$𝑄(𝑥)$$” 또는 “적어도 한 $$𝑥$$에 대하여 $$𝑄(𝑥)$$”
  
  - $$𝑄(𝑥):3<𝑥<5$$, 정의역이 자연수일 때($$\mathcal{D} = \mathbb{N}$$), $$\exists x Q(x) = T$$ 또는 $$\exists x \in \mathbb{N} $$ such that $$ 𝑄(4):3<4<5 \rightarrow T$$
  
  - cf. 유일 한정기호 $$\exists!$$ 또는 $$\exists_{1}$$

- 한정기호에 대한 드 모르간의 법칙

  - $$\neg \forall x P(x) \equiv \exists x \neg P(x)$$: “정의역에 속한 모든 $$𝑥$$가 $$𝑃(𝑥)$$를 만족시키지 않는다”?

  - $$\exists x Q(x) \equiv \forall x \neg Q(x)$$ “정의역에 속한 어떤 $$𝑥$$에 대하여 $$𝑄(𝑥)$$를 만족하는 것이 없다?”

    | 부정                       | 동치 표현                  | 참                                  | 거짓                               | 
	| $$\neg \forall x P(x)$$   | $$\exists x \neg P(x)$$  | $$P(x)$$가 거짓이 되는 $$x$$가 존재할 때  | 모든 $$x$$에 대하여 $$P(x)$$가 참일 때 | 
	| $$\neg \exists x Q(x)$$   | $$\forall x \neg Q(x)$$  | 모든 $$x$$에 대하여 $$Q(x)$$가 거짓일 때  | $$Q(x)$$가 참이 되는 $$x$$가 존재할 때 | 


### 응용해 봅시다!

  - ‘가위바위보’ 게임에서 "이기기 위한 전략"은?
  
  - 경기자(player) 집합 $$ 𝐼 = \{ 1, 2 \} $$
  
  - 경기자 $$ 𝑖 \in 𝐼$$ 의 전략 집합 $$ 𝑆_{𝑖} = \{ \text{가위}, \text{바위}, \text{보} \} $$
  
  - (가위, 보); (바위, 가위); (보; 바위)? 순수전략? 혼합전략?

       |          |       | $$P_{2}$$    |             |             | 
	   |          |       | 가위          | 바위         |     보       | 
	   | $$P_{1}$$| 가위   | $$(0, 0)$$   | $$(-1, 1)$$ | $$(1, -1)$$  | 
	   |          | 바위   | $$(1, -1)$$  | $$(0, 0)$$  | $$(-1, 1)$$  | 
	   |          | 보    | $$(-1, 1)$$  | $$(1, -1)$$  | $$(0, 0)$$  | 

## 증명의 기초

- 핵심만 쏙쏙! 

    {: .note}
	> '증명'은? 그럴듯한 것을 정말로 그러하게!


###  증명에 대한 이해

- 증명(proof)

  - 어떤 수학적 진술(statement)이 ‘참’임을 입증하는 논리적으로 타당한 수학적 논증
  
  - Prove $$\ldots$$, Show $$\ldots$$, Confirm that $$\ldots$$
  
  - 증명의 구성 요소와 추론 규칙으로 ‘참’/’거짓’을 증명

- 증명은 무엇으로부터 시작할 수 있을까?

  - 증명하고자 하는 정리에서 성립한다고 가정한 진술
  
  - ‘참’이라고 가정된 공리(Axiom), 이미 증명된 정리 등

- 증명하고자 하는 진술의 중요도에 따른 분류

  - 정리(Theorem)
  
  - 주장/명제(Proposition)
  
  - 보조정리/기본정리(Lemma)
  
  - 따름정리(Corollary)

- 증명할 필요가 없거나 아직 증명되지 않은 진술

  - 공리(Axiom): 증명하지 않는 정리
  
  - 가설/짐작(Conjecture): 직관에 의해 ‘참’이라고 주장



### 증명 방법: 직접 증명

- 조건문 $$p \rightarrow q $$를 증명하는 절차

  - 전제 $$𝑝$$가 ‘참(True)‘임을 가정
  
  - 추론 규칙을 적용하여 논리를 발전
  
  - 결론 $$𝑞$$가 ‘참(True)’임을 확인

- 조건문을 증명할 때 논리를 발전시키는 방법

  - 전제 $$𝑝$$가 ‘참‘이면 결론 $$𝑞$$가 ‘참’일 수밖에 없음
  
  - 전제 $$𝑝$$가 ‘참‘이면서 동시에 결론 $$𝑞$$가 ‘거짓’일 수 없음

- 예제 1: $$𝑛$$이 홀수이면, $$𝑛^{2}$$도 홀수이다?

  - $$\forall n (P(n) \rightarrow (Q(n)))$$
    
	- $$𝑃(𝑛)$$: $$𝑛$$은 홀수이다
	
	- $$𝑄(𝑛)$$: $$𝑛^{2}$$은 홀수이다
	
  - 전제 $$P(n)$$이 성립한다고 가정

    - 홀수(odd numbers)의 정의는? 
	
	- $$n \in \mathbb{Z}$$ is an odd number if $$\exists k \in \mathbb{Z}, \quad \text{s.t. } n = 2k+1 $$
	
  - 논리 발전 및 결론: $$𝑄(𝑛)$$가 성립함을 도출

    $$ 
	\begin{align}
	𝑛^{2} & = (2𝑘+1)^{2} \\
	      & = 4𝑘^{2}+4𝑘+1 \\
		  & = 2(2𝑘^{2}+2𝑘)+1 \\
	\end{align}
	$$	  
	
	$$
	2𝑘^2+2𝑘 = 𝑘^{'} \in \mathbb{Z} \\
	$$
	
	$$
	𝑛^2=2𝑘^′+1 \quad \blacksquare
	$$

- 예제 2: 실수 $$a, b, x, y$$에 대하여 $$(𝑎^{2}+𝑏^{2})(𝑥^{2}+𝑦^{2}) \geq (𝑎𝑥+𝑏𝑦)^{2}$$?

  - '(좌변) $$\geq$$ (우변)'임을 보이려면?

    - (좌변) $$-$$ (우변) $$\geq 0$$ !
    
	$$
	\begin{align}
	(𝑎^{2} & + 𝑏^{2})(𝑥^{2} + 𝑦^{2})−(𝑎𝑥 + 𝑏𝑦)^{2} \\
	& = (𝑎^{2} 𝑥^{2} + 𝑎^{2} 𝑦^{2} + 𝑏^{2} 𝑥^{2} + 𝑏^{2} 𝑦^{2}) −(𝑎^{2} 𝑥^{2} + 2𝑎𝑏𝑥𝑦 + 𝑏^{2} 𝑦^{2}) \\
	& = 𝑎^{2} 𝑦^{2} − 2𝑎𝑏𝑥𝑦 + 𝑏^{2} 𝑥^{2} \\
	& =(𝑎𝑦 − 𝑏𝑥)^{2} \geq 0 \\
	\end{align}
	$$

    (단, 등호$$(=)$$는 $$𝑎/𝑥=𝑏/𝑦$$일 때 성립) $$\blacksquare$$

### 증명 방법: 대우 증명

- 대우(contraposition) 관계를 이용한 증명

  - 전제로부터 결론에 도달하는 직접 증명을 적용하는 것이 불가능한 상황에서 활용
  
  - 주장하려는 정리와 동치인 정리(대우)를 증명
  
  - cf. $$p \rightarrow q $$의 대우는 $$\neg q \rightarrow \neg p$$

- 대우 증명을 적용하려면?

  - 대우 $$\neg q \rightarrow \neg p$$의 관점에서는 직접 증명과 동일
  
  - 논리를 발전시키는 방향이 달라지면서 증명이 용이해지기도? 

- 예제 1: $$3𝑛+2$$가 홀수이면 $$𝑛$$은 홀수이다?

  - 전제 ‘$$3𝑛+2$$가 홀수’에서 출발하면?

    - $$3𝑛+2=2𝑘+1$$을 만족하는 정수 $$𝑘$$가 존재

    - 이항하여 $$3𝑛+1=2𝑘$$를 이용하려면? 
	
	- 경우 나누기? (how?)
  
  - 대우를 이용하여 증명하면?
  
  - 명제의 대우: "$$𝑛$$이 짝수이면 $$3𝑛+2$$도 짝수이다"
  
  - $$𝑛=2𝑘$$를 만족하는 정수 $$𝑘$$가 존재하면
  
  - $$3𝑛+2=3(2𝑘)+2=2(3𝑘+1)$$ 
  
  - $$3𝑘+1 \in \mathbb{Z} \quad \blacksquare$$
  
- 예제 2: 자연수 $$a$$와 $$b$$에 대하여, $$n=ab$$이면 $$ a \leq \sqrt{n}$$ 또는 $$b \leq \sqrt{n}$$?

  - 직접 증명하려면?

    - $$ n=ab $$로부터 유도할 수 있는 조건은?

    - 인수분해 후 각 인수에 대한 대소관계를 비교하려면?
	
  - 대우를 이용하여 증명하면?
  
  - 명제의 대우: "$$(a > \sqrt{n}) \land ( 𝑏 > \sqrt{𝑛}) \rightarrow n \neq ab$$"
  
  - 두 부등식을 같은 변끼리 곱하면, $$ ab > \sqrt{𝑛}\sqrt{𝑛} = 𝑛$$ $$\blacksquare$$ 



### 증명 방법: 모순 증명

- 모순(contradiction)을 이용한 증명

  - $$𝑝$$: ‘참’임을 증명하고자 하는 정리
  
  - $$\neg 𝑝 \rightarrow 𝑞$$가 ‘참’이 되게 하는 모순 $$𝑞$$를 발견
  
  - 조건문 $$\neg p \rightarrow q$$가 ‘참’이고 모순 $$𝑞$$가 ‘거짓’이면
  
  - $$\neg p$$는 ‘거짓‘일 수밖에 없으므로 $$𝑝$$가 ‘참‘이라는 결론

- 모순 증명은 언제 활용할까?

  - 직접 증명으로 증명하기 어려운 경우
  
  - 모순을 발견하는 게 상대적으로 용이한 경우

- 예제 1: $$\sqrt{2}$$는 무리수이다?
  
  - 무리수(irrational number)의 정의는?

    - 분수꼴 ($$ 𝑏/𝑎, 𝑎 \neq 0, 𝑏$$는 서로소인 정수)로 표현될 수 없는 수
  
  - 분수꼴로 표현되지 않는다는 사실을 활용하려면?
  
  - 모순을 이용하여 증명하면?
  
  - $$\sqrt{2}$$가 유리수라고 가정 
  
  - $$\sqrt{2}= b / a$$인 서로소인 정수 $$ a \neq 0, b $$가 존재
  
  - $$\sqrt{2} = b / a \rightarrow b = \sqrt{2}a 
  
  - \rightarrow$$ 양변을 제곱하면 $$𝑏^{2}=2𝑎^{2}$$ ... (이하 생략) ...

- 예제 2: $$3𝑛+2$$가 홀수이면 $$𝑛$$은 홀수이다?

  - 정리 $$𝑝 \rightarrow 𝑞$$가 ‘거짓’이라 전제하려면?

    - $$𝑝$$가 ‘참’이고 $$𝑞$$는 ‘거짓’!
	
	- 여기에서부터 논리를 발전시켜 모순에 도달
	
  - $$3𝑛+2$$가 홀수이고 $$𝑛$$은 짝수라고 가정
  
  - $$𝑛=2𝑘$$를 만족하는 정수 $$𝑘$$가 존재
  
  - $$\rightarrow 3𝑛+2 = 3(2𝑘)+2 = 2(3𝑘+1)$$이므로 
  
  - 짝수 $$3𝑛+2$$가 홀수이고 동시에 $$3𝑛+2$$가 짝수? 
  
  - 모순! $$\blacksquare$$
  
  - “$$p \rightarrow q$$가 거짓”이라는 전제가 ‘거짓’ $$\rightarrow$$ $$p \rightarrow q$$가 참!

###  응용해 봅시다!

- 게임이론에서 어떤 전략이 ‘유리한지’ 증명하려면?

  - 우월전략(dominant strategy)
  
  - 열등전략(dominated strategy)
  
  - 내쉬균형(Nash Equilibrium)
  
  - 보수 함수 사이의 관계 파악이 중요