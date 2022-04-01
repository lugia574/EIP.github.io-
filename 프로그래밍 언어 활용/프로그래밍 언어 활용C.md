# C. 프로그래밍 언어 활용

## 포인터

    변수의 주소, C 언어에서는 주소를 제어 할 수 있는 기능을 제공

- 포인터 변수

        C언어에서는 변수의 주소를 저장할 때 사용하는 변수

- 포인터 변수 활용 용도

  - 연결된 자료 구조를 구성하기 위해 사용
  - 동적으로 할당된 자료 구조를 지정하기 위해 사용
  - 배열을 인수로 전달하기 위해 사용
  - 문자열을 표현하기 위해 사용

- 선언

            자료형 *포인터이름;
            포인터 = & 변수;

  ```c
  #include <stdio.h>

  int main()
  {
      int *numPtr;      // 포인터 변수 선언
      int num1 = 10;    // int형 변수를 선언하고 10 저장

      numPtr = &num1;   // num1의 메모리 주소를 포인터 변수에 저장

      printf("%p\n", numPtr);    // 0055FC24: 포인터 변수 numPtr의 값 출력
                              // 컴퓨터마다, 실행할 때마다 달라짐
      printf("%p\n", &num1);     // 0055FC24: 변수 num1의 메모리 주소 출력
                              // 컴퓨터마다, 실행할 때마다 달라짐

      return 0;
  }
  ```

  EX)

  ```c
  #include <stdio.h>

  int main()
  {
      int a= 2, *numPtr;
      numPtr = a;


      printf("%d\n", ++*numPtr);
  }
  ```

  > 답은 3

### 문제

    다음 C언어로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```c
#include <stdio.h>

main(){
  char a[] = {'A','B','C','D','E','F'};
  char p*;
  p= &a[3];
  printf("%c, %c\n", *p, *(p-1) );
}
```

> D, C

, 까지 써줘야함

## 사용자 정의 함수

    사용자가 필요한 기능을 직접 만들어 사용할 수 잇는 함수

### 문제

    다음 C언어로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```c
#include <stdio.h>

func(int *p){
    printf("%d\n", *p);
    printf("%d\n", p[2]);

}

main(){     //  *P *P+1 *p+2 *P+3 *P+4
    int a[7] = {10,20,30,40,50};
    func(a);
    func(a+2);
}
```

> 10<br>
> 30<br>
> 30<br>
> 50

## Java 클래스와 메소드

### 클래스와 메소드

    클래스는 객체생성을 위한 필드(속성)와 메소드(함수)를 정의
    Java는 클래스를 만들어 사용해야한다.

### 문제

    다음 Java로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```java
public class Test{
    static int power(int data, int exp){
        int i, result = 1;
        for(i=0; i<exp; i++){
            result = result * data;
        }
        return result;
    }

    public static void main (String args[]){
        system.out.print(power(2,5));
    }
}
```

> 32

## Python 기초

### 기본문법

- 변수 자료형에 대한 선언이 없음

- 문장의 끝을 의미하는 세미콜론(;)을 사용할 필요가 없음

- 여백은 일반적으로 4칸 또는 한개의 탭만큼 띄어야하며, <br>
  같은 수준의 코드들은 반드시 동일한 여백을 가져야함

### 입출력함수

- input()

- print()

### 문자열

- Python 에서는 작은 따옴표와 큰 따옴표 자유롭게 사용

### list

    C와 Java 에서는 여러 요소들을 한개의 이름으로 처리할때
    배열을 사용했는데 Python에서는 리스트 사용

    배열과 달리 하나의  리스트에 정수, 실수, 문자열 등 다양한 자료형을 섞어서 저장 가능

### 문제

    다음 Python으로 구현된 프로그램을 분석하여 그 실행 결과를 쓰시오.

```python
i = 40
f = 123456.789E-3 # 123456.789  * 10^(-3) >> 123.456789
print('%d\n%d'%(i,i), end='/')
print('%.3f'%f)
```

> 40 <br>
> 40/123.457 (반올림 됨)

## Python 활용

- if
- for

- while

- 클래스

  ```py
  class 클래스명:
      # 문장 ~
      def 메소드명(self, 인수):
          # self 는 클래스에 속한 메소드에 반드시 있어야하는 예약어

          # 문장~

          ans = 인수
          return ans

    a = 클래스명()
    print(a.메소드명(인수))
  ```
