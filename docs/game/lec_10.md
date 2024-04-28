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
