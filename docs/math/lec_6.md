---
layout: default
title: 조건부 확률과 사전-사후 확률
parent: 게임이론을 위한 수학
nav_order: 6
---


# 조건부 확률과 사전-사후 확률

- 내쉬균형이란 경기자 모두 상대방의 전략에 최적대응을 하며, 더 이상 전략을 변경하지 않는 상태이다.
	
- 객관적인 사실을 정확히 알 수 없거나 상대방의 행위를 관찰할 수 없는 경우가 존재한다.
	
- 정보의 비대칭성이란 한 경기자는 객관적 사실을 알고 있거나 상대방의 행위를 관찰할 수 있으나, 다른 경기자는 이에 대한 정보가 부족한 경우를 의미한다.
	
- 조건의 변화, 즉 정보의 추가로 최적대응은 변화할 수 있다.

## 분할과 조건부확률

- 핵심만 쏙쏙!

    {: .note}
	> - 상대방의 전략이 주어졌다는 가정 하에 최적대응을 모색하는 것이 내쉬균형이다.  
	>
	> - 상대방이 하나의 Action만을 선택한다면 순수전략 내쉬균형을 구할 수 있다.
	>
	> - 상대방이 여러 Action을 확률변수로 구성하면 혼합전략 내쉬균형을 구할 수 있다.
	>
	> - 베이지안 내쉬균형을 이해하기 위해서는 조건부확률의 개념을 알아야 한다.
	>
	> - 사적정보가 존재하는 경우 즉, 상대방이 Love-type인지 Hate-type인지에 따라
	보수(pay-off)는 상이하다.
	>
	> - 상대방이 Love-type의 확률과 Hate-type의 확률에 따라 전략을 선택하고 그에 따라
	보수가 결정된다.
	

### 집합의 분할(partition of a set)

- 주어진 집합을 여러 개의 집합으로 나누는 문제(분할)를 고려하자!

- 집합의 원소들을 비공(non-empty) 부분집합들에게 할당

- 모든 원소가 각자 정확히 하나의 부분집합에 속하게끔 하는 것

 ![예시표](/images/Lec_6_1_2.png)

- 집합 $$X$$의 분할은 $$X$$의 공집합이 아닌 부분집합들로 이루어진, 분리합집합이 $$X$$인 집합들


    {: .definition}

	> - (정의) 집합 $$X$$의 분할(partition of a set)은 다음 조건을 만족하는 집합족 $$P$$로 정의된다.
	>
	>	- $$P$$는 공집합을 원소로 하지 않는다. 
	>
	> 	$$\emptyset \notin P$$
	>
	>	- $$P$$는 $$X$$를 덮는다.
	>
	>		- 덮개cover는 합집합이 전체 집합인 부분 집합들의 집합족이다.
	>
	> 		$$\bigcup P=X$$
	>
	>	- $$P$$는 서로소 집합족이다.
	>
	> 		- $$A,~B\in P$$이고 $$A\neq B$$이면 $$A \cap B=\emptyset$$


- (예시) $$X=\{1,~2\}$$

	- 분할은 2개

	$$\{\{1,~2\}\}$$, $$\{\{1\},~\{2\}\}$$

- (예시) $$X=\{a,~b,~c\}$$

	- 분할은 5개

	$$\{\{a,~b,~c\}\}$$, $$\{\{a\},~\{b\},~\{c\}\}$$, $$\{\{a,~b\},~\{c\}\}$$, $$\{\{a,~c\},~\{b\}\}$$, $$\{\{a\},~\{b,~c\}\}$$


### 조건부 확률(conditional probability)

- 조건부확률 $$P(B \vert A)$$이란 $$A$$가 발생했다는 조건이 주어졌을 때 $$B$$가 발생할 확률을 말한다.

    {: .definition}

	> - $$P(A)>0$$이면 다음과 같이 정의한다.
	>
	>	$$P(B \vert A)=\frac{P(A\cap B)}{P(A)}$$


- (예제) 사라진 구슬이 방 왼쪽 틈새에 있다는 확신은 30\%, 오른쪽 틈새에 있다는 확신은 50%이다. 오른쪽 틈새에서 찾지 못했다면 다른 틈새에 있을 확률은?

	- 오른쪽($$R$$) 틈새에서 찾지 못했다면 다른 틈새에 있을 확률 $$\rightarrow$$ $$P(L \vert R^{c})$$
	
	$$P(L \vert R^{c})=\frac{P(L \cap R^{c})}{P(R^{c})}=\frac{P(L)}{1-P(R)}=\frac{0.3}{1-0.5}$$
	
 ![예시표](/images/Lec_6_1_1.png)	


