# D. 프로그래밍 언어 활용

## 예외처리

    예외가 발생했을 때 해당 문제에 대비해 작성해 놓은 루틴을 수행하도록 하는것

```py
try:
    r=int(input('실행할 코드임 정수를 입력: ')) # 숫자 입력
    pi=3.141592
    print('원의 반지름: ', r)
    print('원의 둘레: ', 2*pi*r)
    print('원의 면적: ', r*r*pi)

except:
    print('예외발생 정수입력하셈')
else:
    print('예외발생 안되면 이걸 출력')
finally:
    print('무조건 실행할 코드 마무리~')
```

#### 문제

    프로그래밍 코딩과 관련된 다음 설명에서 괄호에 공통으로 들어갈 가장 적합한 용어를 쓰시오.

```
프로그램의 정상적인 실행을 방해하는 조건이나 상태를 (     )라고
 하며, (       ) 가 발생했을때 일반적인 처리 루틴은 프로그램을
 종료시키거나 로그를 남기도록 하는 것이다.
 C++, Ada, Java, 자바스크립와 같은 언어에는 (      )를 처리하기
 위한 기능이 내장되어 있다. (      )는 컴퓨터 하드웨어 문제,
 운영체제의 설정 실수, 라이브러리 손상 등 다양한 원인에 의해 발생할 수 있다.
```

> 예외

## 종합

이제까지 배웠던것들을 문제로 풀어보자

#### 문제 1

![문제1](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C1.png)

<details>
<summary>정답</summary>
A + A + A
</details>

#### 문제 2

![문제2](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C2.png)

<details>
<summary>정답</summary>
10 10 10
</details>

#### 문제 3

![문제3](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C3.png)

<details>
<summary>정답</summary>
3.14 3.14 0.12345678901234568 0.123456789

double 은 17자리까지 반올림
float 8자리하고 반올림

</details>

#### 문제 4

![문제4](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C4.png)

<details>
<summary>정답</summary>
11 11 10 <br>
11 21 20
</details>

#### 문제 5

![문제5](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C5.png)

<details>
<summary>정답</summary>
true <br>
false <br>
true <br>
</details>

#### 문제 6

![문제6](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C6.png)

<details>
<summary>정답</summary>
대문자입니다. <br>
2 또는 3의 배수입니다.<br>
</details>

#### 문제 7

![문제7](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C7.png)

<details>
<summary>정답</summary>
45 25  <br>
</details>

이거 설명 들어보자

※ 쉽게 2진법으로 전환하기

    45를 2진법으로

    ....    32  16  8   4   2   1
    ....    1   0   1   1   0   1

    이런식으로 쌉 가능

    그렇다면 25을 해보자

    ....    32   16  8   4   2   1
    ....    0    1   1   0   0   1

    이렇게 됨

#### 문제 8

![문제8](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C8.png)

<details>
<summary>정답</summary>
90 A  <br>
</details>

#### 문제 9

![문제9](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C9.png)

<details>
<summary>정답</summary>
3번입니다.  <br>
</details>

#### 문제 10

![문제10](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C10.png)

<details>
<summary>정답</summary>
1부터 10까지 합 : 55  <br>
</details>

#### 문제 11

![문제11](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C11.png)

<details>
<summary>정답</summary>
1 <br>
2 <br>
3 <br>
4 <br>
5 <br>
종료 5 <br>
</details>

#### 문제 12

![문제12](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C12.png)

<details>
<summary>정답</summary>
1  <br>
3  <br>
5  <br>
7  <br>
9  <br>
홀수의 합 25  <br>
</details>

#### 문제 13

![문제13](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C13.png)

<details>
<summary>정답</summary>
88  <br>
77  <br>
99  <br>
 총점  264 <br>
 배열의 길이 3  <br>
</details>

#### 문제 14

![문제14](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C14.png)

<details>
<summary>정답</summary>
회사: 나가라자동차  <br>
자동차명: 투싼  <br>
색상: 검정  <br>
최고속도: 300  <br>
현재속도: 0  <br>
수정속도: 80  <br>
</details>

#### 문제 15

![문제15](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C15.png)

<details>
<summary>정답</summary>
1 <br>
화이팅 <br>
</details>

#### 문제 16

![문제16](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C16.png)

<details>
<summary>정답</summary>
부모 클래스입니다. <br>
자식 클래스입니다. <br>
</details>

#### 문제 17

![문제17](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C17.png)

<details>
<summary>정답</summary>
80 가<br>
</details>

#### 문제 18

![문제18](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C18.png)

<details>
<summary>정답</summary>
10 5 <br>
true <br>
false <br>

</details>

#### 문제 19

![문제19](/img/1_programming/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%20%EB%AC%B8%EC%A0%9C19.png)

<details>
<summary>정답</summary>
3747576777 <br>
</details>
