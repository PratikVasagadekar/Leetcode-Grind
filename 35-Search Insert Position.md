## LC-35. Search Insert Position <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a>

```python
class Solution:
    def searchInsert(self, nums: List[int], target: int) -> int:
        start = 0
        end = len(nums) - 1

        if target in nums: return nums.index(target)
        if target < nums[0]: return 0
        if target > nums[end]: return end + 1

        while start <= end:
            mid = (start + end) // 2
            if target < nums[mid]:
                end = mid - 1
            if target > nums[mid]:
                start = mid + 1

        return start
```
