<div align="center">  
  <h1>509. Fibonacci Number</h1>
  <a href="https://leetcode.com/problems/fibonacci-number/">fibonacci number problem</a>
</div>

### Instructions

The Fibonacci numbers, commonly denoted F(n) form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from 0 and 1. That is,

```shell
F(0) = 0,   F(1) = 1
F(N) = F(N - 1) + F(N - 2), for N > 1.
```

Given N, calculate F(N).

### Example 1:

```shell
Input: 2
Output: 1
Explanation: F(2) = F(1) + F(0) = 1 + 0 = 1.
```

### Example 2:

```shell
Input: 3
Output: 2
Explanation: F(3) = F(2) + F(1) = 1 + 1 = 2.
```

### Example 3:

```shell
Input: 4
Output: 3
Explanation: F(4) = F(3) + F(2) = 2 + 1 = 3.
```

### Note:

0 ≤ `N` ≤ 30.

### Solution:

```javascript
// This problem is solved with memoization
// You can remove the memo function and it will work correctly, a little
// bit slowly, but ok.

const memo = function(fn) {
  const cache = {};

  return function(...args) {
    if (cache[args]) {
      return cache[args];
    }

    let result = fn.apply(this, args);
    cache[args] = result;
    return result;
  };
};
var slowFib = function(N) {
  if (N < 2) {
    return N;
  }

  return fib(N - 1) + fib(N - 2);
};
const fib = memo(slowFib);
```
