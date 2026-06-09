# Day 2

Problem: twoSum, maxProfit
leetcode link:

```js
//js solution
var twoSum = function (nums, target) {
  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      if (nums[i] + nums[j] === target) {
        return [i, j];
      }
    }
  }
};

var maxProfit = function (prices) {
  let min = Infinity;
  let profit = 0;
  for (let i = 0; i < prices.length; i++) {
    min = Math.min(min, prices[i]);
    profit = Math.max(profit, prices[i] - min);
  }
  return profit;
};
```

Input:

Output:

Algorith:
twoSum: For each element of nums, iterate through every number after the current element and check if the current element in addition to each of the numbers we're iterating through is equal to target, if it is, we return i and j.

maxProfit: for each value in prices, check if the current price is a new minimum value and then find the max between our current profit vs our profit when we subtract the current price from the minimum we've seen so far.

Python Solution:

```py
# solution here
class Solution(object):
    def twoSum(self, nums, target):
        for i in range(0, len(nums)):
            for j in range(i+1, len(nums)):
                if nums[i] + nums[j] == target: return [i, j]


class Solution(object):
    def maxProfit(self, prices):
        max_prof = 0
        min_stock = float('inf')
        for price in prices:
            min_stock = min(min_stock, price)
            max_prof = max(max_prof, price - min_stock)
        return max_prof
```