### 베이즈 정리(Bayesian rule)

- 사건 $$A$$와 사건 $$B$$

	$$\begin{split}
	P(B \vert A)&=\frac{P(A\cap B)}{P(A)}~~\rightarrow~~P(A\cap B)=P(B \vert A)P(A)\\
	P(A \vert B)&=\frac{P(B\cap A)}{P(B)}~~\rightarrow~~P(B\cap A)=P(A \vert B)P(B)\\
	\end{split}$$
	
- (서로 배반) $$A\cap B^{c}$$, $$A\cap B$$, $$B\cap A^{c}$$

	$$	\begin{split}
	P(A\cap B)&=P(B\cap A)\\
	P(A \vert B)P(B)&=P(B \vert A)P(A)
	\end{split}$$

 ![예시표](/images/Lec_6_1_4.png)	

- 사건 $$A$$와 사건 $$B$$

	$$\begin{split}
	P(B \vert A)&=\frac{P(A\cap B)}{P(A)}\\
	A&=(A\cap B)\cup (A\cap B^{c})\\
	P(A)&=P(A\cap B)+ P(A\cap B^{c})\\
	&=P(A \vert B)P(B)+P(A \vert B^{c})P(B^{c})\\
	&=P(A \vert B)P(B)+P(A \vert B^{c})(1-P(B))\\
	\end{split}$$


	$$\begin{split}
	P(A \vert B)&=\frac{P(B\cap A)}{P(B)}\\
	B&=(B\cap A)\cup (B\cap A^{c})\\
	P(B)&=P(B\cap A)+ P(B\cap A^{c})\\
	&=P(B \vert A)P(A)+P(B \vert A^{c})P(A^{c})\\
	&=P(B \vert A)P(A)+P(B \vert A^{c})(1-P(A))\\
	\end{split}$$

- 간단한 예시를 아래의 표를 통하여 살펴보자.

 ![예시표](/images/Lec_6_2_1.png)	

- 반을 기준으로 앞의 표를 정리하면

 ![예시표](/images/Lec_6_2_2.png)

- 취미를 기준으로 표를 정리하면

 ![예시표](/images/Lec_6_2_3.png)

 ![예시표](/images/Lec_6_2_4.png)

 ![예시표](/images/Lec_6_2_5.png)

- 베이즈 정리를 이용하자.

	$$\begin{split}
	P(B_{j})&=P(B_{j}\vert A_{1})P(A_{1})+P(B_{j}\vert A_{2})P(A_{2})+P(B_{j}\vert A_{3})P(A_{3})\\
	&=\sum_{i=1}^{3}P(B_{j}\vert A_{1})P(A_{i})\\
	\sum_{j=1}^{4}P(B_{j})&=\sum_{j=1}^{4}\sum_{i=1}^{3}P(B_{j}\vert A_{i})P(A_{i})=1\\
	\end{split}$$


	$$\begin{split}
	P(A_{i})&=P(A_{i}\vert B_{1})P(B_{1})+P(A_{i}\vert B_{2})P(B_{2})+P(A_{i}\vert B_{3})P(B_{3})+P(A_{i}\vert B_{4})P(B_{4})\\
	&=\sum_{j=1}^{4}P(A_{i}\vert B_{j})P(B_{j})\\
	\sum_{i=1}^{3}P(A_{i})&=\sum_{i=1}^{3}\sum_{j=1}^{4}P(A_{i}\vert B_{j})P(B_{j})=1\\
	\end{split}$$

- 문제 해결을 위해서 다음의 표를 이용하자.

	- $$A_{i},~i=1,~2,~3$$는 원인으로, $$B_{j},~j=1,~2,~3,~4$$는 결과로 파악하자.
	
 ![예시표](/images/Lec_6_2_6.png)	

- (예제) 혈액검사를 통해 질병에 걸렸을 때 그 질병을 발견하는 97% 효과가 있다고 한다. 하지만 검사를 받은 사람들 중 2%에 대해서는 잘못된 양성반응을 보인다. 인구의 0.4%가 이 질병에 걸렸다면 검사결과가 양성인 사람이 실제로 질병에 걸렸을 확률을 구하라.

 ![예시표](/images/Lec_6_1_5.png)

$$\begin{split}
P(A\vert B)&=\frac{P(B\cap A)}{P(B)}\\
&=\frac{P(B\vert A)P(A)}{P(B\vert A)P(A)+P(B\vert A^{c})P(A^{c})}\\
&=\frac{0.97\times 0.004}{(0.97\times 0.004)+(0.02\times 0.996)}\\
&\approx 0.163025 \approx 16.3\%
\end{split}$$

