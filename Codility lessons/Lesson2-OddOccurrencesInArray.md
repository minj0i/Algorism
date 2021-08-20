# [OddOccurrencesInArray](https://app.codility.com/programmers/lessons/2-arrays/odd_occurrences_in_array/)

```JAVA
import java.util.Set;
import java.util.HashSet;

class Solution {
    public int solution(int[] A) {
        Set<Integer> set = new HashSet<>();

        for (int i : A) {
            if(set.contains(i)) {
                set.remove(i);
            } else {
                set.add(i);
            }
        }

        return set.iterator().next();
    }
}
```

Set은 집합적인 개념의 Collection으로 순서의 의미가 없지만 Data를 중복해서 포함할 수 없는 특징을 가지고 있다.   
HashSet은 add() 메소드를 이용해 데이터 삽입,
next()를 이용해 데이터를 추출 할 수 있다.
Iterator를 이용해서 추출 할 수 있다.