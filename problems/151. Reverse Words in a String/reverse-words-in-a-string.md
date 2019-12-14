<div align="center">
  <h1>151. Reverse Words in a String</h1>
  <a href="https://leetcode.com/problems/reverse-words-in-a-string/" target="_blank">reverse words in a string problem</a>
</div>

### Instructions

Given an input string, reverse the string word by word.

### Example 1

```shell
Input: "the sky is blue"
Output: "blue is sky the"
```

### Example 2

```shell
Input: "  hello world!  "
Output: "world! hello"
Explanation: Your reversed string should not contain leading or trailing spaces.
```

### Example 3

```shell
Input: "a good   example"
Output: "example good a"
Explanation: You need to reduce multiple spaces between two words to a single space in the reversed string.
```

### Note

- A word is defined as a sequence of non-space characters.
- Input string may contain leading or trailing spaces. However, your reversed string should not contain leading or trailing spaces.
- You need to reduce multiple spaces between two words to a single space in the reversed string.

### Solution

```javascript
var reverseWords = function(s) {
  return s
    .split(' ')
    .filter(v => v !== '')
    .reverse()
    .join(' ');
};
```
