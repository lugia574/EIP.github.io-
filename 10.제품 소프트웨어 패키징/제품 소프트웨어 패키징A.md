# A. 제품 소프트웨어 패키징

## 소프트웨어 패키징

    모듈별로 생성한 실행 파일들을 묶어 배포용 설치 파일을 만드는 것

### 작업순서

```
기능식별 >> 모듈화 >> 빌드 진행 >> 사용자 환경분석
>> 패키징 및 적용시험 >> 패키징 변경개선 >> 배포
```

### 문제

    다음은 패키징에 필요한 작업들이다. 순서대로 나열하시오.

```
(1) 기능 식별 (2) 빌드 진행 (3) 패키징 및 적용 시험

(4) 사용자 환경 분석 (5) 모듈화 (6) 패키징 변경 개선
```

> 1 - 5 - 2 - 4 - 3 - 6

## 릴리즈 노트 작성

    개발 과정에서 정리된 릴리즈 정보를 고객과 공유하기 위한 문서

### 초기버전 작성시 고려사항

머리말, 개요, 목적, 문제요약, 재현항목, 수정/개선내용,

사용자 영향도, SW지원 영향도, 노트, 면책조항, 연락처

### 추가버전 작성시 고려사항

버그, 사용자 요청 등

### 작성순서

```
모듈식별 >> 릴리즈 정보확인 >> 릴리즈노트 개요작성
>> 영향도 체크 >> 정식릴리즈 노트작성 >> 추가개선항목식별
```

### 문제

    다음의 설명과 가장 부합하는 용어를 쓰시오.

```
개발 과정에서 소프트웨어가 얼마나 개선되었는지를
정리한 정보를 사용자와 공유하기 위해 작성하는 문서로,
이를 통해 사용자는 소프트웨어에 포함된
서비스나 사용 환경 등을 확인할 수 있다.
```

> 릴리즈노트

## 디지털 저작권 관리(DRM)

### 저작권

    창작자가 가지는 배타적 독점적 권리로
    타인의 침해를 받지 않을 고유한 권한

### 디지털 저작권 관리

    디지털 콘텐츠의 생성, 유통, 이용의 전과정에 걸쳐 사용되는
     디지털 콘텐츠 관리 및 보호기술

### 디지털 저작권 관리흐름

- 클리어링하우스 (저작권 사용권한)
- 콘텐츠제공자
- 패키져 (암호화)
- 콘텐츠분배자
- 콘텐츠소비자
- DRM컨트롤러
- 보안컨테이너

### 디지털 저작권관리의 기술요소

- 암호화
- 키관리
- 암호화파일생성
- 식별기술
- 저작권표현
- 정책관리
- 크랙방지
- 인증

### 문제

    다음의 설명과 가장 부합하는 용어를 쓰시오.

```
소설, 시, 논문, 가연, 연술, 음악, 연극, 무용, 회화, 서예,
 건축물, 사진, 영상, 지도, 도표, 컴퓨터 프로그램 저작물 등에
  대하여 창작자가 가지는 배타적 독점적 권리로
  타인의 침해를 받지 않을 고유한 권한이다.
```

> 저작권

## 소프트웨어 설치 매뉴얼 작성

    개발 초기에서부터 적용된 기준이나 사용자가 소프트웨어를
     설치하는 과정에 필요한 내용을 기록한 설명서와 안내서

### 서문

문서이력, 설치 매뉴얼의 주석, 설치도구의 구성, 설치 환경 체크항목

### 기본사항

소프트웨어 개요, 설치 관련파일, 설치아이콘, 프로그램 삭제, 관련추가정보

### 설치 매뉴얼 작성 순서

```
기능 식별 >> UI 분류 >> 설치파일/백업파일 확인
 >> Uninstall 절차확인 >> 이상Case확인 >> 최종메뉴얼적용
```

### 문제

    다음에 제시된 특징들에 가장 부합하는 용어를 쓰시오.

```
- 개발 초기에는 적용된 기준이나 사용자가
소프트웨어를 설치하는 과정에서 필요한 내용을
기록한 설명서나 안내서이다.

- 사용자를 기준으로 작성한다.

- 설치 과정에서 표시될 수 있는 오류 메시지 및 예외 상황에
관한 내용을 별도로 분류하여 설명한다.
```

> 소프트웨어 설치 메뉴얼

## 소프트웨어 사용자 매뉴얼 작성

    소프트웨어를 사용하는 과정에서 필요한 내용을
    문서로 기록한 설명서

### 목차 및 개요

### 서문 : 문서이력, 사용자 매뉴얼의 주석

### 기본사항

- 소프트웨어 개요
- 소프트웨어 사용환경
- 소프트웨어 관리
- 모델/버전별 특징
- 기능/인터페이스의 특징
- 소프트웨어 구동환경

### 사용자 매뉴얼 작성 순서

```
기능식별 >> 사용자 화면 분류 >> 사용자 환경 파일 확인
>> 초기화 절차 확인 >> 이상Case확인 >> 최종 매뉴얼 적용
```

### 문제

    다음에 제시된 특징들에 가장 부합하는 용어를 쓰시오.

```
- 사용자가 소프트웨어를 사용하는 과정에서
필요한 내용을 문서로 기록한 설명서와 안내서이다.

- 사용자가 소프트웨어 사용에 필요한 절차,
환경 등의 제반 사항이 모두 포함 되도록 작성한다.

- 개별적으로 동작이 가능한 컴포넌트 단위로 작성한다.
```

> 소프트웨어 사용자 메뉴얼
