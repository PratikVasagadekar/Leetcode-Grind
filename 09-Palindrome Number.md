
# LC-09. Palindrome Number

Given an integer x, return true if x is palindrome integer.

An integer is a palindrome when it reads the same backward as forward.



## Solution 

```python 
class Solution:
    def isPalindrome(self, x: int) -> bool:
        reversed_number = 0
        loc = x
        if loc < 0: return False

        while loc > 0:
            reversed_number = (reversed_number * 10) + (loc % 10)
            loc = loc // 10

        if reversed_number == x: 
            return True
        else:
            return False
```

