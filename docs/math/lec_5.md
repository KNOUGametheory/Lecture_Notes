---
layout: default
title: 확률 기초
parent: 게임이론을 위한 수학
nav_order: 5
---


# 확률 기초

## 경우의 수

- 핵심만 쏙쏙!

    {: .note}
	> - (게임의 구성요소) 경기자, 전략, 결과, 보수, 게임의 규칙 $$\rightarrow$$ 공통지식 
	>
	>    - 경기자($$i$$)의 action profile $$(a_{i1},\cdots,a_{ij},\cdots,~a_{in})$$
	>	
	>    - 1회 게임의 순수전략
	>	
	>    - 반복게임을 하는 경우 경기자의 순수전략
	>	
	>   - 각 경기자의 순수전략
	>	
	>   - 각 경기자의 전략에 따른 결과(outcome)는 경우의 수

### 동전 던지기

- 동전을 한 번 던질 때 발생하는 사건

- 동전을 두 번 던질 때 발생하는 사건

- 동전을 $$n$$ 번 던질 때 발생하는 사건

  ![동전 던지기](/images/Lec_1_5_1_2.png)
  
  
### 윷놀이

- 도, 개, 걸, 윷, 모가 나오는 사건

  ![윷 던지기](/images/Lec_1_5_1_1.jpg)
  
  
### 순열(permutation)

- $$n$$개의 대상물이 있고, 순서대로 뽑아서 줄을 세우는 경우의 수

- (a, b, c) 3개 대상물의 순열 $$\rightarrow$$ 6가지(abc, acb, bac, bca, cab, cba)

- (1, 2, 3, 4) 4개 대상물의 순열 $$\rightarrow$$ 24가지

	- 1234, 1243, 1324, 1342, 1423, 1432, 2134, 2143, 2314, 2341, 2413, 2431
		
	- 3124, 3142, 3214, 3241, 3412, 3421, 4123, 4132, 4213, 4231, 4312, 4321


### $$!$$ factorial

$$n!=n\times(n-1)\times(n-2)\times\cdots 3\times2\times1$$

### 순열의 계산  

$$\begin{split}
	P(n,~r)={}_{n}{P}_{r}
	=& \underbrace{n\times (n-1)\times (n-2)\times\cdots \times(n-r+1)}_{\text{r개의 항(term)}} \\
	=&\frac{n\times (n-1)\times\cdots \times(n-r+1)\times(n-r)!}{(n-r)!}=\frac{n!}{(n-r)!}
	\end{split}$$
	

### 조합(combination)

- $$n$$개의 원소를 갖는 집합에서 $$r$$개의 원소를 선택하는 경우의 수

- (a, b, c) 중에서 2개를 뽑는 조합

	- 3가지 (ab, ac, bc)

	- (ab, ba) 동일, (ac, ca) 동일 (bc, cb) 동일
	
- (a, b, c, d) 중에서 2개를 뽑는 조합

	- 6가지 (ab, ac, ad, bc, bd, cd)
	
	- (ab, ba) 동일, (ac, ca) 동일, (ad, da) 동일, (bc, cb) 동일, (bd, db) 동일, (cd, dc) 동일


### 조합의 계산 
- $$n$$ choose $$r$$이라고 읽는다. 

$$
	\begin{split}
	C(n,~r)={}_{n}{C}_{r}={n \choose r}
	=&\frac{\overbrace{n\times (n-1)\times (n-2)\times\cdots \times(n-r+1)}^{\text{r개의 항(term)}}}{r!}\\
	=&\frac{n\times (n-1)\times\cdots \times(n-r+1)\times(n-r)!}{r!(n-r)!}=\frac{n!}{r!(n-r)!}
	\end{split}
$$


### 이항계수(binomial coefficient)

- 동전을 한 번 던지는 경우의 수 ($$2^{1}=2$$개)
	
$${\bf H}ead, {\bf T}ail$$

- 동전을 두 번 던지는 경우의 수 ($$2^{2}=4$$개)
	
	- HH(1개), HT(2개), TT(1개)
	
- 동전을 세 번 던지는 경우의 수 ($$2^{3}=8$$개)
	
	- HHH(1개), HHT(3개), HTT(3개), TTT(1개)
	
