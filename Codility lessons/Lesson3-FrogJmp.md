# [FrogJmp](https://app.codility.com/programmers/lessons/3-time_complexity/frog_jmp/)

```JAVA
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int X, int Y, int D) {
        return (Y-X)%D == 0 ? (Y-X)/D : (Y-X)/D + 1;
        // write your code in Java SE 8
    }
}
```