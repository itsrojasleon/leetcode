<div align="center">  
  <h1>242. Valid Anagram</h1>
  <a href="https://leetcode.com/problems/valid-anagram/">valid anagram problem</a>
</div>

### Instructions

Given two strings s and t , write a function to determine if t is an anagram of s.

### Example 1

```shell
Input: s = "anagram", t = "nagaram"
Output: true
```

### Example 2

```shell
Input: s = "rat", t = "car"
Output: false
```

### Note

You may assume the string contains only lowercase alphabets.

### Follow up

What if the inputs contain unicode characters? How would you adapt your solution to such case?

### Solution

```javascript
function cleanString(str) {
  return str
    .replace(/[^\w]/g, '')
    .toLowerCase()
    .split('')
    .sort()
    .join('');
}
function isAnagram(s, t) {
  return cleanString(s) === cleanString(t);
}
```