- 동전을 $$n$$ 번 던지는 경우의 수

	- $${}_{n}{C}_{r}$$을 이용
	
	- 즉, $$n$$ 번 중 앞면($$r$$ 번) 또는 뒷면($$n-r$$ 번) 나오는 경우의 수를 계산
	
	$${}_{n}{C}_{r}=\frac{n!}{r!(n-r)!}={}_{n}{C}_{n-r}$$
	
  ![이항계수](/images/Lec_1_5_1_4.jpeg)
  
  
### 동전 두 번 던지기 (이항계수 활용)

- 경우의 수는 4개이며, 1개의 $$HH$$, 2개의 $$HT$$, 1개의 $$TT$$

- 이항계수 $${}_{2}{C}_{0}$$, $${}_{2}{C}_{1}$$, $${}_{2}{C}_{2}$$

$${}_{2}{C}_{0}H^{2}T^{0}=\left(\begin{array}{c}2\\ 0\\ \end{array}\right)H^{2}T^{0}=1\times HH$$
		
$${}_{2}{C}_{1}H^{2}T^{1}=\left(\begin{array}{c}2\\ 1\\ \end{array}\right)H^{1}T^{1}=2\times HT$$

$${}_{2}{C}_{2}H^{0}T^{2}=\left(\begin{array}{c}2\\ 2\\ \end{array}\right)H^{0}T^{2}=1\times TT$$


### 동전 세 번 던지기 (이항계수 활용)

- 경우의 수는 8개이며, 1개의 $$HHH$$, 3개의 $$HHT$$, 3개의 $$HTT$$,
1개의 $$TTT$$

- 이항계수 $${}_{3}{C}_{0}$$, $${}_{3}{C}_{1}$$, $${}_{3}{C}_{2}$$, $${}_{3}{C}_{3}$$

$${}_{3}{C}_{0}H^{3}T^{0}=\left(\begin{array}{c}3\\ 0\\ \end{array}\right)H^{3}T^{0}=1\times HHH$$
		
$${}_{3}{C}_{1}H^{2}T^{1}=\left(\begin{array}{c}3\\ 1\\ \end{array}\right)H^{2}T^{1}=3\times HHT$$

$${}_{3}{C}_{2}H^{1}T^{2}=\left(\begin{array}{c}3\\ 2\\ \end{array}\right)H^{1}T^{2}=3\times HTT$$

$${}_{3}{C}_{3}H^{0}T^{3}=\left(\begin{array}{c}3\\ 3\\ \end{array}\right)H^{0}T^{3}=1\times TTT$$


### 동전 $$n$$ 번 던지기 (이항계수 활용)

- 뒷면이 $$r$$ 번, 앞면이 $$n-r$$ 번 나오는 경우의 수 

$${}_{n}{C}_{r}H^{n-r}T^{r}=\left(\begin{array}{c}n\\ r\\ \end{array}\right)H^{n-r}T^{r}$$

- 8 번 던져 뒷면이 $$3$$ 번, 앞면이 $$5$$ 번 나오는 경우의 수 

$${}_{8}{C}_{3}H^{5}T^{3}=\left(\begin{array}{c}8\\ 3\\ \end{array}\right)H^{5}T^{3}
=\frac{8!}{3!\times5!}H^{5}T^{3}
=56\times H^{5}T^{3}$$

- 10 번 던져 뒷면이 $$4$$ 번, 앞면이 $$6$$ 번 나오는 경우의 수 

$${}_{10}{C}_{4}H^{6}T^{4}=\left(\begin{array}{c}10\\ 4\\ \end{array}\right)H^{6}T^{4}
=\frac{10!}{4!\times6!}H^{6}T^{4}
=210\times H^{6}T^{4}$$


### 유용한 조합 등식

- $$n$$개의 대상물에서 한 번에 $$r$$개를 선택하는 선택하는
가능한 \uline{조합의 수}

$$\left(\begin{array}{c}n\\ r\\ \end{array}\right)
=\left(\begin{array}{c}n-1\\ r-1\\ \end{array}\right)
+\left(\begin{array}{c}n-1\\ r\\ \end{array}\right),
~~~~~1\le r \le n$$

