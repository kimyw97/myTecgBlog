1. 목적
	-  첫 랜더링에만 실행되길 원하는 경우
	-  [[State]]와는 상관없이 한번만 실행되길원하는 경우
	- 특정한 상황에만 실행이 되길 원하는 경우

2. 사용법
```JSX
const iRunOnlyOnce = () = {}
useEffect(iRunOnlyOnce, [])// fucntion // deps
//deps 
	useEffect(iRunOnlyOnce, [keyword])// fucntion keyword의 변화가 있을때만 실행
```