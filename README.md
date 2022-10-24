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

## 팀 내 담당 주요 개발 사항
* Spring Framework를 이용한 백엔드 개발
  * MVC패턴 프로젝트 구축
  * 프로젝트에 필요한 백엔드 기능 구현
  
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
  * Kakao 로그인, 일반 로그인 회원 회원정보 테이블의 USERTYPE으로 구분

* 시험 과목 별 연습문제 게시판 구현
  * 시험 과목 코드 별 세션 분리
  * 연습문제 오답 시 해당 문제 ODNOTE(오답노트) 테이블에 자동 추가

## 기능 구현
* 시험장소 조회
  * 지역 선택 후 시험장소를 조회하면 Kakao Maps API를 통해 시험장소를 조회할 수 있습니다.
  
![자공자 시험장소조회](https://user-images.githubusercontent.com/105340836/197484075-6ae3f384-243e-41a1-b277-46294df121b6.gif)



* 연습문제 게시판
  * 시험 과목 별 연습문제를 출제, 풀어볼 수 있습니다.
  * 댓글, 추천 기능을 AJAX로 비동기 처리하여 구현하였습니다.
  * 연습문제 오답 시 해당 문제가 오답노트에 자동 추가됩니다

![자공자 문제](https://user-images.githubusercontent.com/105340836/197484136-70c166d8-fbac-42c0-9a56-a272a043f3f3.gif)

* Kakao 로그인/회원가입
  * Kakao Login API를 이용한 Kakao 로그인/회원가입 가능합니다.
  * 일반회원과 Kakao회원을 회원정보 테이블의 USERTYPE으로 구분하였습니다.
  
![자공자 카카오로그인](https://user-images.githubusercontent.com/105340836/197484726-d6df73f0-a42e-4a5b-9230-c33323a64482.gif)

## 개선 사항
* 비로그인 시에도 회원페이지, 비밀번호 변경 등 페이지 접근 가능한 문제 발생
  * Spring의 Interceptor 기능 활용하여 페이지 접근 권한 부여

* 게시판 추천 시 중복추천 가능한 문제 발생
  * DB에서 추천 테이블(BOARDLIKE)을 추가로 생성하여 게시판번호와 추천한 유저ID 저장, 조회 하여 중복 추천 방지