- (예제) 보험에 가입하는 사람들의 부류는 사고를 잘 당하는 사람과 잘 당하지 않는 사람이다. 주어진 기간 내에 사고를 잘 당하는 사람은 사고가 발생할 확률이 0.3이고, 사고를 잘 당하지 않는 사람은 사고가 발생할 확률이 0.1이다. 사고를 잘 당하는 사람은 인구의 20%라고 알려져 있다. 새로운 보험계약자가 주어진 기간 내에 사고를 당할 확률을 구하라.

 ![예시표](/images/Lec_6_1_6.png)

$$\begin{split}
P(A)&=P(A\vert B)P(B)+P(A\vert B^{c})P(B^{c})\\
&=0.3\times 0.2+0.1\times 0.8\\
&=0.14
\end{split}$$

$$\begin{split}
P(B\vert A)&=\frac{P(A\vert B)P(B)}{P(A)}\\
&=\frac{0.3\times 0.2}{0.14}\\
\end{split}$$


### 오즈(odds) 또는 승산

- 새로운 증거가 나타날 때 어떤 가설에 대한 확률의 변화는 이 가설의 오즈 또는 승산에서의 변화로 간편하게 표현

    {: .definition}

	> - 사건 $$A$$의 오즈는 다음과 같이 정의한다.
	>
	>	$$\frac{P(A)}{P(A^{c})}=\frac{P(A)}{1-P(A)}$$
	>
	> - 즉 사건 $$A$$의 오즈는 사건 $$A$$가 발생할 가능성이 사건 $$A$$가 발생하지 않을 가능성보다 얼마나 큰지를 알려준다. 오즈가 $$\alpha$$이면 그 가설을 지지하는 데 승산이 $$\alpha$$ 대 1이라고 한다.

- 참일 확률이 $$P(H)$$인 새로운 가설 $$H$$를 고려하고 새로운 증거 $$E$$가 도입되었다.

- 새로운 증거 $$E$$가 주어졌을 때 $$H$$가 참일 조건부 확률과 $$H$$가 참이 아닐 조건부 확률은 다음과 같다.

	$$\begin{split}
	P(E\cap H)&=P(E\vert H)P(H)\\
	P(H\vert E)&=\frac{P(E\cap H)}{P(E)}\\
	&=\frac{P(E\vert H)P(H)}{P(E)}\\
	\end{split}$$

	$$\begin{split}
	P(E\cap H^{c})&=P(E\vert H^{c})P(H^{c})\\
	P(H^{c}\vert E)&=\frac{P(E\cap H^{c})}{P(E)}\\
	&=\frac{P(E\vert H^{c})P(H^{c})}{P(E)}\\
	\end{split}$$
	
- 증거 $$E$$가 도입된 후 새로운 오즈는 다음과 같다.

	$$\frac{P(H\vert E)}{P(H^{c}\vert E)}=\frac{P(H)}{P(H^{c})} \frac{P(E\vert H)}{P(E\vert H^{c})}$$
	
	
### 독립사건

- 조건부확률 $$P(A\vert B)$$과 비조건부확률 $$P(A)$$

- 사건 B가 발생했다는 전제 하에 사건 A가 발생할 조건부 확률 $$P(A\vert B)$$와 사건 A가 발생할 확률 $$P(A)$$는 일반적으로 같지 않음

	$$P(A\vert B)\neq P(A)$$

- 특별한 경우 $$P(A\vert B)= P(A)$$

- $$B$$가 발생했다는 사실이 $$A$$가 발생할 확률을 변화시키지 않으면 $$A$$와 $$B$$는 독립이다.

	$$P(A\vert B)= \frac{P(B\cap A)}{P(B)}~~\rightarrow~~P(B\cap A)=P(B)P(A)$$


    {: .definition}

	> $$P(A\cap B)=P(A)P(B)$$이 성립되면 두 사건 $$A$$와 $$B$$는 독립(independent)이라고 한다. 독립이 아닌 두 사건 $$A$$와 $$B$$는 종속(dependent)이라고 한다.
	

### 응용해 봅시다.


