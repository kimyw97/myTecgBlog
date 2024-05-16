### 날짜와 시간

- 날짜: 2024-01-25
- 시간: 12:24

### 주제 또는 키워드
- [[React]]
- [[State]]
- [[Hooks]]

### 간단한 내용
- State
	- React에서 업데이트하기 위해 내장함수 사용해서 업데이트
	- 훅이 발동되면 컨포넌트가 재시작
- Hooks
	- use로 시작하는 함수들이 훅
	- 중첩은 허용하지 않음, 항상 컨포넌트 내 최상위에 존재
- 문법
```JSX
const [val, setVal] = useState('initial state value')
```
### 코드 스니펫 (선택)

```typescript
//Hooks 예시
function App() {
const [val, setVal] = useState(0);
}
// 안되는거

const [val, setVal] = useState(0);
function App() {
}

function App() {
if(condition){
const [val, setVal] = useState(0);
}
}

```
