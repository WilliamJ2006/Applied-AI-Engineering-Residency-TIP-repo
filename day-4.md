# Day 4

Problem:
leetcode link:

```js
//js solution
```

Input:

Output:

Algorith:
containsDuplicate: create a set to remove duplicates and compare length of set to original.

groupAnagrams: sort each value in strs, and check if the sorted string exists in our dictionary, if it doesnt set it to an empty list, if it does append the unsorted string to the array with the key of the sorted string. At the end return the values of the object converted to a list.

Python Solution:

```py
# solution here
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        nums_set = set(nums)
        if len(nums_set) != len(nums): return True
        return False


class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        obj = {}
        for i in range(len(strs)):
            sorted_str = ''.join(sorted(strs[i]))
            if not sorted_str in obj: obj[sorted_str] = []
            obj[sorted_str].append(strs[i])
        return list(obj.values())
```
