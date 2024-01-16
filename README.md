## 136 - 
- Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.
- You must implement a solution with a linear runtime complexity and use only constant extra space.
```
fun findSingleNumber(nums: IntArray): Int {
    var result = 0
    for (num in nums) {
        result = result xor num
    }
    return result
}
```
