<div align="center">  
  <h1>217. Contains Duplicate</h1>
  <a href="https://leetcode.com/problems/contains-duplicate/">contains duplicate problem</a>
</div>

### Instructions

Given an array of integers, find if the array contains any duplicates.

Your function should return true if any value appears at least twice in the array, and it should return false if every element is distinct.

### Example 1:

```shell
Input: [1,2,3,1]
Output: true
```

### Example 2:

```shell
Input: [1,2,3,4]
Output: false
```

### Example 3:

```shell
Input: [1,1,1,3,3,4,3,2,4,2]
Output: true
```

### Solution:

```javascript
const containsDuplicate = function(nums) {
  let numMap = {};
  let result = false;

  for (let num of nums) {
    numMap[num] = numMap[num] + 1 || 1;
  }

  // Object.values(numMap) === [1, 2, 3]

  for (let val of Object.values(numMap)) {
    if (val > 1) {
      result = true;
      break;
    }
  }
  return result;
};
```
