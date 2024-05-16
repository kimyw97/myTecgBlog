### 날짜와 시간

- 날짜: 2023-10-02
- 시간: 18:00

### 주제 또는 키워드

[[React]]
- How to correctly update an object in React state
- How to update a nested object without mutating it
- What immutability is, and how not to break it
- How to make object copying less repetitive with Immer
### 간단한 내용

- object.x 이런식으로 사용하면 state update가 되지 않고 render하지 않음
```JavaScript
setFunction({
...object,
value: target.value
})
```
- 중첩된 객체의 경우 새 객체를 사용하여 spread 구문 사용
- 깊게 중첩된 객체의 경우 immer를 사용하면 편함
	1. Run `npm install use-immer` to add Immer as a dependency
	2. Then replace `import { useState } from 'react'` with `import { useImmer } from 'use-immer'`
``` JavaScript
const [person, updatePerson] = useImmer({
    name: 'Niki de Saint Phalle',
    artwork: {
      title: 'Blue Nana',
      city: 'Hamburg',
      image: 'https://i.imgur.com/Sd1AgUOm.jpg',
    }
  });
  
function handleNameChange(e) {
    updatePerson(draft => {
      draft.name = e.target.value;
    });
  }

```
### 코드 스니펫 (선택)

``` JavaScript
// state 업데이트 안됨
onPointerMove={e => {  

position.x = e.clientX;  

position.y = e.clientY;  

}}
// state 업데이트
onPointerMove={e => {  

setPosition({  

x: e.clientX,  

y: e.clientY  

});  

}}
```