둘째마당 데이터 시각화 기초 목차
========

UNIT 04 기본 그래프 그리기
---------
1. '[matplotlib](https://matplotlib.org, "matplotlib 홈페이지") 라이브러리'란?
2. 기본 그래프 추가하기
3. 그래프에 옵션 추가하기

UNIT 05 내 생일의 기온 변화를 그래프로 그리기
---------
1. 데이터에 질문하기
2. 데이터 시각화하기
3. 날짜 데이터 추출하기

UNIT 06 기온 데이터를 다양하게 시각화하기
---------
1. 데이터에 질문하기
2. 히스토그램
3. 기온 데이터를 히스토그램으로 표현하기
4. 기온 데이터를 상자 그림으로 표현하기

----------------------------------------------

## UNIT 04 기본 그래프 그리기

### 1. 'matplotlib 라이브러리'란?
> matplotlib 라이브러리는 파이썬에서 2D 형태의 그래프, 이미지 등을 그릴 때 사용하는 것으로, 실제 과학 컴퓨팅 연구 분야나 인공지능 연구 분야에서 많이 활용됨

* [matplotlib 홈페이지](https://matplotlib.org, "matplotlib 홈페이지")

matplotlib 라이브러리 중 pyplot 모듈 불러오기

```python
import matplotlib.pyplot
```

이름이 너무 길고 복잡하므로 앞으로 라이브러리를 임포트할 때는 *plt* 라는 별명 사용
```python
import matplotlib.pyplot as plt
```

### 2. 기본 그래프 그리기

> *plot()* 함수는 직선 또는 꺾은선 형태의 그래프를 그릴 때 사용

기본 그래프 그리는 보통의 세 단계
1. import matplotlib.pyplot as plt : 라이브러리 불러오기
2. plt.plot([x축 데이터], [y축 데이터]) : plot() 함수에 데이터 입력하기
3. plt.show() : 그래프 보여주기

**예시 추가**

### 3. 그래프에 옵션 추가하기

* 그래프에 제목 넣기
> *title()* 함수는 제목을 넣는 함수

```python
plt.title('제목에 넣을 문자열')
```

* 그래프에 범례 넣기
> plot() 함수에 label이라는 속성의 레이블 값으로 원하는 문자열을 넣어주고, 그래프를 그리기 전에 legend() ~~전설 아닙니다~~ 함수 실행시키면 레이블 값이 범례로 나타남
 
```python
plt.plot([x축 데이터], [y축 데이터], label='레이블 값')
plt.legend()
```

* 그래프 색상 바꾸기
> color 속성 추가
>> r == red, g == green, b == blue, k == black, y == yellow 등등

```python
plt.plot(~~~, color='원하는 색상')
```

* 그래프 선 모양 바꾸기
> plot() 함수는 기본적으로 직선으로 그래프를 그리지만 linestyle 속성에 원하는 선 모양 지정 가능

```python
plt.plot(~~~, linestyle='-- or :')
```

* 마커 모양 바꾸기

```python
# 빨간색 원형 마커 그래프
plt.plot([데이터], 'r.')

# 초록색 삼각형 마커 그래프
plt.plot([데이터], 'g^')
```
