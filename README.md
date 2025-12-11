# yaswanth
Given a list of Integers return the number of unique elements
import java.util.*;

public class UniqueCount {
    public static int countUnique(int[] nums) {
        if (nums.length == 0) return 0;
        
        Set<Integer> set = new HashSet<>();
        for (int num : nums) {
            set.add(num);
        }
        return set.size();
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 4, 4};
        System.out.println(countUnique(arr)); // Output: 4
    }
}

Explanation 
Step 1: Understand what “unique” means

Unique means each number should be counted only once, even if it appears many times.

Example:
2 appears twice, but we count it only once.

Step 2: How to solve?

Approach 1: Best method → Use a Set

A Set is a data structure that automatically removes duplicates.

If you convert the list into a set, you get only unique values.

Example:

List: [1, 2, 2, 3, 4, 4]
Set : {1, 2, 3, 4}
Now the number of elements in the set is 4, which is the answer.

✔️ Time Complexity: O(n)

We visit each number once.

✔️ Space Complexity: O(n)

Because the set stores unique numbers.

Step 3: Edge Case

If the list is empty:

[]

Then there are no elements, so unique count = 0.

This is why we check:

If list is empty → return 0

