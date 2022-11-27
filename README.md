# 프로젝트 Build 과정

1. 환경 설정
  - Git 설치, Github 계정 생성
  - Github 계정에 <username>.github.io 로 repository 생성
  - Git clone을 통해서 로컬 저장소에 복사

<br>

2. jekyll 설치
  - 윈도우에서 jekyll을 사용하기 위해 ruby+Devkit 설치
  - ruby 터미널에서 "gem install jekyll bundler"를 통해 jekyll 설치
  - 로컬 저장소에 "bundle exec jekyll serve"를 통해 jekyll 기본 페이지 만들기
  - 원격 저장소에 수정사항 반영

<br>

3. 테마 설정
  - 여러 사이트에서 마음에 드는 테마 찾기
  - 원하는 테마를 다운로드 하기
  - 로컬 저장소에 붙여넣기
    + 의존성을 감안하여 테마 덮어쓰기
  - 원격 저장소에 수정사항 반영

<br>

4. 블로그에 글쓰기
  - _posts 폴더에 "YYYY-MM-DD-블로그-제목.markdown" 폴더 만들기
  - 맨 처음에 페이지 형식 작성 
      > \---<br>
      > layout: post<br>
      > title: "블로그 글 제목"<br>
      > date: YYYY-MM-DD HH:mm:ss +0900<br>
      > categories: 카테고리<br>
      > \---
  - 밑에 원하는 글 작성
  - 원격 저장소에 수정사항 반영

