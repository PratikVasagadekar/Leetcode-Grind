
# LC-04. Median of Two Sorted Arrays

Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.



## Solution 

```python 
class Solution:
    def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
        nums = sorted(sorted(nums1) + sorted(nums2))

        if len(nums) % 2 == 0:
            length = len(nums)
            mid_idx= math.ceil(length/2)
            calc = (nums[mid_idx] + nums[mid_idx - 1]) / 2
            return calc
        elif len(nums) % 2 == 1:
            calc= nums[math.ceil(len(nums)/2)-1]
            return calc
        elif len(nums1) == 0 or len(nums2)==0:
            return nums[0]
        else:
            return None
```

