---
layout: default
title: 미분 기초
parent: 게임이론을 위한 수학
nav_order: 4
---


# 미분 기초

## 미분법

- ★ 핵심만 쏙쏙!  

    {: .note}
	> '미분'은?
	>
	> 변화율
	>
	> '변화율'은?
	> 
	> 경제학에서 '한계'


### 함수의 극한과 연속성

- 함수의 수렴(convergence)

    $$
    𝑥 \rightarrow 𝑎 \text{일 때, 함수 } 𝑓(𝑥) \rightarrow 𝐿 \quad \left( \lim_{𝑥 \rightarrow 𝑎} ⁡𝑓(𝑥) = 𝐿 \right)
    $$
	
  - $$ 𝑥 \rightarrow 𝑎$$: 변수 $$𝑥$$의 값이 $$𝑎$$에 한없이 가까워질 때
  
  - $$𝑓(𝑥) \rightarrow 𝐿: 𝑓(𝑥)$$의 값이 $$𝐿$$에 한 없이 가까워진다!
  
  - "$$𝑥 \rightarrow 𝑎$$일 때, 함수 $$𝑓(𝑥)$$의 극한값은 $$𝐿$$이다.”
  
  - “$$𝑥 \rightarrow 𝑎$$일 때, 함수 $$𝑓(𝑥)$$가 $$𝐿$$에 수렴한다.”

- 좌극한과 우극한


  - 좌극한 $$𝑥 \rightarrow 𝑎−$$:
    
	- 변수 $$𝑥$$가 $$𝑎$$보다 작은 값에서(왼쪽에서) $$𝑎$$에 한없이 가까워질 때
	
	- $$\rightarrow$$ 좌극한값은 그때 함수 $$𝑓(𝑥)$$가 수렴하는 값
  
  - 우극한 $$ 𝑥 \rightarrow 𝑎 + $$:

    - 변수 $$𝑥$$가 $$𝑎$$보다 큰 값에서(오른쪽에서) $$𝑎$$에 한없이 가까워질 때
	
	- $$\rightarrow$$ 우극한값은 그때 함수 $$𝑓(𝑥)$$가 수렴하는 값

    $$
    \lim_{𝑥 \rightarrow 𝑎} ⁡𝑓(𝑥) = 𝐿 \Leftrightarrow \lim_{𝑥\rightarrow 𝑎−} ⁡𝑓(𝑥) = \lim_{𝑥 \rightarrow 𝑎 + } ⁡𝑓(𝑥) = 𝐿
    $$

- 함수의 극한값에 대한 사칙연산

  - $$𝑥 \rightarrow 𝑎$$일 때, 수렴하는 $$𝑓(𝑥) \rightarrow \alpha , 𝑔(𝑥) \rightarrow \beta $$ 에 대하여

    - (실수배) $$\lim_{𝑥 \rightarrow 𝑎} 𝑘𝑓(𝑥) = 𝑘 \lim_{𝑥 \rightarrow 𝑎} 𝑓(𝑥) = 𝑘\alpha $$ ($$𝑘$$는 상수)
	
	- (덧셈,뺄셈) $$\lim_{𝑥 \rightarrow 𝑎} \{ 𝑓(𝑥) \pm 𝑔(𝑥) \} = \lim_{𝑥 \rightarrow 𝑎} 𝑓(𝑥) \pm \lim_{𝑥 \rightarrow 𝑎} 𝑔(𝑥) = \alpha \pm \beta $$
	
	- (곱셈) $$\lim_{𝑥 \rightarrow 𝑎} \{𝑓(𝑥)𝑔(𝑥) \} = \{ \lim_{𝑥 \rightarrow 𝑎} 𝑓(𝑥)\} \{\lim_{𝑥 \rightarrow 𝑎} 𝑔(𝑥)\} = \alpha\beta $$
	
	- (나눗셈) $$\lim_{𝑥 \rightarrow 𝑎}  \dfrac{𝑓(𝑥)}{𝑔(𝑥)} = \dfrac{\lim_{𝑥 \rightarrow 𝑎} 𝑓(𝑥)}{\lim_{𝑥 \rightarrow 𝑎} 𝑔(𝑥)} = \dfrac{\alpha}{\beta} $$ (단, $$\beta \neq 0$$)

- 다항함수의 극한

  - 다항함수: $$ 𝑓(𝑥) = 𝑎_{n} 𝑥^{n} + 𝑎_{(n-1)} 𝑥^{𝑛−1)} + \cdots + 𝑎_{1} 𝑥 + 𝑎_{0} $$
  
  - 다항함수 𝑓(𝑥)의 극한:
    
	$$
	\begin{align}
    & \lim_{𝑥 \rightarrow 𝑣}⁡ 𝑓(𝑥) \\
	& = \lim_{𝑥 \rightarrow 𝑣}⁡ \left( 𝑎_{n} 𝑥^{n} + 𝑎_{(𝑛−1)} 𝑥^{(𝑛−1)} + \cdots + 𝑎_{1} 𝑥 + 𝑎_{0} \right) \\
	& = \lim_{𝑥 \rightarrow 𝑣}⁡ \left( 𝑎_{n} 𝑥^{n} \right) + \lim_{𝑥 \rightarrow 𝑣}⁡ \left( 𝑎_{(𝑛−1)} 𝑥^{(𝑛−1)} \right) + \cdots + \lim_{𝑥 \rightarrow 𝑣}⁡ \left(𝑎_1 𝑥 \right) + \lim_{𝑥 \rightarrow 𝑣}⁡ 𝑎_{0} \\
	& = 𝑎_{n} 𝑣^{n} + 𝑎_{(𝑛−1)} 𝑣^{(𝑛−1)} + \cdots + 𝑎_{n} 𝑣 + 𝑎_{0} \\
	& = 𝑓(𝑣) \\
	\end{align}
	$$

