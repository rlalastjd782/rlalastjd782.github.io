---
title:  "JAVA 설치하기"
excerpt : "JAVA를 설치한다."

categories:
  - Java
tags:
  - Java

toc: true
toc_sticky: true
 
date: 2022-04-25
last_modified_at: 2022-05-04
---

# JAVA 설치

- JAVA install
    - 8버전 설치시에 주의점
    - 꼭 윈도우에 jdk jre 파일 만둔 후 진행
    - 이유 : 경로에 공란이 있을 경우 어떤 문제가 벌어질지 모르기때문에 문제를 아예 제외하는것임
    - 경로에는 꼭 영어로된 경로만 있을 것 
    - 경로중에 공란이있다면 새로운 폴더를 만들어 진행한다.
    - 자바 다운로드시 오라클에 회원가입을 해야 할 수도 있음을 명시한다.
    - 어디까지나 참고용 자료이다.
    


- C 드라이브에 jdk 및 jre 폴더를 만든다

![image](https://user-images.githubusercontent.com/101306770/166612304-83193422-2194-4f12-b8af-c8968f743713.png)

![image](https://user-images.githubusercontent.com/101306770/166612212-5d034a21-9fd7-4370-9b45-ff5236275da3.png)


- goole 검색에 java development kit 검색
![image](https://user-images.githubusercontent.com/101306770/166612386-dc1e0911-9b7b-4c61-9b73-4ffad3bcb338.png)

- java downloads 를 클릭하게 되면 아래와 같은 페이지가 나온다

![image](https://user-images.githubusercontent.com/101306770/166612441-6407f432-5fbf-40fe-aeb0-d74ae70ddbc2.png)


- 필요한 버전을 다운로드한다.
- 다운로드시 오라클 회원가입을 해야 할수도 있다.
- 윈도우 64bit 에서는 x64로 된 프로그램을 설치한다.(32비트는 x86으로 설치하면된다.)

![Untitled](https://user-images.githubusercontent.com/101306770/165013777-929e9017-6c5d-4edc-821e-2790a274f636.png)


- 설치 시에 주의 해야 한다. 경로에 공백이 있을 경우 문제가 있을 수 있기 때문에 설치과정에서 경로를 재 설정 해준다.
- 기존의 경로는 아래 경로 처럼 되어 있을 것 이다.

![Untitled 1](https://user-images.githubusercontent.com/101306770/165013816-a52892b9-911b-42ce-830b-e68a0df43bac.png)


- 경로 옆에 있는 change를 눌러 경로를 아래와 같이 변경해준다.

![Untitled 2](https://user-images.githubusercontent.com/101306770/165023390-f6b0d249-037c-4971-a599-6027afcad7b8.png)


- 자바 런타임 환경의 폴더도 동일하게 변경해준다.

![Untitled 3](https://user-images.githubusercontent.com/101306770/165023444-588c9782-f7a5-4b03-8d85-59c514bed9bd.png)


- 똑같이 변경 버튼을 누르고 C드라이브 안에  jre 폴더를 생성하여 바꿔준다.
- 시스템 환경 변수 설정
    - 처음 자바를 시작할 때에 시스템 환경 변수를 설정한다.
    - 윈도우 검색 → 시스템 환경 변수 설정
    
    ![Untitled 4](https://user-images.githubusercontent.com/101306770/165023475-d29c89fd-d85f-4222-b3b4-fbfbd169d266.png)
    - 환경변수(N) 클릭
    
    ![Untitled 5](https://user-images.githubusercontent.com/101306770/165023495-0bdcb74e-892a-41e7-bc2e-d0fce04a9787.png)

    - 현재 우리는 사용자로 설정할 것이기 때문에 사용자 변수에 추가해준다
    
    ![Untitled 6](https://user-images.githubusercontent.com/101306770/165023538-23fc2c21-994b-4112-a7ac-a5327ce24a75.png)
    
    - 사용자 변수를 아래처럼 설정해준다.


![Untitled 7](https://user-images.githubusercontent.com/101306770/165023547-ef16a499-513d-415f-8a30-c1111f6769e5.png)

- PATH에도 추가해준다.
- 아래 화면에서 Path를 누르고 편집

![Untitled 6](https://user-images.githubusercontent.com/101306770/165023538-23fc2c21-994b-4112-a7ac-a5327ce24a75.png)

- 아래 화면의 빈칸을 클릭하여  %JAVA_HOME%\bin 를 추가하고 확인을 누른다.

![Untitled 8](https://user-images.githubusercontent.com/101306770/165023550-322367f3-9cc0-4e52-a791-69666a21a6b5.png)

이렇게 하면 자바는 완료된다.