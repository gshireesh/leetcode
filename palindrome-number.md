## Palindrome Number

### https://leetcode.com/problems/palindrome-number/


```java
class Solution {
    public boolean isPalindrome(int x) {
        String x1 = "" + x;
        int i = 0, j = x1.length() - 1;
        while (i<j) {
            if (x1.charAt(i) != x1.charAt(j)) {
                return false;
            }
            i += 1;
            j -= 1;
        }
        return true;
    }
}
```
