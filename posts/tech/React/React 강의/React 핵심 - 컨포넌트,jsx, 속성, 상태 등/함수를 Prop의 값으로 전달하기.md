### 날짜와 시간

- 날짜: 2024-01-24
- 시간: 23:46

### 주제 또는 키워드
- [[React]]
- 함수를 prop으로 전달하기

### 간단한 내용



### 코드 스니펫 (선택)

```JSX
function handleClick() {  
    
}
<TabButton onSelect={handleClick}>Components</TabButton>
// 

export default function TabButton(props) {  
  return (  
    <li>  
      <button onClick={props.onselect}>{props.children}</button>  
    </li>  
  );  
}
```
