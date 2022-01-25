## LC-70. Climbing Stairs <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def climbStairs(self, n: int) -> int:
        if n == 1:
            return(1)
        web = [1, 2]
        for i in range(2, n, 1):
            web.append(web[i-1] + web[i-2])
        return web[n-1]
```
