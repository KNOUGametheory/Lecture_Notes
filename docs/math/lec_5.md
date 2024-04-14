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
	
	$${}_{n}{C}_{r}=\frac{n!}{r!(n-r)!}=\comb{n}{n-r}$$
	
  ![이항계수](/images/Lec_1_5_1_4.jpeg)