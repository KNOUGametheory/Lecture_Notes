---
layout: default
title: 나비 모형으로 연구하기
parent: simulation
nav_order: 3
---

# 나비 모형으로 연구하기

## 학습개요

기본 모형을 자신의 연구 관심사에 따라 수정하는 방법을 익힌다.

## 학습목표

1.  기본 모형으로부터 분석 가능한 모형으로 발전시킨다.

2.  주석 처리 방법을 안다.

3.  관심을 갖고 있는 변수의 값을 변화시킬 수 있다.

4.  모형이 타당한 지 확인할 수 있다.

5.  외부 자료 파일 불러오기를 할 수 있다.

6.  결과를 그래프 또는 분석 가능한 포맷으로 저장할 수 있다.

## 주요 용어

새 이름으로 저장, `slider`, 전역 변수, 국지 변수, 주석, `boolean`,
`monitor`, `plot`, 시나리오, 실험, `export-plot`, `file-open`,
`user-file`

## 연구의 시작

-   진짜 일은 최초의 모형을 만든 후 시작

    -   논문은 결과물이지, 과정을 자세하게 보여주지 않음

    -   연구 주제에 대한 답을 찾을 때까지 모형 분석과 수정의 반복 작업이
        필요

-   모델 라이브러리

    -   장점: 실현 $\rightarrow$ 선배 연구자들이 세운 가정과 수식이
        어떻게 작동하는지 보여줌

    -   단점: 연구 방법을 알려주지는 않음

        -   어떻게 아이디어와 개념을 만들었고,

        -   가설을 발전시키고 테스트 했는지,

        -   관찰된 현상을 얼마나 좁게 또는 얼마나 일반화시켜서 설명할
            것인지 등을 보여주지 않음

-   나비 모형의 목적: 통로의 창발

    -   즉, 나비를 유인하는 어떤 요소가 없더라도, 나비가 움직이는 경로가
        집중된다는 것

    -   이런 경로가 언제 어떻게 나타나는 지 설명해야함

    -   하지만 현재의 모형은 나비의 움직임을 눈으로 볼 수 있도록
        만들었을 뿐

-   무엇부터 해야할까? $\rightarrow$ ODD와 희망 사항을 다시 확인하자

    -   통로라고 말할 수 있는 구체적인 값이 필요

    -   가상 지형을 실제 지형으로 대체해야 함

-   넷로고 매뉴얼과 사전을 계속 찾아봐야 함

## 나비, 통로를 만들까?

-   통로의 정의가 필요

    -   기본 모형에서 나비는 정해진 시간 동안 계속 움직임 $\rightarrow$
        나비가 국지적 정상에 도달하면 멈춘다는 가정을 추가

        -   국지적 정상: 주변의 8개 `patches`보다 높은 `patches`
            $\rightarrow$ 주변 8개? `neighbors` 사용

    -   모든 나비가 사용하는 통로의 폭
        $$= \dfrac{\text{나비가 지나간 길}}{\text{나비의 출발점과 도착점을 연결하는 (평균) 직선 거리}}$$

    -   모든 나비가 같은 직선 경로를 따라 올라간다고 생각하면, 통로의
        폭은 작을 것 $\rightarrow$ 다른 경로를 따른다면, 폭이 커질 것

-   나비가 곧장 언덕을 오를 확률 $q$ $\rightarrow$ 통로의 폭에 영향을 줄
    것 $\rightarrow$ 이 둘의 관계를 그래프로 그려보자

-   새 이름으로 저장: `butterfly_2.nlogo`

    -   모형에 변화를 줄 때는 항상 이전 모형의 복사 파일을 만든 후에
        진행. 단순한 시도만 하고자 할 때도, 반드시 원본 파일을 남겨두고,
        복제 파일에서 진행할 것

    -   미래의 나와 과거의 나가 대화할 때가 많음 $\rightarrow$ `Code`
        탭에 어떤 변화가 있는 지 기록하거나, 표를 만들어 어떤 변화가
        있는 지 정리해두는 것도 좋음

-   50 마리 생성

                crt 50
                [
                  ...
                ]

-   $q$를 변화시키자

    -   `Interface` 탭, `sliders` 생성 $\rightarrow$ $q$ 변경

    -   0.0에서 1.0까지 0.01씩 증가하도록

-   경고가 나오는 것이 정상

    -   `sliders`, `switches`, `choosers`는 모두 전역 변수를 사용

    -   코드의 값을 반영하지, `Interface`에서 조정한 값을 반영하지 않음

    -   $\rightarrow$ 코드에서의 $q$ 값을 주석 처리 해야 함

                        globals
                        [
                          ;q
                        ]

-   주석 처리: 주석 처리하고 싶은 부분의 앞에 `;`, 편집기의 단축키를
    사용하면 편함

    -   지금 하고 있는 일이 무엇인지 설명

    -   변수 설명

    -   각 단계의 맥락을 설명

    -   끝이 어디인지 확인

    -   긴 프로그램의 경우 해당 절차 가 어디서 끝나는 지 확인할 때

