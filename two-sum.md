# leet code TwoSum
### https://leetcode.com/problems/two-sum/


### golang

```go
func twoSum(nums []int, target int) []int {
    memo := make(map[int]int);

    for idx, num := range(nums) {
        if val, ok := memo[num]; !ok {
            complement := target - num;
            memo[complement] = idx;
        } else {
            return []int{val, idx};
        }
    }
    return nil
}
```

### python

```python
class Solution(object):
    def twoSum(self, nums, target):
        memo = dict()
        for idx, num in enumerate(nums):
            complement = target - num
            if num in memo:
                return [memo[num], idx]
            else:
                memo[complement] = idx
                
```

### java

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> memo = new HashMap<>();
        for (int i = 0; i< nums.length; i++) {
            int complement = target - nums[i];
            if (memo.get(nums[i]) != null) {
                return new int[]{memo.get(nums[i]), i};
            } else {
                memo.put(complement, i);
            }
        }
        return new int[]{};
    }
    
}
```
