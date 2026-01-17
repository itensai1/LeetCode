### codes by *@itensai1*

> Java

```java
class Solution {
    public List<List<String>> groupAnagrams(String[] strs) {
        HashMap<String, List<String>> map = new HashMap<>();
        for (String s : strs) {
            char[] arr = s.toCharArray();
            Arrays.sort(arr);
            String key = new String(arr);
            var updatedValue =  map.getOrDefault(key, new ArrayList<>());
            updatedValue.add(s);
            map.put(key, updatedValue);
        }
        return new ArrayList<>(map.values());
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
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:

        result = {}
        for s in strs:
            key = ''.join(sorted(s))
            if result.get(key):
                result[key] += [s]
            else:
                result[key]=[s]

        return list(result.values())
```


<!-- 17-01-2026 -->