- 수사 단계에서 담당 수사관이 용의자가 범인임을 70% 확신하고 있다. 범인이 특징을 가지고 있음을 보여주는 새로운 증거가 발견되었으며, 인구의 15%가 이 특징을 가지고 있다. 용의자가 이 특징을 가지고 있다고 판명되었다면 담당수사관은 용의자가 범인임을 어느 정도로 확신하는가?

	- (풀이)

	$$\begin{split}
	P(B\vert A)&=\frac{P(A\cap B)}{P(A)}\\
	&=\frac{P(A\vert B)P(B)}{P(A\vert B)P(B)+P(A\vert B^{c})P(B^{c})}\\
	&=\frac{1\times 0.7}{1\times 0.7+0.15\times 0.3}\\
	&=\frac{140}{149}\\
	&\approx 0.939597=94\%
	\end{split}$$

	- 승산을 이용하면 $$\frac{140}{9}:1$$이므로 $$\frac{140}{149}$$임을 알 수 있다.
	
	$$\begin{split}
	\frac{P(B\vert A)}{P(B^{c}\vert A)}&=\frac{P(B)}{P(B^{c})}\frac{P(A\vert B)}{P(A\vert B^{c})}\\
	=&\frac{0.7}{0.3}\frac{1}{0.15}\\
	&=\frac{140}{9}
	\end{split}$$

 ![예시표](/images/Lec_6_1_8.png)
 
 
- 주머니에 A 형태의 동전 3개와 B형태의 동전 2개가 들어 있다. A 형태의 동전은 동전 던지기에서 앞면 확률은 1/3이고, B 형태의 동전은 동전 던지기에서 앞면 확률은 2/3이다. 주머니에서 동전 하나를 무작위로 선택하여 던졌을 때 앞면이 나왔다면 A 형태의 동전일 확률은?

	- (풀이)
	
	$$\begin{split}
	P(A\vert H)&=\frac{P(H\cap A)}{P(H)}\\
	&=\frac{P(H\vert A)P(A)}{P(H\vert A)P(A)+P(H\vert B)P(B)}\\
	&=\frac{\frac{1}{3}\times \frac{3}{5}}{\frac{1}{3}\times \frac{3}{5}+\frac{2}{3}\times \frac{2}{5}}\\
	&=\frac{3}{7}
	\end{split}$$
	
	- 승산을 이용하면 $$\frac{3}{4}:1$$이므로  $$\frac{3}{7}$$임을 알 수 있다.
	
	$$\begin{split}
	\frac{P(A\vert H)}{P(B\vert H)}&=\frac{P(A)}{P(B)}\frac{P(H\vert A)}{P(H\vert B)}\\
	=&\frac{\frac{3}{5}}{\frac{2}{5}}\frac{\frac{1}{3}}{\frac{2}{3}}\\
	&=\frac{3}{4}
	\end{split}$$
	
  ![예시표](/images/Lec_6_1_10.png)
  




- 52장으로 구성된 카드묶음에서 무작위로 1장을 선택할 때 클로버인 사건을 $$A$$, 3인 사건을 $$B$$라고 하자. $$A$$와 $$B$$는 독립인가? 종속인가?

	- $$P(A)=\frac{13}{52}$$

	- $$P(B)=\frac{4}{52}$$

	- $$P(A\cap B)=\frac{1}{52}$$

	- $$P(A\cap B)=\frac{1}{52}$$과 $$P(A)P(B)=\frac{13}{52}\frac{4}{52}=\frac{1}{52}$$는 일치하므로 독립

- 다음의 보수행렬을 보고 물음에 답하시오.

	- Player 2가 $$Center$$를 선택한다면 Player 1의 최적대응은 무엇인가? $$Up$$
	
	- Player 1이 $$Down$$을 선택한다면 Player 2의 최적대응은 무엇인가? $$Center$$

   ![예시표](/images/Lec_5_1_5.png) 
 

## 사전확률과 사후확률


- 핵심만 쏙쏙!

    {: .note}
	> - 상대방의 주어진 전략이 한정된 정보에 의한 것이라면 최적대응이라 할 수 없다. 
	>
	> - 추가적인 정보를 이용하여 상대방의 주어진 전략을 갱신(update)하여 합리적인 의사결정에 활용할 수 있다.

### 베이즈 정리(Bayesian rule)

- 사전 확률(prior probability) $$P(A)$$

	- 사건 B가 발생하기 전에 가지고 있던 사건 A의 확률

- 사후 확률(posterior probability) $$P(A\vert B)$$

	- 사건 B가 발생한 후 갱신된 사건 A의 확률

	$$P(A\vert B)=\frac{P(A\cap B)}{P(B)}$$
	
- 위의 식을 이용하면

	$$\begin{split}
	P(A\vert B)=\frac{P(A\cap B)}{P(B)}&\rightarrow P(A\cap B)=P(A\vert B)P(B)\\
	P(B\vert A)=\frac{P(B\cap A)}{P(A)}&\rightarrow P(B\cap A)=P(B\vert A)P(A)\\
	P(A\vert B)=\frac{P(A\cap B)}{P(B)}&\rightarrow P(A\vert B)=\frac{P(B\vert A)P(A)}{P(B)}\\
	\end{split}$$

    - 사후확률 $$P(A\vert B)$$은 사전확률 $$P(A)$$에 $$\dfrac{P(B\vert A)}{P(B)}$$을 곱하여 얻을 수 있다.
	
	- $$P(B\vert A)$$를 가능도(likelihood)라 하고,
	
	- $$P(B)$$를 정규화 상수(normalizing constant) 또는 증거(evidence)라 한다.

