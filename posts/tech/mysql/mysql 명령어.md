1. **데이터베이스 관련 명령어**
    
    - `CREATE DATABASE [데이터베이스 이름];` - 새 데이터베이스 생성
    - `DROP DATABASE [데이터베이스 이름];` - 데이터베이스 삭제
    - `USE [데이터베이스 이름];` - 사용할 데이터베이스 선택
    - `SHOW DATABASES;` - 데이터베이스 목록 표시
2. **테이블 관련 명령어**
    - `CREATE TABLE [테이블 이름] (...);` - 새 테이블 생성
    - `DROP TABLE [테이블 이름];` - 테이블 삭제
    - `ALTER TABLE [테이블 이름] ...;` - 테이블 구조 변경
    - `SHOW TABLES;` - 현재 데이터베이스의 테이블 목록 표시
    - `DESC [테이블 이름];` - 테이블 구조 설명(컬럼 정보 등)
3. **데이터 조작 언어(DML)**
    
    - `SELECT ... FROM [테이블 이름];` - 데이터 조회
    - `INSERT INTO [테이블 이름] VALUES (...);` - 데이터 삽입
    - `UPDATE [테이블 이름] SET ... WHERE ...;` - 데이터 업데이트
    - `DELETE FROM [테이블 이름] WHERE ...;` - 데이터 삭제
4. **데이터 정의 언어(DDL)**
    
    - 이 명령어들은 테이블과 인덱스의 구조를 정의하는 데 사용됩니다. 예: `CREATE`, `DROP`, `ALTER`
5. **데이터 제어 언어(DCL)**
    
    - 데이터베이스의 보안과 무결성을 관리합니다. 예: `GRANT`, `REVOKE`
6. **트랜잭션 관련 명령어**
    
    - `BEGIN` 또는 `START TRANSACTION;` - 트랜잭션 시작
    - `COMMIT;` - 트랜잭션 내의 모든 변경 사항을 저장하고 트랜잭션 종료
    - `ROLLBACK;` - 트랜잭션 내의 모든 변경 사항을 취소하고 이전 상태로 되돌림