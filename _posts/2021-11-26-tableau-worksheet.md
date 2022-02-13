---
layout: post
permalink: /tableau-worksheet/
title: 'Tableau를 활용한 데이터시각화 1편'
date: 2021-11-26 10:00:00 +09:00
feature: '/img/posts/09/tablea-logo.png'
categories:
  - Solution
tags:
  - 태블로
  - tableau
  - 태블로시트
  - 데이터시각화
description: 'Worksheet 살펴보기 : 데이터 연결, 기본 차트 그리기'
---

<strong>Tableau Desktop</strong>은 태블로에서 제공하는 솔루션 중에서도 <strong>Data visualization</strong>기능을 제공합니다. 참고로 얼마 전부터 <strong>Tableau Public</strong>이라는 서비스 제공이 시작되면서, 웹 환경에 제한되지만 무료로 서비스를 체험할 수 기회가 생겼습니다.

다만 Tableau Desktop과 비교했을 때, Tableau Public에서 제작된 자료는 웹 환경에만 저장 가능하고 데이터 연결에 제한이 있습니다. 만약 데이터 연결의 자동화 및 추후 대시보드를 구축하고자 한다면 유료버전의 Tableau Desktop 사용을 추천드립니다.

우선 아래 경로로 Tableau Public(태블로 퍼블릭)을 시작할 수 있습니다.  
[Tableau Public 다운로드 바로가기](https://www.notion.so/Desktop-Worksheet-5d77b5d6b7924d7fb5ac1981c8ec8909#c6b3cc45e4b94ace8fb31aac8bc394e6)

----

본 글에서는 데이터 예제를 활용해 태블로 데이터 시각화 기능을 제공하는 <strong>Worksheet</strong>를 탐색해 보려고 합니다. 실제 업무에서는 비즈니스 데이터를 사용하지만, 본 글에서는 Kaggle이라는 데이터 공유 사이트에서 다운받은 예제를 활용하였습니다.

활용한 데이터 출처는 아래와 같습니다.  
[데이터 출처: 'Netflix Movies and TV Shows' ](https://www.kaggle.com/shivamb/netflix-shows)

## 1. 데이터 연결하기
Tableau Desktop에선 파일로 데이터를 불러오거나 서버 연결을 통해 데이터를 자동으로 불러올 수 있습니다. 본 글에서는 위 링크에서 다운 받은 엑셀 파일을 열어보도록 하겠습니다.

![tableau image01](/img/posts/09/image01.png)

 먼저 엑셀파일을 살펴보면, ***'Netflix_titles, directors, countries,'*** 등 여러개의 엑셀시트가 존재하는데요. 각 시트마다 콘텐츠를 구분하는 고유키 값인  'show_id'값이 포함되어있습니다.


![tableau image02](/img/posts/09/image02.png)

여기서 Show id 값을 기준으로 각 시트를 연결합니다.   SQL로 연결하면 join 등을 활용해 데이터를 하나씩 붙여야 하지만, 태블로에선 key값을 기준으로 아래처럼 자동으로 데이터간의 관계(Relation)를 형성해줍니다.

![tableau image03](/img/posts/09/image03.png)

## 2. Dimension & Measured Value 확인하기
Data Source에서 데이터 연결을 완료했다면 실제로 Sheet를 열어 조회할 데이터들이 잘 준비되었는지 확인합니다.

준비된 데이터는 왼쪽 Tables에서 확인 가능하며, 보통 파란색으로 표기되는 값들은 차원 값이고, 초록색 #로 표기된 부분은 측정 값으로 활용됩니다.

![tableau image04](/img/posts/09/image04.png)

만약 여기서 추가로 계산하고 싶은 값이 있을 땐, 측정 값들을 연산하여 추가하는 부분도 가능한데요. 이 부분은 별도의 글에서 공부해보도록 하겠습니다.

## 3. 간단한 라인 그래프 그리기
여기까지 모든 데이터 세팅이 완료되었다면 간단한 라인 그래프를 그려보도록 하겠습니다.

연도별 콘텐츠 등록수를 확인하기 위해 Columns에는 Year data, Row에는 콘텐츠 등록 개수를 넣어주면 아래와 같이 간단한 라인 그래프가 그려집니다.

![tableau gif0103](/img/posts/09/0103.gif)

간단한 드래그로 순식간에 그래프가 그려지는 것을 볼 수 있습니다.

## 4. 마크카드 살펴보기
태블로의 편리함을 가장 많이 느끼는 순간은 왼쪽에 보이는 Marks(마크카드)를 활용할 때입니다.

마크카드에서 제공되는 기능은 엑셀에 그래프를 그리면 뜨는 ***'차트 속성'*** 을 압축시켜 놓았다고 생각하시면 됩니다. 엑셀은 하나씩 차트를 선택해 그래프 모양, 색, 종류, 데이터 레이블 등을 변경할 수 있도록 제공한다면 태블로에서는 몇 번의 클릭 만으로도 쉽게 데이터의 형태를 변경할 수 있습니다.

![tableau image05](/img/posts/09/image05.png)

물론 태블로는 편리함과 신속성의 Benefit 뿐 아니라, Customized 기능으로 상세한 설정도 가능하게 도와줍니다. 특히, 데이터 레이블 기능에서 ***데이터의 가운데 정렬, 최소값 최빈값 표기, 하이라이트 등*** 을 빠르게 적용할 수 있으며, 사용자가 직접 설정하는 것도 가능합니다.

![tableau image06](/img/posts/09/image06.png)

## 5. Map 그래프
이번엔 '국가별 등록 콘텐츠 수' 확인을 위해 맵 그래프를 생성해보겠습니다.

아래처럼 Country 데이터를 시트로 드래그 해주면 지도가 생성되는데요, Country라는 데이터 속성이 국가를 의미한다는 것을 태블로가 인식하여, 태블로에 내장된 지도 이미지를 불러오는 구조입니다.

![tableau gif0104](/img/posts/09/0104.gif)

그리고 왼쪽에 '국가별 콘텐츠 수'를 Label에 드래그하면, 국가별 콘텐츠 개수가 숫자로 표기됩니다. 한국은 162개의 콘텐츠가 등록된 것으로 조회되네요. (참고로 데이터의 정확성은 검증되지 않았습니다.^^)

![tableau image07](/img/posts/09/image07.png)

가독성을 높이기 위해 필터를 설정하면 오른쪽에서 필터의 국가명을 클릭할 때마다 '선택한 국가의 콘텐츠 등록 수'를 조회할 수 있습니다.

![tableau image08](/img/posts/09/image08.png)

## 6. 분석 기능 살피기
태블로에서는 데이터 시각화에서 더 나아가 간단한 '분석 모델'까지 지원합니다. 분석 도구는 왼쪽의 Analytics 창에서 확인할 수 있으며 간단한 총계, 평균 계산 뿐 아니라 Trend와 Forecast 데이터도 제공합니다.

아래는 장르별 등록 콘텐츠의 수를 나타낸 그래프입니다. 여기서 전체 장르의 평균 데이터를 아래처럼 추세선을 넣어 조회할 수 있습니다

![tableau gif0105](/img/posts/09/0105.gif)

---

금번 글에서는 태블로에서 지원하는 기능들을 훑어보는 방식으로 살펴보았습니다. 이렇게 생성된 Sheet들이 모여 태블로의 대시보드가 만들어지게 되는데요. 다음 글에서는 간단한 디지털 마케팅 대시보드 생성 과정을 소개해 보도록 하겠습니다.
