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
> Iterating through `array` only one time while adding each value to the `hash map` in a constant time <br/>
> Worst case scenario would be checking every element in the `array`

## Space Complexity: O(n)
> Using extra memory from `hash map` <br/>
> Worst case scenario would be adding every element to the `hash map`

## Explanation:
> 1. Create an empty hash map
> 2. Iterate through nums array to check every value
> 3. Calculate the difference between the target value and current value in the array to use it
> 4. Use the difference to determine if the value exists in the hash map
> 5. If the value exists, then we will return the pair of indices because we found two values that add up to the target value
> 6. If the value does not exist, then we will add that value and its index to the hash map
>> Note: We do not have to `return` anything after the loop because we are guaranteed one solution
