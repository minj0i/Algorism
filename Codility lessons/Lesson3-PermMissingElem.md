# [PermMissingElem](https://app.codility.com/programmers/lessons/3-time_complexity/perm_missing_elem/)

```JAVA
// you can also use imports, for example:
import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int[] A) {
        Arrays.sort(A);

        for (int i = 0; i<A.length; i++) {
            if(i + 1 != A[i]) return i + 1;
        }
        return A.length + 1;
    }
}
```