- a를 포함한 수는 $${}_{n-1}{C}_{r-1}$$

$$\rlap{\overbrace{\phantom{a~~b~~c~~d~~e~~f~~g}}^{\text{7개의 원소}}}\underbrace{a~~b~~c~~d~~e}_{\text{5개의 원소}}~~f~~g~~~~~\rightarrow~~~~~
a~~\rlap{\overbrace{\phantom{b~~c~~d~~e~~f~~g}}^{\text{6개의 원소}}}\underbrace{b~~c~~d~~e}_{\text{4개의 원소}}~~f~~g$$

- a를 포함하지 않는 수는 $${}_{n-1}{C}_{r}$$

$$\rlap{\overbrace{\phantom{a~~b~~c~~d~~e~~f~~g}}^{\text{7개의 원소}}}\underbrace{a~~b~~c~~d~~e}_{\text{5개의 원소}}~~f~~g~~~~~\rightarrow~~~~~
a~~\rlap{\overbrace{\phantom{b~~c~~d~~e~~f~~g}}^{\text{6개의 원소}}}\underbrace{b~~c~~d~~e~~f}_{\text{5개의 원소}}~~g$$



### 이항정리(binomial theorem)

- $$(x+y)^{n}$$은 어떤 형태일까?

$$\begin{split}
	(x+y)^{2}&=x^{2}+2xy+y^{2}\\
	&=1\times x^{2}y^{0}+2\times x^{1}y^{1}+1\times x^{0}y^{2}
	\end{split}
$$

$$
	\begin{split}
	(x+y)^{3}&=x^{3}+3x^{2}y+3xy^{2}+y^{3}\\
	&=1\times x^{3}y^{0}+3\times x^{2}y^{1}+3\times x^{1}y^{2}+1\times x^{0}y^{3}
	\end{split}$$

$$
	\begin{split}
	(x+y)^{4}&=x^{4}+4x^{3}y+6x^{2}y^{2}+4xy^{3}+y^{4}\\
	&=1\times x^{4}+4\times x^{3}y^{1}+6\times x^{2}y^{2}+4\times x^{1}y^{3}+1\times x^{0}y^{4}
	\end{split}
	$$

- 이항계수 활용

$$(x+y)^{n}=\sum_{k=0}^{n}{}_{n}{C}_{k}x^{n-k}y^{k}=\sum_{k=0}^{n}{n \choose k}x^{n-k}y^{k}
=\sum_{k=0}^{n}{n \choose k}x^{k}y^{n-k}$$


- $$(x+y)^{12}$$에서 $$x^{7}y^{5}$$의 계수

$$
{}_{12}{C}_{5}x^{7}y^{5}={}_{12}{C}_{7}x^{7}y^{5}={12 \choose 5}x^{7}y^{5}={12 \choose 7}x^{7}y^{5}
$$

$$
\frac{12!}{5!7!}x^{7}y^{5}=792\times x^{7}y^{5}
$$ 


### 응용해 봅시다.

- 야구 경기의 타자는 9명이다. 타순은 몇 가지인가?
	
	- 순열 $$9!=362,880$$
	
- 남학생 5명과 여학생 3명이 경제학 강의를 수강하고 있다.

	- 두 학생이 동일한 점수를 받을 수 없는 경우 순위는 몇 가지인가?
	
		- 순열 $$8!=40,320$$
	
	- 남학생은 남학생들만의 점수로, 여학생은 여학생들만의 점수로 순위를 정하는 경우는 몇 가지인가?
	
		- 순열 $$5!=120$$, $$3!=6$$, $$5!\times3!=720$$

- 어느 대학의 1학년은 5명, 2학년은 3명, 3학년은 6명, 4학년은 4명이다.
	
	- 각 학년에서 1명씩 뽑아 학생회를 구성하는 경우의 수는?

    $$5\times 3\times 6\times 4=360$$

- 경제학 교과서 3권, 통계학 교과서 4권, 게임이론 교과서 2권을 동일한 과목으로 나란히 정리하려 한다.

	- 경제학 교과서, 통계학 교과서, 게임이론 교과서 순서로 배열하는 경우의 수는?

    $$3!\times4!\times 2!=6\times 24\times 2=288$$


	- 동일한 과목 교과서 순서로 배열하는 경우의 수는?
	
    $$3!\times288=1,728$$


