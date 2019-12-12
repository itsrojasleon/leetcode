<div align="center">
  <h1>344. Reverse String</h1>
  <a href="https://leetcode.com/problems/reverse-string/" target="_blank">reverse string problem</a>
</div>

### Instructions

Write a function that reverses a string. The input string is given as an array of characters char[].

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

You may assume all the characters consist of printable ascii characters.

### Example 1:

```shell
Input: ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
```

### Example 2:

```shell
Input: ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]
```

### Solution

```javascript
const reverseString = function(s) {
  return s.reverse();
};
```
