# 파이선으로 이해하는 분리 현상 

## 학습개요

쉘링의 분리 모형을 파이선으로 구현한다.

## 학습목표 

1.  필요한 패키지를 설치할 수 있다.

2.  모형의 목적에 맞는 계산 절차를 구현할 수 있다.

3.  데이터 시각화의 기초를 익힌다.

## 주요 용어

`pip install`, `seaborn` 패키지, `array`, `len`

## 분리 모형 설정

-   쉘링, 분리 모형 [@Downey:2012aa]

    -   구현 대상: 전체 공간, 밀집도, 행위자 구분, 관용, 행복 등

    -   <https://colab.research.google.com/github/AllenDowney/ThinkComplexity2/blob/master/notebooks/chap09.ipynb>

-   사용하려는 패키지와 파일 가져오기

                import matplotlib.pyplot as plt
                import numpy as np
                
                from os.path import basename, exists
            
                def download(url):
                    filename = basename(url)
                    if not exists(filename):
                        from urllib.request import urlretrieve
                        local, _ = urlretrieve(url, filename)
                        print('Downloaded ' + local)
                    
                download('https://github.com/AllenDowney/ThinkComplexity2/raw/master/notebooks/utils.py')
                download('https://github.com/AllenDowney/ThinkComplexity2/raw/master/notebooks/Cell2D.py')  

    -   `os.path`: 운영체제에서 파일 경로를 불러오기 위해 사용

        -   <https://docs.python.org/3/library/os.path.html#module-os.path>

    -   `urllib.request`: URL 주소를 열기 위해 사용

        -   <https://docs.python.org/3/library/urllib.request.html>

    -   `utils.py`, `Cell2D.py`: 자신이 자주 쓰는 것을 모아, 함수 또는
        클래스로 만들어 둠

        -   장점: `import` 과정을 단순하게 할수 있음

        -   단점: 공동 작업에서 문제가 될 수 있음 $\rightarrow$ 우리
            경우처럼 `github.com`으로 공유하는 방법이 있음

-   (그림) 파일 저장

            from utils import decorate, savefig
            !mkdir -p figs

    -   `savefig`: `utils.py` 를 확인해 볼 것 $\rightarrow$ 축 표시와
        그림 저장

    -   `!`: 외부의 쉘 명령을 사용하기 위해 붙임

    -   `mkdir`: 디렉토리(폴더)를 생성하라는 명령

-   패키지 설치

            try:
                import empiricaldist
            except ImportError:
                !pip install empiricaldist  

    -   `empiricaldist`: 분포 함수에 필요

        -   <https://pypi.org/project/empiricaldist/>

    -   `try`: 예외 상황 `except` 지정하기 위해 사용, 우리의 경우
        `import empiricaldist` 에서 오류가 발생하면 `except` 이후 절을
        실행

    -   `pip install 패키지이름`: 파이선 패키지/모듈 설치를 위해 사용

        -   <https://docs.python.org/3/installing/index.html>

-   공간 만들기

            def locs_where(condition):
                return list(zip(*np.nonzero(condition)))    

    -   `np.nonzero`: `numpy`의 `nonzero`, 0이 아닌 튜플(tuple)의 목록을
        만듦

        -   <https://numpy.org/doc/stable/reference/generated/numpy.nonzero.html>

-   분리 모형 중 행위자 구분 하기

            import seaborn as sns
            from matplotlib.colors import LinearSegmentedColormap
            
            palette = sns.color_palette('muted')
            colors = 'white', palette[1], palette[0]
            cmap = LinearSegmentedColormap.from_list('cmap', colors)    

    -   `seaborn`: 데이터 시각화에 사용

        -   <https://seaborn.pydata.org>

    -   `LinearSegmentedColormap`: 색을 맵핑

        -   <https://matplotlib.org/stable/api/_as_gen/matplotlib.colors.LinearSegmentedColormap.html>

## 분리 모형 구성

-   클래스 설정

            from scipy.signal import correlate2d
            from Cell2D import Cell2D, draw_array
            
            class Schelling(Cell2D):
                
                options = dict(mode='same', boundary='wrap')
            
                kernel = np.array([[1, 1, 1],
                                   [1, 0, 1],
                                   [1, 1, 1]], dtype=np.int8)
                
                def __init__(self, n, p):
                    self.p = p
                    
                    choices = np.array([0, 1, 2], dtype=np.int8)
                    probs = [0.1, 0.45, 0.45]
                    self.array = np.random.choice(choices, (n, n), p=probs)

    -   `correlate2d`: 교차 상관 2차원 어레이

        -   <https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.correlate2d.html>

    -   `kernel`: 행위자 자신과 이웃을 정의

    -   `dtype`: `numpy`의 데이터 유형 정의

    -   속성 초기화

        -   0: 비어 있음, 1: 붉은 색, 2: 파란색

        -   `n`: 행의 수

        -   `p`: 같은 속성의 이웃에 대한 기준

