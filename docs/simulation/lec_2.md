---
layout: default
title: 넷로고의 설치와 기본 문법
parent: 넷로고와 파이선을 활용한 게임이론 시뮬레이션
nav_order: 2
---

# 넷로고의 설치와 기본 문법

## 학습개요

넷로고를 설치하고 간단한 모형을 만든다.

## 학습목표

1.  넷로고를 설치할 수 있다.

2.  ODD 프로토콜의 필요성을 이해하고 모형의 목표에 따라 작성할 수 있다.

3.  간단한 모형을 만들 수 있다.

## 주요 용어

넷로고, 매뉴얼, 사전, ODD 프로토콜, `turtles`, `patches`, `links`,`observer`, `ifelse`, `to`, `end`

## Netlogo 시작하기: 설치, 매뉴얼, 기본 화면

-   Netlogo 설치

    -   <https://ccl.northwestern.edu/netlogo/download.shtml>

    -   2023년 9월 현재, ver. 6.3.0

    -   버전 선택 후 다운로드 `Download` 버튼 클릭

    -   Windows, MacOS, Linux 판 설치 가능

-   매뉴얼/사전과 친해지기

    -   매뉴얼: <https://ccl.northwestern.edu/netlogo/docs/>

    -   사전: <https://ccl.northwestern.edu/netlogo/docs/dictionary.html>

-   세 개의 탭

    -   `Interface`

        -   모형의 설정

        -   모형의 실행 및 상황 확인

        -   모형의 결과 관찰

    -   `Info`

        -   모형에 대한 설명을 기록 또는 확인

        -   `Markdown` 문법: <https://ccl.northwestern.edu/netlogo/docs/infotab.html>

    -   `Code`

        -   모형의 코드 확인 및 작성

-   `Models Library`

    -   메뉴 탭, `File` $$\rightarrow$$ `Models Library`

    -   기존 모형의 예제 모음

-   넷로고 모형 모음

    -   <http://modelingcommons.org/account/login>

## 나비 모형: ODD 프로토콜

-   프로토콜을 사용하는 이유

    -   모형을 만들 설계도가 필요

    -   재현성: 행위자 기반 모형을 재실행하거나 결과를 복제하기 어려울 수 있음 $$\rightarrow$$ 실험실 실험의 재현과 같은 개념

        -   우리가 만드는 모형 안에 연구 목적, 모형 구성, 변수 설정, 정당화 등에 대한 논의를 다 설명하기 어렵기 때문

    -   $$\rightarrow$$ 손 쉽게 이해할 수 있도록 표준화된 설명 방식을
        만들면 되지 않을까?

    -   $$\rightarrow$$ 프로토콜

-   ODD (Overview -- Design Concepts -- Details) 프로토콜 [@Railsback:2019tq p. 37]

    |       Overview       | 1\. 목적과 패턴                          |
	|                      | 2\. 독립체, 상태 변수, 척도                |
	|                      | 3\. 전체 과정과 스케쥴                    |
	|   Design Concepts    | 4\. 설계 개념                           |
	|                      | 기본 원칙, 창발, 적응, 목표, 학습, 예측,      |
	|                      | 지각, 상호 작용, 확률 과정, 집합적 특성, 관찰  |
	|    Details           | 5\. 최초 설정                           |
	|                      | 6\. 입력 자료                           |
	|                      | 7\. 하위 모형                           |


-   나비 모형의 목적

    -   나비의 언덕 오르기 행위와 지형도의 상호 작용으로 통로가
        만들어지는 조건은 무엇인가?

    -   나비의 언덕 오르기에 영향을 미치는 다양한 요소가 통로의 창발에
        영향을 미치는가?

-   독립체, 상태 변수, 척도

    -   나비: 위치

    -   공간: 면적과 높이

        -   `patch`: 150 $$\times$$ 150

        -   `patch`는 하나의 변수만 가짐: `elevation`

        -   하나의 `patch`는 실제 얼마의 넓이에 대응? 지금은 고려하지 말자

    -   시간: 1,000 `steps` 시행 $$\rightarrow$$ 실제 얼마의 시간? 역시 지금은 고려하지 말자

