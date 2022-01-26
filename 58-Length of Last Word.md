## LC-58. Length of Last Word <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def lengthOfLastWord(self, s: str) -> int:
        return (len(s.split()[-1]))
```
