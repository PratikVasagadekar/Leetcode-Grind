## LC-12. Integer to Roman <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def intToRoman(self, num: int) -> str:
        roman_val = {1000:'M',900:'CM',500:'D',400:'CD',100:'C',90:'XC',50:'L',40:'XL',10:'X',9:'IX',5:'V',4:'IV',1:'I'}
        roman = ''
        for each in roman_val.keys():
            if num >= each:
                roman =  roman + roman_val[each] * (num // each)
                num = num % each
        return roman
```
