### 날짜와 시간

- 날짜: 2024-01-24
- 시간: 18:10

### 주제 또는 키워드
- [[JavaScript]]에서 [[Optional chaining]]문법

### 간단한 내용
- 연산자: ?.
- 각 참조가 유효한지 명시적으로 검증하지 않고, 연결된 객체 체인 내에 깊숙이 위치한 속성 값을 읽을 수 있다.
- `?.`연산자는`.`([[Chaining]] 연산자)와 유사하게 작동하지만, 만약 참조가 [[nullish]]라면 에러가 발생하는 것 대신에 표현식의 리턴 값을 undefined로 단락된다. **함수 호출에서 사용될때 만약에 주어진 함수가 존재하지 않는다면, undefined를 리턴한다.
- 함수의 호출과 Optional chaining
	- 함수를 찾을 수 없을때 undefined를 반환

### 코드 스니펫 (선택)

```typescript
const adventurer = {
  name: 'Alice',
  cat: {
    name: 'Dinah',
  },
};

const dogName = adventurer.dog?.name;
console.log(dogName);
// Expected output: undefined

console.log(adventurer.someNonExistentMethod?.());
// Expected output: undefined

let object = {};
object?.property = 1; // Uncaught SyntaxError: Invalid left-hand side in assignment

let arrayItem = arr?.[42];
```


### 참고사이트
https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Optional_chaining