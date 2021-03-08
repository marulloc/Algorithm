# Sort() vs Sort(Compare Function)

- 매개변수가 없는 sort() 메소드는 ASCII 문자 기준으로 오름차순 정렬을 한다.

  - 따라서 `[10,2].sort()`의 경우 [10, 2]가 반환된다.

- Sort(Compare Function)에서 Compare Function은 인자 2개를 받는다.
  - 음수를 반환하면 오름차순으로 정렬하고
  - 양수를 반환하면 내림차순으로 정렬한다.

### Compare Function example

#### 정수 비교의 경우

```js
// 오름차순
arr.sort((a, b) => a - b);
```

- a = 3, b = 2인 경우 a-b는 양수가 반환된다. 따라서 이때는 내림차순으로 반환[2,3]이 된다.
- a = 2, b = 3인 경우 a-b는 음수가 반환된다. 따라서 오름차순[2,3]으로 반환된다.
- 각각의 경우가 양수/음수를 반환하면서 전체적으로 오름차순으로 반환된다.

```js
// 내림차순
arr.sort((a, b) => b - a);
```

- 내림차순의 경우도 위와 같은 로직이다.

#### 문자열, 객체 정렬

- 사전순으로 정렬할 때는 ASCII 순으로 정렬하는 매개변수 없는 sort() 메소드를 쓰면 된다.
- 그러나 문자열의 특정 인덱스로 정렬하는 등 정렬의 조건이 있거나, 객체를 정렬할 때는 분기문에서 양수를 반환하거나 음수를 반환하면서 조절하면 된다.