---
title:  "Oracle 19c 설치하기 1 "
excerpt : "Oracle을 설치한다."

categories:
  - Oracle
tags:
  - Oracle

toc: true
toc_sticky: true
 
date: 2022-04-28
last_modified_at: 2022-04-28
---

# Window10 Oracle 설치하기

- 공부를 위한 설치로 실제로 쓰는 것과 다를 수 있다.
- 19c 버전으로 설치했다.

- C 드라이브에 폴더를   만들어서 설치(오류방지)
    - 필자는 sql_lecture의 폴더를 만들어서 설치했다.

![Untitled](https://user-images.githubusercontent.com/101306770/165666202-6602223d-ca0f-4dee-95f0-ce736edfa5bb.png)

- 해당 홈페이지에서 오라클을 다운받는다.
    - [https://www.oracle.com/kr/database/technologies/oracle-database-software-downloads.html#19c](https://www.oracle.com/kr/database/technologies/oracle-database-software-downloads.html#19c)
    - 각 pc 에 맞는 버전으로 다운로드 받는다.
    
   ![Untitled 1](https://user-images.githubusercontent.com/101306770/165666207-6b64dc26-0e56-4263-8cba-b6a544071c85.png)
    
- zip 파일을 위에서 만든 sql_lecture로 옮겨 압축을 해제한다.

![Untitled 2](https://user-images.githubusercontent.com/101306770/165666225-340ba2e3-30f0-455a-959a-3e4ed40ac951.png)


- 해제 후 WINDOWS.X64_193000_db_home의 폴더로 들어가 setup 클릭

![Untitled 3](https://user-images.githubusercontent.com/101306770/165666214-411c17ab-31f3-49ed-93dd-6446a0b1f940.png)

- 아래와 같은 화면이 나온다.
    - 단일 인스턴스 데이터베이스 생성 및 구성을 누른 후 다음을 누른다

![Untitled 4](https://user-images.githubusercontent.com/101306770/165666246-955dec78-ab0d-4ccc-b173-7300ae57ab38.png)

- 현재 우리는 연습이기 때문에 데스크톱 클래스로 설정한다.

![Untitled 5](https://user-images.githubusercontent.com/101306770/165666252-89909bf5-20a7-49b4-9057-6ceb70e412e4.png)

- 가상 계정 사용
    - 계정은 가상계정을 이용한다.

![Untitled 6](https://user-images.githubusercontent.com/101306770/165666257-5889cfda-9153-4ada-89f2-f44abefd757f.png)

- orcle base의 폴더를 위에서 만든 폴더로 바꿔준다.
    - 전역데이터 베이스이름은 myoracle로 해줫다.
    - 비밀번호는 편의상 1234 로한다.
    - 문자집합은 유니코드로 설정했다.
    - 컨테이너 데이터 베이스는 생성 해제로 하였다
        - 비밀번호가 오류라고 나올수있다. 하지만 무시하여도 된다.

![Untitled 7](https://user-images.githubusercontent.com/101306770/165666283-50c65892-fc5c-43e0-b419-bd0346082844.png)

- 다음을 눌러 설치를 진행한다.

![Untitled 8](https://user-images.githubusercontent.com/101306770/165666289-29b2f932-fa7e-4e98-9c14-9d3a2ff302f0.png)

- 메모리 크기 등 설치 환경 검사가 수행 된다.
- 설치가 가능하면 아래와 같은 화면이 나온다.
    - 설치를 눌러 설치 진행.

![Untitled 9](https://user-images.githubusercontent.com/101306770/165666294-ef7db27c-b233-4347-8818-359db1cb0ae7.png)

- 설치를 하게 되면 아래화면 처럼 나오게 된다.
    - 현재 설치 진행 상태를 확인 할 수 있다.

![Untitled 10](https://user-images.githubusercontent.com/101306770/165666301-1b746a55-8675-40df-874a-ff8728296f81.png)

- 설치 완료 후 닫기.

![Untitled 11](https://user-images.githubusercontent.com/101306770/165666309-76741502-65ba-426d-ab3d-0fb11aec20ce.png)

- 설치가 완료되었다.
- 설치 도중 아래와 같은 오류가 발생 할 수 있다.

![Untitled 12](https://user-images.githubusercontent.com/101306770/165666311-d614dde1-f80b-4c85-9655-843d49c95361.png)


- 위와 같은 오류에 대해서는 다음 게시물에서 다루도록 하겠다.! 끝!