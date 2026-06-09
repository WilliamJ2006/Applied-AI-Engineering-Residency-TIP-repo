# Day 1

Problem: FizzBuzz

leetcode link: https://leetcode.com/problems/fizz-buzz/

```js
function fizzBuzz(n) {
  const result = [];
  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) {
      result.push('FizzBuzz');
    } else if (i % 3 === 0) {
      result.push('Fizz');
    } else if (i % 5 === 0) {
      result.push('Buzz');
    } else {
      result.push(String(i));
    }
  }
  return result;
}
```

Input:

Output:

Algorith: For every number divisible by 15 log fizzbuzz, fizz for divisible by 3, buzz if divisible by 5. Alternatively create an empty string for each value and add to the string depending on what it's divisble by.

Python Solution:

```py
# solution here
class Solution(object):
    def fizzBuzz(self, n):
        arr = []
        for i in range(1, n+1):
            s = ''
            if i%3 == 0: s = s+'Fizz'
            if i%5 == 0: s = s+'Buzz'
            arr.append(s or str(i))
        return arr
```
