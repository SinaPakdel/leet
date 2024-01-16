## 136 - 
- Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.
- You must implement a solution with a linear runtime complexity and use only constant extra space.
```
    fun findSingleNumber(nums: IntArray): Int {
        val n = nums.size
        for (i in 0 until n) {
            var count = 0
            for (j in 0 until n) {
                if (i != j && nums[i] == nums[j]) {
                    count++
                    break
                }
            }
            if (count == 0) {
                return nums[i]
            }
        }
        return -1
    }
```
