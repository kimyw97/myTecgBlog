### 날짜: {date}
### 목표
 - docker로 mysql container 생성

### 내용

1. docker 설치
	- https://doc.skill.or.kr/docker
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
