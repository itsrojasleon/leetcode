<div align="center">
  <h1>66. Plus One</h1>
  <a href="https://leetcode.com/problems/plus-one/" target="_blank">plus one problem</a>
</div>

### Instructions

Given a non-empty array of digits representing a non-negative integer, plus one to the integer.

The digits are stored such that the most significant digit is at the head of the list, and each element in the array contain a single digit.

You may assume the integer does not contain any leading zero, except the number 0 itself.

### Example 1:

```shell
Input: [1,2,3]
Output: [1,2,4]
Explanation: The array represents the integer 123.
```

### Example 2:

```shell
Input: [4,3,2,1]
Output: [4,3,2,2]
Explanation: The array represents the integer 4321.
```

### Solution

```javascript
var plusOne = function(digits) {
  let one = 1;
  let resultItem = 0;
  for (let i = digits.length - 1; i >= 0; i--) {
    resultItem = digits[i] + one;
    one = parseInt(resultItem / 10);
    resultItem == 10 ? (digits[i] = 0) : (digits[i] = resultItem);
  }
  if (one > 0) digits.unshift(one);
  return digits;
};

// plusOne([1,2,3, 0]);
plusOne([6, 1, 4, 5, 3, 9, 0, 1, 9, 5, 1, 8, 6, 7, 0, 5, 5, 4, 3]);
```