-   국지적 최고봉에 올라오면 멈추도록

            to move
               if elevation >= 
               [elevation] of max-one-of neighbors [elevation] 
               [stop]

-   통로 폭을 계산하자

    -   $\rightarrow$ 계산 식을 보면, 우리에게 필요한 것은 출발점과
        도착점의 직선 거리와 나비가 지나간 길

    -   나비의 출발점: `patch-here` 사용

                    turtles-own
                    [
                      start-patch
                    ]
                    
                    ...
                    
                    crt 50
                    [
                      ...
                      set start-patch patch-here
                    ]

    -   우리는 나비가 어떤 `patches` 를 사용할 지 모름

        -   $\rightarrow$ 모든 `patches` 에 나비의 사용 여부 속성을 부여

        -   boolean (true-false) 변수: 변수명 끝에 $?$를 붙여서

        -   초기 설정 변수(initializing variables): 새로운 변수는 다른
            값을 지정하기 전에는 $0$에서 시작. 프로그램 작동에는 문제를
            일으키지 않지만, 분석에서는 문제가 될 수 있는 데, 알기도
            찾기도 어려운 에러가 됨 $\rightarrow$ 값을 주고 시작하는
            습관을 들이도록

        ```{=html}
        <!-- -->
        ```
                        patches-own
                            [
                            used?
                            ]
                        ...
                        ask patches
                            [
                            ...
                            set used? false
                            ] 

    -   나비가 지나간 이후 $\rightarrow$ `patches` 사용 여부를 알 수
        있음

                    to move
                        ...
                        set used? true
                     end

-   이제 통로 폭(corridor width)을 계산해야 함 $\rightarrow$ 값의 보고
    `to-report` 사용

    -   우리가 알고자 하는 값을 구하는 과정을 생각해보자

        -   나비가 지나간 모든 `patches`의 수를 계산 $\rightarrow$
            `count`, `with` 사용

        -   나비 각각의 출발점과 현재 위치의 거리를 계산 $\rightarrow$
            `distance` 사용

        -   나비 전체의 평균 거리를 계산 $\rightarrow$ `mean [] of` 사용

        -   통로 폭: (1)/(3)

                            to-report corridor-width
                              let num-patches-used count patches with [used? = true]
                                  
                              ask turtles
                              [
                                  set the-distance distance start-patch
                                  set mean-of-the-distance mean [the-distance] of turtles  
                              ]
                                 
                              report num-patches-used / mean-of-the-distance
                            end

    -   변수 지정을 잊지 말자

                    globals
                    [
                    ; q
                    mean-of-the-distance
                    ]
                    
                    turtles-own
                    [
                     start-patch
                     the-distance
                    ]

-   실행하면? 통로 폭의 값을 확인하지는 못했음 $\rightarrow$ 계산된 통로
    폭의 값을 확인하자

    -   결과 관찰 $\rightarrow$ 결과 창 만들기

        -   `Interface` 탭 $\rightarrow$ `Monitor`

        -   `reporter`에 `corridor-width` 쓰기

        -   경고가 나오는 것이 정상

    -   결과 값을 모니터 창에 $\rightarrow$ 국지(local) 변수
        `final-corridor-width` 사용, 결과 창에 설명 만들기

                    to go
                     ...
                     let final-corridor-width corridor-width
                     ...
                     if ticks >= 1000 [output-print word "Corridor width: " final-corridor-width stop]
                    end
                    
                    to-report corridor-width
                    end

    -   $q$를 변화시켰을 때, 결과 값이 변화하는가? $\rightarrow$
        변화하지 않음

        -   논리의 문제?

        -   코딩의 문제?

            -   잘못 쓴 변수 이름

            -   문법 오류

            -   `primitives`의 계산 방법을 잘못 알고 있음

            -   결과 창 설정 오류 등

    -   $\rightarrow$ `set q 0.4`를 그대로 두면 $q = 0.4$로 고정

        -   $q$ 관련 명령도 모두 주석 처리해야 함

        -   변수 값을 정확히 불러오는 중인지는 알기도 찾기도 어려운 에러
            중의 하나 $\rightarrow$ 어떻게 확인 가능할 지 모형의 구조를
            면밀히 생각해볼 것

        ```{=html}
        <!-- -->
        ```
                        to setup
                        ...
                        ;  set q 0.4
                        
                          reset-ticks
                        end 

## 결과 확인과 외부 자료 사용

-   끝? 우리는 아직 $q$와 통로의 관계를 확인하지 않았음

    -   그래프 그리기 $\rightarrow$ `plot`

                        to go
                          ask turtles [move]
                          ...
                          plot corridor-width
                          ...
                        end

        -   위 상태에서 코드는 경고없이 잘 저장 되지만, 실행하면 에러를
            만듬 $\rightarrow$ 그래프를 만들어야 함

        -   `Interface` 탭 $\rightarrow$ `Plot`

        -   `Name`: `Corridor Width`

        -   `x-axis`: `Tick`, `y-axis`: `Corridor Width`

        -   `pen update commands`의 내용은 모두 삭제

    -   $q$ 를 변화시키면서, 통로 폭의 변화를 확인하자 $\rightarrow$
        `export-plot`

    -   `.csv` 파일로 내보내기

                    to go
                     ...
                     export-plot "Corridor width" (word "Corridor-output-for-q-" q ".csv")  
                    end

    -   스프레드시트 프로그램이나 통계 패키지에서 `.csv` 파일을 불러와서
        분석

