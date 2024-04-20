---
layout: default
title: 조건부 확률과 사전-사후 확률
parent: 게임이론을 위한 수학
nav_order: 6
---


# 조건부 확률과 사전-사후 확률

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
	P(A\vert B)=\frac{P(A\cap B)}{P(B)}&~~\text{$$\rightarrow$$}~~P(A\cap B)=P(A\vert B)P(B)\\
	P(B\vert A)=\frac{P(B\cap A)}{P(A)}&~~\text{$$\rightarrow$$}~~P(B\cap A)=P(B\vert A)P(A)\\
	P(A\vert B)=\frac{P(A\cap B)}{P(B)}&~~\text{$$\rightarrow$$}~~P(A\vert B)=\frac{P(B\vert A)P(A)}{P(B)}\\
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
	>	- (1)상호종속적일 때, (즉, 서로간에 상관성 있을 때) 한쪽 확률에 조건부확률을 곱한 것
	>	$$P(A\cap B) = P(A\vert B) P(B)=P(B\vert A) P(A)$$
	>	- (2)상호독립적일 때, (즉, 서로간에 상관성 없을 때) 한쪽 확률에 다른쪽 확률을 곱한 것
	>	$$\begin{split}
		P(A\vert B) &= P(A)~~~~~~P(B\vert A) = P(B)\\
		P(A\cap B) &= P(B\vert A)P(A)= P(A\vert B)P(B)=P(A)P(B)\\
		\end{split}$$
	> 	- 따라서, 한쪽 확률에 조건부확률 또는 다른쪽 확률을 곱한 것과 같다.





		






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