# Day 5

Problem:
leetcode link:

```js
//js solution
```

Input:

Output:

Algorith:

palindrome: two pointer, while front pointer is less then or equal to our back pointer, we check our values at both pointers after converting x to a string. if they're not equal return false, if they are increment front and decrement back, once the loop exits, return true.

threeSum:

Python Solution: sort the array, then iterate through each value as the first number in a possible triplet. Use two pointers, one starting after the current value and one at the end of the array, and increment and decrement to move them inward based on whether the sum is too small or too large. When the sum is zero we add the triplet to the output and skip any duplicate values to avoid repeated results.

```py
# solution here
class Solution(object):
    def isPalindrome(self, x):
        front = 0
        back = len(str(x))-1
        while front <= back:
            if str(x)[front] != str(x)[back]: return False
            front=front+1
            back=back-1
        return True

class Solution:
    def threeSum(self, nums: list[int]) -> list[list[int]]:
        nums.sort()
        output = []
        for i in range(len(nums)-2):
            if i > 0 and nums[i] == nums[i-1]:
                continue
            j = i + 1
            k = len(nums) - 1
            while j < k:
                total = nums[i] + nums[j] + nums[k]
                if total == 0:
                    output.append([nums[i], nums[j], nums[k]])
                    while j < k and nums[j] == nums[j+1]:
                        j += 1
                    while j < k and nums[k] == nums[k-1]:
                        k -= 1
                    j += 1
                    k -= 1
                elif total < 0:
                    j += 1
                else:
                    k -= 1
        return output
```