- 백기 3개, 청기 2개, 홍기 4개를 나열하여 신호를 구분하고자 한다. 몇 가지 신호를 만들 수 있는가?

    $$\dfrac{9!}{3!\times 2!\times 4!}=1,260$$


- 다음의 보수행렬을 보고 물음에 답하시오.

  ![연습문제](/images/Lec_5_5_1_5.png)
  
   - Player 1과 Player 2의 순수전략은 무엇인가?

     $$\{Up,~Down\},~~~\{Left,~Center,~Right\}$$

   - 게임의 결과는 몇 가지인가?

     $$(U,~L),~(U,~C),~(U,~R),~(D,~L),~(D,~C),~(D,~R)$$	

## 확률과 확률변수

- 핵심만 쏙쏙!

    {: .note}
	> - 게임 적용
	>
	>	- 전략형 게임에서 유한 개의 행동(예를 들어, $${\bf L}eft, {\bf R}ight$$)을 갖는 경기자의 혼합전략
	>
	>	- 확률 $$p$$를 이용하여 $$p\times L+(1-p)\times R$$로 표현
	>
	>	- 전개형 게임에서 자연선택으로 게임이 어떤 시작 점(Node)에서 출발하는지가 확률로서 결정
	>
	>	- 상대방에 대한 정보가 불완전한 베이즈 게임에서, 상대의 유형(type)을 일정한 확률로 추측

	
### 표본공간(sample space)

- (정의) 실험의 모든 가능한 결과의 집합 $$S$$

- 확실하게 결과를 미리 예측할 수 없는 실험

- 실험의 결과는 미리 알 수 없지만 가능한 모든 결과는 인식

    - 동전 한 번 던지기 $${\bf H}ead, {\bf T}ail$$

    $$S=\{H,~T\}$$
	
    - 동전 두 번 던지기 $$S=\{(i,~j) \vert i,~j=H,~T\}$$

    $$S=\{(H,~H),~(H,~T),~(T,~H),~(T,~T)\}$$	
	
    - 주사위 한 번 던지기

    $$S=\{1,~2,~3,~4,~5,~6\}$$	

    - 주사위 두 번 던지기 $$S=\{(i,~j) \vert i,~j=1,~2,~3,~4,~5,~6\}$$

    $$S=\{(1,~1),~(1,~2),~(1,~3),\cdots,~(6,~4),~(6,~5),~(6,~6)\}$$	


### 확률의 정의

- 확률의 정의

    {: .definition}

	> 고전적 정의 Pierre-Simon, marquis de Laplace
	>
	> $$n$$개의 원소가 있는 표본공간 $$S=\{e_{1},\,\cdots,\,e_{n}\}$$에서 각 근원사건 $$e_{i}$$가 일어날 가능성이 동일한 경우에, $$k$$개의 원소로 구성된 사건 $$A$$가 일어날 확률은 다음과 같다.
	> 
	> $$P(A)=\dfrac{k}{n}$$
	>
	> - 공정한 동전 던지기 앞면 $$\dfrac{1}{2}$$, 뒷면 $$\dfrac{1}{2}$$
	>
	> - 공정한 주사위 던지기 각면 $$\dfrac{1}{6}$$

    {: .definition}
	
	> 빈도학파적 정의
	>
	> 실험횟수를 $$n$$이라 할 때 사건 $$A$$가 일어날 확률은 다음과 같다.
	>
	> $$P(A)=\lim_{n\to\infty}\dfrac{1}{n}\times\{\text{사건 A가 발생한 횟수}\}$$
	>
	> - 주변의 공정한 동전 50번 던지기 $$\rightarrow$$ 앞면 6회 $$\rightarrow$$ $$\dfrac{6}{50}$$  $$\rightarrow$$ 던지는 회수를 늘리면 $$\dfrac{1}{2}$$로 수렴
	>
	> - 주변의 공정한 주사위 60 던지기 $$\rightarrow$$ 3의 눈 21회 $$\rightarrow$$ $$\dfrac{21}{60}$$ $$\rightarrow$$ 던지는 회수를 늘리면 $$\dfrac{1}{6}$$로 수렴
	
	{: .definition}
	
	> 공리론적 정의 Andrey Nikolaevich Kolmogorov
	>
	> 표본공간 $$S$$에서 다음의 공리를 만족하는 $$P(A)$$를 사건 $$A$$의 확률이라고 한다.
	>
	> (공리 1)
	>
	> $$P(S)=1$$
	>
	> (공리 2)
	>
	> $$0\le P(A) \le 1$$
	>
	> (공리 3) 상호배반인 사건 $$A_{1},\,A_{2}\,\cdots\,$$에 대하여 $$A_{i}\cap A_{j}=\emptyset~~\rightarrow~~P(A_{i}\cap A_{j})=0$$
	>
	> $$P\big(\bigcup_{i=1}^{\infty}A_{i}\big)=P(A_{1})+P(A_{2})+\cdots$$
	
	