- 엄밀한 극한의 정의: 입실론($$\epsilon$$)-델타($$\delta$$) 논법

  - $$𝑥 \rightarrow 𝑎$$일 때, 
    
	$$
    𝑓(𝑥) \rightarrow 𝐿 \Leftrightarrow \lim_{𝑥 \rightarrow 𝑎}⁡ 𝑓(𝑥) = 𝐿
	$$
  
  - 임의의 $$ \epsilon > 0 $$에 대하여, 다음을 만족하는 $$\delta$$가 존재

    $$
    0 < \vert𝑥−𝑎\vert < \delta \text{이면, } \vert𝑓(𝑥)−𝐿\vert < \epsilon
	$$
  
  - 입실론-델타 논법으로 $$ \lim_{𝑥 \rightarrow 1}⁡(3𝑥−2) = 1 $$을 증명
    
	$$
	\begin{align}
	\vert(3𝑥−2)−1\vert & = \vert3𝑥−3\vert \\
	          & =3\vert𝑥−1\vert < \epsilon \\
	\end{align}
	$$
    - $$ 0 < \delta < \dfrac{\epsilon}{3} $$ 를 만족하는 $$\delta$$를 설정하면, (예를 들어 $$ \delta = \dfrac{\epsilon}{4} $$ ) 
	
      $$ 
	  0 < \vert𝑥−1\vert < \delta \Rightarrow 0 < 3\vert𝑥−1\vert < 3 \delta < \epsilon
	  $$

- 점 $$ 𝑥 = 𝑎 $$에서 함수 $$ 𝑓(𝑥) $$의 연속

  - 점 $$ 𝑥 = 𝑎 $$ 에서 함수 $$ 𝑓(𝑥) $$ 의 극한값과 함숫값이 일치
    
	$$
	\lim_{𝑥 \rightarrow 𝑎}⁡𝑓(𝑥)=𝑓(𝑎)
	$$

    - 닫힌 구간 $$ [𝑎,𝑏] $$ 에서 함수 $$ 𝑓(𝑥) $$ 의 연속
	
	- 열린 구간 $$ (𝑎,𝑏) $$ 의 임의의 점에서 함수 $$ 𝑓(𝑥) $$ 가 연속
	
	- 닫힌 구간 $$ [𝑎,𝑏] $$ 의 양끝점에서 좌/우극한값과 함숫값 일치
	
	  $$
	  \begin{align}
	  \lim_{𝑥 \rightarrow 𝑎+} ⁡𝑓(𝑥) & = 𝑓(𝑎) \\
	  \lim_{𝑥 \rightarrow 𝑏−} 𝑓(𝑥) & = 𝑓(𝑏) \\
	  \end{align}
	  $$

### 미분 계수와 도함수

- 평균변화율의 정의

  - 닫힌 구간 $$ [𝑎,𝑏]$$ 에서 함수 $$ 𝑓(𝑥) $$ (또는 $$𝑦$$)의 평균변화율

    $$ 
	\dfrac{\Delta 𝑦}{\Delta 𝑥} = \dfrac{\Delta 𝑓(𝑥)}{\Delta 𝑥} = \dfrac{𝑓(𝑏)−𝑓(𝑎)}{𝑏−𝑎} = \dfrac{𝑓(𝑎 + \Delta 𝑥) − 𝑓(𝑎)}{\Delta x}
	$$ 

  - $$ \Delta 𝑥 = 𝑏−𝑎 > 0 $$: $$𝑥$$의 값이 $$𝑎$$부터 $$𝑏$$까지 증가할 때, 그 증가한 값
  
  - $$ \Delta 𝑦 = 𝑓(𝑏)−𝑓(𝑎) $$: $$𝑥$$의 값이 $$𝑎$$부터 $$𝑏$$까지 증가할 때, 함수 $$𝑓(𝑥)$$의 함숫값이 변화한 값
  
- 평균변화율의 기하학적 의미 
  
  - 닫힌 구간 $$[𝑎,𝑏]$$에서 함수 $$𝑓(𝑥)$$(또는 𝑦)의 평균변화율
  
  - 좌표평면 위 닫힌 구간의 양끝점 $$(𝑎, 𝑓(𝑎))$$와 $$(𝑏, 𝑓(𝑏))$$를 지나는 직선의 기울기 직선의 기울기

    ![average](/images/Lec_4_avg.png)

