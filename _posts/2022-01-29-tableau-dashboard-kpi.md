---
layout: post
permalink: /tableau-dashboard-kpi/
title: 'Tableau를 활용한 데이터시각화 2편'
date: 2022-01-29 14:00:00 +09:00
feature: '/img/posts/09/tablea-logo.png'
categories:
  - Solution
tags:
  - 태블로
  - tableau
  - 태블로공부하기
  - 데이터시각화
  - 태블로차트
  - kpi차트
  - kpi

description: '대시보드 : KPI 차트 그리기'
---

본 글에서는 데이터 시각화의 기본 구성 작업 방법 중, 대시보드 상단에 KPI를 표기하는 방법을 소개드리려고 합니다.

## <font color='dodgerblue'> 1. KPI란? </font>
먼저 <b>KPI</b>란 <b>Key Performance Indicator</b>의 약자로 <b>'핵심성과지표'</b>를 의미합니다. 각 비즈니스에서 개인 혹은 집단이 목표 달성을 위해 성과를 측정하는 기준이 되는 지표로, 보통 대시보드 상단에 위치시켜 한 눈에 성과의 흐름과 달성여부를 확인할 수 있게 제작합니다.

KPI 유형과 예 : [태블로에서의 KPI 추가 설명](https://www.tableau.com/ko-kr/learn/articles/types-and-examples-of-kpis)

## <font color='dodgerblue'> 2. KPI 차트 예시 </font>
아래 대시보드는 Workout Wednesday에 참여한 [Brad Werner](https://public.tableau.com/app/profile/brad.werner)라는 분께서 공유한 대시보드의 예시입니다. 필수 지표가 포함된 깔끔한 형태로 디자인되어 있는데요, 태블로 공식 블로그에도 소개되어 있는 것으로 보입니다.

출처 : [바로가기]([https://public.tableau.com/app/profile/brad.werner/viz/WOW2020-Week53Canyoubuildwithcontainers/WOW2020w53](https://public.tableau.com/app/profile/brad.werner/viz/WOW2020-Week53Canyoubuildwithcontainers/WOW2020w53))
![dashboardexample](/img/posts/11/01dashboardexample.png)

여기서 대시보드 상단에 숫자와 지표명으로 이루어진 KPI 박스를 만들어 보겠습니다.

## <font color='dodgerblue'> 3. KPI 박스 만들기 - 첫 번째 방법 </font>


#### 1) 측정값 이름을 열에 표시하기

: 데이터 테이블에서 대시보드의 KPI로 표시할 데이터를 설정하기 위해 ‘측정값 이름’을 ‘열’에 표기해줍니다.

![dashboard](/img/posts/11/02dashboard.png)

### 2) 측정값 이름, 숫자 표시하기

: #로 표시된 값은 측정 값입니다. '측정값 이름'에서 '측정값'을 드래그해 마크에 넣어주면 자동으로 각 지표의 수치가 표시됩니다.

여기서 파란색으로 표기된 ‘측정값 이름’은 차원 값이고, 초록색으로 표기된 ‘측정값’은 말 그대로 측정 값으로 각 지표의 값을 의미합니다.

둘 다 텍스트로 표기하기 위해 마크의 종류를 ‘T’ 텍스트로 지정하였습니다.

![03dashboard](/img/posts/11/03dashboard.png)

### 3) 필터를 통한 KPI 선택

: 위 이미지에서 표기된 모든 측정 값 중에서, 핵심지표를 선택합니다.

![04kpi](/img/posts/11/04kpi.png)

### 4) 표 서식 변경
: 그 다음 형태를 조금 다듬어 보겠습니다. 우선 머리 글 표시를 해제하여 중복 기재된 지표명을 삭제합니다. 그리고 마크에 표시된 순서를 바꿔 ‘측정값’이 먼저 보여지도록 합니다.

![05kpi](/img/posts/11/05kpi.png)

: 다음, 서식의 ‘필드’ 영역에서 ‘측정값’을 선택하고 모두 ‘가운데 정렬’로 변경해줍니다

![06kpi](/img/posts/11/06kpi.png)


### 5) 텍스트 서식 변경

: 금액을 나타내는 지표에 통화($) 표시를 해줍니다.

![07kpi](/img/posts/11/07kpi.png)

: 또한 ‘할인’을 나타내는 지표인 ‘Discount’에서 평균 할인율을 확인하기 위해 측정 값을 ‘평균’으로 변경해줍니다.

변경 완료 후, 수치를 %로 나타내기 위해 ‘서식’의 패널 기본값 표시 방법을 ‘퍼센트’로 변경해주면 됩니다.

![08kpi](/img/posts/11/08kpi.png)

: 마지막으로 텍스트 크기 조절위해, '텍스트'에서 레이블을 편집해줍니다. 저는 수치로 표현되는 '측정값'은 크게, 아래의 '측정값 이름'은 조금 작게 설정합니다.

![09kpi](/img/posts/11/09kpi.png)

### 6) 대시보드 적용 및 완성

: 완성된 워크시트를 대시보드에서 불러오면 아래와 같습니다. 추가로 색상, 배경 등을 넣으면 더 예쁘고 깔끔한 형태를 만들 수 있습니다.  

![10kpi](/img/posts/11/10kpi.png)

## <font color='dodgerblue'> 4. KPI 박스 만들기 - 두 번째 방법 </font>

: 추가로, 태블로의 챔피언 및 강사로 활동중이신 <b>진서연님</b> 강의에서는 더 깔끔한 대시보드를 위해 min(0)값으로 열에 섹터를 만들어 주는 방법을 소개해주셨습니다

1) 상단에 열을 클릭하여 min(0)으로 네 개의 박스와 마크를 만들어줍니다.

![11kpi](/img/posts/11/11kpi.png)

2) 열의 ‘축 편집’에 들어가 -1부터 1값으로 고정을 시켜줍니다.   
3) 각 마크에 측정값을 드래그하고 각 지표에 맞게 수식을 변경합니다.  
4) 위에서 다루었던 방식으로 지표의 속성을 변경하고 ‘라인 서식’에서 축을 모두 없애주면 깔끔히 정리됩니다.   
5) 그리고 서식에서 필터를 ‘월’ 기준으로 넣어주면 아래처럼 월별 KPI를 확인할 수 있습니다.

![12kpi](/img/posts/11/12kpi.gif)


## <font color='dodgerblue'> 5. 첫 번째 방법 + 두 번째 방법 </font>

첫 번째, 두 번째 워크시트를 하나의 대시보드에 합치면 아래처럼 적용됩니다. 기획하는 대시보드의 디자인에 맞추어 적용하면 될 것 같습니다.

![13kpi](/img/posts/11/13kpi.png)

그리고 여기서 더 디자인을 입힌다면 더 멋진 대시보드를 만들 수 있습니다.

대시보드 더 알아보기 :[링크 클릭](https://public.tableau.com/app/profile/yvette/viz/Transactions_16238484390810/Transactions)

![14kpi](/img/posts/11/14kpi.png)  
