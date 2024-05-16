### 날짜와 시간

- 날짜: 2023-10-02
- 시간: 18:39

### 주제 또는 키워드
[[React]]
- How to add, remove, or change items in an array in React state
- How to update an object inside of an array
- How to make array copying less repetitive with Immer

### 간단한 내용
| |avoid (mutates the array)|prefer (returns a new array)|
|---|---|---|
|adding|`push`, `unshift`|`concat`, `[...arr]` spread syntax ([example](https://react.dev/learn/updating-arrays-in-state#adding-to-an-array))|
|removing|`pop`, `shift`, `splice`|`filter`, `slice` ([example](https://react.dev/learn/updating-arrays-in-state#removing-from-an-array))|
|replacing|`splice`, `arr[i] = ...` assignment|`map` ([example](https://react.dev/learn/updating-arrays-in-state#replacing-items-in-an-array))|
|sorting|`reverse`, `sort`|copy the array first ([example](https://react.dev/learn/updating-arrays-in-state#making-other-changes-to-an-array))|

- Immer를 사용해도 좋음
- change object in Array 
```JavaScript
setMyList(myList.map(artwork => {
  if (artwork.id === artworkId) {
    // Create a *new* object with changes
    return { ...artwork, seen: nextSeen };
  } else {
    // No changes
    return artwork;
  }
// 이렇게 안하면 참조될수있음
```
### 코드 스니펫 (선택)

```JavaScript
//adding spread syntax
setArtists(
	[ // with a new array  
		...artists, // that contains all the old items  
		{ id: nextId++, name: name } // and one new item at the end  
	]  
);

//removing
setArtists(  
	artists.filter(a => a.id !== artist.id)  //target id를 제외하고 만든 새로운 배열
);

//transforming
  function handleClick() {
    const nextShapes = shapes.map(shape => {
      if (shape.type === 'square') {
        // No change
        return shape;
      } else {
        // Return a new circle 50px below
        return {
          ...shape,
          y: shape.y + 50,
        };
      }
    });
    // Re-render with the new array
    setShapes(nextShapes);
  }
//replacing
 function handleIncrementClick(index) {
    const nextCounters = counters.map((c, i) => {
      if (i === index) {
        // Increment the clicked counter
        return c + 1;
      } else {
        // The rest haven't changed
        return c;
      }
    });
    setCounters(nextCounters);
  }
//inserting
  function handleClick() {
    const insertAt = 1; // Could be any index
    const nextArtists = [
      // Items before the insertion point:
      ...artists.slice(0, insertAt),
      // New item:
      { id: nextId++, name: name },
      // Items after the insertion point:
      ...artists.slice(insertAt)
    ];
    setArtists(nextArtists);
    setName('');
  }
//reverse() or filter or sort
  function handleClick() {
    const nextList = [...list];
    nextList.reverse();
    setList(nextList);
  }
```
