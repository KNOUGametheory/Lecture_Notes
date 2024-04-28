---
layout: default
title: 반복게임의 응용
parent: 게임이론
nav_order: 10
---

# 반복 게임의 응용

- 기업들이 생산량 경쟁을 하는 경우 담합의 가능성은 무엇인가?

- 기업들이 가격 경쟁을 하는 경우 담합의 가능성은 무엇인가?

- 근로자들이 노력을 하도록 유인하기 위한 보수는 어떻게 책정하는가?

## 생산량 카르텔

- 핵심만 쏙쏙!

    {: .note}
	> - 다음 문제에 답을 할 수 있다.
	>
	> 	- 현실 세계의 전략적 상황 $$\rightarrow$$ 반복적 상호작용 $$\rightarrow$$ 반복게임  
	>
	> 	- 합리적 경기자들은 반복되는 상황에서 어떤 전략을 선택하는가?
	>
	>	- 반복되는 산출량 경쟁 시 각 기업들은 어떤 선택을 하는가?
	>
	> - 다음 문제를 생각하자.
	>
	> 	- 시장수요와 각 기업의 한계비용이 주어지면 각 기업의 전략을 파악해야 한다.
	>
	> 	- 담합의 이득은 무엇이며, 배신으로 말미암아 어떤 이득과 손실이 발생하지 파악할 수 있다.
	
### 생산량 카르텔

- 생산량 배분을 위한 담합 

- 담합의 협조와 배신에 따른 보수

- 죄인의 딜레마

	- Temptation 

	- Reward

	- Punishment

	- Sucker
	
	 ![예시표](/images/Lec_10_1_1.png)
	 
	 $$T>R>P>S$$
	 
	 ![예시표](/images/Lec_10_1_2.png)
	  
- 유한게임의 균형

	- 파레토 비효율적 결과

	- 협조를 통한 효율적 결과가 있음에도, 상대를 신뢰하지 못하여 배신을 선택
	
- Cournot 모형

	- 시장(역)수요함수 $$P=52-4Q$$

	- 기업 1의 생산량 $$Q_{1}$$, 기업 2의 생산량 $$Q_{2}$$ $$\rightarrow$$ $$Q=Q_{1}+Q_{2}$$

	- 각 기업은 동질의 재화를 공급

	- 각 기업의 고정비용은 0

	- 한계비용은 모두 $$C=4$$

	- 각 기업의 이윤 구조
	
	$$\pi_{i}(Q_{i},~Q_{j})=(52-4Q_{i}-4Q_{j})Q_{i}-4Q{i}$$

	- 각 기업의 이윤극대화 조건

		- 1계조건과 2계조건
		
		$$(F.O.C)~~~~\frac{\partial \pi_{i}}{\partial Q_{i}}=0~~~~~~~
		(S.O.C)~~~~\frac{\partial^{2} \pi_{i}}{\partial Q_{i}^{2}}<0$$
		
		$$
		\begin{split}
		(F.O.C)~~~~\frac{\partial \pi_{i}}{\partial Q_{i}}&=48-8Q_{i}-4Q_{j}=0\\
		Q_{i}&=\frac{12-Q_{j}}{2}\\
		Q_{i}&=4~~~~~for~i=1,~2\\
		(S.O.C)~~~~\frac{\partial^{2} \pi_{i}}{\partial Q_{i}^{2}}&<0\\
		\end{split}
		$$
		
		- 각 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{P}=64$$ $$\because P=52-4Q_{1}-4Q_{2}=20,~~MC=4$$
		
### 담합의 유인 

- 두 기업이 담합하여 마치 하나의 독점기업처럼 행동한다면?
	
	$$T>{\color{blue}Reward}>P>S$$
	
	$$
	\pi(Q)=(52-4Q)Q-4Q
	$$
		
- 이윤극대화 조건

	- 1계조건과 2계조건
		
	$$
	\begin{split}
	(F.O.C)~~~~\frac{\partial \pi}{\partial Q}&=52-8Q-4=0\\
	Q&=6~~~~~Q_{1}=3,~~Q_{2}=3\\
	(S.O.C)~~~~\frac{\partial^{2} \pi}{\partial Q^{2}}&<0\\
	\end{split}
	$$

	- 각 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{R}=72$$ $$\because P=52-4Q_{1}-4Q_{2}=28,~~MC=4$$

