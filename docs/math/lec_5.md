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
	
	- $${\bf H}ead, {\bf T}ail$$

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

- 이항계수 \dingto $$\comb{2}{0}$$, $$\comb{2}{1}$$, $$\comb{2}{2}$$
		
		$$\left(\begin{array}{c}2\\ 0\\ \end{array}\right)H^{2}T^{0}=1\times HH,~~
\left(\begin{array}{c}2\\ 1\\ \end{array}\right)H^{1}T^{1}=2\times HT,~~
\left(\begin{array}{c}2\\ 2\\ \end{array}\right)H^{0}T^{2}=1\times TT$$


### 동전 세 번 던지기 (이항계수 활용)

- 경우의 수는 8개이며, 1개의 $$HHH$$, 3개의 $$HHT$$, 3개의 $$HTT$$,
1개의 $$TTT$$

- 이항계수 \dingto $$\comb{3}{0}$$, $$\comb{3}{1}$$, $$\comb{3}{2}$$, $$\comb{3}{3}$$
		
		$$\comb{3}{0}H^{3}T^{0}=\left(\begin{array}{c}3\\ 0\\ \end{array}\right)H^{3}T^{0}=1\times HHH$$$$
$$$$\comb{3}{1}H^{2}T^{1}=\left(\begin{array}{c}3\\ 1\\ \end{array}\right)H^{2}T^{1}=3\times HHT$$$$
$$$$\comb{3}{2}H^{1}T^{2}=\left(\begin{array}{c}3\\ 2\\ \end{array}\right)H^{1}T^{2}=3\times HTT$$$$
$$$$\comb{3}{3}H^{0}T^{3}=\left(\begin{array}{c}3\\ 3\\ \end{array}\right)H^{0}T^{3}=1\times TTT$$


### 동전 $$n$$ 번 던지기 (이항계수 활용)

- \item
뒷면이 $$r$$ 번, 앞면이 $$n-r$$ 번 나오는 경우의 수 

$${}_{n}{C}_{r}H^{n-r}T^{r}=\left(\begin{array}{c}n\\ r\\ \end{array}\right)H^{n-r}T^{r}$$

- 8 번 던져 뒷면이 $$3$$ 번, 앞면이 $$5$$ 번 나오는 경우의 수 

$$\comb{8}{3}H^{5}T^{3}=\left(\begin{array}{c}8\\ 3\\ \end{array}\right)H^{5}T^{3}
=\frac{8!}{3!\times5!}H^{5}T^{3}
=56\times H^{5}T^{3}$$

- 10 번 던져 뒷면이 $$4$$ 번, 앞면이 $$6$$ 번 나오는 경우의 수 

$$\comb{10}{4}H^{6}T^{4}=\left(\begin{array}{c}10\\ 4\\ \end{array}\right)H^{6}T^{4}
=\frac{10!}{4!\times6!}H^{6}T^{4}
=210\times H^{6}T^{4}$$


### 유용한 조합 등식

- $$n$$개의 대상물에서 한 번에 $$r$$개를 선택하는 선택하는
가능한 \uline{조합의 수}

$$\left(\begin{array}{c}n\\ r\\ \end{array}\right)
=\left(\begin{array}{c}n-1\\ r-1\\ \end{array}\right)
+\left(\begin{array}{c}n-1\\ r\\ \end{array}\right),
~~~~~1\le r \le n$$

- a를 포함한 수는 $$\comb{n-1}{r-1}$$

$$\rlap{$$\overbrace{\phantom{a~~b~~c~~d~~e~~f~~g}}^{\text{7개의 원소}}$$}\underbrace{a~~b~~c~~d~~e}_{\text{5개의 원소}}~~f~~g~~~~~\text{\dingto}~~~~~
a~~\rlap{$$\overbrace{\phantom{b~~c~~d~~e~~f~~g}}^{\text{6개의 원소}}$$}\underbrace{b~~c~~d~~e}_{\text{4개의 원소}}~~f~~g$$

- a를 포함하지 않는 수는 $$\comb{n-1}{r}$$

$$\rlap{$$\overbrace{\phantom{a~~b~~c~~d~~e~~f~~g}}^{\text{7개의 원소}}$$}\underbrace{a~~b~~c~~d~~e}_{\text{5개의 원소}}~~f~~g~~~~~\text{\dingto}~~~~~
a~~\rlap{$$\overbrace{\phantom{b~~c~~d~~e~~f~~g}}^{\text{6개의 원소}}$$}\underbrace{b~~c~~d~~e~~f}_{\text{5개의 원소}}~~g$$



### 이항정리 \textsuperscript{binomial theorem}

$$\begin{split}
	(x+y)^{2}&=x^{2}+2xy+y^{2}\\
	&=\text{\ding{172}}\times x^{2}y^{0}+\text{\ding{173}}\times x^{1}y^{1}+\text{\ding{172}}\times x^{0}y^{2}
	\end{split}
	\end{equation*}
	\begin{equation*}
	\begin{split}
	(x+y)^{3}&=x^{3}+3x^{2}y+3xy^{2}+y^{3}\\
	&=\text{\ding{172}}\times x^{3}y^{0}+\text{\ding{174}}\times x^{2}y^{1}+\text{\ding{174}}\times x^{1}y^{2}+\text{\ding{172}}\times x^{0}y^{3}
	\end{split}$$
	
	$$
	\begin{split}
	(x+y)^{4}&=x^{4}+4x^{3}y+6x^{2}y^{2}+4xy^{3}+y^{4}\\
	&=\text{\ding{172}}\times x^{4}+\text{\ding{175}}\times x^{3}y^{1}+\text{\ding{177}}\times x^{2}y^{2}+\text{\ding{175}}\times x^{1}y^{3}+\text{\ding{172}}\times x^{0}y^{4}
	\end{split}
	$$
	
- $$(x+y)^{n}$$은 어떤 형태일까?

	- 이항계수 활용

$$(x+y)^{n}=\sum_{k=0}^{n}\comb{n}{k}x^{n-k}y^{k}=\sum_{k=0}^{n}{n \choose k}x^{n-k}y^{k}
=\sum_{k=0}^{n}{n \choose k}x^{k}y^{n-k}$$
	- 이항계수 활용 $$(x+y)^{12}$$에서 $$x^{7}y^{5}$$의 계수
	
	$$
	\comb{12}{5}x^{7}y^{5}=\comb{12}{7}x^{7}y^{5}={12 \choose 5}x^{7}y^{5}={12 \choose 7}x^{7}y^{5}
	\end{equation*}
	\begin{equation*}
	\frac{12!}{5!7!}x^{7}y^{5}=\uline{\bf{792}}\times x^{7}y^{5}
$$ 