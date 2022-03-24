# A. 프로그래밍 언어 활용

## 데이터 타입

        변수에 저장될 데이터 형식을 나타내는 것.

- 데이터 타입의 유형

  - 정수 타입 (`Integer`)
  - 부동소수점 타입 (`Float point`)
  - 문자 타입 (`Character`)
  - 문자열 타입 (`Character String`)
  - 불린 타입 (`Boolean`)
  - 배열 타입 (`Array`)

방을 만들고 이 방에는 뭐뭐가 들어올꺼야 라고 정함 (`데이터 선언`)

### C, C++ 기준

- 문자 char

        1byte = 8bit

        >> -2^(n-1) ~ (2^(n-1) -1 )

        >> -128 ~ 127

- 부호가 없는 문자 unsinged char

        1byte

        0 ~ 255

- 정수

  - short, unsinged short > 2byte

  - int, unsinged int > 4byte

  - long, unsinged long > 4byte

  - long long > 8byte

- 실수

  - float > 4byte

  - double > 8byte

  - long double > 8byte

### 자바 기준

- 문자 char > 2byte (16bit)

- 정수

  - byte > 1byte
  - short > 2byte
  - int > 4byte
  - long > 8byte

- 실수

  - float > 4byte
  - double > 8byte

- 논리
  - boolean > 1byte

### 파이썬 기준

딱히 형태를 선언하지 않음

- 문자 str
- 정수 int
- 실수 float > 8byte
- complex(복소수. 실수와 허수) > 16 byte

#### 문제

    python 에서는 기본적으로 지원하지만 C,Java 언어에서는 외부 라이브러리를 통해서만 사용할 수 있는 자료형으로 16byte 크기를 갖고 실수와 허수의 합으로 이루어진 숫자 표현을 저장하는 자료 형을 쓰시오.

> complex

## 변수

    컴퓨터가 명령을 처리하는 도중 발생하는 값을 저장

    구분: 정수형, 실수형, 문자형, 포인터형 등...

- 변수명 작성 규칙

  - 영문자, 숫자, \_ 사용 가능
  - 첫 글자는 영문자, \_ 로 시작
  - 글자 수에 제한 없음
  - 공백이나 \* , + , - , / 등의 특수문자 사용 불가
  - 대소문자 구분, 예약어는 변수명으로 불가, 문자 끝에 (세미콜론;)

### 기억 클래스

    메모리 내에 변수 값을 저장하기 위한 기억공간

C 언어 기준

- 자동변수

        우리가  자주 쓰는 변수

        - 저장: 스택
        - 선언: auto (생략 가능)
        - 일시적
        - 지역적

- 레지스터 변수

        - 저장: 레지스터
        - 선언: register
        - 일시적
        - 지역적

- 정적 변수 (내부)

        - 저장: 메모리
        - 선언: static
        - 영구적(프로그램 끝날때까지)
        - 지역적

- 정적 변수 (외부)

        - 저장: 메모리
        - 선언: static
        - 영구적(프로그램 끝날때까지)
        - 전역적

- 외부 변수

        - 저장: 메모리
        - 선언: extend
        - 영구적(프로그램 끝날때까지)
        - 전역적

#### ex)

```c
char a = 'A'
float a_f = 1.5e3f; // float는 숫자 뒤에 f를 붙임
double a_d = -1.3827e-2; // double은 숫자 뒤에 아무것도 붙이지 않음
long double  a_ld = 1.5784e300l; // float는 숫자 뒤에 f를 붙임
```

> 여기 나오는 e 같은것들은 지수표기법임 <br> https://seulcode.tistory.com/461

#### 문제

    프로그램언어에서 이미 용도가 정해져 있어서 정해진 기능을 수행하는 것으로 변수 이름 등 다름 용도로 활용할 수 없는 것은 무엇인지 쓰지오.

> 예약어

## 데이터 입, 출력

### 함수

```c
scanf(서식, 변수);

// C언어의 표준 입력 함수
int a;
scanf("%3d", &a);
// 십진수 3자리를 받아서 변수 a에 넣어라
```

```c
printf(서식, 변수);

// C언어의 표준 출력 함수
/*
%d 십진수
%u 부호 없는 형태
%o 8진수
%x 16진수
%c 문자
%s 문자열
%f 실수
%e 지수
%ld 롱형 10진수
%lo 롱형 8진수
%lx 롱형 16진수
*/

// 제어 문자
/*
\n 줄바꿈
\b backspace 왼쪽으로 한칸이동
\t tap 탭
\r 현재 커서가 있는 줄 맨 앞으로 이동
*/
```