- 순간변화율의 정의

  - 점 $$𝑥=𝑎$$에서 함수 $$𝑓(𝑥)$$의 순간변화율

    $$
    \lim_{𝑏 \rightarrow 𝑎} \dfrac{\Delta y}{\Delta x} = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{\Delta y}{\Delta x} = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑎 + \Delta 𝑥) − 𝑓(𝑎)}{\Delta 𝑥} = \lim_{𝑏 \rightarrow 𝑎} \dfrac{𝑓(𝑏)−𝑓(𝑎)}{𝑏−𝑎}
	$$
	
  - 평균변화율을 정의하는 구간 $$[𝑎,𝑏]$$을 $$𝑏 \rightarrow 𝑎$$ 로 압축시켰을 때, 평균변화율 $$ \dfrac{\Delta 𝑦}{\Delta 𝑥}$$의 극한값
  
- 순간변화율의 기하학적 의미

  - 점 $$ 𝑥 = 𝑎 $$에서 함수 $$𝑓(𝑥)$$의 순간변화율
  
  - 좌표평면 위 한 점 $$(𝑎, 𝑓(𝑎)) $$에서 함수 $$𝑦 = 𝑓(𝑥) $$의 그래프에 접하는 접선의 기울기

    ![average](/images/Lec_4_avg.png)