### 확률변수(random variable)

- 관심의 대상이 되는 양(수량)

- 표본공간에서 정의된 실숫값 함수

- 확률변수의 값은 실험의 결과에 따라 결정 $$\rightarrow$$ 확률변수의 가능한 값에 확률 부여

- 공정한 동전 두 번 던지기 $$\rightarrow$$ 경우의 수 $$\{HH,~HT,~TH,~TT\}$$

	- 앞면의 개수를 $$X$$라고 하면, $$X=0,~1,~2$$ 중에서 한 값을 확률변수
$$
\begin{split}
P\{X=0\}&=P\{TT\}=\frac{1}{4}\\
P\{X=1\}&=P\{HT,~TH\}=\frac{2}{4}=\frac{1}{2}\\
P\{X=2\}&=P\{HH\}=\frac{1}{4}\\
\end{split}
$$
	

- 공정한 동전 세 번 던지기 $$\rightarrow$$ 경우의 수 
	
	$$\{HHH,~HHT,~HTH,~HTT,~THH,~THT,~TTH,~TTT\}$$

	- 뒷면의 개수를 $$Y$$라고 하면, $$Y=0,~1,~2,~3$$ 중에서 한 값을 확률변수
$$
\begin{split}
P\{Y=0\}&=P\{HHH\}=\frac{1}{8}\\
P\{Y=1\}&=P\{HHT,~HTH,~THH\}=\frac{3}{8}\\
P\{Y=2\}&=P\{HTT,~THT,~TTH\}=\frac{3}{8}\\
P\{Y=3\}&=P\{TTT\}=\frac{1}{8}\\
\end{split}
$$

- 공정한 주사위 두 번 던지고 눈의 수를 합 $$\rightarrow$$ 경우의 수 $$\{2,~3,~4,~5,~6,~7,~8,~9,~10,~11,~12\}$$

	- 합의 수를 $$Z$$라고 하면, $$Z=2,~3,~4,~5,~6,~7,~8,~9,~10,~11,~12$$ 중에서 한 값을 확률변수
	
$$
\begin{split}
P\{Z=2\}&=\frac{1}{36},~P\{Z=3\}=\frac{2}{36},~P\{Z=4\}=\frac{3}{36},\\
P\{Z=5\}&=\frac{4}{36},~P\{Z=6\}=\frac{5}{36},~P\{Z=7\}=\frac{6}{36},\\
P\{Z=8\}&=\frac{5}{36},~P\{Z=9\}=\frac{4}{36},~P\{Z=10\}=\frac{3}{36},\\
P\{Z=11\}&=\frac{2}{36},~P\{Z=12\}=\frac{1}{36}\\
\end{split}
$$

  ![윷 던지기](/images/Lec_5_5_2_1.png)

- 공정한 동전 1개와 공정한 주사위 1개를 동시에 던지자.

	- 동전 앞면이 나오면 주사위 수를 2배하고, 뒷면이 나오면 3을 더하는 확률변수 $$X$$
	
	- 합의 수를 $$X$$라고 하면, $$X=2,~4,~5,~6,~7,~8,~9,~10,~12$$ 중에서 한 값을 확률변수
	
