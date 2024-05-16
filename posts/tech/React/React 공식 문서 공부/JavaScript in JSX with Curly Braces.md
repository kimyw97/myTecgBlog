### 날짜와 시간

- 날짜: 2023-10-01
- 시간: 21:30

### 주제 또는 키워드

- [[React]]
- 따음표 문자열 전달 법
- 중괄호 사용하여 JSX내에서 JavaScript 변수 참조하는 방법
- 중괄호 사용하여 JSX내에서 JavaScript 함수 호출하는 방법
- 중괄호 사용하여 JSX내에서 JavaScript 객체 사용하는 방법
### 간단한 내용

-  따옴표 안의 JSX속성은 문자열로 전달
- 중괄호 사용하면 JavaScript 논리와 변수를 마크업으로 가져올 수있음
- JSX태그 콘텐츠 내부 또는 = 속성 바로 뒤에 작동
- {{}} JSX중괄호 안에 집어넣은 JavaScript 객체
### 코드 스니펫 (선택)

``` JSX
export default function Avatar() {
  const avatar = 'https://i.imgur.com/7vQD0fPs.jpg';
  const description = 'Gregorio Y. Zara';
  return (
    <img
      className="avatar"
      src={avatar}
      alt={description}
    />
  );
}

```


### 추후 액션 아이템
[[Passing Props to a Components]]