# 1. Two Sum

**Difficulty:** Easy  
**Topics:** Array, Hash Table  
**LeetCode Link:** https://leetcode.com/problems/two-sum

## Problem Statement

Given an array of integers `nums` and an integer `target`, return the indices of the two numbers that add up to `target`.

You may assume that each input has **exactly one solution**, and you may **not use the same element twice**.

You can return the answer in **any order**.

### Example 1:
```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: nums[0] + nums[1] == 9, so we return [0, 1].
```

### Example 2:
```
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

### Example 3:
```
Input: nums = [3,3], target = 6
Output: [0,1]
```

### Constraints:
- `2 <= nums.length <= 10^4`
- `-10^9 <= nums[i] <= 10^9`
- `-10^9 <= target <= 10^9`
- Only one valid answer exists.

## Approach

**Algorithm:** Hash Map / Dictionary
- Use a hash map to store the value and its index
- For each number, check if `target - num` exists in the map
- If it exists, we found our pair; otherwise, add current number to map

**Time Complexity:** O(n) - Single pass through array
**Space Complexity:** O(n) - Hash map storage

## Solutions

### Java
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        // HashMap to store value and its index
        Map<Integer, Integer> map = new HashMap<>();
        
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            
            // Check if complement exists in map
            if (map.containsKey(complement)) {
                return new int[] { map.get(complement), i };
            }
            
            // Add current number to map
            map.put(nums[i], i);
        }
        
        return new int[] {}; // Should never reach here
    }
}
```

### Python
```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        # Dictionary to store value and its index
        num_map = {}
        
        for i, num in enumerate(nums):
            complement = target - num
            
            # Check if complement exists in dictionary
            if complement in num_map:
                return [num_map[complement], i]
            
            # Add current number to dictionary
            num_map[num] = i
        
        return []  # Should never reach here
```

### C++
```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        // Unordered map to store value and its index
        unordered_map<int, int> map;
        
        for (int i = 0; i < nums.size(); i++) {
            int complement = target - nums[i];
            
            // Check if complement exists in map
            if (map.find(complement) != map.end()) {
                return {map[complement], i};
            }
            
            // Add current number to map
            map[nums[i]] = i;
        }
        
        return {}; // Should never reach here
    }
};
```
