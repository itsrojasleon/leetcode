<div align="center">
  <h1>258. Add Digits</h1>
  <a href="https://leetcode.com/problems/add-digits/" target="_blank">add digits problem</a>
</div>

### Instructions

Given a non-negative integer num, repeatedly add all its digits until the result has only one digit.

### Example

```shell
Input: 38
Output: 2
Explanation: The process is like: 3 + 8 = 11, 1 + 1 = 2.
```

### Solution

```javascript
// function reducer(acc, curr) {
//   return Number(acc) + Number(curr);
// }

// var addDigits = function(num) {
//   let value = num.toString().split('');
//   let n = value.reduce(reducer, 0);
//   while (n > 9) {
//     n = n
//       .toString()
//       .split('')
//       .reduce(reducer, 0);
//   }
//   return n;
// };

var addDigits = function(num) {
  return ((num - 1) % 9) + 1;
};
```
