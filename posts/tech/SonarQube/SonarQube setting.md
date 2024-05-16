### 날짜와 시간

- 날짜: 2023-10-10
- 시간: 17:31

### 주제 또는 키워드
 [[Code Quality]]
- sonarQube setting
### 간단한 내용
1. local에 soarQube docker 설치
	``` bash
	$ docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest
	```
2. generate key
   https://docs.sonarsource.com/sonarqube/latest/try-out-sonarqube/?_gl=1*y9noxq*_gcl_aw*R0NMLjE2OTY5MjQ5ODUuQ2owS0NRanc3Sk9wQmhDZkFSSXNBTDNib2JlSXMzTmFtS0R6eTd2ZkNGWE11dVQ5cnZSeHZjc0ZJN3pTakFqd1kwSjB3WUo3Q29zWHVZUWFBbVR1RUFMd193Y0I.*_gcl_au*MjAyNTA4NjExLjE2OTY5MjQ5ODU.*_ga*ODMxMzU1NDE1LjE2OTY5MjQ5ODU.*_ga_9JZ0GZ5TC6*MTY5NjkyNDk4NC4xLjEuMTY5NjkyNjEzNC4xOC4wLjA.

3. install scanner
   https://docs.sonarsource.com/sonarqube/10.2/analyzing-source-code/scanners/sonarscanner/
	1. download zip
	2. set config(위에서 발급한 키값 넣어주기)
	3. add PATH
		``` bash
		vim ~/.bashrc
		
		//마지막줄에 추가
		export PATH=$PATH:/path/to/your/install_directory/bin
		
		source ~/.bashrc

		```
### 코드 스니펫 (선택)