-   실제 지리적 공간에서 하려면?

    -   UTM 같은 좌표 시스템을 바로 넷로고에서 사용할 수 없음
        $\rightarrow$ 전환 필요. 관련 소프트웨어에서 알아서

        -   가로로 한 줄에, grid point or cell 좌표 정보, 공간 특성
            정보가 들어가도록 작성

        -   넷로고의 `patch` 하나의 크기($1 \times 1$)에 맞춰 실제
            공간의 크기를 보정 해주어야 함

    -   넷로고 에서 공간 설정

        -   `Settings` 창 또는

        -   명령어 `resize-world`

    -   우리는 이미 만들어진 공간 파일을 불러올 것

        -   새 이름으로 저장: `butterfly_3.nlogo`

        -   <https://www.railsback-grimm-abm-book.com/downloads-errata-2nd-edition/>,
            Supporting Materials Chapter 5, "ElevationData.txt\"

        -   불러올 파일을 같은 작업 폴더에 두고 `file-open`을 사용하거나
            아니면 `user-file` 사용

                            to setup
                            ...
                              file-open "ElevationData.txt"
                              while [not file-at-end?]
                              [
                                let next-X file-read
                                let next-Y file-read
                                let next-elevation file-read
                                ask patch next-X next-Y [set elevation next-elevation]
                              ]
                              file-close
                            end

-   최고 높이와 최저 높이에 따라 색을 변화 $\rightarrow$ `max`, `min`
    사용

    -   실행하는 데 오래 걸릴 것

                        to setup
                        ...
                        file-close
                            
                        ask patches
                         [  
                         ... 
                          set pcolor scale-color green elevation 
                            (min [elevation] of patches) 
                            (max [elevation] of patches)
                          set used? false
                         ]
                        end

        -   22,500개의 `patches` 각각의 최소와 최대 높이를 확인하도록
            했기 때문

        -   우리의 1차 목표는 논리적 구조에 맞는 정확한 계산 모형을
            만드는 것

        -   하지만 때로는 계산 속도를 개선할 필요가 있음 $\rightarrow$
            계산 시간이 너무 오래 걸리면, 수정과 평가에 너무 많은 시간을
            소모할 수 있기 때문

    -   지금의 문제를 해결하려면?

                
                    let min-elevation min [elevation] of patches
                    let max-elevation max [elevation] of patches
                        
                    ask patches
                     [  
                      set pcolor scale-color green elevation min-elevation max-elevation
                      set used? false
                     ]
                    end

-   초기 값을 바꿔보자

    -   나비의 출발점을 바꿔보자

                        crt 50
                        [
                            setxy random-pxcor random-pycor
                        ] 

    -   나비의 수를 바꿔보자

                        crt 500
                        ...

-   서로 다른 시나리오가 반복되는 실험(experiments)을 해야 함

    -   모형과 변수/입력 자료/초기 조건의 한 집합이 하나의 시나리오

    -   만약 확률 과정이 없다면, 하나의 시나리오를 여러 번 반복하더라도
        동일한 결과가 나올 것

-   반복 실험은 다른 시나리오를 시행하는 것

    -   무작위로 생성되는 수가 바뀌거나

    -   입력 자료를 바꾸거나

    -   초기 값을 바꾸는 것도 다른 시나리오가 될 수 있음

    -   $\rightarrow$ 모형에서 확률 과정 또는 어떤 한 요소만 변화하고
        다른 요소는 변화하지 않도록 모형을 실행하는 것

-   우리의 경우, $q$

-   반복 시행을 수동으로? $\rightarrow$ BehaviorSpace가 우리를
    구원하리라

    -   `Tools` $\rightarrow$ `BehaviorSpace` $\rightarrow$ `New`

    -   매뉴얼 : Features $\rightarrow$ BehaviorSpace Guide

    -   전역 변수 값을 바꿔서 다수의 시나리오를 생성

    -   각 시나리오를 반복 시행 (repetitions)

    -   각 시행의 결과를 모아서 하나의 파일로 작성

## 정리하기

1.  중요한 변화가 있을 때에는 새로운 버전의 파일을 저장하고 변화 내용을
    기록한다.

2.  필요에 따라 주석 처리를 한다.

3.  모형에서 필요한 계산 과정을 정리하고, 필요한 변수를 지정해야 한다.

4.  연구 주제에 따라 신뢰할만한 답을 얻기 위해 수정과 반복 시행을
    해야한다.

5.  필요에 따라 외부 자료 파일을 불러올 수 있다.

6.  시뮬레이션의 결과값을 별도의 파일로 기록한다.

7.  결과 그래프를 만들고 별도의 파일로 저장한다.

8.  필요에 따라 외부 데이터 파일을 모형에 입력할 수 있다.

9.  필요에 따라 계산 시간을 줄일 수 있는 방법을 찾는다.
