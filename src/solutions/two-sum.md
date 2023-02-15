---
title: Two Sum
problemUrl: https://leetcode.com/problems/two-sum/
tags:
  - python
---

**My Solution**:

```py
def twoSum(nums: List[int], target: int) -> List[int]:
    for i in range(len(nums)):
      y = target - nums[i]
      sublist = nums[i+1:]
      if y in sublist:
          return [i, nums.index(y, i+1)]
```

```py
# O(n^2)

def twoSum(nums: List[int], target: int) -> List[int]:
    for i in range(len(nums) - 1):
        for num in nums[i+1:]:
            if nums[i] + num == target:
                return [i, nums[i+1:].index(num) + i + 1]
```
