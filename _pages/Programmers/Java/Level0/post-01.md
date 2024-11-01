---
title: "중복된 숫자 개수"
date: "2024-11-01"
thumbnail: "/images/programmers.png"
tags:
    - Programmers
    - java
    - level0
    - algorithm
---



-----
# 문제 설명

<p>정수가 담긴 배열 <code>array</code>와 정수 <code>n</code>이 매개변수로 주어질 때, <code>array</code>에 <code>n</code>이 몇 개 있는 지를 return
  하도록 solution 함수를 완성해보세요.</p>

<hr>

# 제한사항

<ul>
  <li>1 ≤ <code>array</code>의 길이 ≤ 100</li>
  <li>0 ≤ <code>array</code>의 원소 ≤ 1,000</li>
  <li>0 ≤ <code>n</code> ≤ 1,000</li>
</ul>

<hr>

# 입출력 예
<table class="table">
  <thead>
    <tr>
      <th>array</th>
      <th>n</th>
      <th>result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>[1, 1, 2, 3, 4, 5]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <td>[0, 2, 3, 4]</td>
      <td>1</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<hr>

# 입출력 예 설명

### 입출력 예 #1
[1, 1, 2, 3, 4, 5] 에는 1이 2개 있습니다.
### 입출력 예 #2
[0, 2, 3, 4] 에는 1이 0개 있습니다.

<hr>

# 문제 풀이
``` java
public int solution(int[] array, int n) {
    int answer = 0;
    for (int i : array) {
        if (i == n) {
            answer += 1;
        }
    }
    return answer;
}
```

<hr>

# 문제 해석
배열 array 변수를 반복문을 통해 각각의 원소에 접근하여, 매개변수 n 의 값과 동일한 값이 존재하는지 비교하고 만약, 값이 일치하는경우 answer 변수에 +1 처리 후 반복문이 종료되는 시점에서 answer 변수를 return 한다


