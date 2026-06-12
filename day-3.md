# Day 3

Problem:
leetcode link:

```js
//js solution
```

Input:

Output:

Algorith:
reverseString: create a copy of either front or back values in the array to reassign the front and back to the corresponding copies.

lols: sliding window and a dictionary to keep track of the most recent index of each character. When a duplicate character is found in current window, move the front pointer past the right and update the maximum substring length found so far.

Python Solution:

```py
# solution here
class Solution:
    def reverseString(self, s: List[str]) -> None:
        front = 0
        back = len(s)-1
        while front < back:
            frontValue = s[front]
            backValue = s[back]
            s[front] = backValue
            s[back] = frontValue
            front+=1
            back-=1
        return s


class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        seen = {}
        front = 0
        max_length = 0
        for right in range(len(s)):
            if s[right] in seen and seen[s[right]] >= front:
                front = seen[s[right]]+1
            seen[s[right]] = right
            max_length = max(max_length, right-front+1)
        return max_length
```
