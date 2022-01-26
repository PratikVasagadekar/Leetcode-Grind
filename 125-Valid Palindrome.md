## LC-125. Valid Palindrome <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
		def isPalindrome(self, s: str) -> bool:
			re_string = "".join(re.findall("[a-zA-Z0-9]+", s)).lower()
			N = int(len(re_string)/2)+1
			for i in range(1, N):
				if re_string[i-1] != re_string[-i]:
					return False
			return True
```
