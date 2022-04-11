# B. 프로그래밍 언어 활용

## 연산자

- 대입연산자
  ```c
  a+=1  //  a= a+1
  a-=1  //  a= a-1
  a*=1  //  a= a*1
  a/=1  //  a= a/1
  a<<=1 // a= a<<1
  ```
- 조건연산자

  ```c
  // 조건? 수식1: 수식2;
  c = a>b? a:b;

  ```

- 기타 연산자
  -Sizeof
  -,(콤마)
  -(자료형) a=int(1.4) + int(1.3)
- 연산자 우선순위
  - 단항 > 산술 > 시프트 > 관계 > 비트 > 논리 > 조건 > 대입 > 순서

### 문제

    다음 C언어로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```c
#include <stdio.h>
main(){
    int a = 5, b = 10, c = 15, d = 30, result;
    z = a * 3 + b > d || c - b / a <= d && 1;
    printf("%d\n", z)
}
```

> 1 <br>
> a \* 3 + b >> (5 \* 3) + 10 >> 25 <br>
> c - b / a >> 15 - (10 / 5) >> 13 <br>
> 25 > d >> 0 <br>
> 13 <= 30 >> 1 <br>
> 1 && 1 >> 1
> 0 || 1 >> 1

## 제어문

    프로그램의 순서를 변경할때 사용하는 명령문

- if 문

        조건에 따라 실행할 문장을 달리하는 제어문

- switch 문

        조건에 따라 분기할 곳이 여러 곳인 경우 간단하게 처리할 수 있는 제어문

- goto문

        프로그램 실행 중 건너뛰어 수행을 계속하기 위해 사용하는 제어문

  ```c
  int a;
  korea;
  scanf("%d", a)
  if(a<=5>)
      goto korea;
  else
      printf("요호호홓")

  ```

### 문제

    다음 C 언어로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```c
#include <stdio.h>
main(){
    int a =3, b = 10;
    if(b>7)
        printf("%x\n", a+b)
    else
        printf("%x\n", b-a)
}
```

> d (%x 에서 x가 소문자니까 d로 )

## 반복문

    일정한 횟수를 반복하는 명령문

- for 문

  초기값, 최종값, 증가값을 지정하는 수식을 이용해 정해진 횟수를 반복하는 제어문

- while 문

  조건이 참인 동안 실행할 문장을 반복 수행하는 제어문

- do ~ while 문

  실행할 문장을 무조건 한번 실행한 다음 조건을 판단하여 탈출 여부를 결정

※ break, continue 차이

![이미지](/img/1_programming/break_continue.png)

### 문제

    다음 C 언어로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```c
#include <stdio.h>
main(){
    int i = 10, hap = 0;
    while (i>1)
    {
        i--;
        if(i % 3 == 0)
            hap += i;
    }

    printf("%d\n", hap)
}
```

> 9 + 6 + 3 == 18

## 배열과 문자열

### 배열

    여러개의 변수들을 조합해서 하나의 이름으로 정의해 사용하는 것

- 1차원 배열

  변수들을 일직선상의 개념으로 조합한 배열

- 2차원 배열

  변수들을 평면, 즉 행과 열로 조합한 배열

### 문제

    다음 C 언어로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```c
#include <stdio.h>
main(){
    int exint[] = {3, 4, 5, 77, 6, 4, 7, 2, 3, 4, 7};
    int len = sizeof(exint)/sizeof(int);
    // sizeof(exint)/sizeof(int) >> 40(byte) / 4(byte) >> len == 10

    int value = 0;

    for (int i = 0; i < len; i++ ){
        if (exint[i]== 4){
            value ++;
        }
    }

    printf("%d", value)
}
```

> 3
