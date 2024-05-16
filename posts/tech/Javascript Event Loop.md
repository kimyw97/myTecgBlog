### 날짜와 시간

- 날짜: 2024-05-02
- 시간: 13:16

### 주제 또는 키워드
[[JavaScript]]
[[Event Loop]]
### 간단한 내용
- 구성 요소
	- Call [[Stack]]
		- 실행중인 코드의 함수 호출을 추적
		- 함수가 호출되면 스택에 푸시되고 끝나면 pop함
		- 스택이 비어 있으면 task 큐에서 다음 작업을 가져옴
	- [[Heap]]
		- 객체가 저장되는 메모리 영역, 단순히 메모리의 큰 영역을 지칭
		- 동적으로 생성된 데이터를 저장
	- Task [[Queue]]
		- 외부 비동기 처리 함수에서 발생하는 이벤트와 콜백 함수를 저장
		- 이벤트 루프가 Call Stack이 비어을때 확인해서 실행할 task를 가져옴
	- Microtask [[Queue]]
		- promise 같은 비동기 작업의 콜백을 저장
		- Task Queue보다 우선순위가 높음
- 동작 과정
	1. Call Stack 확인
		- 호출 스택 확인하여 테스크가 남아있는지 확인
		- 비어 있으면 다음 단게
	2. Microtask Queue 처리
		- 비어 있지 않다면 모든 테스크를 처리
		- 새로운 task가 추가되면 계속 처리
	3. 랜더링
		- 브라우저는 특정 조건에서 화면을 업데이트
	4. Task Queue 확인
		- Microtask Queue가 비어 있다면 Task Queue에서 가져와서 Call Stack에 넣어주고 실행
		- Task Queue가 비워질 때까지 반복

### 코드 스니펫 (선택)

```typescript
```
