---
layout: post
title: gitblog에 Google analytics 설정하기
subtitle: google analytics를 Github 홈페이지에 적용하는 방법에 대한 설명글
author: hyni03
categories: analytics
banner:
  video: https://vjs.zencdn.net/v/oceans.mp4
  loop: true
  volume: 0
  start_at: 8.5
  image: https://bit.ly/3xTmdUP
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: Github Google Analytics
sidebar: []
comments: true
---

## Google Analytics란?
: 구글에서 무료로 제공하고 있는 웹분석 서비스

<br><br><br>

## Google analytics 설정하기

<br>

### **1. Google analytics 계정 생성**

[google anayltics 바로가기](https://analytics.google.com)

<br>

1.사이트에 접속하여 측정 시작 누르기

> ![1-1. 측정 시작](/image/1-1.%20%EC%B8%A1%EC%A0%95%20%EC%8B%9C%EC%9E%91.png)

<br><br>

2-1. 계정 설정하기

> ![1-2.계정 설정](/image/1-2.%20%EA%B3%84%EC%A1%8D%20%EC%84%B8%EB%B6%80%20%EC%A0%95%EB%B3%B4.png)

<br>
개인 이름 설정하기 (직접적인 영향은 없다)


<br><br>

2-2. 속성 설정하기

> ![1-3.속성 설정](/image/1-3.%20%EC%86%8D%EC%84%B1%20%EC%84%A4%EC%A0%95.png)

속성 이름에 블로그 주소와 시간대를 **대한민국**, 통화는 **대한민국** **원**으로 설정

<br>

2-3. 비지니스 정보는 필요에 따라 설정(건너뛰어도 된다) 후 만들기 

<br><br><br>

### **2. 블로그와 연결 및 측정ID 확인**

<br>

1.analytics 계정과 블로그 연결

데이터 스트림에 들어가 웹 선택
> ![1-4. 블로그와 연결](/image/1-4.%20%EC%9B%B9%20%EC%84%A0%ED%83%9D.png)

<br>


블로그 주소와 이름 작성하기
> ![1-5. 블로그와 연결](/image/1-5.%20%EB%B8%94%EB%A1%9C%EA%B7%B8%20%EC%A3%BC%EC%86%8C%20%EC%9E%85%EB%A0%A5.png)

<br><br>

2.측정 ID 확인하기

> ![1-6. 측정 ID](/image/1-6.%20%EC%B8%A1%EC%A0%95%20ID.png)

**측정ID는 코드 작성 시 필요하므로 기억해두기**

<br><br><br>

### **3. 코드 수정하기**

<br>

1.태그 설치하기

analytics 기능을 사용하기 위해 태그 설치가 필요
데이터 스트림에서 **태그 안내 보기** 선택 후 **직접 설치** 클릭. 코드 복사하기

> ![1-7. 태그 설치](/image/1-7.%20%ED%83%9C%EA%B7%B8%20%EC%84%A4%EC%B9%98.png)

<br><br>

복사한 코드를 /_includes 폴더안에 analytics.html 파일을 생성하여 붙여넣기

> ![1-8. analytics](/image/1-8.%20analytics.png)

<br><br>

2.default 파일 수정
<br>
_layouts 폴더에 있는 default.html의 body 맨 마지막에 다음 코드 추가
```html
{% include analytics.html %}
```

<br>

3.config.yml 수정하기
<br>
config.yml에 다음 코드 추가하기
```sh
# Analytics
analytics:
  provider: "google-gtag"
  google:
    tracking_id: "측정ID"
```

<br><br><br>

### **4. 측정 확인하기**

<br>

위에 과정들을 다 완료하면 블로그와 analytics가 정상적으로 연결됐을 것입니다.
다시 analytics에 접속해보면 방문자 수가 카운팅됩니다.

> ![1-9. 측정 완료](/image/1-9.%20%EC%B8%A1%EC%A0%95%20%EC%99%84%EB%A3%8C.png)