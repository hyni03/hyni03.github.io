---
layout: post
title: Git & Github 정리
subtitle: Git과 Github에 대한 간단한 정리글
author: hyni03
categories: Git
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
tags: Git Github
sidebar: []
comments: true
---

## Git

### 버전 관리 시스템(VCS)란?
: 파일 변화를 시간에 따라 기록했다가 나중에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템

- 로컬 버전 관리
- 중앙집중식 버전 관리
- 분산 버전 관리 -> **Git**

<br><br>

### Git 기본 용어
* Repository: Git으로 관리되는 파일이나 폴더들의 저장소

| Repository | Git으로 관리되는 파일이나 폴더들의 저장소 |
| ----- | ----- |
| Local Repository | - 본인의 컴퓨터에 저장된 로컬 저장소. 개인 전용 저장소 |
| Remote Repository | - 내 컴퓨터가 아닌 원격 서버에 저장되는 원격 저장소. 여러명과 공유하기 위한 저장소 |


* Clone : 원격 저장소를 로컬 저장소로 복제하는 것을 의미

<br><br>

### Git 저장소에서 파일의 상태
 
* Committed : 데이터가 로컬 저장소에 안전하게 저장된 상태
* Modified: 수정한 파일을 아직 로컬 저장소에 커밋하지 않은 상태
* Staged: 수정한 파일을 곧 커밋할 것이라 표시한 상태 <br>

![Git status](/image/Git%20status.png)

<br><br>

### Git의 저장

* Add
    >  현재 작업 폴더에서 수정한 파일이 있을 경우 **add**를 통해 staging area로 옮김

        git add .


* Commit
    > git add 명령어로 스테이지에 추가한 파일을 로컬 저장소에 저장

        git commit -m "커밋 메세지"


* Push
    > commit한 파일들을 원격 저장소에 저장 **(push하기 이전 꼭 add, commit을 해줘야 변경사항 저장됨)**

        git push

<br><br>

### Git의 Branch


<br>원래 코드와는 상관없이 독립적으로 개발을 진행할 수 있음

코드의 흐름을 분산시켜 더욱 효율적인 개발 가능! <br><br>

![Git Branch](/image/Git%20Branch.png)

<br>

* Branch 생성
    > git branch <branch 이름> 을 통해 branch 생성

        git branch <branch_name>


* Branch 전환
    > 현재 작업중인 branch 전환

        git checkout <branck_name>

* Branch 병합
    > 현재 작업중인 branch를 원하는 branch에 병합

        git merge <branch_name>

    * branch끼리 merge 중 같은 파일이 수정되었을 경우 merge conflict 발생. 
    * 이런 경우 수동으로 충돌이 일어난 부분을 merge 하면 정상적으로 branch 병합 가능

<br>

* Branch 삭제
    > git branch -d <branch 이름> 을 통해 branch 삭제
    
        git branch -d <branch_name>

<br><br>

## Github

### Github란?

* [깃허브(Github)](https://github.com/)


: 깃허브(Github)는 분산 버전 컨트롤 소프트웨어 **Git** 을 기반으로 소스 코드를 호스팅 하고, 협업 지원 기능들을 지원하는 Microsoft의 웹서비스로, 2020년 현재 가장 인기 있는 소스 코드 호스팅 서비스이자 소프트웨어 개발 플랫폼

<br>

> 깃허브(Github)의 로고
![Github Logo](/image/Github%20Logo.png)

<br><br>

### Github의 플랜과 요금

* 개인용 플랜: 무료 플랜(Free)와 프로 플랜(Pro)
    - 무료 플랜(Free)
        + 깃허브 액션 시간 (2000분/월), 패키지 스토리지 500MB 제공
        +  협업자 수의 제한과 일부 기능 제약이 있는 비공개 저장소
    - 프로 플랜(Pro)
        + 깃허브 액션 시간 (3000분/월), 패키지 스토리지 1GB
        + 제약없는 비공개 저장소

<br>

* 팀용 플랜: 팀 플랜(Team)과 엔터프라이즈 플랜(Enterprise)
    - 팀 플랜(Team)
        + Organization을 만들고, 이 아래에 저장소를 관리하는 방식
        + 다수의 팀을 만들고 관리할 수 있는 기능과 추가적인 협업 기능이 제공
    - 엔터프라이즈 플랜(Enterprise)
        + 다수의 Organization을 관리해야하는 경우 사용
        + 감사 로그, 싱글 사인온, LDAP 인증과 같은 기능을 추가적으로 제공

<br>

* 무료 지원

    - 깃허브에서는 오픈소스와 교육, 비영리 단체에 대한 지원을 하고 있음 - [요금 페이지](https://github.com/pricing) 참고<br><br>
    ![Github support](/image/Github%20support.png)

<br><br>


### 저장소(Repository)

* 깃허브의 핵심 기능은 **Git** 원격 저장소 호스팅<br>
* 깃허브를 통해 로컬 개발 환경과 온라인에서 안전하게 깃 저장소에 접근 가능 <br>
* 단순히 깃 저장소를 원격에서 호스팅할 뿐만 아니라, 이슈 트랙커, 풀리퀘스트, 소스코드 탐색, 위키, 인사이트 등의 기능을 제공

    - *무료 플랜의 경우 프라이빗 저장소에서는 위키, 인사이트, 깃허브 페이지 기능을 사용할 수 없습니다.*

![Github Repository](/image/Github%20Repository.png)

<br><br>

### 참고 사이트

* [깃허브(GitHub)의 공식 블로그](https://github.blog/)
* [깃허브(GitHub)의 공식 문서 - GitHub Help](https://docs.github.com/en)
* [깃허브(GitHub)의 공식 유튜브](https://www.youtube.com/@GitHub)





