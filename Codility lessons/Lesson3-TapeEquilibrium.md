# [TapeEquilibrium](https://https://app.codility.com/programmers/lessons/3-time_complexity/tape_equilibrium/)

```java
// you can also use imports, for example:
import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int[] A) {
        int[] dp = new int[A.length+3];

        final int len = A.length;
        dp[0] = A[0];

        for (int i=1; i<len; i++) {
            dp[i] = dp[i-1] + A[i];
        }

        int mini = Integer.MAX_VALUE;
        for (int i=1; i<len; i++) {
            int left = dp[i-1];
            int right = dp[len-1]-dp[i-1];
            int temp = Math.abs(left-right);
            mini = Math.min(temp, mini);
        }
        return mini;
    }

    public static void main(String[] args) {
        Solution s = new Solution();
        System.out.println(s.solution(new int[] {3,1,2,4,3}));
    }
}

```
