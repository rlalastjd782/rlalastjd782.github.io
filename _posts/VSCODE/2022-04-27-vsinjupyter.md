# Visual Studio에서 Jupyterlab 실행하기

- Visual Studio 에서 jupyter lab 실행하는 방법을 알아보자
    - 보고자하는 폴더에서 Visual Stidio를 실행한다.
        - 실행방법
        - 폴더를 오른쪽 마우스로 클릭하여 git bash 실핼
        - 
        
        ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled.png)
        
    - git bash 에서 code . 실행
    
    ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%201.png)
    
    - visual studio 가 실행된다.
- visual studio 에서 jupyterlab 설치
    - 화면이 켜지면 terminal에서 bash 로 들어간다.
    
    ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%202.png)
    
    - 현재 필자는 가상환경에서 실행하겟다.
    - 가상환경으로 접속한다.
    - 아래 코드를 실행하여 가상환경에 접속한다.
    
    ```jsx
    (venv)
    mskim@DESKTOP-O9NUUBO MINGW64 ~/Desktop/Pyspark_study
    $ source venv/Scripts/activate
    ```
    
    ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%203.png)
    
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
    
    ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%204.png)
    
    - 잘 설치가 된 것을 확인햇다.
    - 실행해본다.
    - 
    
    ```jsx
    (venv) 
    mskim@DESKTOP-O9NUUBO MINGW64 ~/Desktop/Pyspark_study
    $ jupyter lab
    ```
    
    - 실행된 것을 확인한다.
    
    ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%205.png)
    
    - 잘 실행이된다.
    
- 사용종료
    - 사용종료 시에는 윈도우 창을 닫아도 되지만 visual studio에 bash에서 종료를 해주면된다,
    - 종료는 bash 클릭후 ctrl + c 를 눌러주면 서버가 종료된다.
    
    ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%206.png)
    
    - 종료가 되었다면 웹에서 에러메시지와 함께 종료된다.
        - 사용시 서버가 종료되는지 확인하면서 사용하면 더 좋을 것 같다.
        
        ![Untitled](Visual%20Studio%E1%84%8B%E1%85%A6%E1%84%89%E1%85%A5%20Jupyterlab%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%92%E1%85%A2%E1%86%BC%E1%84%92%E1%85%A1%E1%84%80%E1%85%B5%20bcb12c2b7b414919a85476170e66195a/Untitled%207.png)