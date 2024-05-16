### 날짜와 시간

- 날짜: 2023-10-02
- 시간: 17:09

### 주제 또는 키워드

[[React]]
- How setting state triggers re-renders
- When and how state updates
- Why state does not update immediately after you set it
- How event handlers access a “snapshot” of the state

### 간단한 내용
- set State => re-render
- useState를 호출하면 React는 그 렌더링의 snapshot을 제공
- 모든 랜더링은 항상 그 랜더링의 snapshot을 봄
- 과거에 생선된 이벤트 핸들러는 그것들이 생성된 랜더링에서의 상태 값을 가짐

### 코드 스니펫 (선택)
``` JavaScript
// alert 0 이 보임
export default function Counter() {
  const [number, setNumber] = useState(0);

  return (
    <>
      <h1>{number}</h1>
      <button onClick={() => {
        setNumber(number + 5);
        setTimeout(() => {
          alert(number);
        }, 3000);
      }}>+5</button>
    </>
  )
}
```
