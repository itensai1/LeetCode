### codes by *@itensai1*

> Java

```java
class Solution {
    public boolean isAnagram(String s, String t) {
        int[] cnt = new int[26];
        for (int i = 0; i < s.length(); i++) {
            cnt[s.charAt(i) - 'a']++;
        }
        for (int i = 0; i < t.length(); i++) {
            cnt[t.charAt(i) - 'a']--;
        }
        for (int i : cnt)
            if (i != 0)
                return false;   
        return true;
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
    def isAnagram(self, s: str, t: str) -> bool:
        return sorted(s) == sorted(t)
```


<!-- 17-01-2026 -->