- 미분계수 $$f^{'}(𝑎)$$
  
  - 점 $$𝑥 = 𝑎$$에서 함수 $$𝑓(𝑥)$$의 순간변화율

    $$
    f^{'}(a) = \lim_{𝑥 \rightarrow 𝑎} \dfrac{𝑓(𝑥)−𝑓(𝑎)}{𝑥−𝑎} = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑎 + \Delta 𝑥) − 𝑓(𝑎)}{\Delta 𝑥}
    $$  
	
  - 미분계수의 다른 표현: $$ 𝑦^{'}\vert_{ 𝑥 = 𝑎}$$, $$\dfrac{dy}{dx}\vert_{𝑥=𝑎} $$
  
  - $$ 𝑦 = 𝑓(𝑥) = 𝑥^{2} + 2𝑥 − 3 $$의 $$ 𝑥 = 2$$ 에서 미분계수

    $$
	\begin{align}
	f^{'}(2) & = \lim_{𝑥 \rightarrow 2} \dfrac{𝑓(𝑥)−𝑓(2)}{𝑥−2} \\
	         & = \lim_{𝑥 \rightarrow 2} \dfrac{(𝑥^{2} + 2𝑥−3)−(2^{2} + 2 \times 2−3)}{𝑥−2} \\
			 & = \lim_{𝑥 \rightarrow 2} \dfrac{𝑥^{2} + 2𝑥−8}{𝑥−2} \\
			 & = \lim_{𝑥 \rightarrow 2} \dfrac{(𝑥 − 2)(𝑥 + 4)}{𝑥−2} \\
			 & = \lim_{𝑥 \rightarrow 2} (𝑥 + 4) \\
		     & = 6 \\
	\end{align}
	$$

- 도함수 $$f^{'}(x$$)

  - 함수 $$𝑓(𝑥)$$의 정의역 임의의 점에 대한 순간변화율
  
  - 미분계수 $$f^{'}(a) = \lim_{𝑥 \rightarrow 𝑎}  \dfrac{𝑓(𝑥)−𝑓(𝑎)}{𝑥−𝑎} = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑎 + \Delta 𝑥)−𝑓(𝑎)}{\Delta 𝑥} $$
  
  - 도함수 $$ f^{'}(x) = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑥 + \Delta 𝑥)−𝑓(𝑥)}{\Delta 𝑥} $$
  
  - 도함수의 다른 표현: $$ 𝑦^{'}, \dfrac{𝑑𝑦}{𝑑𝑥}, \dfrac{𝑑𝑓(𝑥)}{𝑑𝑥}, \dfrac{𝑑}{𝑑𝑥}𝑓(𝑥) $$

- 다항함수의 도함수

  - $$ 𝑓(𝑥) = 𝑥$$

    $$
    \begin{align}
	f^{'}(x) & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑥 + \Delta 𝑥)−𝑓(𝑥)}{\Delta 𝑥} \\
	         & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{(𝑥 + \Delta 𝑥)−𝑥}{\Delta 𝑥} \\
			 & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{\Delta 𝑥}{\Delta 𝑥} \\
			 & = \lim_{\Delta 𝑥 \rightarrow 0} (1) \\
			 & = 1 \\	
	\end{align}
	$$

  - $$ 𝑓(𝑥) = 𝑥^{2} $$

    $$
    \begin{align}
	f^{'}(x) & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑥 + \Delta 𝑥)−𝑓(𝑥)}{\Delta 𝑥} \\
	         & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{(𝑥 + \Delta 𝑥)^{2}−𝑥^{2}}{\Delta 𝑥} \\
			 & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{2x \Delta 𝑥 + (\Delta x)^{2}}{\Delta 𝑥} \\
			 & = \lim_{\Delta 𝑥 \rightarrow 0} (2x + \Delta x) \\
			 & = 2x \\	
	\end{align}
	$$

  - $$ 𝑓(𝑥) = 𝑥^{3} $$

    $$
    \begin{align}
	f^{'}(x) & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{𝑓(𝑥 + \Delta 𝑥)−𝑓(𝑥)}{\Delta 𝑥} \\
	         & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{(𝑥 + \Delta 𝑥)^{3}−𝑥^{3}}{\Delta 𝑥} \\
			 & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{3x^{2} (\Delta 𝑥) + 3x (\Delta x)^{2} + (\Delta x)^{3}}{\Delta 𝑥} \\
			 & = \lim_{\Delta 𝑥 \rightarrow 0} (3x^{2} + 3x(\Delta x) + (\Delta x)^{2}) \\
			 & = 3x^{2} \\	
	\end{align}
	$$
	
  - $$ \vdots $$

    $$  
	𝑓(𝑥) = 𝑥^{n} \rightarrow f^{'}(x) = 𝑛 𝑥^{𝑛−1}
	$$


### 함수의 연산과 미분법

- 미분법 기본 공식

  - 함수 $$𝑓(𝑥)$$와 $$𝑔(𝑥)$$의 도함수 $$𝑓^{'}(𝑥)$$와 $$𝑔^{'}(𝑥)$$가 존재할 때

    $$ 
	\begin{align}
    𝑓(𝑥) = 𝑐 \quad (𝑐\text{는 상수}) & \Rightarrow f^{'}(x) = 0 \\
    𝑓(𝑥) = 𝑥^{n}                   & \Rightarrow f^{'}(x) = 𝑛 𝑥^{𝑛−1} \\
	𝑦 = 𝑐𝑓(𝑥)                      & \Rightarrow 𝑦^{'} = 𝑐 f^{'}(x) \\
	𝑦 = 𝑓(𝑥) \pm 𝑔(𝑥)              & \Rightarrow 𝑦^{′} = f^{'}(x) \pm 𝑔^{′}(𝑥) \\
	𝑦 = 𝑓(𝑥)𝑔(𝑥)                   & \Rightarrow 𝑦^{′} = f^{'}(x)𝑔(𝑥) + 𝑓(𝑥) 𝑔^{′}(𝑥) \\
	𝑦 = \dfrac{𝑓(𝑥)}{𝑔(𝑥)}         & \Rightarrow 𝑦^{′}= \dfrac{f^{'}(x)𝑔(𝑥) − 𝑓(𝑥)𝑔^{′}(𝑥)}{𝑔(𝑥)^{2}} \\
	\end{align}
	$$
  
- 합성함수의 미분법(연쇄법칙, Chain Rule)

  - 합성함수 $$𝑦 = 𝑓(𝑔(𝑥))$$ 의 도함수

    - $$ 𝑦 = 𝑓(𝑢), 𝑢 = 𝑔(𝑥)$$로 단순화

	    $$
	    \begin{align}
	    \dfrac{𝑑𝑦}{𝑑𝑥} & = \lim_{\Delta 𝑥 \rightarrow 0}  \dfrac{\Delta 𝑦}{\Delta 𝑥} \\
	                  & = \lim_{\Delta 𝑥 \rightarrow 0} \dfrac{\Delta 𝑦}{\Delta 𝑢} \times \dfrac{\Delta u}{\Delta 𝑥} \\
					  & = \lim_{\Delta 𝑥 \rightarrow 0} \left( \dfrac{\Delta 𝑦}{\Delta 𝑢} \right) \times \lim_{\Delta 𝑥 \rightarrow 0} \left( \dfrac{\Delta 𝑢}{\Delta 𝑥} \right) \\
	    \end{align}
	    $$
	  
	- $$ 𝑦 = (2𝑥 + 1)^{3} 의 도함수

	    $$
		\begin{align}
	    𝑦 & = 𝑢^{3} \\
		𝑢 & = 2𝑥 + 1 \\
		\end{align}
		$$
		
	    $$
	    \begin{align}
		\dfrac{𝑑𝑦}{𝑑𝑥} & = \dfrac{𝑑𝑦}{𝑑𝑢} \times \dfrac{𝑑𝑢}{𝑑𝑥} \\ 
		              & =(3𝑢^{2}) \times (2) \\
					  & =6 𝑢^{2} \\
					  & =6(2𝑥 + 1)^{2} \\
	    \end{align}
	    $$

- 음함수 미분법
  
  - 음함수(implicit function): $$ 𝑦 = 𝑓(𝑥)$$ 꼴(양함수)로 표현이 되지 않은 함수
  
  - 음함수를 미분하려면? 관계식을 정리하여 $$\dfrac{𝑑𝑦}{𝑑𝑥}$$를 유도
  
  - $$𝑦 = \sqrt{𝑥 + 1} $$ 의 도함수는?

    - 양변을 제곱하여 $$ 𝑦^{2} = 𝑥 + 1 $$
    
	- 양변을 $$𝑥$$로 미분하면 $$ 2𝑦 \dfrac{𝑑𝑦}{𝑑𝑥} = 1 \rightarrow \dfrac{𝑑𝑦}{𝑑𝑥} = \dfrac{1}{2𝑦} = \dfrac{1}{2\sqrt{𝑥 + 1}} $$

### 응용해 봅시다!

- 평균수입함수로부터 한계수입함수 계산

  - 평균수입(average revenue)함수: $$ 𝐴𝑅 = 20−𝑄 $$
  
  - 수입함수: $$ 𝑅 = 𝐴𝑅 \times 𝑄 = (20−𝑄)𝑄 = 20𝑄 − 𝑄^{2} $$
  
  - 한계수입(marginal revenue) 함수

    $$
	𝑀𝑅 = \dfrac{dR}{dQ} = \dfrac{d}{dQ}(20𝑄 − 𝑄^{2}) = 20−2𝑄 
	$$

  - 수입, 평균수입, 한계수입 사이의 관계는?


    ![AR_MR](/images/Lec_4_AR_MR.png)



## 편미분

- ★ 핵심만 쏙쏙!  

    {: .note}
	> '편미분'은?
	> 
	> 관심 변수만 증가할 때 변화율!


### 다변수함수의 그래프

- 다변수함수의 정의

  - $$ 𝐷 \subseteq 𝑅^{n} $$일 때, $$𝐷$$에서 정의된 함수 $$𝑓$$가 임의의 순서쌍 $$(𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n}) \in 𝐷$$와 실수 $$ 𝑧 = 𝑓(𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n} )$$ 사이 관계를 지정하는 규칙

  - 다변수함수 예시

    - 가로의 길이가 $$𝑥$$, 세로의 길이가 $$𝑦$$인 직사각형의 넓이 $$𝐴 = 𝑥𝑦$$
	
	- 반지름의 길이 $$𝑟$$, 높이가 $$ℎ$$인 직원기둥의 부피 $$ 𝑉 = \pi 𝑟^{2}h $$

- 다변수함수의 정의역(domain)

  - 다변수함수 $$𝑓$$의 정의역이 특별히 명시되지 않았다면,$$𝑓$$의 정의역 $$𝐷$$는 $$𝑓$$를 가장 잘 정의하는 최대(maximal) 집합
  
  - $$ 𝑧 =\sqrt{𝑥^{2} + 𝑦^{2}} $$의 정의역:

    $$
    𝐷 = \{ (𝑥, 𝑦) \vert 𝑥^{2} + 𝑦^{2} \geq 0 \} = \mathbb{R}^{2} \rightarrow \text{좌표평면 전체}
    $$
	
  - $$ 𝑧 = \sqrt{9 − 𝑥^{2} − 𝑦^{2}} $$의 정의역:

    $$
    \begin{align}
    𝐷 & = \{ (𝑥, 𝑦) \vert 9 − 𝑥^{2} − 𝑦^{2} \geq 0 \}  \\
	& = \{(𝑥, 𝑦) \vert 𝑥^{2} + 𝑦^{2} \leq 9 \} \rightarrow \text{원의 내부} \\
    \end{align}
    $$


- 다변수함수의 치역(range)

  - 다변수함수 $$𝑓$$와 그 정의역 $$𝐷$$가 주어졌을 때, $$𝑓$$가 가질 수 있는 값의 집합
  
  - $$ 𝑧 =\sqrt{𝑥^{2} + 𝑦^{2}} $$의 치역: 정의역 $$ 𝐷 = \mathbb{R}^{2} $$

    $$
    𝑓(𝐷) = \{ 𝑧 \in \mathbb{R} \vert 𝑧 \geq 0 \} \rightarrow \text{좌표공간의} 𝑧 \geq 0 \text{인 반공간}
    $$
	
  - $$𝑧 = \sqrt{9−𝑥^{2}−𝑦^{2}}$$의 치역: 정의역 $$𝐷$$는 원의 내부

    $$
    𝑓(𝐷) = \{ 𝑧 \in \mathbb{R} \vert 0 \leq 𝑧 \leq 3 \} \rightarrow \text{좌표공간 중 } 0 \leq z \leq 3 \text{인 영역(공간)}
    $$
 
- 절단면(cross-section)

  - 다변수함수 $$ 𝑧 = 𝑓(𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n} ) $$의 $$𝑥_{𝑖} = 𝑐 $$에서 절단면은 $$ 𝑧 = 𝑓(𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n} )$$ 와 $$ 𝑥_{𝑖} = 𝑐$$ 의 교집합
  
  - $$ 𝑧 = \sqrt{4−𝑥^{2}−𝑦^{2} } $$의 $$𝑦 = 1$$ 에서 절단면:

    - 반구 $$ 𝑥^{2} + 𝑦^{2} + 𝑧^{2} = 4 ( z \geq 0)$$과 평면 $$𝑦 = 1$$의 교집합
	
      -  $$ \rightarrow 𝑥^{2} + (1)^{2} + 𝑧^{2} = 4 (𝑧 \geq 0) $$
	
      - 반원 $$ 𝑥^{2} + 𝑧^{2} = 3 (𝑧 \geq 0) $$
	
   - $$ 𝑧 = \sqrt{4−𝑥^{2}−𝑦^{2} } $$의 $$ 𝑥 = 0$$에서 절단면

     - 반구 $$𝑥^{2} + 𝑦^{2} + 𝑧^{2} = 4 (𝑧 \geq 0)$$과 평면 $$𝑥=0$$의 교집합
	 
     -  $$\rightarrow (0)^{2} + 𝑦^{2} + 𝑧^{2} = 4 (𝑧 \geq 0) $$

     - 반원 $$𝑦^{2} + 𝑧^{2} = 4 (𝑧 \geq 0) $$

- 등위선(level curve)

  - 다변수함수 $$ 𝑧 = 𝑓(𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n} )$$가 같은 높이(level) $$ 𝑧 = 𝑘$$인 값을 갖는 순서쌍 $$ (𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n})$$의 집합

    - $$ 𝑧 = 𝑓(𝑥_{1}, 𝑥_{2}, \cdots, 𝑥_{n} )$$와 $$ 𝑧 = 𝑘$$ 의 교집합
	
      - $$ 𝑧 = 𝑓(𝑥, 𝑦) = 𝑥^{2} + 𝑦^{2}$$의 그래프? 포물면(paraboloid)
	
	$$
     	\begin{align}
        𝑧=0: & 0 = 𝑥^{2} + 𝑦^{2} \\
        𝑧=1: & 1 = 𝑥^{2} + 𝑦^{2} \\
        𝑧=2: & 2 = 𝑥^{2} + 𝑦^{2} \\
	        & \vdots \\
	\end{align}
	$$
	
	![paraboloid](/images/Lec_4_paraboloid.png)

      - $$ 𝑧 = 𝑓(𝑥, 𝑦) = \sqrt{𝑥^{2} + 𝑦^{2}}$$의 그래프? 원뿔(cone)
	
	$$
     	\begin{align}
        𝑧=0: & 0 = \sqrt{𝑥^{2} + 𝑦^{2}} \\
        𝑧=1: & 1 = \sqrt{𝑥^{2} + 𝑦^{2}} \\
        𝑧=2: & 2 = \sqrt{𝑥^{2} + 𝑦^{2}} \\
	        & \vdots \\
	\end{align}
	$$
	
	![cone](/images/Lec_4_Cone.png)

      - $$ 𝑧 = 𝑓(𝑥, 𝑦) = 𝑥^{2} - 𝑦^{2}$$의 그래프? 포물면(paraboloid)
	
	$$
     	\begin{align}
        𝑧=0: & 0 = 𝑥^{2} - 𝑦^{2} \\
        𝑧=1: & 1 = 𝑥^{2} - 𝑦^{2} \\
        𝑧=2: & 2 = 𝑥^{2} - 𝑦^{2} \\
	        & \vdots \\
	\end{align}
	$$
	
	![hyperboloid](/images/Lec_4_hyperboloid.png)


### 편미분과 편도함수

- 편미분계수

  -  $$ 𝑧 = 𝑓(𝑥,𝑦)$$에 대하여 $$ 𝑦 = 𝑏 $$ 이고 $$𝑥$$만 변화할 때
  
  -  $$ 𝑔(𝑥) = 𝑓(𝑥, 𝑏) $$일 때, $$𝑔(𝑥)$$가 $$𝑥 = 𝑎$$에서 미분가능

     $$
     𝑔^{′}(𝑎) = \lim_{h \rightarrow 0} \dfrac{𝑔(𝑎 + ℎ)−𝑔(𝑎)}{h} 
     $$

     - $$ \rightarrow (𝑎,𝑏)$$에서 $$𝑓$$의 $$𝑥$$에 대한 편미분계수

  - 편미분계수의 표현: $$𝑓_𝑥 (𝑎,𝑏); \dfrac{\partial f }{\partial 𝑥} (𝑎,𝑏); \dfrac{\partial 𝑧}{\partial 𝑥} \vert_{(𝑥,𝑦)=(𝑎,𝑏)} $$

     ※ $$\partial$$ : 라운드 $$𝑑$$ 
	
	<!-- \textreferencemark  -->

-  $$ 𝑧 = 𝑓(𝑥,𝑦)$$에 대하여 $$𝑥 = 𝑎$$ 이고 $$𝑦$$ 만 변화할 때

  - $$𝑘(𝑦) = 𝑓(𝑎, 𝑦)$$일 때, $$𝑘(𝑦)$$가 $$𝑦 = 𝑏$$에서 미분가능

     $$
     𝑘^{′}(𝑏) = \lim_{ℎ \rightarrow 0}  \dfrac{𝑘(𝑏 + ℎ)−𝑘(𝑏)}{ℎ}
     $$

    - $$\rightarrow (𝑎,𝑏)$$에서 $$𝑓$$의 $$𝑦$$에 대한 편미분계수
	
 - 편미분계수의 표현: $$𝑓_{𝑦} (𝑎,𝑏); \dfrac{\partial 𝑓}{\partial y} (𝑎,𝑏); \dfrac{\partial 𝑧}{\partial 𝑦} \vert_{(𝑥,𝑦)=(𝑎,𝑏) }$$

    ※ $$\partial$$ : 라운드 $$𝑑$$
	
	<!-- \textreferencemark  -->

- 편도함수(partial derivative)

  - $$ 𝑧 = 𝑓(𝑥,𝑦)$$에 대하여 $$𝑓$$의 $$𝑥$$에 대한 편도함수:

    $$
    𝑓_{𝑥} (𝑥,𝑦)= \dfrac{\partial 𝑓}{\partial 𝑥} (𝑥,𝑦) = \lim_{ℎ \rightarrow 0} \dfrac{𝑓(𝑥 + ℎ, 𝑦)−𝑓(𝑥,𝑦)}{ℎ}
    $$
  
  - $$ 𝑧 = 𝑓(𝑥,𝑦)$$에 대하여 $$𝑓$$의 $$𝑦$$에 대한 편도함수:

    $$
    𝑓_{𝑦} (𝑥,𝑦) = \dfrac{\partial 𝑓}{\partial 𝑦} (𝑥,𝑦) = \lim_{ℎ \rightarrow 0} \dfrac{𝑓(𝑥, 𝑦 + ℎ)−𝑓(𝑥,𝑦)}{ℎ}
    $$
  
  - $$ 𝑧 = 𝑓(𝑥,𝑦) = 3𝑥^{2} + 𝑥𝑦 + 4𝑦^{2}$$의 $$𝑥$$에 대한 편도함수:
    
    $$
    𝑓_{𝑥} = \dfrac{\partial 𝑓}{\partial 𝑥} = 6𝑥 + 𝑦
    $$
  
  - $$ 𝑧 = 𝑓(𝑥,𝑦) = 3𝑥^{2} + 𝑥𝑦 + 4𝑦^{2}$$의 $$𝑦$$에 대한 편도함수:

    $$
    𝑓_{y} = \dfrac{\partial 𝑓}{\partial y} = 𝑥 + 8𝑦
    $$
  
- 편도함수와 일차근사(linear approximation)

  - 함수 $$𝑓$$의 편도함수가 점 $$(𝑥_{0}, 𝑦_{0})$$에서 연속일 때, 곡면 위의 점 $$(𝑥_{0}, 𝑦_{0}, 𝑓(𝑥_{0}, 𝑦_{0} ))$$에서 $$ 𝑧 = 𝑓(𝑥, 𝑦) $$의 접평면
  
  - 함수 $$𝑓$$의 편도함수가 점 $$(𝑥_{0}, 𝑦_{0} )$$에서 연속일 때, 점 $$(𝑥_{0}, 𝑦_{0} )$$와 인접한 $$(𝑥, 𝑦)$$에서 함숫값 $$𝑓(𝑥, 𝑦)$$의 일차근사

    $$
    𝑧 = 𝑓(𝑥_{0}, 𝑦_{0}) + 𝑓_{𝑥} (𝑥_{0}, 𝑦_{0})(𝑥−𝑥_{0}) + 𝑓_{𝑦} (𝑥_{0}, 𝑦_{0})(𝑦−𝑦_{0})
    $$

  - $$𝑧 = 𝑓(𝑥, 𝑦) = 5−𝑥^{2}−2𝑦^{2}$$에 대하여 $$𝑓(1.1, 0.9)$$의 근삿값을 $$(1, 1)$$의 일차근사를 이용하여 계산

    $$
    \begin{align}
    𝑓(1.1, 0.9) & = 𝑓(1 + 0.1, 1−0.1)  \\
    𝑓_{𝑥} & = \dfrac{\partial 𝑓}{\partial 𝑥} = −2𝑥 \rightarrow 𝑓_{𝑥}(1, 1) = −2 \\
    𝑓_{𝑦} & = \dfrac{\partial 𝑓}{\partial 𝑦} =−4𝑦 \rightarrow 𝑓_{𝑦} (1, 1) = −4 \\
    𝑓(1.1, 0.9) & \simeq 𝑓(1,1) + 𝑓_{𝑥} (1,1)(0.1) + 𝑓_{𝑦} (1,1)(−0.1) \\ 
	             & = 2 + (−2)(0.1) + (−4)(−0.1) \\ 
		     & = 2.2
    \end{align}
    $$


### 기울기 벡터
- 기울기 벡터(gradient vector)의 정의

  - $$𝑧 = 𝑓(𝑥,𝑦)$$ 위 임의의 점에서 접평면의 법선벡터; 접평면이 수직으로 바라보는 평면의 벡터
  
  - $$𝑧 = 𝑓(𝑥,𝑦)$$ 위 임의의 점에서 계산한 $$𝑥, 𝑦$$에 대한 편도함수로 이루어진 벡터
  
  - $$grad𝑓(𝑥_{0}, 𝑦_{0}); \nabla 𝑓 = (𝑓_{𝑥} (𝑥_{0}, 𝑦_{0} ), 𝑓_𝑦 (𝑥_{0}, 𝑦_{0})) $$

- 기울기 벡터 예제

  - $$z = 𝑓(𝑥,𝑦) = 𝑥^{2} 𝑦 + 6𝑥𝑦^{3} $$ @ $$ 𝑃 = (1,2)$$ 기울기 벡터는?

    $$
	\begin{align}
       𝑓_{𝑥} &= \dfrac{\partial 𝑓}{\partial 𝑥} = 2𝑥𝑦 + 6𝑦^{3} \\
       𝑓_{𝑦} &= \dfrac{\partial 𝑓}{\partial 𝑦} = 𝑥^{2} + 18𝑥𝑦^{2} \\
        \end{align}
    $$

    - 기울기 벡터 
	
	$$ 
	\begin{align}
	\nabla 𝑓 & = \left( \dfrac{\partial 𝑓}{\partial 𝑥}, \dfrac{\partial 𝑓}{\partial 𝑦} \right) \\
	              & = (2𝑥𝑦 + 6𝑦^{3}, 𝑥^{2} + 18𝑥𝑦^{2} ) \\
       \nabla 𝑓 \vert_{(𝑥,𝑦)=(1,2)} & = (𝑓_{𝑥} (1, 2), 𝑓_{𝑦} (1, 2)) \\
	                                         & = (52, 73) 
       \end{align}
       $$

- 기울기 벡터와 등위선 사이의 관계: 서로 <span style="color:#FF0000">수직!</span>

  - 높이가 $$ 𝑧 = 𝑘$$인 등위선의 방정식: $$ 𝑘 = 𝑓(𝑥, 𝑦) $$

    - 등위선의 방정식을 $$𝑥$$에 대하여 편미분
	
	$$
	0 = 𝑓_{𝑥} (𝑥,𝑦) + 𝑓_{𝑦} (𝑥,𝑦) \cdot 𝑦^{′} \rightarrow 𝑦^{′} = −\dfrac{𝑓_{𝑥}(𝑥,𝑦)}{𝑓_{y}(𝑥,𝑦)}
	$$
	
    - 기울기 벡터 $$ \nabla 𝑓 = \left( 𝑓_{𝑥}(𝑥,𝑦), 𝑓_{𝑦}(𝑥,𝑦) \right) $$의 기울기: $$\dfrac{𝑓_𝑦 (𝑥,𝑦)}{𝑓_𝑥 (𝑥,𝑦)} $$

    - (등위선의 기울기) $$\times$$ (기울기 벡터의 기울기) $$=−1$$

- 기울기 벡터와 등위선의 증가/감소

  - 점 $$(𝑥_{0}, 𝑦_{0})$$에서 함수 $$ 𝑧 = 𝑓(𝑥, 𝑦)$$는

    - <span style="color:#105AD2">$$\overrightarrow{𝑣} = \nabla 𝑓(𝑥_{0}, 𝑦_{0})$$</span> 방향으로 <span style="color:#105AD2">가장 빠르게 증가</span>
	
  - 점 $$(𝑥_{0}, 𝑦_{0})$$에서 함수 $$ 𝑧 = 𝑓(𝑥, 𝑦)$$는 
	
    - <span style="color:#FF0000">$$\overrightarrow{u} = -\nabla 𝑓(𝑥_{0}, 𝑦_{0})$$</span> 방향으로 <span style="color:#FF0000">가장 빠르게 감소</span>

- 기울기 벡터와 등위선의 증가/감소 예제

  - $$𝑧 = 𝑓(𝑥, 𝑦) = 5−𝑥^{2} − 2𝑦^{2}$$ 위의 점 $$(1, 1)$$에 $$𝑓$$가 가장 빠르게 증가하는/감소하는 방향은?

    $$
	\begin{align}
	𝑓_{𝑥} = \dfrac{\partial 𝑓}{\partial 𝑥} = −2𝑥 \rightarrow 𝑓_{𝑥} (1, 1) = −2 \\
	𝑓_{𝑦} = \dfrac{\partial 𝑓}{\partial 𝑦} = −4𝑦 \rightarrow 𝑓_{𝑦} (1, 1) = −4 \\
	\end{align}
    $$
  
  - 가장 빠르게 증가하는 방향: $$\nabla 𝑓(1, 1) = (−2, −4) $$
  
  - 가장 빠르게 감소하는 방향: $$−\nabla 𝑓(1, 1) = (2, 4) $$

### 응용해 봅시다!

- 수요와 공급의 관계에서 균형의 변동성을 구하면?

  - 수요함수: $$𝑄_{𝑑} = 𝑎−𝑏𝑃 $$ $$ (𝑎, 𝑏 > 0)$$
  
  - 공급함수: $$𝑄_{𝑠} = −𝑐 + 𝑑𝑃$$ $$(𝑐, 𝑑>0)$$
  
  - 균형조건($$𝑄_{𝑑} = 𝑄_{𝑠}$$)을 적용하면? 
    
	$$
    (𝑃^{∗}, 𝑄^{∗}) = \left( \dfrac{𝑎 + 𝑐}{𝑏 + 𝑑}, \dfrac{𝑎𝑑−𝑏𝑐}{𝑏 + 𝑑} \right)
	$$
  
  - 편도함수를 활용하여 균형을 정태적으로 비교

    $$
	\begin{align}	
    \dfrac{\partial 𝑃^{*}}{\partial 𝑎} & = \dfrac{1}{𝑏 + 𝑑} > 0 \\
    \dfrac{\partial 𝑃^{*}}{\partial b} & = -\dfrac{a+c}{(𝑏 + 𝑑)^{2}} < 0 \\
    \dfrac{\partial 𝑃^{*}}{\partial c} & = \dfrac{1}{𝑏 + 𝑑} = \dfrac{\partial 𝑃^{*}}{\partial 𝑎} > 0 \\
    \dfrac{\partial 𝑃^{*}}{\partial d} & = -\dfrac{a+c}{(𝑏 + 𝑑)^{2}} = \dfrac{\partial 𝑃^{*}}{\partial b} < 0 \\
	\end{align}
	$$



## 정리하기

- 미분은 극한을 이용하여 변화율을 계산

- 미분은 경제학 분야에서 ‘한계’의 개념으로 활용

- 다변수함수를 미분할 때는 편미분을 적용하며, 편미분을 활용하여 균형의 정태적 비교가 가능