-   전체 과정과 스케쥴

    -   과정: 나비의 움직임

    -   한 번의 단계에서 나비는 한 번 움직임

    -   지금 만드는 기본 모형에서는 상호작용이 없음 $$\rightarrow$$ 나비의 움직임 순서는 중요하지 않음

-   설계 개념

    -   관심 변수: 통로를 어떻게 정의할 것인가?

    -   통로는 모형의 두 가지 요소로부터 창발

        -   나비의 적응적 움직임: 즉, 언덕 오르기

        -   나비가 움직이고 있는 지형

    -   나비는 자신의 주변에서 가장 높은 곳을 파악할 수 있어야 함 $$\rightarrow$$ 얼마나 먼거리에 있는 `patch`의 높이까지 알 수 있는가에 따라 다양한 시나리오가 가능

    -   모형에는 상호 작용(interaction)이 없음

    -   확률 과정(stochasticity)

        -   현실에서 항상 언덕 오르기를 할 수 있는 것은 아님

        -   가장 높은 지역을 찾는 능력에 제한이 있고, 지형 이외에 다른 요소, 이를 테면 꽃을 따라 간다든지

        -   이를 묘사하기 위해 단순한 파라미터, 언덕을 곧장 오를 확률 $$q$$ 도입

-   최초 설정

    -   지형도

        -   단순 가상 공간에서

        -   실재 공간으로

    -   나비 50마리 $$\rightarrow$$ 하나의 patch 또는 좁은 지역에 위치

-   입력 자료

    -   환경 변화 없음 $$\rightarrow$$ 입력 자료 없음

-   하위 모형

    -   나비가 어떻게 언덕을 오르는가? 곧장 또는 무작위로?

## 나비, 언덕을 날기: ODD로부터 Netlogo로

### 기초 문법

