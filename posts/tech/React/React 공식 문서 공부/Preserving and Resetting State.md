### 날짜와 시간

- 날짜: 2023-10-15
- 시간: 15:36

### 주제 또는 키워드
[[React]]
- How React “sees” component structures
- When React chooses to preserve or reset the state
- How to force React to reset component’s state
- How keys and types affect whether the state is preserved

### 간단한 내용

- react는 ui tree를 사용, JSX로 부터
- state는 트리 위치와 연결되어 있다
- state는 같은 컨포넌트가 같은 위치에 랜더링하는 한 계속 유지된다
- 즉 react에서 ui tree에 위치에서 랜더링되는 동안 component의 state를 유지한다
- 예를 들어 css만 변경하는 checkbox를 이용해서 다시 randering하면 state값은 보존된다
- 같은 위치에 다시 rendering할경우 state는 초기화
- 그렇다면 state가 변경되면 랜더링을 다시하는것이지 초기화하는것이 아니다
- reset하고 싶다면 두가지 방법
	- 다른위치에 랜더링하기
	- key를 사용해서 랜더링하기
	- 
``` JSX
 <Chat key={to.id} contact={to} />

```
### 코드 스니펫 (선택)