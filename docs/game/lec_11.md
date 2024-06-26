---
layout: default
title: 베이지언 게임
parent: 게임이론
nav_order: 11
---

# 베이지언 게임

- 모든 경기자가 동일한 정보를 갖고 있는가? 아니면 정보의 차이가 있는가?

- 불완전한 정보의 상황을 묘사한 베이지안 게임에서, 경기자의 전략과 균형은 무엇일까? 

- 공공재의 무임승차문제는 왜 발생하는가?

- 과연 보다 많은 정보와 정확한 정보가 있다고 자신에게 이득을 보장하는가?

## 베이지언 게임 개념

- 핵심만 쏙쏙!

    {: .note}
	> - 다음 문제에 답을 할 수 있다.
	>
	> 	- 완전정보와 불완전정보를 구분할 수 있는가?  
	>
	> 	- 완비정보와 불완비정보를 구분할 수 있는가?
	>
	>	- 특히 불완비정보게임의 균형을 구할 수 있는가?
	>
	> - 다음 문제를 생각하자.
	>
	> 	- 상대방은 나의 type을 어떻게 생각하고 있는지 고려하자.
	>
	> 	- 어떤 경기자는 다른 경기자가 알지 못하는 정보를 가지고 있다.
	>
	> 	- 사적정보가 있을 때 각 경기자는 어떤 결정을 하는지 살펴보자.

### 정보
	
- 완전한 정보(perfect information)

	- 하나의 정보신호가 주어지면 어떤 불확실한 상태가 발생할지 확실하게 알 수 있는 정보

- 불완전한 정보(imperfect information)

	- 하나의 정보신호가 여러 개의 불확실한 상태와 관련되어 있기에 그 가운데 어떤 불확실한 상태가 실현될지 더 이상 알 수 없는 정보

- 정보의 구분

	- 대칭정보(symmetric information)

		- 모든 경제주체들이 완전한 정보를 보유하고 있는 정보적 상황

	- 비대칭정보(asymmetric information)

		- 일부 경제주체는 완전한 정보를 보유하고, 나머지는 아무런 정보가 없는 상황

- 비대칭정보 발생 원인

	- 감춰진 속성(hidden type)

	- 감춰진 행동(hidden effort)
	
- 감춰진 속성(hidden type)

	- 거래의 한쪽이 상대방의 유형에 대해 잘 모르는 경우

	- 보험의 경우 (사고 확률, 특정 질환등을 앓고 있는 여부), 고용 시장의 경우(업무 능력, 생산성), 중고차 시장(침수차량 여부)

- 감춰진 행동(hidden effort)

	- 계약체결 후 상대방의 행동을 완벽히 감시할 수 없는 상황

	- 권한을 위임하는 주인(principal)과 위임받은 대리인(agent)

	- 전문경영자는 주주가치의 극대화를 위해 최선을 다한다는 약속

	- 계약 후 전문경영인은 주주의 이익보다는 자신의 이익을 우선시 하나 이를 주주가 관찰하기 어려움.

- 상대방 유형의 인지

	- 완비정보게임(complete information)

	- 불완비정보게임(incomplete information) 또는 미비게임

### 베이지안 게임
	
- 베이지안 게임(Bayesian games)

	- 한 경기자가 다른 경기자가 가지지 못한 정보를 가지는 경우를 베이지안 게임 또는 불완비정보게임

	- 서로 다른 정보, 예) 성대결 게임, 과점시장(상이한 한계비용)

	- 한 경기자가 다른 경기자가 가지지 못한 사적정보(private information)

	![예시표](/images/Lec_11_p311.png)
	
- 여자가 남자를 좋아하는 경우

	- 순수전략 내쉬균형 (야구, 야구), (발레, 발레) 

	- 순수혼합전략 내쉬균형 (2/3 야구 + 1/3 발레, 1/3 야구 + 2/3 발레) 	

- 여자가 남자를 싫어하는 경우

	- 순수전략 내쉬균형 존재하지 않는다. 

	- 순수혼합전략 내쉬균형 (1/3 야구 + 2/3 발레, 1/3 야구 + 2/3 발레)
	
	![예시표](/images/Lec_11_p311.png)
	
### 응용해 봅시다.

- 여자는 남자가 알지 못하는 사적정보 보유

