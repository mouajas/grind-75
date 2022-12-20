## Two Sum:
> Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.
> You may assume that each input would have ***exactly one solution***, and you may not use the same element twice.
> You can return the answer in any order. <br/><br/>
> [LeetCode Link](https://leetcode.com/problems/two-sum/description/)

## Solution: 
``` python
prev = {}
for i, n in enumerate(nums):
    diff = target - n
    if diff in prev:
        return [prev[diff], i]
    prev[n] = i
```

## Time Complexity: O(n)
> Explanation here

## Space Complexity: O(n)
> Explanation here

## Explanation:
> Explanation here
