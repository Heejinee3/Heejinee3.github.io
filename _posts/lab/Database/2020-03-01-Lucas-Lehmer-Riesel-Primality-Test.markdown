---
index: 4 # labs number
num: 0 # lab number
permalink: /lab/Database/Lab1 # link
category: lab # project or lab
---

#### **Database**

---

The figure below shows the schema of the Sakila database. This database has 23 tables:
16 normal tables and 8 view tables. You can use view tables, but we recommend that you
use only normaltables. You can find the information related to the schema in the following
link: [Sakila](https://dev.mysql.com/doc/sakila/en/sakila-structure.html)

![ref: https://database.guide/what-is-a-database-schema/sakila_full_database_schema_diagram/](/assets/lab/Database/Figure1.png)
<br>

#### **메르센 소수**

---

메르센 소수는 특별한 형태의 소수로, 다음과 같은 형식으로 표현되는 소수이다:

> M<sub>p</sub> = 2<sup>p</sup> − 1

여기서 p는 자연수이고, 결과적으로 2의 거듭제곱에서 1을 뺀 형태이다. 예를 들어, p가 2일 때, 메르센 소수는 2<sup>2</sup> - 1 = 3이 된다. 또 다른 예로, p가 3일 때, 메르센 소수는 2<sup>3</sup> - 1 = 7이 된다.

메르센 소수는 이름을 받은 프랑스의 수학자 마린 메르센(Marin Mersenne)에 의해 연구되었다. 그는 17세기에 이러한 형태의 소수들을 성질과 특성을 연구하였다. 그러나 그 당시에는 메르센 소수의 일반적인 성질을 밝히는 데에 실패하였다.

메르센 소수는 암호학, 컴퓨터 과학, 그리고 소수론 등의 분야에서 중요한 역할을 한다. 또한, 소수의 분포와 소수 검사 알고리즘 개발 등에도 활용된다. 그러나 메르센 소수는 일반적으로 소수가 아닌 경우가 많고, 발견하기 어려운 특성을 가지고 있기 때문에 연구와 발견이 꾀별한 주제 중 하나이다.

<br>

#### **뤼카-레머 소수 판별법**

---

루카-레머 소수 판별법은 메르센 소수를 효율적으로 판별하는 알고리즘이다. 이 알고리즘은 루카 수열이라고 불리는 특별한 수열을 사용하여 메르센 소수를 검사한다. 루카-레머 소수 판별법은 아래의 단계로 구성된다:

1. 주어진 지수 p에 대해 메르센 수를 계산한다. 메르센 수는 2<sup>p</sup> - 1로 표현된다.

2. 루카 수열을 사용하여 루카 수를 계산한다. 루카 수열은 L(0) = 4, L(1) = 14, L(n) = L(n-1)<sup>2</sup> - 2로 정의된다.

3. 루카 수열에서 L(p-2)를 계산한다. 이 값은 p가 소수인 경우에만 메르센 소수에 대응하는 루카 수열 값이다.

4. 루카 수열 값이 0인지 확인한다. 만약 L(p-2)가 0이라면, 메르센 수는 소수일 가능성이 있다. 그렇지 않으면, 메르센 수는 소수가 아니다.

루카-레머 소수 판별법은 특히 메르센 소수가 큰 경우에 유용하다. 이 알고리즘은 간단하고 빠르게 수행되며, 특정한 소수 p에 대해 메르센 소수를 판별할 수 있다. 그러나 이 판별법은 모든 소수에 대해 적용되지 않으며, p가 소수인지 확인하는 데에만 사용된다.

루카-레머 소수 판별법은 현재까지 발견된 가장 큰 메르센 소수들을 찾는 데에 활용되었으며, 프라임그리드(Priemgrid)와 같은 기술과 결합하여 대규모의 소수를 검사하는 데에도 사용된다.

<br>

#### **Link**

---

[Github](https://github.com/Heejinee3/Discrete-Mathematics/tree/master/Lucas-Lehmer-Riesel%20Primality%20Test)
