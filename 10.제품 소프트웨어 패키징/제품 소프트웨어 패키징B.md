# B. 제품 소프트웨어 패키징

## 소프트웨어 버전 등록

### 소프트웨어 패키징의 형상 관리

형상 관리(SCM; Software Configuration Management)

    소프트웨어의 개발 과정에서 소프트웨어의 변경 사항을 관리하기 위해 개발된 일련의 활동

### 형상관리기능

- 형상식별
- 버전제어
- 형상통제
- 형상감사
- 형상기록

### 용어

- 저장소(Repository)
- 가져오기(import)
- check out
- check in
- commit
- 동기화

### 소프트웨어 버전 등록 과정

```
가져오기(Import) >> 인출(Check-out) >> 예치(Commit)
>> 동기화(Update) >> 차이(Diff)
```

### 문제

    소프트웨어 버전 등록과 관련된 용어 중
    최신 버전의 파일들과 변경 내역에 대한 정보들이
    저장되어 있는 곳의 명칭을 쓰시오.

> 저장소

## 소프트웨어 버전 관리 도구

- 공유 폴더 방식
- 클라이언트/서버 방식
- 분산 저장소 방식
- Subversion(서브버전, SVN)

  CVS 개선 (공동 개발을 편리하게 도와주는 도구)
  trunk, branches

  ```
   Add, commit, update,
   checkout, lock/unlock,
   import, export, info, diff, merge
  ```

- Git(깃)

  ```
  Add, commit, branch,
  checkout, merge, init,
  remote add, push, fetch,
  clone, fork
  ```

### 문제

    소프트웨어 버전 관리 도구인 Subversion 에서
    사용하는 명령어 중 다음에 제시된 기능을
    수행하는 명령어를 쓰시오.

```
- 서버의 최신 commit 이력을 클라이언트의 소스 파일에 적용한다.

- commit 전에는 매번 수행하여 클라이언트에 적용되지 않은 서버의
 변동내역을 클라이언트에 적용한다
```

> update

## 빌드 자동화 도구

    - 빌드 : 소스 코드 파일들을 컴파일한 후
    여러 개의 모듈을 묶어 실행 파일로 만드는 과정

    - 빌드 자동화 도구 : Ant, Make, Maven, Gradle, Jenkins 등

- Jenkins

  JAVA 기반 오픈 소스(가장 마니 사용)

  서블릿 컨테이너에 실행되는 서버 기반 도구

  친숙함, 분산 빌드/ 테스트

- Gradle

  안드로이드 개발 앱/ 오픈소스

  TASK 단위로 실행/ 빌드 속도 향상

### 문제

    다음에 제시된 특징에 가장 부합하는 빌드 자동화 도구를 쓰시오.

```
- Java 기반의 오픈 소스 형태로,
가장 많이 사용되는 빌드 자동화 도구이다.

- 서블릿 컨테이너에서 실행되는 서버 기반 도구이다.

- SVN, Git 등 대부분의 형상 관리 도구와 연동이 가능하다.

- 친숙한 Web GUI 제공으로 사용이 쉽다.

- 여러 대의 컴퓨터를 이용한 분산 빌드나 테스트가 가능하다.
```

> Jenkins
