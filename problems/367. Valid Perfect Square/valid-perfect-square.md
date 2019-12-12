<div align="center">  
  <h1>367. Valid Perfect Square</h1>
  <a href="https://leetcode.com/problems/valid-perfect-square/">valid perfect square problem</a>
</div>

### Instructions

Given a positive integer num, write a function which returns True if num is a perfect square else False.

Note: Do not use any built-in library function such as `sqrt`.

### Example 1:

```shell
Input: 16
Output: true
```

### Example 2:

```shell
Input: 14
Output: false
```

### Solution:

```javascript
const isPerfectSquare = num => {
  for (let i = 1; i <= num; i++) {
    if (i * i === num) {
      return true;
    }
  }
  return false;
};
```
