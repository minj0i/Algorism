# [FrogRiverOne](https://app.codility.com/programmers/lessons/4-counting_elements/frog_river_one/)

```JAVA
// you can also use imports, for example:
import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int X, int[] A) {
        int result = -1;
        HashSet<Integer> set = new HashSet<>();
        for (int i=0; i< A.length; i++){
            set.add(A[i]);
            if(set.size() == X) {
                result = i;
                return result;
            }
        }
        return result;
    }
}
```