$$
\begin{split}
P\{X=2\}&=\frac{1}{12},~P\{X=4\}=\frac{2}{12},~P\{X=5\}=\frac{1}{12},\\
P\{X=6\}&=\frac{2}{12},~P\{X=7\}=\frac{1}{12},~P\{X=8\}=\frac{2}{12},\\
P\{X=9\}&=\frac{1}{12},~P\{X=10\}=\frac{1}{12},~P\{X=12\}=\frac{1}{12}\\
\end{split}
$$

  ![동전주사위 던지기](/images/Lec_5_5_2_2.png)
  
  
### 확률에 관한 몇 가지 명제

- (명제 1) $$A$$와 $$A^{c}$$는 항상 상호배반이고 $$A\cup A^{c}=S$$이므로$$P(S)=P(A\cup A^{c})=P(A)+P(A^{c})=1$$이다. 따라서,
	$$P(A)=1-P(A^{c})$$
	
	- 공정한 주사위를 던져 홀수가 나오는 사건을 $$A$$라고 하자.
	
	$$P(A)=\frac{3}{6}=\frac{1}{2}~~\rightarrow~~P(A^{c})=1-\frac{1}{2}=\frac{1}{2}$$
	
  ![동전주사위 던지기](/images/Lec_5_5_2_3.png)

- (명제 2) $$B\subset A\text{이면}~P(B)\le P(A)$$
	
	- (증명) $$B\subset A$$이므로 $$A=B\cup (B^{c}\cap A)$$이고, $$B$$와 $$(B^{c}\cap A)$$는 상호배반이기에 $$P(A)=P(B)+P(B^{c}\cap A)$$이다. 그리고 $$0\le P(B^{c}\cap A)\le 1$$이므로 증명된다.
	
	- 공정한 주사위를 한 번 던지자. $$A$$는 5이하의 수가 나오는 사건, $$B$$는 소수(prime)가 나오는 사건이라 하자.
	
$$A=\{1,~2,~3,~4,~5\},~~~B=\{2,~3,~5\}$$

$$P(A)=\frac{5}{6}, P(B)=\frac{3}{6}~~\rightarrow~~P(B)=\frac{3}{6}\le P(A)=\frac{5}{6}$$

  ![주사위 던지기](/images/Lec_5_5_2_4.png)
  
- (명제 3) $$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$

	- (증명) $$A\cup B$$를 상호 배반인 사건 $$A$$와 $$A^{c}\cap B$$의 합집합으로 나타낼 수 있기에
	
$$
\begin{split}
A\cup B&=A\cup (A^{c}\cap B)~~\rightarrow~~P(A\cup B)=P(A)+P(A^{c}\cap B)\\
B&=(A\cap B)\cup (A^{c}\cap B)~~\rightarrow~~P(B)=P(A\cap B)+P(A^{c}\cap B)\\
P(A\cup B)&=P(A)+P(A^{c}\cap B)=P(A)+P(B)-P(A\cap B)\\
\end{split}
$$

   - 공정한 주사위를 한 번 던지자.
	$$A$$는 짝수가 나오는 사건, $$B$$는 소수(prime)가 나오는 사건이라 하자.
	
$$A=\{2,~4,~6\},~~~B=\{2,~3,~5\},~~~A\cap B=\{2\}$$

$$$P(A)=\frac{3}{6}, P(B)=\frac{3}{6}~~\rightarrow~~P(A\cup B)=P(A)+P(B)-P(A\cap B)=\frac{5}{6}$$

  ![주사위 던지기](/images/Lec_5_5_2_5.png)
  
   - 집합 3개인 경우

$$	
	\begin{split}
	&P(A\cup B\cup C)\\
	=&P(A)+P(B)+P(C)-P(A\cap B)-P(B\cap C)-P(C\cap A)+P(A\cap B\cap C)
	\end{split}
$$

  ![주사위 던지기](/images/Lec_5_5_2_6.png)
  
  
### 응용해 봅시다.

