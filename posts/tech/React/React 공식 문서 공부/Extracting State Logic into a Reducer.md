### 날짜와 시간

- 날짜: 2023-10-15
- 시간: 16:27

### 주제 또는 키워드
[[React]]
- What a reducer function is
- How to refactor `useState` to `useReducer`
- When to use a reducer
- How to write one well
### 간단한 내용

- `useState`에서 `useReducer`로 migration하는 3단계
	1. **Move** from setting state to dispatching actions.
	2. **Write** a reducer function.
	3. **Use** the reducer from your component
- Comparing `useState` and `useReducer`
	- **Code size**: 일반적으로  `useState` 가 미리 작성해야하는 코드르 줄이지만 `useReducer`를 사용하면 reducer 함수와 dispatch action을 둘다 작성해야함, 대신 다양한 이벤트 변경의 상황에서는 줄이는데 효율적임
	- **Readability**: `useState`가  간단히 업데이트 할 때 보통 쉽다. 하지만 그것들이 복잡해질때는 고착될수있고 스캔하기 어려워진다. 이경우에는 `useReducer`가 좋음
	- **Debugging**: `useState`를 사용할경우 어디서 버그가 생겼는지 알기 힘들지만 `useReducer`를 사용 할 경우 어떤 action에서 발생했는지 console을 통해 알수 있다. 하지만 `useState`보다 더 많은 코드를 작성해야한다
	- **Testing**:  Reducer는 컨포넌트에 의존하지 않는 함수이다. 그렇기 때문에 독립된 환경에서 분리하여 테스트하고 내보내기 쉽다. 일반적으로 실제 환경과 비슷한 환경에서 테스트하는것이 좋지만 
	- **Personal preference**: 둘다  개인적인 선호도 차이
- Reducers 잘 사용하기
	- **Reducers must be pure.**
	- **Each action describes a single user interaction, even if that leads to multiple changes in the data.**
### 코드 스니펫 (선택)
