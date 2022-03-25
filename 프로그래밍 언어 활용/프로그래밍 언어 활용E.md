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

---

#### 문제 1

이제까지 배웠던것들을 문제로 풀어보자

![문제1](/img/%EB%AC%B8%EC%A0%9C1.png)

<details>
<summary>정답</summary>
A + A + A
</details>

#### 문제 2

![문제2](/img/%EB%AC%B8%EC%A0%9C2.png)

<details>
<summary>정답</summary>
10 10 10
</details>

#### 문제 3

![문제3](/img/%EB%AC%B8%EC%A0%9C3.png)

<details>
<summary>정답</summary>
3.14 3.14 0.12345678 0.123456789

double 은 8자리까지
float 9자리

</details>

#### 문제 4

![문제4](/img/%EB%AC%B8%EC%A0%9C4.png)

<details>
<summary>정답</summary>
11 11 10 <br>
11 21 20
</details>

#### 문제 5

![문제5](/img/%EB%AC%B8%EC%A0%9C5.png)

<details>
<summary>정답</summary>
true <br>
false <br>
true <br>
</details>

#### 문제 6

![문제6](/img/%EB%AC%B8%EC%A0%9C6.png)

<details>
<summary>정답</summary>
대문자입니다. <br>
2 또는 3의 배수입니다.<br>
</details>

#### 문제 7

![문제7](/img/%EB%AC%B8%EC%A0%9C7.png)

이거 설명 들어보자

<details>
<summary>정답</summary>
45 25  <br>
</details>

#### 문제 8

![문제8](/img/%EB%AC%B8%EC%A0%9C8.png)

<details>
<summary>정답</summary>
90 90  <br>
</details>

#### 문제 9

![문제9](/img/%EB%AC%B8%EC%A0%9C9.png)

<details>
<summary>정답</summary>
3번입니다.  <br>
</details>

#### 문제 10

![문제10](/img/%EB%AC%B8%EC%A0%9C10.png)

<details>
<summary>정답</summary>
1부터 10까지 합 : 55  <br>
</details>

#### 문제 11

![문제11](/img/%EB%AC%B8%EC%A0%9C11.png)

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

![문제12](/img/%EB%AC%B8%EC%A0%9C12.png)

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

![문제13](/img/%EB%AC%B8%EC%A0%9C13.png)

<details>
<summary>정답</summary>
88  <br>
77  <br>
99  <br>
 총점  264 <br>
 배열의 길이 3  <br>
</details>

#### 문제 14

![문제14](/img/%EB%AC%B8%EC%A0%9C14.png)

<details>
<summary>정답</summary>
1부터 10까지 합 : 55  <br>
</details>
