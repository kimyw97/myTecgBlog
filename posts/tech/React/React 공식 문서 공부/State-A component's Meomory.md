### 날짜와 시간

- 날짜: 2023-10-02
- 시간: 16:15

### 주제 또는 키워드
[[React]]

- How to add a state variable with the [`useState`](https://react.dev/reference/react/useState) Hook
- What pair of values the `useState` Hook returns
- How to add more than one state variable
- Why state is called local
### 간단한 내용

- useState hook이 제공하는것
	- 랜더링 사이에 상태 변수를 유지
	- 변수를 업데이트하고 컴포넌트를 랜더링 하기위해 트리거
	- 다시 랜더링 할때 데이터를 저장하고 싶을때 사용ㅇ
- useState를 사용해서 선언, 두가지를 return, 상태와 상태업데이트 함수
- [[use]]에 의해 시작됨,
- top level에서 사용, import 와 비슷
- 여러개 선언 가능
- component끼리 isolated and private
### 코드 스니펫 (선택)

``` JavaScript
const [something, somethingSetFunction] = useState('initValue')
```
