---
layout: post
permalink: /python/
title: '파이썬 독학하기 - 데이터 시각화'
date: 2022-06-12 17:00:00 +09:00
feature: '/img/posts/13/title.jpg'
categories:
  - Data
tags:
  - 파이썬
  - Matplotlib
  - 파이썬독학
  - 데이터시각화


description: 'Mataplotlib 활용한 데이터 시각화'
---

평소 관심있던 <strong>데이터 시각화 분야를 파이썬(Python)</strong>을 개인적으로 공부하고 있습니다.

금번 글은 웹 브라우저에서 파이썬 소스 코드를 편집할 수 있는 <strong>주피터 노트북(Jupyter Notebook)</strong>을 활용하여, 혼자 공부했던 기본적인 사항들을 정리해보도록 하겠습니다.

## 1. Matplotlib(맷플롯리브)  
파이썬을 활용한 데이터 분석 시, 가장 기본적으로 활용되는 패키지입니다. 본 패키지를 활용해 다양한 형태의 차트를 그릴 수 있고 PDF,SVG,PNG 등 다양한 형식으로 그래프 파일을 저장할 수 있다고 합니다.

맷플롯리브로 그릴 수 있는 그래프의 예제는 아래 링크에서 확인할 수 있습니다.

[▶ Mataplotlib Documentation 바로가기](https://matplotlib.org/stable/gallery/index.html)

Matplotlib는 주로 plt의 이름으로 import 합니다.
```python
import matplotlib.pyplot as plt
```
## 2. 선 그래프 그리기
가장 기본적인 라인 그래프 먼저 그려보겠습니다. 서브패키지의 plot 명령을 사용해 호출하며, X축 Y축의 값을 넣으면 아래와 같이 그래프가 그려집니다.

```python
#그래프이름 지정 및 표기
plt.title('Graph example')
x = [1,2,3,4,5]
y = [1,4,8,16,32]
plt.plot(x,y)
```
![02](/img/posts/13/20220612_02.png)

여기서 그래프 서식을 다양하게 활용하려면 <strong>한글 폰트 설정, 폰트 사이즈 조정, 마이너스 기호 설정</strong>이 필요합니다. 여기선 간단히만 소개드립니다. 실제로 아래 내용 외에도 여러가지 방법으로 설정할 수 있으니 검색하여 확인해보시길 바랍니다.

```python
#나눔바른고딕의 한글폰트 설정
matplotlib.rcParams['font.family'] = 'NanumBarunGothic'
#폰트사이즈 조정
matplotlib.rcParams['font.size'] = 12
#마이너스 기호 인식
matplotlib.rcParams['axes.unicode_minus'] = False
```
![03](/img/posts/13/20220612_03.png)

## 3. 그래프 스타일 적용
추가로 그래프의 스타일을 지정 하겠습니다. 약자로 표기된 내용은 아래 링크에서 상세히 보실 수 있습니다. 예제의 출처도 링크에서 확인할 수 있습니다.

- color (c) : 선 색깔
- linewidth (lw) : 선 굵기
- linestyle (ls) : 선 스타일
- marker : 마커 종류
- markersize (ms) : 마커 크기
- markeredgecolor (mec) : 마커 선 색깔
- markeredgewidth (mew) : 마커 선 굵기

```python
plt.title('그래프 예제')
plt.plot([10, 20, 30, 40], [1, 4, 9, 16],
         c='b', lw=5, ls=':', marker='o', ms=10, mec='yellow', mew=3, mfc='r')
plt.xlim(0, 50)
plt.ylim(-10, 30)
plt.show()
```
![04](/img/posts/13/20220612_04.png)
[▶ 출처 바로가기](https://matplotlib.org/stable/gallery/index.html)

## 4. 그래프 응용
이번엔 동일한 값으로 3가지 형태의 그래프를 그려보도록 하겠습니다.
우선 a,b,c의 값을 각각 지정해주고 그래프에 표기해줍니다.

여기서 활용된 DataFrame의 plot 인자 몇가지만 소개드리겠습니다.

- subplots : 각 DataFrame의 Column을 별개의 그래프에 그림
- sharey : True인 경우 Y축 공유 (참고로, sharey : False인 경우는 X축을 공유함)
- figsize : 그래프의 크기 지정

```python
fig, axs = plt.subplots(1, 3, figsize=(9, 3), sharey=True)
axs[0].bar(names, values)
axs[1].scatter(names, values)
axs[2].plot(names, values)
fig.suptitle('abc 그래프')
```
![05](/img/posts/13/abc.png)

이렇게 위와같이 Y축을 공유하는 3가지 형태의 그래프를 그릴 수 있습니다.

---

Matplotlib를 활용하여 그릴 수 있는 그래프는 매우 다양합니다. 저는 아직 기초를 공부하는 단계라서 금번 글에는 기본적인 내용만을 담았지만 앞으로 조금씩 다양한 형태의 그래프를 그려보며 발전해 나가고자 합니다.  