- 사적정보의 내용을 여자의 'type'라 하며, $$L(ove)$$-type과 $$H(ate)$$-type, 각각의 확률 $$\dfrac{1}{2}$$ 

	- 여자의 전략 $$\{L,H\}$$에서 $$\{\text{야구},\text{발레} \}$$로 가는 함수

	  $$
	  S_{2}=\{(\text{야구},\text{야구}),(\text{야구},\text{발레}),(\text{발레},\text{야구}),(\text{발레},\text{발레}) \}
	  $$
	  
	  $$
	  S_{1}=\{\text{야구},\text{발레} \}
	  $$
	
	![예시표](/images/Lec_11_p311_1.png)
	
- 기대보수

![예시표](/images/Lec_11_p311_2.png)

- 남자의 대응 

	- $$\text{(야구,야구)}$$ $$\rightarrow ~\text{야구}$$ 

	- $$\text{(야구, 발레)}$$ $$\rightarrow ~\text{야구}$$ 

	- $$\text{(발레, 야구)}$$ $$\rightarrow ~\text{야구}$$ 

	- $$\text{(발레,발레)}$$ $$\rightarrow ~\text{발레}$$ 

- 여자의 대응 

	- $$\text{야구}$$ $$\rightarrow ~\text{(야구,발레)}$$ 

	- $$\text{발레}$$ $$\rightarrow ~\text{(발레,야구)}$$ 
	
- 베이지안 순수전략 내쉬균형 $$\text{(야구, (야구,발레))}$$ 

![예시표](/images/Lec_11_p311_3.png)


## 공공재 공급

- 핵심만 쏙쏙!

    {: .note}
	> - 다음 문제에 답을 할 수 있다.
	>
	> 	- 공공재는 어떤 속성을 가지고 있는가? 
	>
	> 	- 무임승차는 왜 발생하는가?
	>
	> - 다음 문제를 생각하자.
	>
	> 	- 친구와 공동으로 사용하려는 TV에 얼마까지 지불할 의사가 있는가?
	>
	> 	- TV가 구비되었을 때 TV가 없을 때보다 과연 순가치가 증가하는가?
	>
	> 	- 친구는 얼마까지 지불한다고 생각하는가?
	>
	> 	- 친구 덕분에 TV를 공짜로 시청하고자 하는가?

### 재화의 구분
	
- 비배제성(non-exclusiveness)

	- 어느 누구도 편익으로부터 배제되지 않는 재화

	- 공공재 추가적인 이용으로 한계비용이 발생하지 않으므로 양의 가격을 책정하여 이용자를 배제하는 것은 불가능

- 비경합성(non-rivalry)

	- 어떤 사람의 추가적인 소비가 타인의 소비를 감소시키지 않으므로 양의 가격을 책정하는 것은 바람직하지 못하다.

- 재화의 구분

![예시표](/images/Lec_11_p311_4.png)

### 공공재

- 공공재의 구분

	- 순수공공재(pure public goods)

		- 비배제성과 비경합성의 특성을 모두 지니고 있는 재화

	- 비순수공공재(impure public goods)

		- 공공재 특성 중 하나만 가지고 있는 재화}

	- 클럽재(club goods)

		- 소비자(이용자)가 많아질수록 정체비용으로 인해 이용자들의 편익 감소

- 공공재 공급주체

	- 공공재의 공급주체는 정부 또는 민간기업으로 공급주체와는 무관

	- 사적재도 정부가 공급 가능, 자연독점인 경우에 공적으로 공급

	- 공공재, 사적재의 구분은 상품의 특성에 따른 구분
	
- 공공재 공급측면

	- 개별 수요자들의 공공재 편익 파악 불가 $$\rightarrow$$ 무임승차(free-riding)

	- 공공재 소비의 비배제성으로 인하여 공공재에 지불하지 않았다고 하여 소비자 배제 불가능

	- 공공재 건설에 소비자들은 비용을 지불하지 않고 건설된 공공재를 사용하려는 유인

	- 합리적 소비자는 무임승차 유인이 있기에 시장기구에서는 사회적 최적수준보다 과소생산

- 무임승차 문제를 게임이론에 적용

	- 소비자 1과 소비자 2

	- 공공재 생산에 기여(contribution)할지 말지를 고민

	- 개별소비자의 행동집합 $$A_{1}=A_{2}=\{\text{기여},~\text{무임승차}\}$$

- 공통지식

	- 소비자 $$i$$의 기여비용 $$c_{i}$$은 각각 $$-\beta$$와 $$1+\alpha$$ 사이의 균등분포

	- 형집합 $$T_{1}=T_{2}=[-\beta,~1+\alpha]$$

