### 날짜와 시간

- 날짜: 2023-10-17
- 시간: 19:31

### 주제 또는 키워드
	[[Refactoring]]
- Refactoring의 간단한 예시, 체험해보기

### 간단한 내용
- 설계가 나쁜 시스템은 수정하기 어렵다. 원하는 동작을 수행하도록 하기 위해서 수정해야할 부분을 찾고, 기존 코드와 잘 맞물려 작동하게 할 방법을 강구하기가 어렵기 때문이다.
<br>
- <strong style='color: red'>프로그램이 새로운 기능을 추가하기에 편한 구조가 아니라면, 먼저 기능을 추가하기 쉬운 형태로 리팩터링하고 나서 원하는 기능을 추가한다</strong>
<br>
- <strong style='color: red'>리팩토링하기 전에 제대로 된 테스트부터 마련한다. 테스트는 반드시 자가진단하도록 만든다.</strong>
<br>
- <strong style='color:red'>리팩터링은 프로그램 수정을 작은 단계로 나눠 진행한다. 그래서 중간에 실수하더라도 버그를 쉽게 찾을 수 있다.</strong>
<br>
- 매개변수의 역할이 뚜렷하지 않을 때는 부정관사(a,an)를 붙이자
<br>
- <strong style='color:red'>컴퓨터가 이해하는 코드는 바보도 작성할 수 있다. 사람이 이해하도록 작성하는 프로그래머가 진정한 실력자다</strong>
<br>
- 반복문이 많아저 성능이 걱정되어 리팩터링을 주저하지 말것, 대체로 미비하고 그 후에 성능을 개선해도 충분하다

- 먼저 프로그램의 논리적인 요소를 파악하기 쉽도록 코드의  구조를 보강하는데 주안점을 두고 리팩터링
<br>
- 캠핑자들에게는 "도착했을 때보다 깔끔하게 정돈하고 떠난다"는 규칙이 있다. 프로그래밍도 마찬가지다. 항싱 코드베이스를 작업 시작 전보다 건강하게 만들어놓고 떠나야 한다.
<br>
- <strong style='color:red'>좋은 코드를 가늠하는 확실한 방법은 '얼마나 수정하기 쉬운가'</strong>

### 코드 스니펫 (선택)

```JSON
/plays.json
{
  "hamlet": { "name": "Hamlet", "type": "tragedy" },
  "as-like": { "name": "As YOu Like it", "type": "comedy" },
  "othello": { "name": "Othello", "type": "tragedy" }
}
```

```JSON
/invoice.json
[
  {
    "customer": "BigCo",
    "performances": [
      { "playID": "hamlet", "audience": 55 },
      { "playID": "as-like", "audience": 35 },
      { "playID": "othello", "audience": 40 }
    ]
  }
]
```

``` JavaScript
function statement(invoice, plays) {
	let totalAmount = 0;
	let volumeCredit = 0;
	let result =`청구 내역 ( 고객명: ${invoice.customer}\n`;
	const format = new Intl.NumberFomat('en-Us', {style: 'currency', currency: 'USD', minimumFractionDigits: 2}).format;
	for (let perf of invoice.performances) {
		const play = play[perf.playID];
		let thisAmount = 0;
		switch (play.type) {
			case 'tragedy':
				thisAmount = 40000;
				if (perf.audience > 30) {
					thisAmount += 1000 * (perf.audience -30);
					break;
				}
			case 'comedy':
				thisAmount = 30000;
				if(perf.audience > 20) {
					thisAmount += 10000 + 500 * (perf.audience -20);
				}
				thisAmount += 300 * perf.audienc;
				break;
			default:
				throw new Error(`알 수 없는 장르: ${play.type}`);
		}
		// 포인트 적립
		volumeCredit += Math.max(perf.audience -30, 0);
		// 희극 관객 5명마다 추가 포인트 정립
		if ('comedy' === play.type) volumeCredit += Math.floor(perf.audience / 5);

		// 청구 내역 출력한다
		result += ` ${play.name}: ${format(thisAmount/100)} (${perf.audience}석\n`;
		totalAmount += thisAmount;
	}
	result += `총액: ${format(totalAmount/100)}\n`;
	result += `적립 포인트: ${volumeCredits}점\n`;
	return result;
}
```

- Intl: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl