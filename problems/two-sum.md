<div align="center">
  <h1>1. Two Sum</h1>
  <a href="https://leetcode.com/problems/two-sum" target="_blank">two sum problem</a>
</div>

### Instructions
Given an array of integers, return **indices** of the two numbers such that 
they add up to a specific target.

You may assume that each input would have **exactly** one solution,
and you may not use the same element twice.

### Examples
```shell
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

### Solution
```javascript
let val = [];

  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      if (nums[j] === target - nums[i]) {
        val.push(i, j);
      }
    }
  }
return val;
```