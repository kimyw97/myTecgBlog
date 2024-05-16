### 날짜와 시간

- 날짜: 2024-04-29
- 시간: 11:24

### 주제 또는 키워드
[[Algorithm]]

### 간단한 내용
- 입력 데이터를 변형시킬때 추가적인 저장 공간을 거의 사용하지 않는 알고리즘
- 공간 복잡도를 최소화하기 위해 사용

### 코드 스니펫 (선택)

```typescript
function reverseInPlaceWithFor(arr: number[]): number[] {
    let n = arr.length;
    for (let i = 0; i < n / 2; i++) {
        let temp = arr[i];
        arr[i] = arr[n - 1 - i];
        arr[n - 1 - i] = temp;
    }
    return arr;
}

function reverseNonInPlace(arr: number[]): number[] {
    let result: number[] = [];
    for (let i = arr.length - 1; i >= 0; i--) {
        result.push(arr[i]);
    }
    return result;
}


```
