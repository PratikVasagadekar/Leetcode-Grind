## LC-09. Palindrome Number <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

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
