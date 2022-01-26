## LC-30. Substring with Concatenation of All Words <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def findSubstring(self, s: str, words: List[str]) -> List[int]:
        word_length = len(words[0])
        word_counter = Counter(words)
        op = []
        for i in range(len(s)-len(words)*word_length+1):
            freq=[s[i+j*word_length:i+(j+1)*word_length] for j in range(len(words))]
            if word_counter==Counter(freq):
                op.append(i)
        return op
```
