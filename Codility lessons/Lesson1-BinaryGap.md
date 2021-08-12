# [BinaryGap](https://app.codility.com/programmers/lessons/1-iterations/binary_gap/)

```JAVA
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int N) {
        // write your code in Java SE 8
        int gap = 0;
        String binaryString = Integer.toBinaryString(N);

        int startIndex = binaryString.indexOf("1");

        if(startIndex == -1) {
            return 0;
        }

        while(true) {
            int secondIndex = binaryString.indexOf("1", startIndex + 1);

            if (secondIndex == -1) {
                break;
            }

            int diff = secondIndex - startIndex - 1;
            gap = Math.max(diff, gap);

            startIndex = secondIndex;
        }

        return gap;
    }
}

```