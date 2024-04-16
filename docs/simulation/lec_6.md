---
layout: default
title: 파이선의 설치와 기본 문법
parent: 넷로고와 파이선을 활용한 게임이론 시뮬레이션
nav_order: 6
---

# 파이선의 설치와 기본 문법

## 학습개요

파이선을 설치하고 기본 문법을 익힌다.

## 학습목표

1.  파이선 환경을 로컬 컴퓨터에 설치한다.

2.  기초적인 파이선 구문을 익힌다.

3.  간단한 함수를 만든다.

4.  간단한 클래스를 만든다.

## 주요 용어

파이선, 아나콘다, 쥬피터 노트북, 패키지, 함수, 클래스, 인스턴스, 메소드

## 파이선 시작하기

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음을 할 수 있다.
    > 	
    >     -   클라우드에서 파이선을 사용할 수 있다.
    >		
    >     -   로컬 컴퓨터에 파이선 환경을 설치할 수 있다.
    >	
    >     -   쥬피터 노트북의 기본적인 기능을 사용할 수 있다.
    >
    > -   다음을 해보자.
    > 	
    >     -   관심가는 모형의 쥬피터 노트북 파일을 찾아보자.

-   파이선(Python)

    -   1989년 네덜란드의 귀도 반 로섬(Guido van Rossum, 1956--)이 공개한 고 수준 일반 목적 프로그래밍 언어

    -   [가장 인기 있는 프로그래밍 언어 중의 하나](https://spectrum.ieee.org/the-top-programming-languages-2023){:target="_blank"}

    -   컴퓨터 과학을 비롯 많은 학문 분야에서 폭 넓게 사용됨

    -   기계 학습, 데이터 과학, 천문학, 화학, 계산 생물학, 자연어 처리 등의 분야에서 널리 사용됨

    -   각 목적에 맞는 패키지 개발이 활발

        -   행렬: [`NumPy`](https://numpy.org/){:target="_blank"}

        -   대수: [`SymPy`](https://www.sympy.org/en/index.html){:target="_blank"}

        -   통계: [`pandas`](https://pandas.pydata.org/){:target="_blank"}

        -   그래프 이론: [`NetworkX`](https://networkx.org/){:target="_blank"}

        -   기계학습: [`PyTorch`](https://pytorch.org/){:target="_blank"}

        -   그림과 그래프: [`Matplotlib`](https://matplotlib.org/){:target="_blank"}

-   파이선 사용: 크게 두 가지 방법

    1.  클라우드에서 사용

    2.  로컬 컴퓨터에 설치 후 사용

-   클라우드에서 파이선 사용

    -   파이선이 이미 설치된 원격 서버를 사용하는 것

    -   [Google Colab](https://colab.research.google.com){:target="_blank"}

    -   학습용 수준에서는 무료 요금제로 사용해도 충분

-   로컬 컴퓨터에 설치 후 사용

    -   [코어 파이선 패키지](https://www.python.org/downloads/){:target="_blank"}

        -   많은 경우, 연구에 필요한 패키지를 추가로 설치해야 함

        -   필요한 것을 하나씩 설치하기는 힘들 수 있음

        -   $$\rightarrow$$ 패키지가 포함된 배포판 사용을 추천

    -   [아나콘다](https://docs.anaconda.com/free/anaconda/install/){:target="_blank"}

        -   권고, 앞으로 이를 기준으로 설명

        -   가장 최신 버전을 설치

        -   자신의 컴퓨터 시스템에에 맞는 배포판을 선택

        -   아나콘다를 기본 파이선으로 사용하겠냐는 대화창에서 "예\"를 선택

    -   아나콘다 업데이트

        -   터미널 실행

            -   윈도우즈: 시작 메뉴 검색 창에서 $$\rightarrow$$ `cmd` 또는 `명령 프롬프트` 입력

            -   맥: 파인더 $$\rightarrow$$ `/응용프로그램/유틸리티 폴더` 에서 터미널 더블 클릭

        -   `conda update anaconda` 입력 후 엔터

-   파이선 사용 방법: 아래 두 가지 방법 외에도 다양

    1.  터미널 (또는 커맨더) 창에서 파이선 사용

    2.  [쥬피터 노트북(`Jupyter Notebooks`)](https://jupyter.org/){:target="_blank"} $$\rightarrow$$ 우리가 사용

-   쥬피터 노트북 실행

    -   실행 프로그램 메뉴에서 쥬피터 노트북을 찾거나

    -   터미널 창을 열고, `jupyter notebook` 입력

    -   특징

        -   브라우저 기반 인터페이스

        -   파이선 명령을 작성하고 실행할 수 있음

        -   표, 그림, 애니메이션 등을 포함시킬 수 있음

        -   텍스트와 수식 등을 포함한 문서 작업도 같이 할 수 있음

    -   `jupyter notebook` 입력한 후, 터미널 창을 보면,

        -   `http://localhost:8888` 주소가 있음

        -   터미널을 종료하지 않았다면,

        -   웹 브라우저의 주소 창에 `http://localhost:8888` 를 입력한 후 접속시켜도, 쥬피터 노트북이 실행됨
		
	-   2024년 5월 현재, ver. 7.1.2
	
	    -   동영상 강의는 ver. 6.5.6으로 제작되었으나, 강의에서 수정이 필요한 코드는 없음
		
		-   UI가 다소 다르지만, 큰 차이는 아니며 실습에 지장은 없음

-   `new` $$\rightarrow$$ `Python 3 (ipykernel)` 클릭

    -   `File` $$\rightarrow$$ `Save as` $$\rightarrow$$ `practice_h`

    -   `In [   ]:` 옆의 박스에, `print("Hello World!")` 입력

        -   `Enter` 키 누르면 $$\rightarrow$$ 줄 바꿈

        -   `Ctrl-Enter`: 셀 실행

    -   다음 셀에 `1+1` 입력 후

        -   -   `Alt-Enter`: 셀 실행, 다음 셀 추가

            -   `Shift-Enter`: 셀 실행, 다음 셀 선택

    -   셀 빠져 나오기: `Esc` 또는 `Ctrl-m`: `command mode`

    -   셀 다시 들어가려면 `Enter` 키 누르거나, 셀을 클릭: `edit mode`

    -   셀 삭제: 셀 선택 후, `d` $$+$$ `d` (`d` 두 번 누르기)

    -   셀을 추가한 후

        -   `Esc` $$\rightarrow$$ `m`: `Markdown` 문서 작성으로 변경

        -   $$\rightarrow$$ `y`: `Code` 작성으로 변경

            -   드롭--다운 메뉴 박스에서도 변경 가능

## 함수

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음을 할 수 있다.
    > 	
    >     -   패키지 불러오기를 할 수 있다.
    >		
    >     -   코드 블록의 들여쓰기 규칙을 기억한다.
    >	
    >     -   함수를 정의할 수 있다.
    >
    > -   다음을 해보자.
    > 	
    >     -   관심가는 모형의 쥬피터 노트북 파일을 읽어보자.


-   새 노트북: `File` $$\rightarrow$$ `New Notebook`

-   새 이름으로 저장: `File` $$\rightarrow$$ `Save as` $$\rightarrow$$ `practice_f`

-   첫 셀에 다음을 입력하고, 셀 하나 추가

    ```python
    import numpy 
    ```

    -   `import 패키지(모듈)이름`: 사용하려는 패키지 불러올 때

-   두 번째 셀에 다음을 입력하고, 셀 하나 추가

    ```python
    numpy.sqrt(4)
    ```

    -   `패키지(모듈).모듈`: 패키지 안에 포함된 모듈을 사용할 때

    -   `numpy` 패키지의 `sqrt` 모듈을 실행 $$\rightarrow$$ $$\sqrt{4}$$를 계산 $$\rightarrow$$ 값은 2

    -   `numpy` 패키지의 `sqrt` 모듈이 궁금하다면 `numpy.sqrt?`

-   다음을 실행하고 값을 확인

    ```python
	np.sqrt(4)
    ```

    -   이름 오류가 있는 것이 정상. 우리는 `np`를 정의하지 않았으므로

-   모든 셀 지우고, 커널 재시작: `0` $$+$$ `0`

-   첫 셀에 다음을 모두 입력, 실행, 값을 확인

    ```python
    import numpy as np
	np.sqrt(4)
    ```

    -   패키지 이름을 줄여서 쓸 수 있음 $$\rightarrow$$ 편리 $$+$$ 보편적 용례

    -   `numpy.sqrt(4)`를 해보자.

        -   이름 오류가 있는 것이 정상. 우리는 `np`로 정의해 사용하기로 했으므로

-   함수

    -   기본 내장 함수: `max`, `print`, `str`, `type`, `any`, `all` 등

    -   패키지의 함수: `sqrt`의 예에서 설명

    -   직접 정의해보자

        -   $$f(x) = 2x+1$$ $$\rightarrow$$ 아래 코드 입력 후 실행

            ```python
			def f(x):
			return 2 * x + 1
            ```

            -   들여쓰기 에러가 뜨는 것이 정상

            -   코드 블록은 항상 들여쓰기: 같은 칸 수 만큼 들여쓰기, 표준 4칸
			
                ```python
                def f(x):
				    return 2 * x + 1
                ```

        -   `f(1)` 입력 실행 후, 값을 확인
		
             ```python
             f(1)
             ```

        -   $$f(x) = a+bx$$ $$\rightarrow$$ 아래 코드 입력 후 실행

            ```python
			def f(x, a=1, b=1):
			    return a + b * x
            ```

            -   `f(2)` 입력 실행 후, 값을 확인
			
                ```python
                f(2)
                ```

            -   `f(2, a=4, b=5)` 입력 실행 후, 값을 확인
			
               ```python
               f(2, a=4, b=5)
               ```
			

        -   이미 정의된 함수도 다시 정의할 수 있음

            ```python
			def new_abs_function(x):                
			    if x < 0:
				    abs_value = -x
				else:
				    abs_value = x
				return abs_value
            ```

            -   `def 함수이름(변수,변수,...)`: 함수를 정의하고자 할 때 사용

            -   `new_abs_function(x)`: $$x$$에 대한 `new_abs_function`라는 이름의 함수

            -   그 다음은 함수 내용 $$\rightarrow$$ 잊지 말고 콜론으로 끝내고, 코드 블록은 들여 쓰기

            -   `return 돌려줄값`: 입력된 $$x$$에 대해 정의된 `abs_value`의 값을 `abs_value`로 돌려줘야 함

        -   $$x = 3, -3$$일 때, 결과 값은?

            -   $$x = 3 > 0$$ $$\rightarrow$$ `abs_value` $$= x = 3$$

            -   $$x = -3  < 0$$ $$\rightarrow$$ `abs_value` $$= -x = 3$$

        -   확인해보자
		
            ```python
			print(new_abs_function(3))
			print(new_abs_function(-3)) 
            ```

## 클래스

-   들어가기

    {: .note}

    > -   이 강의를 마친 후 다음을 할 수 있다.
    > 	
    >     -   간단한 소비 모형의 구조를 생각해본다.
    >		
    >     -   클래스를 만들 수 있다.
    >
    > -   다음을 해보자.
    > 	
    >     -   클래스는 언제 유용할 지 생각해보자.
    > 	
    >     -   관심가는 모형의 쥬피터 노트북 파일에서 클래스를 찾아보고, 이를 읽어보자.

-   소비자(`Consumer`): 자산(`wealth`), 소득(`earn`), 지출(`spend`)을 하는 경제 주체를 생각해보자

    -   이 소비자의 소득과 소비를 다음과 같이 생각할 수 있음

        -   최초 자산

        -   최초 자산 $$+$$ 1기 소득

        -   최초 자산 $$+$$ 1기 소득 $$-$$ 1기 지출 $$=$$ 2기 자산

        -   2기 자산 $$+$$ 2기 소득

        -   2기 자산 $$+$$ 2기 소득 $$-$$ 2기 지출 $$=$$ 3기 자산

        -   $$\ldots$$

    -   `File` $$\rightarrow$$ `New Notebook`

    -   `File` $$\rightarrow$$ `Save as`

    -   소득(`earn`), 지출(`spend`) 함수 만으로 이 관계를 만들어보자
	
	    ```python
		def earn(w,y):
		    return w+y
		
		def spend(w,x):
		    new_wealth = w -x
			if new_wealth < 0:
			    print("자산 부족!!!")
			else:
			    return new_wealth
        ```

    -   다음을 입력해보자
	
        ```python
		w0=100
		w1=earn(w0,10)
		w2=spend(w1,20)
		w3=earn(w2,10)
		w4=spend(w3,20)
		print("w0,w1,w2,w3,w4 = ", w0,w1,w2,w3,w4)
        ```

        -   즉, 최초 자산 100, 매기 소득 10, 매기 지출 20을 의미

    -   아래 결과가 나오는 것을 확인하자
        ```python
		w0,w1,w2,w3,w4 =  100 110 90 100 80
        ```

-   같은 행위를 하는 경제 주체들이지만 갖고 있는 변수 값은 서로 다른 경우 $$\rightarrow$$ 클래스(`class`)

    -   클래스: 인스턴스, 인스턴스의 데이터, 이 데이터를 사용하는 함수의 모음

    -   인스턴스(instance): 우리의 경우, 소비자

        -   인스턴스의 데이터는 소득과 소비에 의해 계속 변화

    -   메소드(methods): 인스턴스의 데이터(자산)와 함수(소득과 소비)

        -   `earn`: 소비자의 소득 $$y$$에 따른 자산 변화 $$earn(y)$$

        -   `spend`: 소비자의 소비 $$x$$에 따른 자산 변화 $$spend(x)$$, 만약 자산이 충분하지 않으면 경고를 알림

    -   다음을 입력, 실행, 셀 추가 해보자
	
        ```python
        class Consumer:
		    def __init__(self, w):
			    self.wealth = w
				
			def earn(self, y):
			    self.wealth += y
				
			def spend(self, x):
			    new_wealth = self.wealth - x
				if new_wealth < 0:
				    print("자산 부족!!!")
				else:
				    self.wealth = new_wealth
        ```

    -   다음을 입력, 실행, 셀 추가해보자
        ```python
        c1 = Consumer(10) 
        c2 = Consumer(15)
        print("소비자 1의 최초 자산: ", c1.wealth, ", " "소비자 2의 최초 자산: ", c2.wealth)
        ```
		
        -   클래스 생성은 `class`로 알려줌

        -   `__init__`: 클래스의 인스턴스를 만들 때, 자동으로 불러오는 메소드 $$\rightarrow$$ 인스턴스 데이터를 불러올 이름 공간(namespace)을 만듬

        -   `self`

            1.  인스턴스 데이터는 항상 앞에 `self.` 붙어야함: `self.wealth`

            2.  메소드도 `self` 로 불러 와야 함: `def earn(self, y)`

            3.  `+=`: $$i = i + 1$$ $$\rightarrow$$ `i += 1`

    -   다음을 입력, 실행, 셀 추가해보자
        ```python
        c1.earn(10)
		c2.earn(20)
		print("소비자 1의 소득 후 자산: ", c1.wealth, ", " "소비자 2의 소득 후 자산: ", c2.wealth)
        ```

    -   다음을 입력, 실행, 셀 추가해보자
        ```python
		c1.spend(10)
		c2.spend(40)
		print("소비자 1의 소비 후 자산: ", c1.wealth, ", " "소비자 2의 소비 후 자산: ", c2.wealth)
        ```

        -   아래 결과가 나오는 것이 맞음
            ```python
			자산 부족!!!
			소비자 1의 소비 후 자산: 10 ,소비자 2의 소비 후 자산: 35
            ```

    -   `c1.__dict__`를 입력, 실행, 셀 추가해보자
	
        ```python
        c1.__dict__
        ```

    -   `c2.__dict__`를 입력, 실행해보자
	
        ```python
        c2.__dict__
        ```

    -   각각의 인스턴스 `c1`, `c2`은 각각 독립된 이름 공간 사전(dictionary)에 데이터를 저장

        -   그 값을 불러오는 명령

## 정리하기

1.  파이선은 가장 인기 있는 프로그래밍 언어의 하나로, 다양한 학문 분야에서 활용된다.

2.  파이선을 로컬 컴퓨터에 설치해 사용할 때에는 코어와 자주 쓰는 패키지가 포함된 배포판 설치를 권한다.

3.  쥬피터 노트북은 편집, 실행, 문서 작업을 동시에 할 수 있다는 장점이 있다.

4.  `import` 명령은 패키지를 불러올 때 사용하고 보통 `as`와 함께 사용한다.

5.  함수 정의는 def로 시작한다.

6.  코드 블록은 시작하기 전 `:` (콜론)으로 끝을 표시하고, 같은 코드 블록은 들여쓰기를 같게 한다. 들여쓰기 표준은 4칸이다.

7.  같은 행위를 하는 경제 주체이지만, 변수 값은 서로 다른 경우, 이를 클래스로 표현할 수 있다.

8.  클래스에는 인스턴스, 인스턴스의 데이터, 이 데이터를 사용하는 함수가 포함된다.

9.  클래스의 정의는 class로 시작한다.
