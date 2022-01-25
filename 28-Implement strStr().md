## LC-28. Implement strStr() <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def strStr(self, haystack: str, needle: str) -> int:
        idx = haystack.index(needle) if needle in haystack else (-1 if not needle in haystack else 0)
        return idx
```
