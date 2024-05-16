[[react tutorial]] [[React]]

### 날짜와 시간

- 날짜: 2023-09-28
- 시간: 12:11

### 주제 또는 키워드

- ReactJS 개요

### 간단한 내용

- React란 Javascript 라이브러리
- 컴포넌트라는 작고 고립된 코드의 파편을 이용하여 복잡한 ui 구성
- 개별 컨포넌트는 <span style='color: purple'> props</span>라는 매개변수를 받아오고 <span style='color: purple'> render</strong>함수를 통해 표시할 뷰계층 구조를 반환
- render 함수는 화면을 보고자 하는 내용을 반환

### 코드 스니펫 (선택)

``` javascript
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}
```


### 추후 액션 아이템
