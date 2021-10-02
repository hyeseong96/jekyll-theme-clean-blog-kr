---
layout: post
permalink: /adobe-analytics-report/
title: 'Adobe Analytics에서 쉽고 빠르게 대시보드 만들기'
date: 2021-10-02 10:00:00 +09:00
feature: '/img/posts/08/adobeanalyticslogo.png'
categories:
  - Solution
tags:
  - 어도비애널리틱스
  - 어도비
  - 애널리틱스
  - AdobeAnalytics
description: '어도비애널리틱스(Adobe Analytics)의 Workspace 구성'
---

본 글에서는 구글 애널리틱스와 함께 웹/모바일 분석 솔루션으로 많이 활용되는 <strong>어도비 애널리틱스 (Adobe Analytics)</strong>의 <strong>Workspace 기능</strong>을 살펴보고자 합니다.

### 어도비애널리틱스 구성
어도비 애널리틱스에 접속하면 상단 메뉴의 'Reports'과 'Workspace'에서 수집된 데이터의 결과를 확인할 수 있습니다.

Report 탭에서는 '권장 보고서'와 '실시간 보고서'를 통해 기본지표의 성과를 쉽고 빠르게 확인할 수 있는 장점이 있습니다. 그러나 오늘 살펴볼 Workspace에서는 수집된 데이터를 자유롭게 드래그하여 나만의 대시보드를 구성할 수 있습니다.


### Workspace 구성
Workspace에서 프로젝트를 생성하면 아래처럼 수집된 데이터가 각각 Dimensions, Metrics, Segments로 분류되어 있습니다. 각 components를 드래그&드롭하여 쉽고 빠르게 대시보드를 구축할 수 있습니다.

![workspace](/img/posts/08/workspace01.png)

각 구성들을 간단히 설명하자면,
<ul>
<li>Dimensions : 측정 기준을 의미합니다. 문자형태로 row에 표시됩니다. </li>
<li>Metrics : Dimensions 의 측정값입니다. 숫자 형태로 column에 표시됩니다.</li>
<li>Segmentation : 리포트에서 특정 기준으로 결과 값을 세분화하는 설정입니다.</li>
</ul>

각 구성들이 반영된 모습은 아래와 같습니다.

![workspace02](/img/posts/08/workspace02.png)

이 밖의 자세한 설명은 [어도비애널리틱스 블로그](https://experienceleague.adobe.com/docs/analytics/components/home.html?lang=ko)를 참고해주세요!

### Workspace의 장점 : 직관성과 단순함

 Workspace의 기능은 쉽고 직관적이라 어도비 애널리틱스를 처음 접하시는 분들도 몇번의 클릭만으로 쉽게 대시보드를 생성할 수 있습니다.

위에서 언급한 것처럼 정리된 지표를 드래그앤 드롭하여 대시보드를 구축할 수 있고, 10가지 템플릿을 활용해 분석 목적에 맞는 차트를 생성할 수 있습니다.

추가로 생성해둔 대시보드에서 deep-dive한 분석이 필요할 경우, 숫자를 쪼개고 그래프를 그리는 등의 작업을 몇번의 클릭만으로 수행할 수 있습니다.

### 자주 활용하는 Workspace 기능들

Workspace에서는 아래 10가지 Panel을 통해 이용자가 쉽고 빠르게 대시보드를 생성할 수 있도록 돕습니다. 여기서 제가 자주 활용하는 몇가지 기능만 소개드리려고 합니다.

![workspace03](/img/posts/08/workspace03.png)

#### 1) Freeform table
가장 많이 활용되는 표 형식의 기본 템플릿입니다. 측정 기준의 값들을 표 형식으로 볼 수 있고 각 지표를 세분화하며 추가 인사이트를 얻을 수 있습니다.

출처: 어도비애널리틱스 블로그
![workspace04](/img/posts/08/workspace04.png)

이 기능의 가장 편리한 점은 데이터의 트렌드를 마우스 오른쪽 클릭으로 쉽게 시각화하여 확인할 수 있다는 점입니다. 저의 경우, 웹사이트 분석의 기본 지표인 '페이지뷰, 방문수, 이탈율, 체류시간'을 weekly 지표로 확인하고 있습니다.

![workspace05](/img/posts/08/workspace05.png)

#### 2) Flow chart
홈페이지 방문자의 흐름을 분석할 수 있는 차트입니다. 저의 경우, referring domain과 paid 광고의 유입에 따른 방문자의 이동경로와 이탈을 분석하는 용도로 활용합니다. 아래처럼 왼쪽의 Dimensions을 drag하여 오른쪽에 추가하면서 분석의 깊이를 더해갈 수 있습니다.

![workspace06](/img/posts/08/workspace06.png)

#### 3) Cohort chart
홈페이지 방문자의 재방문을 파악할 때 활용하고 있습니다. 저희 홈페이지는 고관여 제품의 정보 제공 목적으로 운영되어, 프로모션 중인 캠페인별 홈페이지 재방문 빈도를 주로 체크하고 있습니다.

만약 웹사이트에 특정 이벤트가 있거나 고객정보를 수집할 수 있다면 본 차트를 더 심도있게 활용할 수 있을 것 같습니다.

![workspace07](/img/posts/08/workspace07.png)

#### 4) Fallout Report
Touch point를 지정하여 방문자의 트래픽 플로우를 파악하는 작업에 유용합니다. 예를들어 방문자별 이벤트 발생, 장바구니 추가, 구매 등의 플로우를 파악할 때 많이 사용될 것으로 보입니다.

저의 경우, paid 광고를 통한 유입 지표의 daily 트렌드를 파악하고 데이터가 튀는 일자에만 자세히 살펴 보고 있습니다.

![workspace08](/img/posts/08/workspace08.png)

이 밖에도 'Quick insight'통해 쉽게 기본 대시보드를 구축하거나 'Segment comparison'으로 지정한 방문자를 분석할 수 있으며 'Map'으로 지역 정보를 활용한 차트를 만들 수 있습니다.

### Workspace에서 제공하는 차트 활용하기

어도비 애널리틱스는 모든 데이터를 쉽게 차트로 만들 수 있습니다. 어도비의 가이드에 따라 제공되는 차트를 각 목적에 맞도록 사용하실 것을 권장드립니다!

![charts](/img/posts/08/charts.png)

### 어도비 애널리틱스 사용 후기

저는 어도비 애널리틱스를 처음 접했지만 쉽고 직관적인 인터페이스 덕분에 하나씩 기능들을 클릭해보면서 사용법을 배워나가고 있습니다.

국내에서는 구글 애널리틱스보다 대중적인 솔루션이 아니라서 정보가 제한적인 단점은 있습니다. 특히 솔루션의 기능을 100% 활용하지 못하는 느낌이 드는 경우가 있는데요.

 저처럼 솔루션 활용에 추가 정보가 필요하신 분들 아래 어도비 애널리틱스를 방문해 업데이트 사항과 정보를 주기적으로 확인해보실 것을 권장드립니다.

 [어도비 애널리틱스 툴 안내 바로가기](https://experienceleague.adobe.com/docs/analytics/analyze/home.html?lang=ko)
