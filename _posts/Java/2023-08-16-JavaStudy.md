---
title:  "JAVA JSONObject"
excerpt : "JSONObject"

categories:
  - Java
tags:
  - Java

toc: true
toc_sticky: true
 
date: 2023-08-16
last_modified_at: 2023-08-16

--- 

# 어노테이션 @Component

- @Component 어노테이션을 이용하면  Bean Configuration 파일에 Bean을 따로 등록하지 않아도 사용할 수 있다.
- 빈 등록자체를 빈 클래스 자체에다가 할 수 있다는 의미이다.
- @Component 어노테이션은 기본적으로 타입기반의 자동주입 어노테이션이다
- @Autowired, @Resource와 비슷한 기능을 수행한다고 할 수 있겠다.
- @Component 어노테이션을 xml 설정파일에서 설정하는 방법이다.


## XML 파일에서 @Component 어노테이션 설정하기

- xml파일에 <context:component-scan base-package="패키지경로" /> 태그를 설정해주면, 지정된 패키지 안에 있는 bean클래스의 어노테이션을 분석할 수 있도록 지정해주는 것이다.

- 설정한 패키지 경로안에 bean 클래스를 만들고 @Component 어노테이션을 붙여주면 해당 bean 클래스는 자동으로 빈이 생성될수 있게 된다

- 아이디를 사용하지 않고 타입으로 빈을 지정해서 찾는거랑 비슷한 느낌이다. 이름이없기 때문에 타입으로서 빈을 받아낼수없다



