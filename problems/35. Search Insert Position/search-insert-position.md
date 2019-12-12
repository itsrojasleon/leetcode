<div align="center">
  <h1>35. Search Insert Position</h1>
  <a href="https://leetcode.com/problems/search-insert-position/" target="_blank">search insert position problem</a>
</div>

### Instructions

Given a sorted array and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

You may assume no duplicates in the array.

### Example 1:

```shell
Input: [1,3,5,6], 5
Output: 2
```

### Example 2:

```shell
Input: [1,3,5,6], 2
Output: 1
```

### Example 3:

```shell
Input: [1,3,5,6], 7
Output: 4
```

### Example 4:

```shell
Input: [1,3,5,6], 0
Output: 0
```

### Solution

```javascript
var searchInsert = function(nums, target) {
  let low = 0;
  let high = nums.length - 1;
  let mid;

  while (low <= high) {
    mid = low + Math.floor((high - low) / 2);
    if (nums[mid] === target) {
      return mid;
    } else if (nums[mid] < target) {
      low = mid + 1;
    } else {
      high = mid - 1;
    }
  }
  return low;
};

searchInsert([1, 3, 5, 6], 5);
searchInsert([1, 3, 5, 6], 2);
searchInsert([1, 3, 5, 6], 0);
searchInsert([1, 3, 5, 6], 7);
searchInsert([2, 5], 1);
```