### 담합의 배신 유인

- Cournot 모형 1계조건
		
$$
\begin{split}
(F.O.C)~~~~Q_{i}&=\frac{12-Q_{j}}{2}\\
\end{split}
$$
		
- 상대방이 협조하여 $$Q_{j}=3$$을 생산할 때,  자신의 최적량은 $$Q_{i}=\dfrac{9}{2}$$

- 배신 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{T}=81$$ $$\because P=52-4Q_{1}-4Q_{2}=22,~~MC=4$$
		
$${\color{blue}Temptation}>R>P>S$$
		
- 배신당한 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{S}=54$$ $$\because P=52-4Q_{1}-4Q_{2}=22,~~MC=4$$
		
$$T>R>P>{\color{blue}Sucker}$$


### 응용해 봅시다.

- 각 기업의 전략적 상황

![예시표](/images/Lec_10_1_3.png)

![예시표](/images/Lec_10_1_4.png)

$$T(81)>R(72)>P(64)>S(54)$$

- 균형
	
	- 1회 게임 균형 (배신, 배신)
	
	- 유한반복게임 균형 (배신, 배신)
	
	
- 신사전략(nice) 

	- 경기자 2의 신사전략을 가정

	- 경기자 1이 신사전략을 고수
		
	$$
	\begin{split}
	V&=72+72\delta+72\delta^{2}+\cdots=\frac{72}{1-\delta}\\
	v&=(1-\delta)V=72\\
	\end{split}
	$$
		
	- 경기자 1이 깡패전략으로 변경
		
	$$
	\begin{split}
	V&=81+81\delta+81\delta^{2}+\cdots=\frac{81}{1-\delta}\\
	v&=(1-\delta)V=81\\
	\end{split}
	$$
	
	![예시표](/images/Lec_10_1_4.png)

	- 신사전략에서 깡패전략으로 바꿀 유인이 있기에 (신사전략, 신사전략)은 내쉬균형이 아니다.

- 깡패전략(nasty) 

	- 경기자 2의 깡패전략을 가정

	- 경기자 1이 깡패전략을 고수
		
	$$
	\begin{split}
	V&=64+64\delta+64\delta^{2}+\cdots=\frac{64}{1-\delta}\\
	v&=(1-\delta)V=64\\
	\end{split}
	$$

	- 경기자 1이 신사전략으로 변경
		
	$$
	\begin{split}
	V&=54+54\delta+54\delta^{2}+\cdots=\frac{54}{1-\delta}\\
	v&=(1-\delta)V=54\\
	\end{split}
	$$

	![예시표](/images/Lec_10_1_4.png)

	- 깡패전략에서 신사전략으로 바꿀 유인이 없기에 (깡패전략, 깡패전략)은 내쉬균형이다.
	
- 무자비전략(grim)

	- 경기자 2의 무자비전략을 가정

	- 경기자 2는 1기에 $$C$$를 선택하고 있다고 가정

	- 경기자 1이 $$C$$를 선택
		
	$$
	\begin{split}
	V&=72+72\delta+72\delta^{2}+\cdots=\frac{72}{1-\delta}\\
	v_{C}&=(1-\delta)V=72\\
	\end{split}
	$$

	- 경기자 1이 $$D$$를 선택
		
	$$
	\begin{split}
	V&=81+64\delta+64\delta^{2}+\cdots=81+\delta\frac{64}{1-\delta}\\
	v_{D}&=(1-\delta)V=(1-\delta)(81)+\delta(64)\\
	\end{split}
	$$
	
	![예시표](/images/Lec_10_1_4.png)

	- 모든 경기자에 대해 $$v_{C}\ge v_{D}~\rightarrow~\delta\ge \dfrac{9}{17}$$일 때, (무자비전략, 무자비전략)은 내쉬균형이다.
	