- 어떤 학급의 학생 중 24명은 축구, 15명은 야구, 20명은 농구를 한다.
	학생 중 10명은 축구와 야구를, 7명은 야구와 농구를, 6명은 농구와 축구를 한다.
	또한, 5명은 축구, 야구, 농구를 모두 하며, 8명은 전혀 운동을 하지 않는다.
	이 학급의 학생은 몇 명인가?
	
	- (풀이) 적어도 하나의 운동을 하는 학생은 41명, 운동을 하지 않는 학생은 8명이므로 49명으로 구성된 학급이다.
	
$$
	\begin{split}
	&n(A\cup B\cup C)\\
	=&n(A)+n(B)+n(C)\\&-n(A\cap B)-n(B\cap C)-n(C\cap A)+n(A\cap B\cap C)\\
	=&24+15+20-10-7-6+5\\
	=&41
	\end{split}
$$

  ![학급편성](/images/Lec_5_5_2_7.png)
  
- 공정한 공 4개가 항아리에 들어 있으며, 적색 공 2개와 청색 공 2개로 구성된다. 무작위로 2개의 공을 추출하는 실험에서 1개는 적색 공, 1개는 청색 공일 확률을 구하자

	- (풀이) 각 공에 숫자를 부여하면 $${}_{4}{P}_{2}=4\times 3=12$$이다.
	
	- 첫 번째 공이 적색 공, 두 번째 공이 청색 공인 경우 $$2\times 2=4$$
	
	- 첫 번째 공이 청색 공, 두 번째 공이 적색 공인 경우 $$2\times 2=4$$
	
	- 따라서, $$\dfrac{4+4}{12}=\frac{2}{3}$$
	
	- 다른 풀이 방법
	
$$
\frac{
\left(
\begin{array}{c}
2\\
1\\
\end{array}
\right)
\left(
\begin{array}{c}
2\\
1\\
\end{array}
\right)
}{
\left(
\begin{array}{c}
4\\
2\\
\end{array}
\right)
}=\frac{4}{6}=\frac{2}{3}
$$
	
- 공정한 공 9개가 항아리에 들어 있으며, 적색 공 6개와 청색 공 3개로 구성된다. 무작위로 3개의 공을 추출하는 실험에서 2개는 적색 공, 1개는 청색 공일 확률을 구하자. 

	- (풀이) 각 공에 숫자를 부여하면 $${}_{9}{P}_{3}=9\times 8\times 7=504$$이다.
		
	- 첫 번째 공이 적색 공, 두 번째 공이 적색 공, 세 번째 공이 청색 공인 경우 $$6\times 5\times 3=90$$
		
	- 첫 번째 공이 적색 공, 두 번째 공이 청색 공, 세 번째 공이 적색 공인 경우 $$6\times 3\times 5=90$$
		
	- 첫 번째 공이 청색 공, 두 번째 공이 적색 공, 세 번째 공이 적색 공인 경우 $$3\times 6\times 5 =90$$
		
	- 따라서, $$\dfrac{90+90+90}{504}=\dfrac{15}{28}$$
		
	- 다른 풀이 방법
		
$$
\frac{
\left(
\begin{array}{c}
6\\
2\\
\end{array}
\right)
\left(
\begin{array}{c}
3\\
1\\
\end{array}
\right)
}{
\left(
\begin{array}{c}
9\\
3\\
\end{array}
\right)
}=\frac{15\times 3}{84}=\frac{15}{28}
$$

- 다음의 보수행렬을 보고 물음에 답하시오.

  ![연습문제](/images/Lec_5_5_1_6.png)
  
	- Player 1의 전략 $$Up$$의 확률이 0.7, Player 2의 전략 $$Left$$와 $$Right$$의 확률이
	각각 0.2와 0.3이라고 하자. 
	$$(Down,~Center)$$의 결과가 발생할 확률은 얼마인가?
	
	$$(1-0.7)\times (1-0.2-0.3)=0.15$$
	
## 확률분포와 기댓값

- 핵심만 쏙쏙!

    {: .note}
	> - 게임 적용
	>
	>	- 혼합전략 내쉬균형
	>
	>	- 베이지안 내쉬균형
	
### 확률변수(random variable)

- 관심의 대상이 되는 양

