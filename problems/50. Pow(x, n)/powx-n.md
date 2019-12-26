<div align="center">
  <h1>50. Pow(x, n)</h1>
  <a href="https://leetcode.com/problems/powx-n/">pow n problem</a>
</div>

### Instructions

Implement pow(x, n), which calculates x raised to the power n (xn).

### Example 1:

```shell
Input: 2.00000, 10
Output: 1024.00000
```

### Example 2:

```shell
Input: 2.10000, 3
Output: 9.26100
```

### Example 3:

```shell
Input: 2.00000, -2
Output: 0.25000
Explanation: 2-2 = 1/22 = 1/4 = 0.25
```

### Note:

```shell
-100.0 < x < 100.0
n is a 32-bit signed integer, within the range [−231, 231 − 1]
```

### Solution

```javascript
var myPow = function(x, n) {
  return x ** n;
};
```