### 응용해 봅시다.

- 공공재건설게임

	- 공공재 이용으로 얻을 수 있는 가치는 모두에게 1

	- 기여에 따라 보수 결정 $$1-c_{i}$$, $$1$$, $$0$$

	- 전략형게임
	
	![예시표](/images/Lec_11_p311_5.png)
	
	- 개별경기자의 최적전략
	
		- 경기자 $$i$$의 기부비용 $$c_{i}< 0$$이면 무조건 기부 (무임승차는 강열등전략이기에)
	
		- 경기자 $$i$$의 기부비용 $$0\le c_{i}\le 1$$이면  상대방의 기부가능성이냐? 확실한 $$1-c_{i}$$이냐?
	
		- 기여비용이 미비하면 기여를 통해 확실한 $$1-c_{i}$$를 추구
	
		- 기여비용이 1보다 약간 작다면 무임승차하고 상대방의 기부가능성을 기대
	
		- 경기자 $$i$$의 기부비용 $$c_{i}> 1$$이면 모조건 무임승차 (기부는 강열등전략이기에)

	- 임계전환성(cutoff property)

		- 소비자 1

			- $$c_{1}$$이 임계치 $$c_{1}^{*}$$보다 작으면 기여

			- $$c_{1}$$이 임계치 $$c_{1}^{*}$$보다 크면 무임승차 시도

		- 소비자 2

			- $$c_{2}$$이 임계치 $$c_{2}^{*}$$보다 작으면 기여

			- $$c_{2}$$이 임계치 $$c_{2}^{*}$$보다 크면 무임승차 시도

	- 임계치 구하기

		- 소비자 1은 자신의 유형 $$c_{1}$$을 아는 상태에서 기여와 무임승차 중 선택

		- 소비자 1이 기여할 때 얻는 기대보수 
		
		$$E_{1}^{\text{기여}}=1-c_{1}$$

		- 무임승차를 시도할 때 얻는 기대보수
		
		$$
		\text{(경기자 2가 기여할 확률)}\times 1+\text{(경기자 2가 무임승차할 확률)}\times 0=E_{1}^{\text{무임승차}}(c_{2} < c_{2}^{*})
		$$
		
	- 소비자 1의 입장에서 생각하자.

		- 소비자 2의 유형 $$c_{2}$$는 균등분포를 따르는 확률변수
	
		$$[-\beta,~1+\alpha]~~~~~~~(\alpha,~\beta >0)$$

		- 확률밀도함수
	
		$$f(c_{2})=\frac{1}{1+\alpha+\beta}$$
		
		![예시표](/images/Lec_11_p311_6.png)
		
		- $$c_{2}\le c_{2}^{*}$$인 누적확률
		
		$$\frac{c_{2}^{*}+\beta}{1+\alpha+\beta}$$
		
		- 소비자 1이 무임승차를 시도할 때 얻는 기대보수
		
		$$E_{1}^{\text{무임승차}}(c_{2} < c_{2}^{*})=\frac{c_{2}^{*}+\beta}{1+\alpha+\beta}$$
		
		![예시표](/images/Lec_11_p311_7.png)
		
		- $$E_{1}^{\text{기여}}>E_{1}^{\text{무임승차}}$$ $$\rightarrow$$ 기여
		
		$$1-c_{1}>\frac{c_{2}^{*}+\beta}{1+\alpha+\beta}~~~~\text{또는}~~~~
		c_{1}<\frac{1+\alpha-c_{2}^{*}}{1+\alpha+\beta}~~~~~~~~\rightarrow~~~~\text{기여}$$
		
		- $$E_{1}^{\text{기여}}<E_{1}^{\text{무임승차}}$$ $$\rightarrow$$ 무임승차 시도
		
		$$1-c_{1}<\frac{c_{2}^{*}+\beta}{1+\alpha+\beta}~~~~\text{또는}~~~~
		c_{1}>\frac{1+\alpha-c_{2}^{*}}{1+\alpha+\beta}~~~~~~~~\rightarrow~~~~\text{무임승차 시도}$$
		
		- 소비자 1의 전략이 임계전환성을 갖기 위한 조건
		
		$$c_{1}^{*}=\frac{1+\alpha-c_{2}^{*}}{1+\alpha+\beta}$$
		
	- 소비자 2의 입장에서도 동일하게 적용
	
	- 소비자 1과 소비자 2의 입장에서 동시 고려
	
		- 임계전환성
	
		$$c_{i}^{*}=\frac{1+\alpha-c_{j}^{*}}{1+\alpha+\beta}$$
	
		- 대칭 논리
	
		$$c_{1}^{*}=c_{2}^{*}=\frac{1+\alpha}{2+\alpha+\beta}$$
		
	- 개별소비자
	
		- 자신의 기여비용이 임계치 이하이면 기여

		- 자신의 기여비용이 임계치를 초과하면 무임승차 시도
	
	- 베이지언 내쉬균형
			
		- $$\alpha,~\beta >0$$ 조건에서는 유일한 순수전략 균형
		