- 표본공간에서 정의된 실수값 함수

	- 동전을 $$n$$번 던질 때 나오는 앞면(Head)의 수 $$X$$
	
	$$f(\{T\})=0,~f(\{H\})=1,~f(\{HT\})=1,~f(\{HH\})=2,~f(\{THHH\})=3,\cdots$$
	
	$$X=0,~1,~2,\cdots,~n$$

	- 윷을 던질 때 도가 나오면 1, 개가 나오면 2, 걸이 나오면 3, 윷이 나오면 4, 모가 나오면 5
	
		$$f(\{\text{도}\})=1,~f(\{\text{개}\})=2,~f(\{\text{걸}\})=3,~f(\{\text{윷}\})=4,~f(\{\text{모}\})=5$$
		
	$$X=1,~2,~3,~4,~5$$

### 이산확률변수(discrete random variable)

- 기껏해야 가산 무한개의 가능한 값을 갖는 확률변수

- 이산확률변수 $$X$$에 대해 $$X$$의 확률질량함수(probability mass function)

	$$p(a)=P\{X=a\}$$

- 확률질량함수 $$p(a)$$는 기껏해야 무한개의 $$a$$ 값에 대해 양수 또는 0

	$$X=x_{1},~x_{2},~x_{3},\cdots$$
	
$$
	\begin{split}
	&p(x_{i})\ge 0,~~~~~i=1,~2,~3,\cdots\\
	&p(x)=0,~~~~~~\text{다른 모든 x 값에 대해}\\
	\therefore&\sum_{i=1}^{\infty}p(x_{i})=1
	\end{split}
$$

- 공정한 주사위를 한 번 던질 때 눈의 확률질량함수

	- 확률변수  $$X$$
	
	$$f(\{1\})=1,~~~f(\{2\})=2,~~~f(\{3\})=3,~~~f(\{4\})=4,~~~f(\{5\})=5,~~~f(\{6\})=6$$
	
	- 확률질량함수
	
	$$p(1)=p(2)=p(3)=p(4)=p(5)=p(6)=\frac{1}{6}$$
	
	$$p(1)+p(2)+p(3)+p(4)+p(5)+p(6)=1$$
	
- 공정한 동전을 세 번 던질 때 앞면이 나오는 수의 확률질량함수

	- 확률변수와 확률질량함수

$$\begin{split}
f(\{HHH\})&=3,~~~f(\{TTT\})=0\\
f(\{HHT\})&=f(\{HTH\})=f(\{THH\})=2\\
f(\{HTT\})&=f(\{THT\})=f(\{TTH\})=1\\
\end{split}$$

$$
\begin{array}{cccc}
&p(1)=\dfrac{_{3}C_{1}}{2^{3}}=\dfrac{3}{8}&p(2)=\dfrac{_{3}C_{1}}{2^{3}}=\dfrac{3}{8}&\\
p(0)=\dfrac{_{3}C_{1}}{2^{3}}=\dfrac{1}{8}&&&p(3)=\dfrac{_{3}C_{1}}{2^{3}}=\dfrac{1}{8}\\
\end{array}
$$
	
$$p(0)+p(1)+p(2)+p(3)=1$$

- 공정한 윷을 1 번 던질 때 말이 이동하는 수의 확률질량함수

	- 윷을 1 번 던지는 것은 윷가락 1 개를 네 번 던지는 것과 동일 (단, 백도는 없다) $$\rightarrow$$ $${}_{n}{C}_{r}$$

	
	- 확률변수와 확률질량함수
	
$$f(\{\text{도}\})=1,~f(\{\text{개}\})=2,~f(\{\text{걸}\})=3,~f(\{\text{윷}\})=4,~f(\{\text{모}\})=5$$


$$
\begin{array}{ccccc}
&&p(2)=\dfrac{3C1}{2^{4}}=\dfrac{6}{16}&&\\
&p(1)=\dfrac{3C1}{2^{4}}=\dfrac{4}{16}&&p(3)=\dfrac{3C1}{2^{4}}=\dfrac{4}{16}&\\
p(5)=\dfrac{3C1}{2^{4}}=\dfrac{1}{16}&&&&p(4)=\dfrac{3C1}{2^{4}}=\dfrac{1}{16}\\
\end{array}
$$

$$p(1)+p(2)+p(3)+p(4)+p(5)=1$$