[진수 자바 표현](https://darksilber.tistory.com/21)

```c

char c;
getchar();
c = getchar();
// 왜 getchar(); 그냥하는지 몰겠음 여튼 그럼
putchar(80); // P 반환

// 한개의 문자 입출력

gets();
puts();

// 문자열 입출력
```

#### ex)

```c
#include <stdio.h>

int main()
{
    scanf("%2d",a);
    // a 에 235 입력


    scanf("%c",k);
    // k에 korean 입력

    int a;
    float b;

    scanf("%3d %5f", &a, &b);
    printf("%d\n%f", a,b);
    // 123456789 입력
}

// 이렇게 하면 a 는 23을 출력하고
// k는 k 를 출력
// b는 123 c 는 45678.000000
```

#### 문제

    다음 C언어의 <코드> 와 <입력>을 보고 프로그램을 분석하여 그 실행 결과를 쓰시오 (입력: 13#22)

```c
#include <stdio.h>
main(){
    int i,j;
    scanf("%o#%x", &i, &j);
    printf("%d %d",i, j);
}
```

> 8진수로 13 을 i에 담고 <br>
> 16진수로 22 을 j에 담아 <br>
> 각각 10진수로 출력하는것

> 그러면 13(8), 22(16) 의 10진수 변환한 값임 <br>
> 11 34

## 연산자

- 산술연산자

        가,감,승,제 등의 산술계산에 사용되는 연산자

  - ++a, a++ 의 차이점

          a = 1
          b = ++a >> b = 2
          c = a++ >> c = 1

- 관계연산자

        두 수의 관계를 비교하여 참, 거짓을 반환하는 연산자

- 비트연산자

            비트별 0,1 연산하여 결과를 얻는 연산자

  - a & b (AND)
  - a | b (OR)
  - a ^ b (XOR)

    ```c
    #include <stdio.h>


    int main()
    {
        unsigned char num1 = 1; // 0000 0001
        unsigned char num2 = 3; // 0000 0011

        printf("%d\n", num1 & num2);
        // 0000 0001: 01과 11을 비트 AND하면 01이 됨

        printf("%d\n", num1 | num2);
        // 0000 0011: 01과 11을 비트 OR하면 11이 됨

        printf("%d\n", num1 ^ num2);
        // 0000 0010: 01과 11을 비트 XOR하면 10이 됨

        return 0;

    }

    /*실행창
    1
    3
    2
    */
    ```

    | 연산자 | 비트1 | 비트2 | 결과2 |
    | :----- | :---: | :---: | :---: |
    | & AND  |   0   |   0   |   0   |
    |        |   1   |   0   |   0   |
    |        |   0   |   1   |   0   |
    |        |   1   |   1   |   1   |
    | \ OR   |   0   |   0   |   0   |
    |        |   1   |   0   |   1   |
    |        |   0   |   1   |   1   |
    |        |   1   |   1   |   1   |
    | ^ XOR  |   0   |   0   |   0   |
    |        |   1   |   0   |   1   |
    |        |   0   |   1   |   1   |
    |        |   1   |   1   |   0   |

  - ex

  ```c
  int a = 5;
  int b = 7;
  int c = a&b;

  /*
    0101
  + 0111
  -------
    0101
  즉 c 값은 5
  */
  ```

  - shift 연산자

    ```c
    #include <stdio.h>

    int main()
    {
        // 비트 0000 ~~~ 0000 에서 맨 앞자리는 부호임 1이면 음수
        // unsigned 는 부호 없음

        unsigned char num1 = 3;     //  3: 0000 0011
        unsigned char num2 = 24;    // 24: 0001 1000

        printf("%u\n", num1 << 3);
        // 24: 0001 1000: num1의 비트 값을 왼쪽으로 3번 이동

        printf("%u\n", num2 >> 2);
        //  6: 0000 0110: num2의 비트 값을 오른쪽으로 2번 이동

        int num3 = 5; // 32비트임 // 0000 ~~ 0101
        printf("%u\n", num3 >> 2);
        // 1: 0000 ~ 0001: num1의 비트 값을 오른쪽으로 3번 이동

        printf("%u\n", num2 << 2);
        // 4+ 16 = 20 : 0000 ~ 0001 0100: num2의 비트 값을 왼쪽으로 2번 이동
        return 0;


        /* ※ 음수일때
        left shift 일땐 0 으로 채워지고
        right shift 일떈 1 로 채워짐
        */


        unsigned char num1 = 131;    //  131: 1000 0011
        char num2 = -125;            // -125: 1000 0011

        unsigned char num3;
        char num4;

        num3 = num1 >> 5;
        // num1의 비트 값을 오른쪽으로 5번 이동

        num4 = num2 >> 5;
        // num2의 비트 값을 오른쪽으로 5번 이동

        printf("%u\n", num3);
        //  4: 0000 0100: 맨 뒤의 11은 사라지고 0000 0100이 됨

        printf("%d\n", num4);
        // -4: 1111 1100: 모자라는 공간은 부호 비트의 값인 1로

        // 채워지므로 1111 1100이 됨
    }
    ```

- 논리연산자

      두개의 논리 값을 연산하여 참, 거짓을 반환하는 연산자
