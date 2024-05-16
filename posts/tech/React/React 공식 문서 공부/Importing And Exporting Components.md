### 날짜와 시간

- 날짜: 2023-10-01
- 시간: 16:40

### 주제 또는 키워드

- [[React]]
- 리액트에서 Root component란
- Component를 가져오고 내보내는 법
- default and named exporting
- 하나의 파일에서 여러 component import export
- 여러 components 분할

### 간단한 내용

- export는 두가지
- default, named 
	- 관련 링크 https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/export#using_the_default_export
``` javascript
export default name1();
export name2();
////////

import name1 from '...'
import {name2} from '...'
```
### 코드 스니펫 (선택)

```
// Redux 예시 
const initialState = { count: 0 };
function reducer(state = initialState, action) {   // ... }
```


### 추후 액션 아이템

[[Writing Markup with JSX]]