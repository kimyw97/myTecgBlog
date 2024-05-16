### 날짜와 시간

- 날짜: 2023-09-28
- 시간: 10:33

### 주제 또는 키워드

- [[React]]까지의 과정

### 간단한 내용

- 왜 react가 만들어진 이유
- 바닐라 자바스크립는 작은 기능을 많드는데 많은 시간이 소모(자원)
- 모든걸 자바스크립트를 통해 만들수 있음,
### 코드 스니펫 (선택)

```html
<!DOCTYPE html>
<-- 바닐라 자바스크립트 -->
<html>
	<body>
		<span>Total clicks: 0</span>
		<button id='btn'>Click me</button>
	</body>
	<script>
		let counter = 0;
		const button = document.getElementById('btn');
		const span = document.querySelector('span');
		function handleClick() {
			console.log('hi')
			counter = counter + 1;
			span.innerText = `Total clicks: ${{counter}}``
		}
		button.addEventListenr('clikc', handleClick);
	</script>
<html>

<-- 리액트 -->
<html>
	<body>
	<div id='root'> </div>
	</body>
	<script src='https://unpkg.com/react==@17.0.2==/umd/react.production.min.js'></script>
	<script src='https://unpkg.com/react-dom==@17.0.2==/umd/react-dom.production.min.js'></script>
	<script>
		const root = document.getElementById('root');
		const span = React.createElement('span', {id:'sexy-span'}, 'hello');
		ReactDOM.render(span,root)
	</script>
<html>

```
