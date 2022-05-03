---
title:  " Oracle  Pl/sql 문법"
excerpt : "Oracle  Pl/sql 문법"

categories:
  - Oracle
tags:
  - Oracle

toc: true
toc_sticky: true
 
date: 2022-05-03
last_modified_at: 2022-05-03
---

# PL/SQL 연산자

- 연습 도서는 ‘오라클 SQL 과 PL/SQL을 다루는 기술. 길벗, 홍형경’  도서를 참고하였다
- 아래 데이터는 ORCLE 의 기본 DB 인 EMPLOYEES 를 사용하였다.
- 용어 정리(나름 대로 정리)

# 비교 조건식(ANY, SOME, ALL)

- 여러가지의 연산들을 알아본다

# ANY 문

- ANY 문은 OR값과 같은 값이 나온다
    - 즉 데이터 안에 해당 값이 같은 값만 추출한다

```sql
SELECT
    employee_id
    , salary
FROM employees
WHERE salary = ANY( 3000, 4000);

```

- ANY문 결과 값
    
![Untitled](https://user-images.githubusercontent.com/101306770/166401959-f7506c9f-6edf-46aa-98d5-fdb046307295.png)


```sql
-- ANY문과 같은문
SELECT
    employee_id
    , salary
FROM employees
WHERE salary = 3000 or salary = 4000;

```

- ANY 문을 풀어 정리한 수식의 결과 값

![Untitled 1](https://user-images.githubusercontent.com/101306770/166401964-3f7a7cab-7236-4e5c-8725-952cc382d166.png)

- 같은 값이 나온다

# All 문

```sql
-- ALL
-- 모든 조건을 동시에 만족해야함
SELECT
    employee_id
    , salary
FROM employees
WHERE salary = ANY(2000, 3000, 4000)
ORDER BY employee_id;
```

- ALL 문은 모든 조건을 동시에 만족 해야 한다.
- 아래는 실행 했을 때의 결과
- 모두 만족하는 결과가 없기 때문에 결과가 안 나온다

![Untitled 2](https://user-images.githubusercontent.com/101306770/166401970-fb920df3-ed8a-4d19-bdca-810f20b8a4b2.png)

```sql
SELECT
    employee_id
    , salary
FROM employees
WHERE salary = SOME(3000, 4000)
ORDER BY employee_id;
```

# SOME 문

- OR 과 같은 방식이라고 보면 된다. () 안에 있는 값을 포함하는 값을 모두 추출한다.
- 결과
    
![Untitled 3](https://user-images.githubusercontent.com/101306770/166401974-dd82c5ae-e03f-4b0c-ba86-1bc98f24c16e.png)
    

# 논리 조건 식(NOT)

- 논리 조건 식에 대해 알아본다

```sql
-- 논리조건식
SELECT
    employee_id
    , salary
FROM employees
WHERE NOT (salary >= 2500)
ORDER BY employee_id;
```

- 위 문장을 해석하면 salary의 값들 중에 2500 이하 인 것들만 보여 달라는 뜻이다.
- 결과는 아래 사진처럼 나온다.
    
![Untitled 4](https://user-images.githubusercontent.com/101306770/166401977-3fd90235-d556-43fd-93fd-31ba9e859a3a.png)

    

# BETWEEN 문

```sql
SELECT
    employee_id
    , salary
FROM employees
WHERE salary BETWEEN 2000 AND 2500
ORDER BY employee_id;
```

- 
    - 해당 문을 풀어서 말하자면 salary 내에 있는 값 중에 2000~ 2500 사이에 있는 값들만 보여달라는 뜻이다.
- 결과

![Untitled 5](https://user-images.githubusercontent.com/101306770/166401981-bdd64ccf-559f-4455-b233-52aab4b86355.png)
# IN , NOT IN 조건 식

- IN 조건 식은 등호 연산자가 빠진다.

```sql
SELECT
    employee_id
    , salary
FROM employees
WHERE salary IN(3000, 4000)
ORDER BY employee_id;
```

- 위에 문장을 해석하면 salary 에서 () 값들만 추출한다는 뜻이다.
    - some 문과 비슷하지만 등호가 안 들어간다.
- 결과

![Untitled 6](https://user-images.githubusercontent.com/101306770/166401987-f3523e4c-b5fb-4646-bdb9-c880a0ec2b39.png)

- NOT IN 예제 코드

```sql
SELECT
    employee_id
    , salary
FROM employees
WHERE salary NOT IN(3000, 4000)
ORDER BY employee_id;
```

- 결과 값
    - IN 과는 반대로 ()안에 있는 것을 제외한 모든 값들을 추출한다.
    - IN 과 똑같이 등호는 제외한다.

![Untitled 7](https://user-images.githubusercontent.com/101306770/166402001-b6fc95f1-9207-4c77-8242-3889cb4585a4.png)

```sql
SELECT
    employee_id
    , salary
FROM employees
WHERE salary <> ALL(2000, 3000, 4000)
ORDER BY employee_id;
```

- 위와 같은 코드로도 사용 할 수 있다.
- ANY, SOME문에는 등호가 사용 가능 하지만 IN구문에서는 등호가 사용 불 가능 하다.

# EXISTS 조건 식

- IN과 비슷하나 서브 쿼리 절에서만 사용 가능하다.

```sql
SELECT 
    department_id
    , department_name
From departments a
WHERE EXISTS (SELECT *
              FROM employees b
              WHERE a.department_id = b.department_id
              AND b.salary > 3000)
ORDER BY a.department_name;
```

- EXISTS 뒤에 오는 ()안에 문장 즉, 서브 쿼리의 범위 내 에서 값을 추출하는 것이다.
- 문장을 해석해보자면
    1. SELECT ⇒ department_id와 department_name의 값을 가져 올 것이다.
    2. FROM ⇒departments 내에서 단 a 로 명시한다
    3. WHERE ⇒어떻게 ?
        1. ()안에서
            1. SELECT * → 모든 값을 가져온다.
            2. FROM →  employees 에서 단 employess는 b 로 명시 하겠다.
            3. WHERE→ a.department_id = b.department_id 값이 같을 때
                1. AND 그리고 b.salary 가 3000 이상 일 때
    4. ORDER BY → a.department_name의 값을 추출한다.
- 아래 결과 값이다.

![Untitled 8](https://user-images.githubusercontent.com/101306770/166402013-0a516320-021b-43a6-a153-c36b4e378fbe.png)


# Like 조건식

- 문자열의 패턴을 검색 할 때 사용하는 조건 식이다.

```sql
SELECT emp_name
FROM employees
WHERE emp_name Like '%a'
ORDER BY emp_name;
```

- 문장을 해석해보면
    - emp_name에서 emp_name 를 출력 할 것이다 단 맨 뒤 글자가 a 인 글자를
        - 앞에 어떤 글자가 와도 상관없다.

![Untitled 9](https://user-images.githubusercontent.com/101306770/166402085-5f39beea-5eac-4a63-b8a5-56be4913df7f.png)

- 위에 결과 창이다. 보는 것처럼 a가 모두 맨끝에있다.
- %를 기준으로 앞인지 뒤인지 구별하면된다.

```sql
--(공백갯수)뒤 a 포함된 글자를 가져와라
SELECT emp_name
FROM employees
WHERE emp_name Like '__a%'
ORDER BY emp_name;
```

- 위에 LIKE 문은 공백이 2개이다
    - 해서 앞에서 2칸 뒤에 a가 들어가는 이름을 가져오는 것이 된다.

![Untitled 10](https://user-images.githubusercontent.com/101306770/166402075-22e53d53-fd6e-4025-93a6-53e1957ac405.png)

- 위 사진이 결과다.