# JAGONGJA (팀프로젝트, 인원 : 5, 기여도 : 90%, 2022.08 ~ 2022.09)

## 프로젝트 개요
국가기술자격시험을 준비하는 사람들에게 시험 일정, 장소 등의 정보를 제공해주고 사용자들이 과목 별 연습문제를 직접 출제, 풀어볼 수 있는 커뮤니티 사이트 입니다.  

## 기술스택
* 개발 환경
  * JAVA
  * Spring Framework
  * JavaScript
  * Oracle Database
  * MyBatis
  * JSP
  
* OPEN API
  * 공공데이터포탈 API
  * Kakao Login API
  * Kakao Maps API

## ERD
* JGJUSER : 회원정보 테이블
* WORKBOOK : 과목 별 연습문제(게시판) 테이블
* WBREPLY : WORKBOOK 댓글 테이블
* BOARDLIKE : WORKBOOK 추천 테이블 (유저아이디, 게시글번호로 중복추천제한)
* ODNOTE : 오답노트 테이블(WORKBOOK 문제 오답 시 자동 추가)
* EXLIST : 시험 과목 코드 테이블
* EXLOCATION2 : 시험 장소 테이블
![image](https://user-images.githubusercontent.com/105340836/197439949-3cb90d6f-db6d-4fca-847e-b51650f2ad53.png)

## 주요 개발 사함
* Spring Framework를 이용한 MVC패턴 백엔드 개발
  * 카테고리 별 게시판 구현
  * 회원가입, 로그인, 회원정보 변경 등 
  
* Oracle Database 이용한 DB 구축
  * DB 테이블 설계
  * MyBatis로 백엔드 서버와 연결 및 SQL Query 
  
* AJAX 이용한 프론트, 백엔드 비동기 통신
  * 댓글(작성, 삭제), 추천 기능 등 동적 처리
  * 비밀번호 확인, 사용자 정보 중복 확인
  * 시험장소 조회 시 데이터 전송

* Open API 이용한 시험 정보 제공
  * 공공데이터포탈 API 이용한 시험 정보(과목, 일정, 장소) 조회
  * Kakao Maps API 이용한 지역 별 시험장소 조회 기능 구현
  
* Kakao Login API 이용한 회원가입, 로그인 기능 구현
  * Kakao 로그인, 일반 로그인 회원 USERTYPE으로 구분

* 시험 과목 별 연습문제 게시판 구현
  * 시험 과목 코드 별 세션 분리
  * 연습문제 오답 시 해당 문제 ODNOTE(오답노트) 테이블에 자동 추가

## 기능 구현
* 게시판 작성 (음원 등록)
  * 아티스트와 음악제목을 검색하고 YOUTUBE URL을 추가합니다.

![addex](https://user-images.githubusercontent.com/105340836/197394642-5d45e98f-8d06-4aa1-aa69-052581656f5f.gif)

* 게시판
  * 게시판 작성 시 등록한 YOUTUBE URL과 YouTube Iframe Player API를 활용하여 음원을 재생할 수 있습니다.
  * 앨범 게시판의 경우 앨범 전체를 연속 재생할 수 있습니다. (트랙 종료 시 다음트랙 자동 재생)

![albumplayex](https://user-images.githubusercontent.com/105340836/197396080-1633a66d-a607-4fa4-aea6-bc3cf0e96711.gif)


