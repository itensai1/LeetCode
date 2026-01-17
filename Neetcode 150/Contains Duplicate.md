### codes by *@itensai1*

> Java

```java
class Solution {
    public boolean hasDuplicate(int[] nums) {

       Arrays.sort(nums);
        for (int i = 1; i < nums.length; i++) {
            if (nums[i] == nums[i-1]) return true;
        }
        return false;
    }
}
```
<!--
> C++

```cpp

```
-->
> Python

```py
class Solution:
    def hasDuplicate(self, nums: List[int]) -> bool:

        return len(set(nums)) < len(nums)
```


<!-- 17-01-2026 -->
