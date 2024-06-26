### 날짜와 시간

- 날짜: 2024-03-31
- 시간: 21:53

### 주제 또는 키워드
[[REST]]
[[RESTful API]]


### 간단한 내용
- RESTful api는 [[REST]]원칙을 철저하게 준수하는 api
- 작동 방식
	- 인터넷 브라우징과 동일함
	1. 클라이언트가 서버에 요청 전송, 클라이언트가 API 문서에 따라 서버가 이해하는 방식으로 요청 형식 지정
	2. 서버가 클라이언트를 인증하고 해당 요청을 수행할 수 있는 권한이 클라이언트에 있는지 확인
	3. 서버가 요청 수신하고 처리
	4. 응답 반환, 성공 여부도 포함, 클라이언트가 요청한 모든 정보도 포함
- 클라이언트 요청에 포함된 내용
	- 고유 리소스 식별자, 일반적으로 URL사용
	- 매서드
		- GET: 서버의 지정된 URL에 있는 리소스에 액서스, 요청을 캐싱하고 전송전 데이터를 필터링 하도록 서버에 지시 가능
		- POST: 서버에 데이터 전송, 요청에 데이터 표현이 포함, 동인한 POST요청 전송시 동일한 리소스 생성하는 부작용
		- PUT: 기존 리소스를 업데이트, POST와 달리 여러번 전송해도 결과는 동일
		- DELETE: 리소스 제거,DELETE 요청은 서버  상태를 변경할 수 있음, 적절한 인증이 없을 경우 실패
	- HTTP 헤더
		- 클라 서버간 메타 데이터
		- 데이터
		- 파라미터
- 인증 방법
	- HTTP 인증
		- 기본 인증: 요청 헤더에 사용자 이름과 암호를 넣어 전송, 안전한 전송을 위해 base64로 인코딩해서 전달
		- 전달자 인증: bearer 인증, 토큰 전달자에 대한 액세스 제어를 제공하는 프로세스, 서버가 로그인 요청에 대한 응답으로 생성하는 암호화된 문자열(토큰)을 클라이언트에서 헤더에 넣어 전송 
	- API 키
		- 서버는 고유하게 생성된 값을 클라이언트에 할당, 클라이언트는 리소스에 액세스 할려고 할때마다 고유한 API 키를 사용해서 검증, 이경우 클라이언트에서 키를 전송해야해서 네트워크 도난에 취약
	- OAuth
		- 암호와 토큰을 결합, 서버는 먼저 암호를 요청한다음 권한 부여 프로세스를 완료하기 위해 추가 토큰 요청
- 응답 내용
	- 상태 표시줄
	- 메시제 본문
	- 헤더

### 코드 스니펫 (선택)

```typescript
```
