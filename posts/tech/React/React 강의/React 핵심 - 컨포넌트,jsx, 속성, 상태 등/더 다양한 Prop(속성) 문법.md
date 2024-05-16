### 날짜와 시간

- 날짜: 2024-01-24
- 시간: 22:53

### 주제 또는 키워드
- [[React]]
- 다양한 Prop(속성) 문법

### 간단한 내용
- 단일 Prop 객체 전달
```JSX
<CoreConcept
title={CORE_CONCEPTS[0].title}
description={CORE_CONCEPTS[0].description}
image={CORE_CONCEPTS[0].image} />

// or

<CoreConcept
{...CORE_CONCEPTS[0]} />
```
- 받은 Prop들을 단일 객체로 그룹화
	- 받는 쪽에서 [[Rest Property]]문법 사용해서 단일 객체로 그룹화
```JSX
export default function CoreConcept({ ...concept }) {
// ...concept groups multiple values into a single object
// Use concept.title, concept.description etc.
// Or destructure the concept object: const { title, description, image } = concept;
}
```
- default set
```JSX
export default function Button({ caption, type = "submit" }) {
// caption has no default value, type has a default value of "submit"
}
// or

<Button type="submit" caption="My Button" />
```
### 코드 스니펫 (선택)

```typescript
```
