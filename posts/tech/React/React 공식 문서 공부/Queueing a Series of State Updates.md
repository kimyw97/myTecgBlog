### 날짜와 시간

- 날짜: 2023-10-02
- 시간: 17:41

### 주제 또는 키워드

[[React]]
- What “batching” is and how React uses it to process multiple state updates
- How to apply several updates to the same state variable in a row

### 간단한 내용

- React는 이벤트 핸들러의 코드가 모두 끝난뒤 State를 업데이트한다(주문을 다 받은 후 주방에 전달)
- React는 클릭과 같은 이벤트를 일괄 처리하지않음(별도로 처리)
- 상태 설정 내부에서는 기존 랜더링 변수를 변경하지 않지만 새 랜더링을 요청
- 하나의 이벤트에서 일부 상태를 여러번 업데이트하면 업데이트 기능을 사용할수 있음

### 코드 스니펫 (선택)