## 정보의 가치

- 핵심만 쏙쏙!

    {: .note}
	> - 다음 문제에 답을 할 수 있다.
	>
	> 	- 정보가 충분하다고 더 좋은 이득을 얻을 수 있는가?
	>
	> 	- 정보가 부족하다고 이득이 감소하는가?
	>
	> - 다음 문제를 생각하자.
	>
	> 	- 아는 게 병? 모르는 게 약?
	>
	> 	- 연구개발에 성공한 것을 다른 기업에게 공표하는 것이 반드시 이익이 되는지 살펴보자.
	>
	> 	- 연구개발에 실패했다고 자인하는 것으로 반드시 이익이 감소하는지 살펴보자.

### 산출량 경쟁
	
- 기업 1과 기업 2의 산출량 경쟁

- 역수요함수와 비용

$$P(Q)=a-bQ, ~~~~MC_{1}=c_{1},~~MC_{2}=c_{2},~~FC_{1}=FC_{2}=0$$

- 한계비용의 사적정보

	- 기업 2의 한계비용 $$c_{2}$$ : 두 기업 사이의 공통지식 
	
	$$p_{1}(c_{2}\vert c_{L})=p_{1}(c_{2}\vert c_{H})=1$$
	
	- 기업 1의 한계비용 : 기업 1의 연구개발에 의해 기업1은 자신의 한계비용을 정확히 알고 있지만 기업2는 기업 1의 한계비용을 정확히 알고 있지 못하다. 

- 조건부 확률

	- 기업 1의 연구개발 성공 확률로 한계비용 $$c_{L}$$의 확률 $$\alpha$$ $$\rightarrow$$ 즉, $$p_{2}(c_{L}\vert c_{2})=\alpha$$

	- 기업 1의 연구개발 실패 확률로 한계비용 $$c_{H}$$의 확률 $$1-\alpha$$ $$\rightarrow$$ 즉, $$p_{2}(c_{H}\vert c_{2})=1-\alpha$$

- 각 기업의 전략

	- 기업1의 전략 : $$s_{1}:\{c_{L},c_{H}\}\rightarrow [0,\infty)$$, $$s_{1}=(q_{L},q_{H})$$

	- 기업2의 전략 : $$s_{2}:q_{2}\in [0,\infty)$$


- 각 기업의 이윤함수

	- 기업 1의 연구개발 성공 시 이윤
	
	$$
	\pi_{L}(s_{1},q_{2})=(a-bq_{L}-bq_{2})q_{L}-c_{L}q_{L}=(a-c_{L}-bq_{L}-bq_{2})q_{L}
	$$

	- 기업 1의 연구개발 실패 시 이윤
	
	$$
	\pi_{H}(s_{1},q_{2})=(a-bq_{H}-bq_{2})q_{H}-c_{H}q_{H}=(a-c_{H}-bq_{H}-bq_{2})q_{H}
	$$	

	- 기업 2의 기대이윤
	
	$$
	\pi_{2}(s_{1},q_{2})=\alpha(a-c_{2}-bq_{L}-bq_{2})q_{2}+(1-\alpha)(a-c_{2}-bq_{H}-bq_{2})q_{2}
	$$	

- 최적대응

	- 기업 1의 연구개발 성공시 최적대응 산출량
	
	$$
	\frac{\partial \pi_{L}(s_{1},q_{2})}{\partial q_{L}}=0~~~\rightarrow~~~~q_{L}=\frac{a-c_{L}-bq_{2}}{2b}
	$$

	 - 기업 1의 연구개발 실패시 최적대응 산출량	
	$$
	\frac{\partial \pi_{H}(s_{1},q_{2})}{\partial q_{H}}=0~~~\rightarrow~~~~q_{H}=\frac{a-c_{H}-bq_{2}}{2b}
	$$

	 - 기업 2의 최적대응 산출량
	
	$$
	\frac{\partial \pi_{2}(s_{1},q_{2})}{\partial q_{2}}=0~~~\rightarrow~~~~q_{2}=\frac{a-c_{2}-b(\alpha q_{L}+(1-\alpha) q_{H})}{2b}
	$$