- 팃포탯(tit-for-tat) 전략 

	- 경기자 2의 팃포탯(tit-for-tat) 전략을 가정

	- 경기자 2는 1기에 $$C$$를 선택하고 있다고 가정

	- 경기자 1이 $$C$$를 선택
		
	$$
	\begin{split}
	V&=72+72\delta+72\delta^{2}+\cdots=\frac{72}{1-\delta}\\
	v_{C}&=(1-\delta)V=72\\
	\end{split}
	$$
	
	- 경기자 1이 $$D$$를 선택
		
	$$
	\begin{split}
	V&=81+54\delta+81\delta^{2}+54\delta^{3}+\cdots=\frac{81}{1-\delta^{2}}+\delta\frac{54}{1-\delta^{2}}\\
	v_{D}&=(1-\delta)V=\frac{81}{1+\delta}+\delta\frac{54}{1+\delta}\\
	\end{split}
	$$

	![예시표](/images/Lec_10_1_4.png)
	
	- 경기자 1이 $$D$$를 선택할 때의 순이득
			
	$$
	\begin{split}
	V_{C}&=72+72\delta+72\delta^{2}+72\delta^{3}+\cdots\\
	V_{D}&=81+54\delta+81\delta^{2}+54\delta^{3}+\cdots\\
	net=V_{C}-V_{D}&=(-9)+18\delta+(-9)\delta^{2}+18\delta^{3}+\cdots\\
	\end{split}
	$$

	- 모든 경기자가 $$9+(-18)\delta>0$$, 순현재가치가 0보다 크면 배신, 즉  $$\delta<\dfrac{1}{2}$$이면 팃포탯(tit-for-tat) 전략으로 대응하지 않는다.

	- 모든 경기자가 $$9+(-18)\delta\le 0$$, 순현재가치가 0보다 작으면 협조, 즉  $$\delta\ge\dfrac{1}{2}$$이면 팃포탯(tit-for-tat) 전략으로 대응하므로 팃포탯(tit-for-tat)은 균형전략이다.
	
	
## 가격 카르텔

- 핵심만 쏙쏙!

    {: .note}
	> - 다음 문제에 답을 할 수 있다.
	>
	> 	- 현실 세계의 전략적 상황 $$\rightarrow$$ 반복적 상호작용 $$\rightarrow$$ 반복게임  
	>
	> 	- 합리적 경기자들은 반복되는 상황에서 어떤 전략을 선택하는가?
	>
	>	- 반복되는 가격 경쟁 시 각 기업들은 어떤 선택을 하는가?
	>
	> - 다음 문제를 생각하자.
	>
	> 	- 시장수요와 각 기업의 한계비용이 주어지면 각 기업의 전략을 파악해야 한다.
	>
	> 	- 담합의 이득은 무엇이며, 배신으로 말미암아 어떤 이득과 손실이 발생하지 파악할 수 있다.
	
### 가격 카르텔

- 가격 담합 

- 담합의 협조와 배신에 따른 보수

- 죄인의 딜레마

	- Temptation 

	- Reward

	- Punishment

	- Sucker
	
	![예시표](/images/Lec_10_1_1.png)
	
### Bertrand 모형

- 각 기업의 수요함수 

$$Q_{i}=20-P_{i}+\frac{2}{3}P_{j}$$

- 기업 1의 가걱 $$P_{1}$$, 기업 2의 가격 $$P_{2}$$ 

- 각 기업의 고정비용과 한계비용은 모두 0

- 각 기업의 이윤 구조

$$\pi_{i}(P_{i},~P_{j})=(P_{i}-0)(20-P_{i}+\frac{2}{3}P_{j})$$

- 각 기업의 이윤극대화 조건

	- 1계조건과 2계조건
	$$(F.O.C)~~~~\frac{\partial \pi_{i}}{\partial P_{i}}=0~~~~~~~
	(S.O.C)~~~~\frac{\partial^{2} \pi_{i}}{\partial P_{i}^{2}}<0$$

- Bertrand 모형 이윤극대화 조건

	- 1계조건과 2계조건
		
	$$
	\begin{split}
	(F.O.C)~~~~\frac{\partial \pi_{i}}{\partial P_{i}}&=20-2P_{i}+\frac{2}{3}P_{j}=0\\
	P_{i}&=\frac{20+\frac{2}{3}P_{j}}{2}\\
	P_{i}&=15~~~~~for~i=1,~2\\
	(S.O.C)~~~~\frac{\partial^{2} \pi_{i}}{\partial P_{i}^{2}}&<0\\
	\end{split}
	$$