- 사건 B가 진실이라는 것을 알게 됨으로써 사건 A가 어떻게 변화하는지를 표현한 정리

- 새로운 정보(E)가 기존의 추론(H)에 어떻게 영향을 미치는지를 파악 가능

	$$P(H\vert E)=\frac{P(E\vert H)}{P(E)}P(H)$$

    {: .definition}

	> - 확률의 승법 정리(Multiplication Theorem of Probability) (결합확률 또는 동시확률)
	>
	>	- 두 사건 A, B 모두 만족하는$$A\cap B$$가 일어날 (즉, 동시에 또는 함께 일어날) 확률은,
	>	- (1) 상호종속일 때, (즉, 서로간에 상관성 있을 때) 한쪽 확률에 조건부확률을 곱한 것
	>
	>	$$P(A\cap B) = P(A\vert B) P(B)=P(B\vert A) P(A)$$
	>
	>	- (2) 상호독립일 때, (즉, 서로간에 상관성 없을 때) 한쪽 확률에 다른쪽 확률을 곱한 것
	>
	>	$$P(A\vert B) = P(A)$$
	>
	>	$$P(B\vert A) = P(B)$$
	>
	>	$$P(A\cap B) = P(B\vert A)P(A)= P(A\vert B)P(B)=P(A)P(B)$$
	>
	> 	- 따라서, 한쪽 확률에 조건부확률 또는 다른쪽 확률을 곱한 것과 같다.


### 분할 이용 $$i=1,~2,\cdots,~n$$

- 사건 $$A_{i}$$와 사건 사건 $$A_{j}$$는 서로 배타적

	$$A_{i}\cap A_{j}=\emptyset~~~~~i\ne j$$

- 사건 $$A_{i}$$는 완전

	$$A_{1}\cup A_{2}\cup\cdots A_{n}=\Omega$$

    {: .definition}

	> - 전확률 공식(Law of Total Probability)
	>
	>	- $$A_{1},\,\cdots\,A_{n}$$이 표본공간 $$S$$의 한 분할(partition)일 때, 임의의 사건 $$B$$에 대하여 다음이 성립한다.
	>
	>	$$P(B)=P(B\mid A_{1})P(A_{1})+\cdots+P(B\mid A_{n})P(A_{n})$$



	$$\begin{split}
	P(A_{k}\mid B)&=\dfrac{P(A_{k}\cap B)}{P(B)}\\
	&=\dfrac{P(B\mid A_{k})P(A_{k})}{P(B)}\hspace{2.8cm}\because \text{승법공식}\\
	&=\dfrac{P(B\mid A_{k})P(A_{k})}{\sum_{i=1}^{n}P(B\mid 	A_{i})P(A_{i})}\hspace{2cm}\because \text{전확률공식}
	\end{split}$$

- 전확률 공식을 이용한 베이즈 정리의 확장 $$A_{1}$$, $$A_{2}$$, $$A_{3}$$

- B라는 힌트에 따라 $$A_{1}$$, $$A_{2}$$, $$A_{3}$$ 중 B에 대한 조건부 확률

	$$\begin{split}
	P(A_{1}\vert B)&=\frac{P(B\mid A_{1})P(A_{1})}{P(B\mid A_{1})P(A_{1})+P(B\mid A_{2})P(A_{2})+P(B\mid A_{3})P(A_{3})}\\
	P(A_{2}\vert B)&=\frac{P(B\mid A_{2})P(A_{2})}{P(B\mid A_{1})P(A_{1})+P(B\mid A_{2})P(A_{2})+P(B\mid A_{3})P(A_{3})}\\
	P(A_{3}\vert B)&=\frac{P(B\mid A_{3})P(A_{3})}{P(B\mid A_{1})P(A_{1})+P(B\mid A_{2})P(A_{2})+P(B\mid A_{3})P(A_{3})}\\
	\end{split}$$

- 전확률(total probability) 공식 $$A\ne A^{c}$$

	$$P(B)=P(B\mid A)P(A)+P(B\mid A^{c})P(A^{c})$$
	
