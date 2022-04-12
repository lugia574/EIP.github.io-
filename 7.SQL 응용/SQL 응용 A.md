# A. SQL 응용

## 분류

- DDL (data define 정의어)

  - CREATE (정의)
  - ALTER (수정)
  - DROp (삭제)

- DML (조작어)

  - INSERT (삽입)
  - DELETE (삭제)
  - UPDATE (갱신)
  - SELECT (검색)

- DCL (제어어)

  - COMMIT (정상완료)
  - ROLLBACK (복귀)
  - GRANT (권한 부여)
  - REVOKE (권한 취소)

### DDL(Data Define Language, 데이터 정의어)

```sql
Create schema 대학 authorization 문
Create domain juso(char(10)
default=‘서울’
Create view 서울고객(성명, 전화번호)
as select 성명, 전화번호
from 고객
where 주소=‘서울시‘
Create index 고객번호_idx
on 고객(고객번호 desc)
```

![1](/img/7_sql/DDL_1.png)

### 문제

    <직원> 테이블에 대해 '이름' 속성을 '직원_name' 이라는
    인덱스를 정의하는 sql 문을 작성하시오.

> ```
> CREATE INDEX 직원_name ON 직원(이름);
> ```

### DCL (Data Control Language, 데이터 제어어) 개념

    데이터의 보안, 무결성, 회복, 병행 제어 등을 정의하는데 사용

종류

- GRANT
- REVOKE
- COMMIT
- ROLLBACK
- SAVEPOINT

![DCL](/img/7_sql/DCL_1.png)

```sql
SAVE POINT S1;
DELETE * FROM 사원 WHERE 사원번호 = 20;

-----

ROLLBACK TO S1;

이럼 * FROM 사원 WHERE 사원번호 = 20; 부분 롤백 됨
```

### 문제

    김하늘에게 <학생> 테이블에 대한 접근 및 조작에 관한
    모든 권한을 부여하는 SQL 문을 작성하시오

> ```sql
> GANT ALL ON 학생 TO 김하늘;
> ```

### DML (Data Manipulation Language, 데이터 조작어)의 개념

    저장된 데이터를 관리하는데 사용되는 언어

유형

- SELECT
- INSERT
- DELETE
- UPDATE

```sql
INSERT INTO 테이블명(속성1, 속성2...) VALUES(데이터1, 데이터2..)
INSERT INTO 학생(번호, 이름, 학년, 학과) VALUES('010', '정수현', 2, '사이버안보');
INSERT INTO 학생 VALUES ('홍길동','컴퓨터','서울')
INSERT INTO 학생 (이름,수강료) VALUES (홍길동,120)
INSERT INTO 수강정보(이름, 과목, 수강료) SELECT 이름, 과목, 수강료 FROM 학생 WHERE 주소='서울'
DELETE FROM 테이블명 WHERE 조건
DELETE FROM 학생 WHERE 번호=‘101’
DELETE FROM 학생 WHERE 과목='컴퓨터'
UPDATE 테이블명 SET 속성명=데이터 WHERE 조건;
UPDATE 학생 SET 이름='홍길동' WHERE 번호='101'
UPDATE 학생 SET 수강과목='컴퓨터' WHERE 이름='홍길동'
UPDATE 학생 SET 수강료=수강료+10000 WHERE 수강과목='컴퓨터'
```

```sql
SELECT [DISTINCT] 속성명
FROM 테이블명
WHERE 조건
ORDER BY 정렬할 속성명 [ASC] 또는 [DESC]
GROUP BY 그룹화 속성명
HAVING 그룹조건;
```

```sql
Select * From 사원;
Select 사원.* From 사원;
Select 이름, 부서, 생일, 주소, 급여 From 사원;
Select 사원.이름, 사원.부서, 사원.생일, 사원.주소, 사원.급여 From 사원;
Select Distinct 주소 From 사원;
Select 부서, '부서의 ', 이름, '의 급여는 ', 급여+10, ' 입니다 'From 사원;
Select * From 사원 Where 부서=‘편집’;
Select * From 사원 Where 부서=‘편집’ And 주소=’후월동‘;
Select * From 사원 Where 부서=‘편집’ Or 부서=‘기획’
Select * From 사원 Where 이름 Like '홍%';
Select * From 사원 Where 생일 Between #1970-01-01# And #1980-12-31#;
Select * From 사원 Where 급여 Between 210 And 220
```

```sql
Select *From 사원Where 주소 Is Null
Select Top 2 From 사원Order By 주소 Asc;
Select *From 사원Order By 부서 Asc, 이름 Desc;
Select 부서, Avg(급여) As 평균 From 사원 Group By 부서;
Select 부서, Count(*) As 사원수 From 사원 Group By 부서;
Select 부서, Count(*) As 사원수 From 사원 Where 급여>=200 Group By 부서 Having Count(*)>=2
Select * From 사원 Where 이름 Not in(Select 이름 From 활동)
Select 사원.이름, 사원.부서, 활동.특기, 활동.경력 From 사원, 활동 Where 활동.경력>8 And 사원.이름=활동.
이름
```

### 문제

    다음 <처리 조건>에 부합하는 SQL 문을 작성하시오

```
1. 학생 테이블에서 이름이 Scott 인 튜플을 삭제하시오.
2. 문자형은 싱글(작은)따옴표로 입력하고 문장의 끝에는
  세미콜론(;)을 반드시 표기하시오.

```

> ```sql
> DELET * FROM 학생 WHERE 이름= 'Scott';
> ```

### 문제

    관계 데이터베이스의 테이블 수강(학번, 과목명, 중간성적, 기말성적)에서
    과몽멱이 "DB"인 모든 튜플들을 성적에 의해 정렬된 형태로
    검새하고자 한다. 정렬 기준은 기말성적의 내림차순이며,
    기말성적이 같은 경우 중간성적의 오름차순으로 정렬하고자 한다.
    다음 SAL문의 괄호에 적합한 명령을 넣어 완성하시오.

> ```SQL
> -- 정렬 기준은 기말성적의 내림차순이며,
> -- 기말성적이 같은 경우 중간성적의 오름차순으로 정렬하고자 한다.
>
> SELECT * FROM 수강 WHERE 과목명 = "DB"
> ORDER BY 기말성적 DESC, 중간성적 ASC
> ```

### 문제

    <결제> 테이블을 이용하여 결제여부별 학생수를 검새하는
    SQL문을 작성하시오. 검색 결과는 다음과 같다.

검색결과

| 결제여부 | 학생수 |
| :------: | :----: |
|   미납   |   5    |
|   완납   |   4    |

```SQL
SELECT 결제여부, COUNT(*) AS 학생수 FROM 결제 GROUP BY 결제여부;
```
