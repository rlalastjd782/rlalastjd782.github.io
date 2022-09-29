---
title:  "JavaScript"
excerpt : "JavaScript 기초공부."

categories:
  - Javascript
tags:
  - Javascript

toc: true
toc_sticky: true
 
date: 2022-06-08
last_modified_at: 2022-06-08
---

# 자바스크립트

- 자바스크립트
    - const 변수는 끝까지 변하지 않음
    - 자바스크립트는 다른프로그램과 달리 프로그램이 실행되면서 값의 타입을 정의함
    - 변수의 타입을 사전에 정의 안해도 됨. (객체지향의 레퍼런스타입으로 정의됨)
    - 모두 var, let, const 로 변수를 선언하면됨
    
- 배열변수
    - push pop(stack 방식)
    - push는 배열 쌓기 (파이썬 append)
        - ex)  nums.push(5);
    - pop 는 데이터 제거
        - ex) var n1 = nums.pop()
    
    ![Untitled](https://user-images.githubusercontent.com/101306770/172568323-70a163bb-8162-41a9-8c5c-925a77870407.png)
    
    ![Untitled 1](https://user-images.githubusercontent.com/101306770/172568333-1833a9b8-9d81-44c7-ab56-e447167ac747.png)
    

# var const let 차이점

- var
    - var 은 변수를 지정하여도 에러가 나지않음
    - 허나 뒤에 다른변수를 지정한다면 초기화가되고 마지막에 지정된 변수로 지정된다.
- let
    - let 은 중복 선언이 불가하다
    - 하지만 값을 재 할당 하는 것은 가능하다.
    
    let a = 100;
    
    let a = 200; → 오류
    
    a=  200
    
    consol.log(a) → 200  가능
    
- const
- 변수 명을 중복으로 선언해도 에러 재 할당을 해도 에러 결국 const는 변경이 불가 하다.
- 

- 데이터 객체
- object 객체 활용

- json
- 

![Untitled 2](https://user-images.githubusercontent.com/101306770/172568341-5635d86a-49d4-4b40-b662-a38e62f16c7c.png)

![Untitled 3](https://user-images.githubusercontent.com/101306770/172568346-30b2105d-aafa-4668-b0f1-7e6888150d78.png)


함수

![Untitled 4](https://user-images.githubusercontent.com/101306770/172568352-a91d2c66-e26f-4697-b58c-3fc9359254ee.png)

# confirm 선택

![Untitled 5](https://user-images.githubusercontent.com/101306770/172568362-161c26ba-4dfc-41cb-a565-be51d597a4ca.png)


![Untitled 6](https://user-images.githubusercontent.com/101306770/172568373-1f900933-c452-4e48-9f89-b98bd950707e.png)

- 확인시에

![Untitled 7](https://user-images.githubusercontent.com/101306770/172568383-d7b65ad4-e195-4da7-b71d-cf77a614c54c.png)


- 취소시에

![Untitled 8](https://user-images.githubusercontent.com/101306770/172568398-c135d76b-8298-414f-9b6c-d1431027fbc8.png)

![Untitled 9](https://user-images.githubusercontent.com/101306770/172568413-74c85094-7925-41aa-99e4-55769713ffec.png)


![Untitled 10](https://user-images.githubusercontent.com/101306770/172568419-319dce75-992d-4f91-a97f-166b5e3051ff.png)


- 클릭 3을 하였을 때 btn1이 함수내에서 변경되므로 밸류의 클릭의 값이 더해진 값으로 변경됨

![Untitled 11](https://user-images.githubusercontent.com/101306770/172568433-a04500e5-6b6c-419a-8311-3684688a46d3.png)

- 타입 추가시 변경

![Untitled 12](https://user-images.githubusercontent.com/101306770/172568447-f2026e5d-878e-4bb2-aaad-b1625038f554.png)


- 결과

![Untitled 13](https://user-images.githubusercontent.com/101306770/172568458-6e0e638c-4dc9-4d17-85e7-26067ddcfa9a.png)