- 시장균형가격 $$\rightarrow$$ $$P=20$$

- 각 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{P}=225$$ $$\because P_{i}Q_{i}=15\times15=225$$

$$T>R>{\color{blue}Punishment}>S$$

### 담합의 유인

- 독점의 이윤 구조
	
$$
\begin{split}
\pi_{all}(Q_{i},~Q_{j})&=(52-4Q_{i}-4Q_{j})(Q_{i}+Q_{j})\\
\pi(P_{1},~P_{2})&=P_{1}(20-P_{1}+\frac{2}{3}P_{2})+P_{2}(20-P_{2}+\frac{2}{3}P_{1})
\end{split}
$$

- 이윤극대화 조건

	- 1계조건과 2계조건
		
	$$
	\begin{split}
	(F.O.C)~~~~\frac{\partial \pi}{\partial P_{1}}&=20-2P_{1}+\frac{4}{3}P_{2}=0~~~~~
	and~~~~~\frac{\partial \pi}{\partial P_{2}}=20-2P_{2}+\frac{4}{3}P_{1}=0\\
	P_{1}=P_{2}&=30~~~~~Q_{1}=10,~~Q_{2}=10\\
	(S.O.C)~~~~\pi_{11}&<0,~~\pi_{22}<0,~~\pi_{11}\pi_{22}-\pi_{12}^{2}>0
	\end{split}
	$$

- 각 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{R}=300$$

$$T>{\color{blue}Reward}>P>S$$

### 담합의 배신 유인

- Bertrand 모형 1계조건
		
	$$
	\begin{split}
	(F.O.C)~~~~P_{i}&=\frac{20+\frac{2}{3}P_{j}}{2}\\
	\end{split}
	$$

- 상대방이 협조 $$P_{j}=30$$이라면 자신은 $$P_{i}=20$$

- 배신 기업의 이윤 $$\rightarrow$$ $$\pi_{i}^{T}=400$ $$\because Q_{i}=20-P_{i}+\frac{2}{3}P_{j}=20$$

$${\color{blue}Temptation}>R>P>S$$

- 배신당한 기업의 이윤 $$\rightarrow$$ $$\pi_{j}^{S}=100$$ $$\because Q_{j}=20-P_{j}+\frac{2}{3}P_{i}=\frac{10}{3}$$

$$T>R>P>{\color{blue}Sucker}$$

### 응용해 봅시다.

- 각 기업의 전략적 상황

![예시표](/images/Lec_10_2_3.png)

![예시표](/images/Lec_10_2_4.png)

$$T(400)>R(300)>P(225)>S(100)$$

- 균형

	- 1회 게임 균형 (배신, 배신)

	- 한반복게임 균형 (배신, 배신)
	
- 신사전략(nice)

	- 경기자 2의 신사전략을 가정

	- 경기자 1이 신사전략을 고수
		
	$$
	\begin{split}
	V&=300+300\delta+300\delta^{2}+\cdots=\frac{300}{1-\delta}\\
	v&=(1-\delta)V=300\\
	\end{split}
	$$

	- 경기자 1이 깡패전략으로 변경
		
	$$
	\begin{split}
	V&=400+400\delta+400\delta^{2}+\cdots=\frac{400}{1-\delta}\\
	v&=(1-\delta)V=400\\
	\end{split}
	$$
	
	![예시표](/images/Lec_10_2_4.png)

	- 신사전략에서 깡패전략으로 바꿀 유인이 있기에 (신사전략, 신사전략)은 내쉬균형이 아니다.
	
- 깡패전략(nasty)

	- 경기자 2의 깡패전략을 가정

	- 경기자 1이 깡패전략을 고수
		
	$$
	\begin{split}
	V&=225+225\delta+225\delta^{2}+\cdots=\frac{225}{1-\delta}\\
	v&=(1-\delta)V=225\\
	\end{split}
	$$

	- 경기자 1이 신사전략으로 변경
		
	$$
	\begin{split}
	V&=100+100\delta+100\delta^{2}+\cdots=\frac{100}{1-\delta}\\
	v&=(1-\delta)V=100\\
	\end{split}
	$$
	
	![예시표](/images/Lec_10_2_4.png)

	- 깡패전략에서 신사전략으로 바꿀 유인이 없기에 (깡패전략, 깡패전략)은 내쉬균형이다.
	
