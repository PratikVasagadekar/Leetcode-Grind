## LC-66. Plus One <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def plusOne(self, digits: List[int]) -> List[int]:
        return list(str(int(''.join(map(str, digits))) + 1))
```
