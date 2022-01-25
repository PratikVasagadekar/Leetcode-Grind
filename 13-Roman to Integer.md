## LC-13. Roman to Integer <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def romanToInt(self, s: str) -> int:
        baseval = 0

        roman_val = dict(zip(["I","V","X","L","C","D","M"], [1,5,10,50,100,500,1000]))
        roman_val2 = dict(zip(["IV","IX","XL","XC","CD","CM"], [4,9,40,90,400,900]))

        for each in roman_val2.keys():
            if each in s:
                baseval = baseval + roman_val2[each]
                s = s.replace(each,"",1)

        for each in s:
            if each in roman_val.keys():
                baseval = baseval + roman_val[each]

        return baseval
```