- 위 세 조건을 연립하여 풀어보자.

- 유일한 베이지안 내쉬균형

	- 기업 1의 연구개발 성공시 최적 산출량
	$$
	q_{L}^{*}=\frac{a-2c_{L}+c_{2}}{3b}-\frac{(1-\alpha)(c_{H}-c_{L})}{6b}
	$$

	- 기업 1의 연구개발 실패시 최적 산출량
	
	$$
	q_{H}^{*}=\frac{a-2c_{H}+c_{2}}{3b}+\frac{\alpha(c_{H}-c_{L})}{6b}
	$$

	- 기업 2의 최적 산출량
	
	$$
	q_{2}^{*}=\frac{a-2c_{2}+\alpha c_{L}+(1-\alpha )c_{H}}{3b}
	$$	
	
	- 경쟁기업이 산출량을 늘리면 자신의 산출량은 줄여야 한다.
	
	- 기업2의 산출량은 자신의 한계비용에는 감소함수, 기업1의 한계비용에는 증가함수이다. 

	- $$q_{2}^{*}$$\는 $$c_{1}=c_{L}$$일 경우보다는 크고, $$c_{1}=c_{H}$$일 경우보다는 작다.

- 함의

![예시표](/images/Lec_11_p311_8.png)

   - 기업 1의 한계비용
   
   $$c_{L}<\alpha c_{L}+(1-\alpha )c_{H}<c_{H}$$

   - 경쟁기업이 산출량을 늘리면 자신의 산출량은 줄여야 한다.


   - 기업1의 입장에서

		- 성공시 기업2가 더 생산하게 되므로 기업1의 산출량은 완비정보 하보다 적게 생산

		- 실패시 기업2가 덜 생산하므로 완비정보 하보다 많이 생산

   - 기업 1은 연구개발 실패의 존재 가능성 때문에 연구개발 성공 시 완비정보 하에서보다 손해

   - 기업 1은 연구개발 성공의 존재 가능성 때문에 연구개발 실패 시 완비정보 하에서보다 이득

- 정확하고 많은 정보가 더 큰 이익을 주는가? 전략적 상호작용의 게임에서는 그렇지 않다.

- 단기적 추가정보로 오히려 해악 가능성

### 응용해 봅시다.

- 기업 1과 기업 2의 산출량 경쟁

- 역수요함수와 비용

$$P(Q)=16-\frac{1}{3}Q=16-\frac{1}{3}Q_{1}-\frac{1}{3}Q_{2}, ~~~~~~FC_{1}=FC_{2}=0$$

- 한계비용의 사적정보

	- 기업 2의 한계비용 $$c_{2}=4$$ : 두 기업 사이의 공통지식

	- 기업 1의 한계비용 : 기업 1의 연구개발에 의해 기업1은 자신의 한계비용을 정확히 알고 있지만 기업2는 기업 1의 한계비용을 정확히 알고 있지 못하다. 

- 확률

	- 기업 1의 연구개발 성공 확률로 한계비용 $$c_{L}=0$$의 확률 $$p$$

	- 기업 1의 연구개발 실패 확률로 한계비용 $$c_{H}=4$$의 확률 $$1-p$$

- 기업 1과 기업 2의 산출량 경쟁

	![예시표](/images/Lec_11_p311_9.png)
	
	- 기업 1이 확실히 성공하더라도 성공확률변수 $$0< p<1$$로 산출량 감소 $$18+2p<20$$
	
	- 기업 1이 확실히 실패하더라도 성공확률변수 $$0< p<1$$로 산출량 증가 $$12<18+2p$$

- 성공시는 자신이 성공했다는 것을 공표하더라도 상대방은 위협으로 생각하지 않는다.

- 실패시는 자신이 실패했다는 것을 공표하더라도 상대방은 위협으로 생각한다.

## 정리하기

- 불완비정보가 존재하는 게임의 균형을 찾을 수 있다.

- 상대방의 type에 따라 전략을 고려한다.

- 조건부 확률을 적용하여 기대보수를 구할 수 있다.

- 정보가 많다고 반드시 이득이 되지 않으며, 정보가 부족하다고 반드시 손실이 초래되는 것은 아니다.