
# LC-13. Roman to Integer

Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M.

Symbol       Value
I             1
V             5
X             10
L             50
C             100
D             500
M             1000
For example, 2 is written as II in Roman numeral, just two one's added together. 12 is written as XII, which is simply X + II. The number 27 is written as XXVII, which is XX + V + II.

Roman numerals are usually written largest to smallest from left to right. However, the numeral for four is not IIII. Instead, the number four is written as IV. Because the one is before the five we subtract it making four. The same principle applies to the number nine, which is written as IX. There are six instances where subtraction is used:

I can be placed before V (5) and X (10) to make 4 and 9. 
X can be placed before L (50) and C (100) to make 40 and 90. 
C can be placed before D (500) and M (1000) to make 400 and 900.
Given a roman numeral, convert it to an integer.



## Solution 

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

