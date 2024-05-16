### 날짜: {date}
### 목표
 - docker로 mysql container 생성

### 내용
- [[strapi]]를 학습하기전에 내 로컬에 db가 있어야 테스트가 가능해서 먼저 docker로 mysql container를 생성 할려고한다.

1. docker 설치
	- 이미 설치되어있으므로 생략하고 넘어간다
2. Mysql 이미지 pull
	- 아래의 명령어 터미널에서 실행
	- 특정 버전 원할경우 `mysql:<version>`
	``` bash
	docker pull mysql 
```
3. container 실행
```bash
docker run --name [컨테이너 이름] -e MYSQL_ROOT_PASSWORD=[루트 비밀번호] -p 3306:3306 -d mysql

```
4. docker container 상태 확인
```bash
docker ps
```
5. mysql 접속
```bash
docker exec -it [컨테이너 이름] mysql -uroot -p
```

- 나의 생각
	- docker 명령어들을 맨날 찾아보는게 시간낭비가 좀 있고 귀찮다. 언제 날잡고 외워야겠다
	- docker 이미지도 맨날 있는거 가져와서 사용했었는데 한번 공부해서 만들어보고싶다.