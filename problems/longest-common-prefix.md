<div align="center">
  <h1>14. Longest Common Prefix</h1>
  <a href="https://leetcode.com/problems/longest-common-prefix/" target="_blank">longest common prefix problem</a>
</div>

### Instructions

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string "".

### Example 1:

```shell
Input: ["flower","flow","flight"]
Output: "fl"
```

### Example 2:

```shell
Input: ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.
```

### Note:

All given inputs are in lowercase letters a-z.

### Solution:

```javascript
const longestCommonPrefix = function(strs) {
  if (strs === null || strs.length === 0) return '';

  let prefix = strs[0];
  for (let i = 1; i < strs.length; i++) {
    let s = strs[i];
    let j = 0;
    while (
      j < prefix.length &&
      j < s.length &&
      prefix.charAt(j) === s.charAt(j)
    ) {
      j += 1;
    }
    prefix = prefix.substring(0, j);
  }
  return prefix;
};

// longestCommonPrefix(["flower","flow","flight"]);
// longestCommonPrefix(["a","a","b"]);
// longestCommonPrefix(["a"]);
// longestCommonPrefix([]);
// longestCommonPrefix(["c", "c"]);
```
