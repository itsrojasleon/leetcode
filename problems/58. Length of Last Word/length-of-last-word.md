<div align="center">
  <h1>58. Length of Last Word</h1>
  <a href="https://leetcode.com/problems/length-of-last-word/">length of last word problem</a>
</div>

### Instructions

Given a string s consists of upper/lower-case alphabets and empty space characters ' ', return the length of last word in the string.

If the last word does not exist, return 0.

### Note:

A word is defined as a character sequence consists of non-space characters only.

### Example:

```shell
Input: "Hello World"
Output: 5
```

### Solution

```javascript
var lengthOfLastWord = function(s) {
  if (!s || !s.split(' ').join('')) return 0;

  let splitted = s.split(' ');

  if (splitted.length > 1) {
    splitted = s.trim().split(' ');
  }

  let result = splitted[splitted.length - 1].length;
  return result > 0 ? result : 1;
};

// lengthOfLastWord("Hello World"); // === 5
// lengthOfLastWord("a "); // 1
//lengthOfLastWord(" a"); // 1
//lengthOfLastWord("       "); // 0
//lengthOfLastWord("    day "); // 3
lengthOfLastWord('Today is a nice day '); // 3
```
