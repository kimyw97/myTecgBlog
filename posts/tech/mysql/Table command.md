```mysql
CREATE TABLE [테이블 이름] (...);
DROP TABLE [테이블 이름];
ALTER TABLE [테이블 이름] ...; #테이블 구조 변경
SHOW TABLES; #현재 데이터베이스의 테이블 목록 표시
DESC [테이블 이름]; #테이블 구조 설명(컬럼 정보 등)
```

## CREATE TABLE
```mysql
CREATE TABLE tableName (
	column1 dataType
	column2
	column3
	column4
	column5
)
```

### dataType
- https://dev.mysql.com/doc/refman/8.0/en/data-types.html