- 전확률 공식을 이용한 베이즈 정리의 확장 $$A$$, $$A^{c}$$

	$$\begin{split}
	P(A\vert B)&=\frac{P(B\mid A)P(A)}{P(B\mid A)P(A)+P(B\mid A^{c})P(A^{c})}\\
	&=\frac{P(B\mid A)P(A)}{P(B\mid A)P(A)+P(B\mid A^{c})(1-P(A))}\\
	P(A^{c}\vert B)&=\frac{P(B\mid A^{c})P(A^{c})}{P(B\mid A)P(A)+P(B\mid A^{c})P(A^{c})}\\
	&=\frac{P(B\mid A^{c})(1-P(A))}{P(B\mid A)P(A)+P(B\mid A^{c})(1-P(A))}\\
	\end{split}$$


### 응용해 봅시다.

- 제약사에서 환자가 특정한 병균을 보유하고 있는지 확인하는 시약을 만들었다. 병균을 보유한 환자에게 시약을 테스트한 결과 99%의 확률로 양성 반응을 보였다. 병균보유가 확인되지 않은 어떤 환자가 이 시약을 테스트한 결과 양성 반응을 보였다면 이 환자가 그 병균을 보유하고 있을 확률을 구하시오.

	- 병균을 보유하고 있는 사건 $$A$$

	- 양성반응을 보이는 사건 $$B$$

	- 병균을 보유하고 있는 사람이 양성반응을 보이는 조건부 사건 $$B\vert A$$

	- 양성반응을 보이는 사람이 병균을 보유하고 있는 조건부 사건 $$A\vert B$$

	- (정보) 병균을 보유한 환자에게 시약을 테스트한 결과 99\%의 확률로 양성 반응

	$$P(B\vert A)=0.99$$

	- (의문) 어떤 환자가 양성 반응을 보였다면 이 환자가 그 병균을 보유하고 있을 확률

	$$P(A\vert B)=\frac{P(B\cap A)}{P(B)}=\frac{P(B\vert A)P(A)}{P(B)}=\frac{P(B\vert A)P(A)}{P(B\vert A)P(A)+P(B\vert A^{c})(1-P(A))}$$

	- 추가 정보 필요 $$P(A)$$, $$P(B\vert A^{c})$$

		- 전체 인구 중 병균을 보유하고 있는 확률 0.2% $$P(A)=0.002$$

		- 잘못된 결과가 나타난 확률 $$P(B\vert A^{c})=0.05$$

		$$\begin{split}
		P(A\vert B)&=\frac{P(B\vert A)P(A)}{P(B\vert A)P(A)+P(B\vert A^{c})(1-P(A))}\\
		&=\frac{0.99\times 0.002}{0.99\times 0.002+0.05\times(1-0.002)}\\
		&\approx 0.038=3.8\%
		\end{split}$$
		
		- 정리하면

  ![예시표](/images/Lec_6_3_1.png)

- Player 1은 Player 2가 $$Center$$와 $$Right$$만 순수전략으로 가지고 있다고 알고 있다. Player 1의 $$Up$$ 선택에 따른 Player 2의 최적대응은 무엇이라고 Player 1은 기대하는가? 또한, Player 1의 $$Down$$ 선택에 따른 Player 2의 최적대응은 무엇이라고 Player 1은 기대하는가?

  ![예시표](/images/Lec_5_1_5.png)

   - $$Up\rightarrow Right$$, $$Down \rightarrow Center$$ 

- Player 1은 Player 2가 $$Center$$와 $$Right$$뿐만 아니라 $$Left$$도 순수전략으로 가지고 있다고 알고 있다. Player 1의 $$Up$$ 선택에 따른 Player 2의 최적대응은 무엇이라고 Player 1은 기대하는가? 또한, Player 1의 $$Down$$ 선택에 따른 Player 2의 최적대응은 무엇이라고 Player 1은 기대하는가?


  ![예시표](/images/Lec_5_1_5.png)

   - $$Up\rightarrow Left$$, $$Down \rightarrow Center$$


## 사전확률과 사후확률의 응용

- 핵심만 쏙쏙!

    {: .note}
	> - 사전적으로 주어진 확률을 알면 베이즈 정리를 활용하여 사후확률을 구할 때 응용할 수 있다. 
	>
	> - 정보가 불완전한 상황을 묘사하는 베이지안 게임의 경우에 경기자가 분명히 모르는 상대방의 유형(type)에 따라 자신의 보수가 결정된다.
	>	
	> - 상대방의 유형(type)에 대한 조건부 확률을 이용하여 각 경기자는 자신의 기대보수를 계산하고, 이를 바탕으로 베이지안 균형을 도출할 수 있다.

### 원인과 결과

