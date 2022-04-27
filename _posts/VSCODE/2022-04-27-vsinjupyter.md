---
title:  "VS에서 Jupyterlab 실행하기"
excerpt : "Jupyterlab을 실행해본다."

categories:
  - Vscode
tags:
  - Vscode

toc: true
toc_sticky: true
 
date: 2022-04-27
last_modified_at: 2022-04-27
---


# Visual Studio에서 Jupyterlab 실행하기

- Visual Studio 에서 jupyter lab 실행하는 방법을 알아보자
    - 보고자하는 폴더에서 Visual Stidio를 실행한다.
        - 실행방법
        - 폴더를 오른쪽 마우스로 클릭하여 gitbash 실핼
        
        
    ![Untitled](https://user-images.githubusercontent.com/101306770/165431216-11fcd9f3-ed69-4e74-a759-6eaf855cce43.png)
        
    - git bash 에서 code . 실행
    
    ![Untitled 1](https://user-images.githubusercontent.com/101306770/165431225-1f063454-d46c-4f30-8600-b27a0cc9ec7a.png)
    
    - visual studio 가 실행된다.
- visual studio 에서 jupyterlab 설치
    - 화면이 켜지면 terminal에서 bash 로 들어간다.
    
    ![Untitled 2](https://user-images.githubusercontent.com/101306770/165431229-c10b936c-8dbd-4b60-8dbf-21ff77169da5.png)
    
    - 현재 필자는 가상환경에서 실행하겟다.
    - 가상환경으로 접속한다.
    - 아래 코드를 실행하여 가상환경에 접속한다.
    
    ```jsx
    (venv)
    mskim@DESKTOP-O9NUUBO MINGW64 ~/Desktop/Pyspark_study
    $ source venv/Scripts/activate
    ```
    
    ![Untitled 3](https://user-images.githubusercontent.com/101306770/165431237-b47825f1-cb8f-4586-8de4-c52931a9ed6a.png)
    
    - 경로 앞에 venv 가있으면 가상환경에 접속한 상태이다.
    - jupyterlab 을 설치한다.
    - 아래 명령어를 입력한다.
    
    ```jsx
    (venv)
    mskim@DESKTOP-O9NUUBO MINGW64 ~/Desktop/Pyspark_study
    $ pip install jupyterlab
    ```
    
    - 설치가 되면 무수히 많은 버전이 확인된다.
    - version을 확인한다.
    
    ```jsx
    (venv)
    mskim@DESKTOP-O9NUUBO MINGW64 ~/Desktop/Pyspark_study
    $ pip show jupyterlab
    ```
    
    ![Untitled 4](https://user-images.githubusercontent.com/101306770/165431245-357c425e-cee5-4781-b168-dbe07582964e.png)

    
    - 잘 설치가 된 것을 확인햇다.
    - 실행해본다.
    - 
    
    ```jsx
    (venv) 
    mskim@DESKTOP-O9NUUBO MINGW64 ~/Desktop/Pyspark_study
    $ jupyter lab
    ```
    
    - 실행된 것을 확인한다.
    
    ![Untitled 5](https://user-images.githubusercontent.com/101306770/165431249-9cc9897b-2b00-48f9-8d92-c208804fc984.png)
    
    - 잘 실행이된다.
    
- 사용종료
    - 사용종료 시에는 윈도우 창을 닫아도 되지만 visual studio에 bash에서 종료를 해주면된다,
    - 종료는 bash 클릭후 ctrl + c 를 눌러주면 서버가 종료된다.
    
   ![Untitled 6](https://user-images.githubusercontent.com/101306770/165431255-1182d2dc-76fa-4dbb-9088-6c5a5ab995ad.png)
    
    - 종료가 되었다면 웹에서 에러메시지와 함께 종료된다.
        - 사용시 서버가 종료되는지 확인하면서 사용하면 더 좋을 것 같다.
        
    ![Untitled 7](https://user-images.githubusercontent.com/101306770/165431260-e9faab3a-b359-4e1c-b5c0-b5fdffe81b23.png)