- 무자비전략(grim)

	- 경기자 2의 무자비전략을 가정

	- 경기자 2는 1기에 $$C$$를 선택하고 있다고 가정

	- 경기자 1이 $$C$$를 선택
		
	$$
	\begin{split}
	V&=300+300\delta+300\delta^{2}+\cdots=\frac{300}{1-\delta}\\
	v_{C}&=(1-\delta)V=300\\
	\end{split}
	$$

	- 경기자 1이 $$D$$를 선택
		
	$$
	\begin{split}
	V&=400+225\delta+225\delta^{2}+\cdots=400+\delta\frac{225}{1-\delta}\\
	v_{D}&=(1-\delta)V=(1-\delta)(400)+\delta(225)\\
	\end{split}
	$$
	
	![예시표](/images/Lec_10_2_4.png)

	- 모든 경기자에 대해 $$v_{C}\ge v_{D}~\rightarrow~\delta\ge \dfrac{4}{7}$$일 때, (무자비전략, 무자비전략)은 내쉬균형이다.
	
- 팃포탯(tit-for-tat) 전략

	- 경기자 2의 팃포탯(tit-for-tat) 전략을 가정

	- 경기자 2는 1기에 $$C$$를 선택하고 있다고 가정

	- 경기자 1이 $$C$$를 선택
		
	$$
	\begin{split}
	V&=300+300\delta+300\delta^{2}+\cdots=\frac{300}{1-\delta}\\
	v_{C}&=(1-\delta)V=300\\
	\end{split}
	$$

	- 경기자 1이 $$D$$를 선택
		
	$$
	\begin{split}
	V&=400+100\delta+400\delta^{2}+100\delta^{3}+\cdots=\frac{400}{1-\delta^{2}}+\delta\frac{100}{1-\delta^{2}}\\
	v_{D}&=(1-\delta)V=\frac{400}{1+\delta}+\delta\frac{100}{1+\delta}\\
	\end{split}
	$$
	
	![예시표](/images/Lec_10_2_4.png)
	
	- 경기자 1이 $$D$$를 선택할 때의 순이득
			
	$$
	\begin{split}
	V_{C}&=300+300\delta+300\delta^{2}+300\delta^{3}+\cdots\\
	V_{D}&=400+100\delta+400\delta^{2}+100\delta^{3}+\cdots\\
	net=V_{D}-V_{C}&=100+(-200)\delta+100\delta^{2}+(-200)\delta^{3}+\cdots\\
	\end{split}
	$$

	- 모든 경기자가 $$100+(-200)\delta>0$$, 순현재가치가 0보다 크면 배신, 즉  $$\delta<\dfrac{1}{2}$$이면 팃포탯(tit-for-tat) 전략으로 대응하지 않는다.

	- 모든 경기자가 $$100+(-200)\delta\le 0$$, 순현재가치가 0보다 작으면 협조, 즉  $$\delta\ge\dfrac{1}{2}$$이면 팃포탯(tit-for-tat) 전략으로 대응하므로 팃포탯(tit-for-tat)은 균형전략이다.
	
## 효율성임금

- 핵심만 쏙쏙!

    {: .note}
	> - 다음 문제에 답을 할 수 있다.
	>
	> 	- 현실 세계의 전략적 상황 $$\rightarrow$$ 반복적 상호작용 $$\rightarrow$$ 반복게임  
	>
	> 	- 합리적 경기자들은 반복되는 상황에서 어떤 전략을 선택하는가?
	>
	>	- 반복되는 임금협상 시 고용주는 어떤 임금을 제시하는가?
	>
	>	- 근로자는 노력의 유인이 있는가?
	>
	> - 다음 문제를 생각하자.
	>
	> 	- 고용주는 근로자들의 노력을 유인하기 위한 추가 지급 금액을 모색해야 한다.
	>
	> 	- 근로자가 수령하는 추가 지급 금액은 태업, 이직 등의 기회비용이다.

