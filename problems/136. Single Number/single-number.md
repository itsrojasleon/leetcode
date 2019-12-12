<div align="center">
  <h1>136. Single Number</h1>
  <a href="https://leetcode.com/problems/single-number/" target="_blank">single number problem</a>
</div>

### Instructions

Given a non-empty array of integers, every element appears twice except for one. Find that single one.

### Note:

Your algorithm should have a linear runtime complexity. Could you implement it without using extra memory?

### Example 1:

```shell
Input: [2,2,1]
Output: 1
```

### Example 2:

```shell
Input: [4,1,2,1,2]
Output: 4
```

### Solution

```javascript
var singleNumber = function(nums) {
  let extra;
  let charMap = {};

  for (let num of nums) {
    charMap[num] = charMap[num] + 1 || 1;
  }

  for (let char in charMap) {
    if (charMap[char] === 1) {
      extra = parseInt(char);
    }
  }
  return extra;
};

singleNumber([4, 1, 2, 1, 2]);
```
