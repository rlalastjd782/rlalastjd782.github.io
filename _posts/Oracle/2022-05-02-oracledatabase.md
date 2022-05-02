---
title:  "Window10 Oracle database 오류"
excerpt : "Oracle database 오류시 설정방법"

categories:
  - Oracle
tags:
  - Oracle

toc: true
toc_sticky: true
 
date: 2022-05-02
last_modified_at: 2022-05-02
---

# Window10 Oracle database 오류

- Oracle 설치 시에 database 오류가  나는 상황에서 실행하면 된다.
- 연습 도서는 ‘오라클 SQL 과 PL/SQL을 다루는 기술. 길벗, 홍형경’  도서를 참고하였다

# Database Configuration Assistant

- 처음 오라클을 설치하게 되면 해당 앱이 같이 설치된다
    - 해당 앱을 실행한다.

![Untitled](https://user-images.githubusercontent.com/101306770/166200291-d2e00284-ae23-44e7-958a-ce2631a40b08.png)

- 데이터 베이스 생성

![Untitled 1](https://user-images.githubusercontent.com/101306770/166200303-f908b612-cb8c-4595-a993-5df5a86e1937.png)
- 데이터 베이스 이름은 현재 공부하고 있는 책 내용 대로 하였다.
    - 데이터 베이스 이름 : myoracle
    - 비밀번호 1234
- 컨테이너 데이터 베이스 생성 해제


![Untitled 2](https://user-images.githubusercontent.com/101306770/166200310-0bb834b2-f7ec-48ee-a3bf-a4864f581ea6.png)

- 비밀번호 오류는 무시한다
- 다음을 눌러 쭉 진행한다.
- 완료가 되었으면 확인 작업을 한다.
- sql plus 실행

![Untitled 3](https://user-images.githubusercontent.com/101306770/166200312-3eb4776f-fed6-42c5-9b32-a4aad273a440.png)
- 사용자명 : system
- 비밀번호 : 1234

![Untitled 4](https://user-images.githubusercontent.com/101306770/166200321-da0d6634-1d2c-438d-9963-9aef7829efbd.png)

- 해당 문구가 나오면 완성이다!