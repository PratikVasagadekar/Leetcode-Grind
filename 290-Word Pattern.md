## LC-290. Word Pattern <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def wordPattern(self, pattern: str, s: str) -> bool:
        words = s.split(" ")

        dictp = dict()

        if len(pattern) != len(words): return False
        if len(set(pattern)) != len(set(words)): return False

        for word, letter in zip(words,list(pattern)):
            if word not in dictp:
                dictp[word] = letter
            elif dictp[word] != letter:
                return False

        return True
```
