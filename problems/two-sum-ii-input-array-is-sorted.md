<div align="center">
  <h1>167. Two Sum II - Input array is sorted</h1>
  <a href="https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/" target="_blank">two sum ii input array is sorted problem</a>
</div>

### Instructions

Given an array of integers that is already sorted in ascending order, find two numbers such that they add up to a specific target number.

The function twoSum should return indices of the two numbers such that they add up to the target, where index1 must be less than index2.

### Note

- Your returned answers (both index1 and index2) are not zero-based.
- You may assume that each input would have exactly one solution and you may not use the same element twice.

### Example

```shell
Input: numbers = [2,7,11,15], target = 9
Output: [1,2]
Explanation: The sum of 2 and 7 is 9. Therefore index1 = 1, index2 = 2.
```

### Solution

```javascript
var twoSum = function(numbers, target) {
  const visited = [];

  for (let index = 0; index < numbers.length; index++) {
    const element = numbers[index];
    if (visited[target - element] !== void 0) {
      return [visited[target - element], index + 1];
    }
    visited[element] = index + 1;
  }
  return [];
};
twoSum([0, 0, 0, 5, 2, 4], 9);
```