- 효율성임금(efficiency wage)

	- (노동이직모형)  높은 실질임금이 이직률을 낮춘다. 

	- (태업방지모형)  높은 임금을 지급할수록 노동자의 태업의 기회비용은 커진다. 

	- (역선택모형)  효율성임금이 노동의 평균적인 질을 향상 시킨다.
	
- 역선택(adverse selection)

	- 필요한 정보가 충분하지 않은 시장에서 나쁜 품질의 상품이 많아지고, 좋은 품질의 상품이 사라지는 문제

	- 노동시장에서 노동수용자인 기업은 노동공급자의 정확한 생산성에 대한 파악이 불가능

	- 노동공급자인 가계는 자신의 생산성 파악 가능

	- 노동수요자인 기업이 평균적인 임금을 제시하면, 생산성이 낮은 노동공급자들과 거래

	- 기업은 노동자의 유보임금보다 높은 임금으로 역선택 방지
	
### 응용해 봅시다.

- 무한반복게임

	- $$t$$기

		- 고용주는 근로자에게 $$w^{*}$$의 임금 제안 

	- $$t+1$$기

		- (정상국면) 만일 전기 $$t$$기에 고수입($$y$$)이 실현되었다면, 이번 기 $$t$$기에도 $$w^{*}$$의 임금 제안

		- (보복국면) 만일 전기 $$t$$기에 저수입이 실현되었다면, 근로자를 해고하고 다시는 재고용하지 않는다.
- 근로자의 보수

	- 근로자의 순임금 $$w-c$$, 임금 $$w$$, 노력비용 $$c$$

	- 근면하게 일하는 노동자의 평균할인보수
	
	$$v_{\text{근면}}=(1-\delta)(w^{*}-c)+\delta(w^{*}-c)=w^{*}-c$$

	- 노동자가 태업을 하면 $$(1-\beta)$$ 확률로 해고 당하고 타직장에서 계속 임금 $$w_{0}$$ 수령
	
	$$
	\begin{split}
	v_{\text{태업}}&=(1-\delta)w^{*}+\delta\{\beta v_{\text{태업}}+(1-\beta)w_{0}\}\\
	v_{\text{태업}}&=\frac{(1-\delta)w^{*}+\delta(1-\beta)w_{0}}{1-\delta\beta}
	\end{split}
	$$ 

	- 근로자가 노력하여 일하려는 유인
		
	$$
	\begin{split}
	v_{\text{근면}}&\ge v_{\text{태업}}\\
	w^{*}-c&\ge\frac{(1-\delta)w^{*}+\delta(1-\beta)w_{0}}{1-\delta\beta}\\
	w^{*}&\ge w_{0}+\frac{1-\delta \beta}{\delta(1-\beta)}c
	\end{split}
	$$
	
- 무한반복게임의 유일한 하위게임완전균형

	- (고용주의 전략) $$w^{*}= w_{0}+\frac{1-\delta \beta}{\delta(1-\beta)}c$$ 제안

	- (근로자의 전략) $$w^{*}$$ 수락 후 노력

	- (고용주의 보수) $$y-w^{*}$$

	- (근로자의 보수) $$w^{*}-c$$		
	
- 효율성임금(efficiency wage)

	- 효율성임금 $$w^{*}$$은 유보임금 $$w_{0}$$보다 크다.
		
	$$
	w^{*}- w_{0}\ge\frac{1-\delta \beta}{\delta(1-\beta)}c
	$$

- 임금프리미엄(wage premium)

	- 현직장에 고용된 근로자가 노력하려는 유인을 주기 위하여 필요한 최소한의 추가 지급액
		
	$$
	\frac{1-\delta \beta}{\delta(1-\beta)}c
	$$

	- 근로자의 할인인자 $$\delta$$가 낮을수록 임금프리미엄은 높아진다.

	- 근무태만이 적발되지 않을 확률 $$\beta$$가 클수록 임금프리미엄은 높아진다.

	- 노력비용 $$c$$가 클수록 임금프리미엄은 높아진다.

## 정리하기

- 담합이 영원할 수 있는 전략은 지금 당장의 보수보다 미래의 보수를 높게 평가하는 것이다.

- 지속적인 근로자들의 노력을 유인하기 위해서는 지금의 태만보다 미래의 순임금을 높게 평가하도록 하는 것이다.

	