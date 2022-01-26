## LC-168. Excel Sheet Column Title <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def convertToTitle(self, columnNumber: int) -> str:
        title = ""
        while columnNumber:
            columnNumber, remainder = divmod(columnNumber - 1, 26)
            title += chr(remainder + ord('A'))

        return title[::-1]
```