-   이웃의 속성 확인하기

                def count_neighbors(self):

                    a = self.array
                    
                    empty = a==0
                    red = a==1
                    blue = a==2
            
                    num_red = correlate2d(red, self.kernel, **self.options)
                    num_blue = correlate2d(blue, self.kernel, **self.options)
                    num_neighbors = num_red + num_blue
            
                    frac_red = num_red / num_neighbors
                    frac_blue = num_blue / num_neighbors
                    
                    frac_red[num_neighbors == 0] = 0
                    frac_blue[num_neighbors == 0] = 0
                    
                    frac_same = np.where(red, frac_red, frac_blue)
            
                    frac_same[empty] = np.nan
                    
                    return empty, frac_red, frac_blue, frac_same

    -   `==`: 같음을 확인

        -   이외에 `!=`, `<`, `<=`, `>`, `>=`

        -   <https://docs.python.org/3/reference/expressions.html#comparisons>

    -   이웃의 속성을 세기: `num_red`, `num_blue`

    -   이웃의 비중을 세기: `frac_red`, `frac_blue`

    -   이웃이 없으면, 같은 속성의 이웃이 없는 것으로 간주

    -   같은 속성의 이웃을 세기: `frac_same`

    -   같은 속성이 공집합인 경우: `nan` 숫자가 아닌 것으로 간주(Not a
        Number)

-   같은 속성의 이웃의 평균 비중 계산

                def segregation(self):
                    _, _, _, frac_same = self.count_neighbors()
                    return np.nanmean(frac_same)

    -   `_, _, _, `: `_`(underscore), 특정 값을 무시, 우리의 경우,
        `empty, frac_red, frac_blue,`

-   만족하지 못하는 경우 $\rightarrow$ 무작위로 이동

                def step(self):
                
                    a = self.array
                    empty, _, _, frac_same = self.count_neighbors()
                    
                    with np.errstate(invalid='ignore'):
                        unhappy = frac_same < self.p
                    unhappy_locs = locs_where(unhappy)          
                    empty_locs = locs_where(empty)
            
                    if len(unhappy_locs):
                        np.random.shuffle(unhappy_locs)
                        
                    num_empty = np.sum(empty)
                    
                    for source in unhappy_locs:
                        i = np.random.randint(num_empty)
                        dest = empty_locs[i]
                        
                        a[dest] = a[source]
                        a[source] = 0
                        empty_locs[i] = source
                    
                        num_empty2 = np.sum(a==0)
                        assert num_empty == num_empty2
                    
                    return np.nanmean(frac_same)

    -   `errstate`: 오류 처리 기준 알려줌, 우리의 경우 NaN인 경우를
        무시(`ignore`)하라는 의미

        -   <https://numpy.org/doc/stable/reference/generated/numpy.errstate.html>

    -   행복하지 않은 행위자 확인

    -   이동할 수 있는 비어 있는 공간 확인

    -   `len`: 객체의 길이(length)를 계산, 우리의 경우 행복하지 않은
        행위자의 수

    -   행복하지 않은 행위자를 무작위 목적지로 이동시킴

        -   비어 있는 셀이 목적지

    -   비어 있는 셀의 수가 변화 없는 지 확인

    -   같은 속성의 이웃 비중을 다시 계산

-   결과 그리기

                def draw(self):
                    return draw_array(self.array, cmap=cmap, vmax=2)    

## 분리 모형 실험하기

-   작은 규모로 그려보기

            grid = Schelling(n=10, p=0.3)
            grid.draw()
            grid.segregation()  

-   애니메이션을 추가해 큰 규모로 그려보기

            grid = Schelling(n=100, p=0.3)
            grid.animate(frames=30, interval=0.1)   

-   분리 정도를 계산하고, 저장하기

            from utils import three_frame
            
            grid = Schelling(n=100, p=0.3)
            three_frame(grid, [0, 2, 8])
            
            savefig('figs/chap09-1')    

    -   `savefig`: 그림 파일 이름과 저장 위치

    -   `three_frame` 등 관련된 내용은 `utils.py` 확인 바람

-   관용 수준을 0.2부터 0.5까지 높여가면서 계산해보자

            from utils import set_palette
            set_palette('Blues', 5, reverse=True)
            
            np.random.seed(17)
            for p in [0.5, 0.4, 0.3, 0.2]:
                grid = Schelling(n=100, p=p)
                segs = [grid.step() for i in range(12)]
                plt.plot(segs, label='p = %.1f' % p)
                print(p, segs[-1], segs[-1] - p)
                
            decorate(xlabel='Time steps', ylabel='Segregation',
                            loc='lower right', ylim=[0, 1])
            
            savefig('figs/chap09-2')    

    -   관련된 내용은 `utils.py` 확인 바람

## 정리하기

1.  `os` 패키지를 사용해 운영체제 수준의 명령어를 실행할 수 있다.

2.  `pip install` 를 사용해 필요한 패키지를 설치할 수 있다.

3.  `array`를 사용해 행렬을 구성할 수 있다.

4.  모형의 목적을 충족할 수 있는 계산의 순서와 어떤 계산 값을 돌려줘야
    할 지 정리한 후, 코딩을 시작한다.

5.  어떤 데이터를 시각화할 지 그리고 어떻게 시각화할 지 정리한 후, 이를
    구현할 수 있는 패키지를 활용한다.
