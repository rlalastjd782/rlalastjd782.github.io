---
title:  "JAVA 기초공부"
excerpt : "자바기초문법01."

categories:
  - Java
tags:
  - Java

toc: true
toc_sticky: true
 
date: 2022-06-15
last_modified_at: 2022-06-15
---
# Java 기초

- 자바 기초에 대해 알아보자.
    - 참고자료 점프 투 파이썬(박응용)
- 자료형
    - 숫자
        - 정수형 (int , long)
            - int의 표현범위  -2147483648 ~ 2147483647
            - long의 표현범위 9223372036854775808 ~ 9223372036854775807
            - 위의 내용을 보면 표현할 수 있는 숫자는 long 의 범위가 더 크다
            - long 변수에 값을 대입할 때는 대입하는 숫자 값이 int 자료형의 최대 값인 2147483647 보다 큰 경우 `8764827384923849L`
            과 같이 `L` 접미사(또는 소문자 `l`, 소문자 'l'은 숫자 1과 비슷하게 보이므로 추천하지 않는다.)를 붙여 주어야 한다. 만약 큰 숫자에 'L'과 같은 접미사를 누락하면 컴파일 에러가 발생한다.
        - 실수(float , double)
        - 마찬가지로 double 가 fliat보다 표현 범위 가 넓다.
        - 자바에서 실수형은 디폴트가 double이므로 위의 예에서 보듯이 float 변수에 값을 대입할 때에는 3.14F 와 같이 `F`접미사(또는 소문자 `f`)를 꼭 붙여 주어야 한다. float 자료형에 값을 대입할 때 접미사를 누락하면 컴파일 에러가 발생한다.
        - 사칙연산 +, -, *, /,%
        - 실행 예제 코드
        
        ```java
        
        public class sample {
        
        	public static void main(String[] args) {
        			
        		// 사칙연산 예제
        		int a = 300;
        		int b = 3;
        		int c = 10;
        		int d = 7;
        		//더하기
        		System.out.println(a+b);
        		// 곱셈		
        		System.out.println(a*b);
        		//나누기
        		System.out.println(a/b);
        		//빼기
        		System.out.println(a-b);
        		//나머지값
        		System.out.println(c%d);
        		
        	}
        
        }
        ```
        
        - 위부터 실행한 코드의 값이다.
        
       ![Untitled](https://user-images.githubusercontent.com/101306770/173708191-5dc6df27-dbd3-4043-ab3a-b2ec34cf0b07.png)
        
        - 증감연산 ****(++, --)****
        - 자바는 `++`, `--` 기호를 이용하여 값을 증가하거나 감소시킬 수 있다. 이러한 `++`
        , `--` 기호를 증감 연산자 라고 도 한다.
        - 예제 코드
        
        ```java
        public class sample {
        
        	public static void main(String[] args) {
        			
        	//증감연산 예제
        		int i = 0;
        		int j = 10;
        		i++;
        		j--;
        		System.out.println(i);
        		System.out.println(j);
        		
        		
        	}
        
        }
        ```
        
        - 출력
        
        ![Untitled 1](https://user-images.githubusercontent.com/101306770/173708202-86530455-8065-4bf5-b2a7-7a626ff8b406.png)
        
        - ++ 는 1만큼 증가시키고 - - 는 1만큼 감소시킨다. 해당연산자는 연산자의 위치가 중요하다.,
        - 즉 `i++` 와 같이 ++ 연산자가 변수 명 뒤에 붙으면 해당 코드가 실행되는 순간에는 i 값이 변경되지 않는다. 다만 `i++` 문장이 실행된 이후에 i값이 증가하게 된다. 이와는 반대로 `i++` 대신 `++i`라고 사용하게 되면 i 값이 먼저 증가된 후에 해당 코드가 실행된다.
        - i++ 은 값이 참조된 후에 증가
        - ++i 는 값이 참조되기전에 증가한다.
- 위의 내용을 가지고 기본적인 함수 몇가지를 만들어보자.
    1. 2개의 정수를 입력 받아 합친수를 리턴하는 함수 add를 만들어보세요.
    
    ```java
    public class example {
    	public int add(int num1, int num2) {
    		return num1+num2;
    	}
    }
    ```
    
    - 위 내용 중 public int 의 int인 이유는 출력값이 int형이기 때문에 int로 선언이되었다 (void대신)
    1. 2개의 정수를 입력받아 앞의 수에서 뒤의 수를 뺀수를 리턴하는 함수 minus를 만들어보세요.
    
    ```java
    public class example{
    	public int minus(int num1, int num2) {
    		return num1-num2;
    	}
    }
    ```
    
    1. 2번문제를 큰수에서 작은수를 빼도록 업그레이드 해보세요.
    
    ```java
    public class example {
    	public int minus2(int num1, int num2) {
    			if(num1>num2) {
    				return num1-num2;
    			}else {
    				return num2-num1;
    			}
    		}
    }
    ```
    
    - 위의 코드를 해석하자면
        - 출력은 int형로출력되는 minus2 의 함수를 만든다 . 2개의 값이 들어가는데 해당값은 int 형으로 들어간다.
        - if 만약 num1 이 num2 보다 크다면 리턴을 num1-num2 로 해라
        - else 그렇지 않다면 num2-num1 로 계산을 해라.