- $$A_{i}~~i=1,~2,~3$$는 원인을, $$B_{j}~~j=1,~2,~3,~4$$는 결과라고 하자.

- 다음의 표를 완성하고 $$P(B_{j}) ~~j=1,~2,~3,~4$$를 구하라.

  ![예시표](/images/Lec_6_2_7.png)
  
- 표를 완성하면

  ![예시표](/images/Lec_6_2_8.png)

$$P(B_{1})=0.4\times0.2+0.2\times0.5+0.1\times0.3=0.21$$

$$P(B_{2})=0.15\times0.2+0.4\times0.5+0.3\times0.3=0.32$$

$$P(B_{3})=0.35\times0.2+0.15\times0.5+0.45\times0.3=0.28$$

$$P(B_{4})=0.1\times0.2+0.25\times0.5+0.15\times0.3=0.19$$


### 사전확률(초기확률)(prior probability)

- 상호배반이며 전체를 이루는 가능한 가설 $$n$$개 있다고 하자.

$$\sum_{i=1}^{n}P(H_{i})=1$$

### 사후확률(posterior probability) 또는 갱신될 확률(updated probability)

- 사건 $$E$$가 발생했다는 정보를 접하면 $$H_{i}$$가 참인 가설일 조건부확률

$$P(H_{i}\vert E)=\frac{P(E\vert H_{i})P(H_{i})}{\sum_{j=1}^{n}P(E\vert H_{j})P(H_{j})}$$

- $$E_{1}$$ 발생

	- 사건 $$E_{1}$$가 발생했다는 정보를 접하면 $$H_{i}$$가 참인 가설일 조건부확률

$$P(H_{i}\vert E_{1})=\frac{P(E_{1}\vert H_{i})P(H_{i})}{\sum_{j=1}^{n}P(E_{1}\vert H_{j})P(H_{j})}$$	

- $$E_{1}$$ 발생 후 $$E_{2}$$ 발생 $$\rightarrow$$ $$E_{1}E_{2}=E_{1}\cap E_{2}$$

	- 추가로 사건 $$E_{2}$$가 발생했다는 정보를 접하면 $$H_{i}$$가 참인 가설일 조건부확률

$$P(H_{i}\vert E_{1}E_{2})=\frac{P(E_{1}E_{2}\vert H_{i})P(H_{i})}{\sum_{j=1}^{n}P(E_{1}E_{2}\vert H_{j})P(H_{j})}$$

- $$E_{1}$$과 $$E_{2}$$가 조건부 독립이라면

	- 추가로 사건 $$E_{2}$$가 발생했다는 정보를 접하면 $$H_{i}$$가 참인 가설일 조건부확률

$$\begin{split}
		P(E_{1}E_{2}\vert H_{j})&=P(E_{2}\vert H_{j})P(E_{1}\vert H_{j})~~~~~for~j=1,~2,\cdots,~n\\
		P(H_{i}\vert E_{1}E_{2})&=\frac{P(E_{1}E_{2}\vert H_{i})P(H_{i})}{P(E_{1}E_{2})}
		=\frac{P(E_{2}\vert H_{i})P(E_{1}\vert H_{i})P(H_{i})}{P(E_{1}E_{2})}\\
		&=\frac{P(E_{2}\vert H_{i})P(E_{1}\cap H_{i})}{P(E_{1}E_{2})}
		=\frac{P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})P(E_{1})}{P(E_{1}E_{2})}\\
		&=\frac{P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})P(E_{1})}{P(E_{1}E_{2})}\\
		&=\frac{P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})}{Q(1,~2)}~~~~~~~~~~~\because
		Q(1,~2)=\frac{P(E_{1}E_{2})}{P(E_{1})}\\
		\end{split}$$

   - 모든 $$i$$에 대해서 위의 식이 타당하기에

	$$\begin{split}
	1=\sum_{i=1}^{n}P(H_{i}\vert E_{1}E_{2})&=\sum_{i=1}^{n}\frac{P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})}{Q(1,~2)}~~~~~~~~
	\therefore Q(1,~2)=\sum_{i=1}^{n}P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})\\
	\end{split}$$

   - 따라서, 다음과 같은 결론을 얻는다.

$$
P(H_{i}\vert E_{1}E_{2})=\frac{P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})}{\sum_{i=1}^{n}P(E_{2}\vert H_{i})P(H_{i}\vert E_{1})}$$


### 혼합전략에 적용

- 경기자 1의 전략은 $$A_{1}$$, $$A_{2}$$, $$A_{3}$$ $$P(A_{i})$$, $$P(B_{j}\vert A_{i})$$ $$\rightarrow$$ $$P(B_{j})$$