-   행위자: 넷로고 programming guide (<https://ccl.northwestern.edu/netlogo/docs/programming.html>)

    -   `turtles`: 이동형, 사망/재생산 능력, 네트워크의 노드 등

    -   `patches`: 고정형, 2차원 직사각형 격자의 정사각형 셀 집합

    -   `links`: `turtles`의 연결

    -   `observer`: `turtles`, `patches`, `turtles`에게 속성을 부여, 결과 값을 관찰

-   변수

    -   행위자에 따라 이미 할당된 변수

        -   `turtles`: `breed`, `color`, `heading`, `hidden?` $$\cdots$$.

        -   `patches`: `pcolor`, `plabel`, $$\cdots$$.

        -   `links`: `breed`, `color`, `end1`, `end2`, $$\cdots$$.

    -   각 행위자별로 변수를 추가할 수 있음

    -   `observer` 변수는 자동으로 전역 변수(global variables) $$\rightarrow$$ 모든 행위자가 읽거나 쓸 수 있는 변수

-   행위자는 자신의 타입이 사용할 수 있는 변수만 접근할 수 있음

    -   즉, `turtles`의 변수에 `patches`가 접근할 수 없음

    -   예외

        -   `observer` 변수는 전역 변수로서 모든 행위자가 사용 가능

        -   `turtles`은 자신이 현재 올라 있는 `patches`의 변수를 자동으로 사용 가능

-   `primitive`

    -   행위자가 할 것을 지시하는 내장된 절차 또는 명령 $$\rightarrow$$ 사전을 잘 봐둘 것

        -   `commands`: 행위자에게 행동을 지시

        -   `reporters`: 값을 계산하고 이를 사용할 수 있도록 보고

    -   맥락이 있음

        -   `turtles`, `patches`, `links`, `observer` 가 사용할 수 있는 `primitive`가 정해져 있음

        -   사전에 아이콘으로 표시됨: `uphill`은 `turtles` 만

        -   오류 메세지: "`using a patch command in a turtle context.`\"

### 나비 모형

-   새로운 파일: `butterfly_1.nlogo`

-   `Info` 탭에 작성

    -   <https://www.railsback-grimm-abm-book.com/E2-Downloads/Chapter04/ButterflyModelODD.txt>

-   다음 단계로 갑시다 $$\rightarrow$$ `Code` 탭

-   독립체, 상태 변수, 척도

    ```netlogo
    globals
    [
    ]

    patches-own
    [
    ]

    turtles-own
    [
    ]
	````

    -   `Check` 클릭 $$\rightarrow$$ 아무 문제 없어야 정상

    -   ODD를 보면,

        -   `turtles`의 상태 변수는 위치 $$\rightarrow$$ 따로 정할 필요 없음

        -   `patches`의 상태 변수 높이 `elevation` $$\rightarrow$$ 정해야 함

-   다음 단계로 갑시다 $$\rightarrow$$ 모형의 공간

    -   `Interface` 탭 $$\rightarrow$$ `Settings`

        -   공간의 크기, 중심, 유형 등 설정

        -   설정 가능한 공간의 종류: <https://ccl.northwestern.edu/netlogo/docs/programming.html#topology>

        -   `World wraps horizontally` checked $$+$$ `World wraps vertically` checked $$\rightarrow$$ 토러스(Torus)

        -   `World wraps horizontally` checked $$+$$ `World wraps vertically` unchecked $$\rightarrow$$ 수평 실린더 공간

        -   `World wraps horizontally` unchecked $$+$$ `World wraps vertically` checked $$\rightarrow$$ 수직 실린더 공간

        -   `World wraps horizontally` unchecked $$+$$ `World wraps vertically` unchecked $$\rightarrow$$ 박스

    -   `Location of origin` $$\rightarrow$$ `Corner` and `Bottom Left`

    -   `max-pxcor` 와 `max-pycor` $$\rightarrow$$ 149, 149

    -   `World wraps horizontally`와 `World wraps vertically` 체크 해제

    -   `World` 창이 너무 크게 보일 것, 수정해봅시다

        -   `Interface` 탭 $$\rightarrow$$ `Settings`

        -   `Patch size` $$\rightarrow$$ 3

-   초기 설정

    ```netlogo
	turtles-own
	[
	]
	
	to setup
	ca
	ask patches
	[
	
	]
	reset-ticks
	end
	```

    -   `ca` 또는 `clear-all` 쓰는 것을 잊지 말자

        -   계속 수정하면서 작업을 하게되므로, 이전의 설정값을 모두 지워버려야 함

-   지형 생성: ODD에서 구체적인 지형은 언급하지 않음 $$\rightarrow$$ 만들어야 함

    ```netlogo
	ask patches
	[
	 let elev1 100 - distancexy 30 30
	 let elev2 50 - distancexy 120 100
	 
	 ifelse elev1 > elev2
	 [set elevation elev1]
	 [set elevation elev2]
	 
	 set pcolor scale-color green elevation 0 100
	]
    ```

    -   Netlogo의 명령어는 의미별로 모두 띄어쓸 것

    -   경고가 나오는 것이 정상: "Nothing named ELEVATION has been defined\"

    ```netlogo
	
	patches-own
	[
	 elevation
	]
    ```

    -   문제가 없으면 `check`가 비활성화 되고, 저장 가능해짐

-   지형 설명

    -   $$(30,30)$$과 $$(120, 100)$$에 정상이 있는 두 개의 언덕

    -   첫번째 언덕의 정상 높이는 100 units

    -   두번째 언덕의 정상 높이는 50 units

    -   `patch`의 높이는 위의 두 정상으로부터 수평 거리가 한 단위씩 멀어질 수록 1 unit 씩 감소

    -   `ifelse` $$\rightarrow$$ 두 개의 높이 중 항상 높은 값을 갖도록

    -   `scale-color` $$\rightarrow$$ 높이에 따라 음영 처리

-   지도를 잘 그렸나 확인

    -   `Interface` 탭 $$\rightarrow$$ `Add` 옆 $$\rightarrow$$ `Button` $$\rightarrow$$ "`setup`\"

-   우리 모형의 나비 $$\rightarrow$$ 움직이는 행위자 `turtle`

    ```netlogo
	 set pcolor scale-color green elevation 0 100
	]
	
	crt 1
	[
	 set size 2
	 setxy 85 95
	]
    ```

-   나비를 잘 만들었나 확인

    -   나비에서 마우스 오른쪽 클릭 $$\rightarrow$$ `Inspect` $$\rightarrow$$ $$x, y$$ 위치 확인

-   스케쥴 $$\rightarrow$$ 나비(`turtle`)는 한 번의 단계에서 한 번 움직임

    ```netlogo
	 reset-ticks
	end
	
	to go
	 ask turtles [move]
	end
	
	to move
	
	end
    ```

-   몇 번이나 움직이도록? $$\rightarrow$$ 1,000 단계, 즉 1,000번 움직이고자 할 때

    ```netlogo
	to go
	 ask turtles [move]
	 tick
	 if ticks >= 1000 [stop]
	end
    ```

-   `Interface`에 `go` 버튼 `button` 추가

    -   `Interface`에서 구성을 움직이거나, 크기를 바꾸거나, 편집하고 싶다면,

    -   구성 요소를 선택하고 마우스 오른쪽 클릭 후, "`Select`\" 선택

-   `go` 눌러 봅시다

    -   $$\rightarrow$$ 아무 일도 없어야 정상: `to move`의 내용을 채우지 않았기 때문

-   $$q$$의 확률로 곧장 언덕을 오르고, $$1-q$$의 확률로 무작위 이동 $$\rightarrow$$ 국지적인 정상에 오를 때까지

    ```
	to move
	 ifelse random-float 1 < q
	  [uphill elevation]
	  [move-to one-of neighbors]
	 end
    ```
	
    -   경고가 나오는 것이 정상 $$\rightarrow$$ $$q$$ 정의 필요

    ```netlogo
	globals
	[
	 q
	]
	
	to setup
	 set q 0.4
	 reset-ticks
	end
    ```

    -   `to move`

        -   `random-float NUMBER` $$\rightarrow$$ manual 참고

        -   `uphill`, `move-to`, `one-of`, `neighbors`: 모두 `primitives`

-   나비를 움직여 보자

    -   `Interface` $$\rightarrow$$ `go` 클릭

-   한번에 보내고 싶다면

    -   `Interface` 탭 $$\rightarrow$$ `go` 버튼 $$\rightarrow$$ 오른쪽 클릭 $$\rightarrow$$ `edit` 선택 $$\rightarrow$$ `forever` 박스 체크

-   나비의 움직임을 보고 싶다면

    ```netlogo
	
	crt 1
	[
	 set size 2
	 setxy 85 95
	 pen-down
	]
    ```

    -   변화를 반영하고 싶다면 $$\rightarrow$$ `setup`을 누를 것

-   우리는 완전히 작동하는 모형을 만들었음

    -   완성은 아님

    -   이제 시작일 뿐

    -   하지만, 한 번에 완성으로 갈 수 없으므로, 작동하는 가장 단순한 모형에서 출발해야 함

## 정리하기

1.  넷로고는 Windows, MacOS, Linux 에 설치 가능하다.

2.  넷로고 홈페이지의 매뉴얼과 사전을 확인하자.

3.  넷로고의 모델 라이브러리와 온라인 커뮤니티의 이미 만들어진 모형을 활용하자.

4.  ODD 프로토콜은 모형을 만들기 위한 설계도와 모형의 결과 재현을 위해 사용할 수 있다.

5.  `setup`, `ask`, `ifelse` 등을 사용해 ODD 프로토콜을 기반으로 작동하는 간단한 모형부터 만들자.

6.  필요에 따라 변수 정의를 할 수 있고, 넷로고 코드의 끝은 `]` 또는 `end`로 마감해야한다.
