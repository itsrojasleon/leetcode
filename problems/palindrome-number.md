<div align="center">
  <h1>9. Palindrome Number</h1>
  <a href="https://leetcode.com/problems/palindrome-number/" target="_blank"></a>
</div>

### Instructions

Determine whether an integer is a palindrome. An integer is a palindrome when it it reads the same backward as forward.

### Example 1:

```shell
Input: 121
Output: true
```

### Example 2:

```shell
Input: -121
Output: false
Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.
```

### Example 3:

```shell
Input: 10
Output: false
Explanation: Reads 01 from right to left. Therefore it is not a palindrome.
```

### Solution

```javascript
var isPalindrome = function(x) {
  let reversed = parseInt(
    x
      .toString()
      .split('')
      .reverse()
      .join('')
  );
  return reversed === x;
};
```