- 경기자 2의 전략은 $$B_{1}$$, $$B_{2}$$, $$B_{3}$$, $$B_{4}$$ $$P(B_{j})$$, $$P(A_{i}\vert B_{j})$$ $$\rightarrow$$ $$P(A_{i})$$

  ![예시표](/images/Lec_6_2_6.png)

### 응용해 봅시다.

- 공정한 카드 3장이 있다. 첫 번째 카드는 양면이 모두 파란색, 두 번째 카드는 양면이 모두 하얀색, 세 번째 카드는 한면은 파란색, 다른 면은 하얀색이다. 무작위로 1장을 뽑을 때, 카드의 파란색이면 다른 면이 하얀색일 확률을 구하라.

	
	- 3장의 카드를 BB, WW, BW라고 칭하자.

	- 각 카드의 확률을 $$P(BB)$$, $$P(WW)$$, $$P(BW)$$이라고 하면,

	$$\begin{split}
	P(BW\vert B)&=\frac{P(B\cap BW)}{P(B)}\\
	&=\frac{P(B\vert BW)P(BW)}{P(B\vert BW)P(BW)+P(B\vert BB)P(BB)+P(B\vert WW)P(WW)}\\
	&=\frac{\frac{1}{2}\times\frac{1}{3}}{\frac{1}{2}\times\frac{1}{3}+1\times\frac{1}{3}+0\times\frac{1}{3}}=\frac{1}{3}
	\end{split}$$


- 3 종류의 건전지가 있다. 건전지가 20시간 이상 사용할 수 있는 확률이 각각 0.6, 0.2, 0.4이라고 알려져 있다. 총 건전지 중 종류 1은 30%, 종류 2는 45%, 종류 3은 25%이다.

	- 각 건전지의 종류를 $$A_{1}$$, $$A_{2}$$, $$A_{3}$$라 하고, 20시간 이상 사용할 사건을 $$B$$라 하자. 

	- (1) 무작위로 건전지를 선택할 때 20시간 이상 사용할 수 있는 확률을 구하라.

	$$\begin{split}
	P(B)&=P(B\vert A_{1})P(A_{1})+P(B\vert A_{1})P(A_{1})+P(B\vert A_{1})P(A_{1})\\
	&=0.6\times 0.3+0.2\times 0.45+0.4\times 0.25\\
	&=0.37
	\end{split}$$

   - (2) 건전지를 20시간 이상 사용하였다면 어떤 종류일지 조건부확률을 구하라.

	$$\begin{split}
	P(B)&=0.6\times 0.3+0.2\times 0.45+0.4\times 0.25=0.37\\
	P(A_{1}\vert B)&=\frac{0.18}{0.37},~~~
	P(A_{2}\vert B)=\frac{0.09}{0.37},~~~
	P(A_{3}\vert B)=\frac{0.1}{0.37}~~~\\
	\end{split}$$


- 공정한 동전을 두 번 던지자. (1) 첫 번째 동전이 앞면, (2) 적어도 한 번 앞면이 나온다는 각각의 조건이 주어졌을 때 두 번 모두 앞면이 나올 조건부 확률을 구하라.

	- 표본공간 $$S=\{HH,~HT,~TH,~TT\}$$, 앞면 $$H$$, 뒷면 $$T$$
	
	- (1) 첫 번째 동전이 앞면, 두 번째 동전이 앞면

		- 첫 번째 동전이 앞면인 사건 $$A=\{HH,~HT\}$$, 두 번째 동전이 앞면인 사건 $$B=\{HH,~TH\}$$

		$$P(B\vert A)=\frac{P(A\cap B)}{P(A)}=\frac{\{HH\}}{\{HH,~HT\}}=\frac{1}{2}$$

	- (2) 적어도 한 번 앞면이 나온다는 각각의 조건이 주어졌을 때 두 번 모두 앞면

		- 첫 번째 동전이 앞면인 사건 $$C=\{HH,~HT,~TH\}$$, 두 번째 동전이 앞면인 사건 $$D=\{HH\}$$

		$$P(D\vert C)=\frac{P(C\cap D)}{P(C)}=\frac{\{HH\}}{\{HH,~HT,~TH\}}=\frac{1}{3}$$

- 다음의 표를 이용하여 $$P(Up\vert Center)$$를 구하시오.

  ![예시표](/images/Lec_6_3_2.png)

  ![예시표](/images/Lec_6_3_3.png)


## 정리하기

- 게임이론에 응용하여 답할 수 있다.

	- 정보가 주어지면 상대방이 어떤 전략을 가지고 있는지 파악할 수 있다.

	- 상대방의 전략에 따라 자신의 최적 대응을 구할 수 있다.