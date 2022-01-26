## LC-238. Product of Array Except Self <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution(object):
    def productExceptSelf(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        arr3 =[]
        arr3 = [1 for i in range(len(nums))]
        i, temp = 1, 1
        for i in range(len(nums)):
            arr3[i] = temp
            temp *= nums[i]
        temp = 1
        for i in range(len(nums) - 1, -1, -1):
            arr3[i] *= temp
            temp *= nums[i]
        return arr3
```
