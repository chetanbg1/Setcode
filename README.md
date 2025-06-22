# Setcode
1. Create a HashSet and Add Elements
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class HashSetExample {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("Apple");
        set.add("Banana");
        set.add("Cherry");
        System.out.println("HashSet: " + set);
    }
}
2. Remove an Element from HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class RemoveElement {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>();
        set.add(10);
        set.add(20);
        set.add(30);
        set.remove(20);
        System.out.println("After removal: " + set);
    }
}
3. Check if HashSet Contains an Element
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ContainsElement {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("Java");
        set.add("Python");
        System.out.println("Contains Java? " + set.contains("Java"));
        System.out.println("Contains C++? " + set.contains("C++"));
    }
}
4. Iterate Over a HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class IterateSet {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("Red");
        set.add("Green");
        set.add("Blue");
        for(String color : set) {
            System.out.println(color);
        }
    }
}
5. Get Size of a HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SetSize {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>();
        set.add(1);
        set.add(2);
        set.add(3);
        System.out.println("Size of set: " + set.size());
    }
}
6. Clear All Elements from a HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ClearSet {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("A");
        set.add("B");
        set.clear();
        System.out.println("Set after clear: " + set);
    }
}
7. Check if a HashSet is Empty
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class IsEmptySet {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>();
        System.out.println("Is set empty? " + set.isEmpty());
        set.add(100);
        System.out.println("Is set empty? " + set.isEmpty());
    }
}
8. Convert HashSet to Array
java
Copy
Edit
import java.util.Arrays;
import java.util.HashSet;
import java.util.Set;

public class SetToArray {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("One");
        set.add("Two");
        set.add("Three");
        String[] array = set.toArray(new String[0]);
        System.out.println(Arrays.toString(array));
    }
}
9. Create a TreeSet and Add Elements
java
Copy
Edit
import java.util.Set;
import java.util.TreeSet;

public class TreeSetExample {
    public static void main(String[] args) {
        Set<Integer> set = new TreeSet<>();
        set.add(50);
        set.add(10);
        set.add(30);
        System.out.println("TreeSet: " + set);
    }
}
10. Find the First and Last Elements in TreeSet
java
Copy
Edit
import java.util.TreeSet;

public class FirstLastTreeSet {
    public static void main(String[] args) {
        TreeSet<Integer> set = new TreeSet<>();
        set.add(10);
        set.add(20);
        set.add(30);
        System.out.println("First element: " + set.first());
        System.out.println("Last element: " + set.last());
    }
}
11. Get a SubSet from TreeSet
java
Copy
Edit
import java.util.NavigableSet;
import java.util.TreeSet;

public class TreeSetSubset {
    public static void main(String[] args) {
        TreeSet<Integer> set = new TreeSet<>();
        set.add(10);
        set.add(20);
        set.add(30);
        set.add(40);
        NavigableSet<Integer> subset = set.subSet(15, true, 35, true);
        System.out.println("Subset: " + subset);
    }
}
12. Use LinkedHashSet to Maintain Insertion Order
java
Copy
Edit
import java.util.LinkedHashSet;
import java.util.Set;

public class LinkedHashSetExample {
    public static void main(String[] args) {
        Set<String> set = new LinkedHashSet<>();
        set.add("Banana");
        set.add("Apple");
        set.add("Mango");
        System.out.println("LinkedHashSet: " + set);
    }
}
13. Find Union of Two Sets
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SetUnion {
    public static void main(String[] args) {
        Set<Integer> set1 = new HashSet<>();
        set1.add(1);
        set1.add(2);
        set1.add(3);

        Set<Integer> set2 = new HashSet<>();
        set2.add(3);
        set2.add(4);
        set2.add(5);

        Set<Integer> union = new HashSet<>(set1);
        union.addAll(set2);

        System.out.println("Union: " + union);
    }
}
14. Find Intersection of Two Sets
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SetIntersection {
    public static void main(String[] args) {
        Set<Integer> set1 = new HashSet<>();
        set1.add(1);
        set1.add(2);
        set1.add(3);

        Set<Integer> set2 = new HashSet<>();
        set2.add(2);
        set2.add(3);
        set2.add(4);

        Set<Integer> intersection = new HashSet<>(set1);
        intersection.retainAll(set2);

        System.out.println("Intersection: " + intersection);
    }
}
15. Find Difference Between Two Sets
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SetDifference {
    public static void main(String[] args) {
        Set<Integer> set1 = new HashSet<>();
        set1.add(1);
        set1.add(2);
        set1.add(3);

        Set<Integer> set2 = new HashSet<>();
        set2.add(2);
        set2.add(4);

        Set<Integer> difference = new HashSet<>(set1);
        difference.removeAll(set2);

        System.out.println("Difference: " + difference);
    }
}
16. Check if Two Sets are Disjoint
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class AreSetsDisjoint {
    public static boolean areDisjoint(Set<?> set1, Set<?> set2) {
        for(Object elem : set1) {
            if(set2.contains(elem)) return false;
        }
        return true;
    }
    public static void main(String[] args) {
        Set<Integer> set1 = new HashSet<>();
        set1.add(1);
        set1.add(2);

        Set<Integer> set2 = new HashSet<>();
        set2.add(3);
        set2.add(4);

        System.out.println("Are disjoint? " + areDisjoint(set1, set2));
    }
}
17. Count Unique Elements in an Array Using HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueCount {
    public static int countUnique(int[] arr) {
        Set<Integer> set = new HashSet<>();
        for(int num : arr) {
            set.add(num);
        }
        return set.size();
    }
    public static void main(String[] args) {
        int[] arr = {1,2,2,3,4,4,5};
        System.out.println("Unique count: " + countUnique(arr));
    }
}
18. Remove Duplicates from an Array Using HashSet
java
Copy
Edit
import java.util.Arrays;
import java.util.HashSet;
import java.util.Set;

public class RemoveDuplicates {
    public static int[] removeDuplicates(int[] arr) {
        Set<Integer> set = new HashSet<>();
        for(int num : arr) {
            set.add(num);
        }
        int[] result = new int[set.size()];
        int i = 0;
        for(int num : set) {
            result[i++] = num;
        }
        return result;
    }
    public static void main(String[] args) {
        int[] arr = {1,2,2,3,4,4,5};
        System.out.println(Arrays.toString(removeDuplicates(arr)));
    }
}
19. Find the Intersection of Two Arrays Using HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ArrayIntersection {
    public static int[] intersection(int[] nums1, int[] nums2) {
        Set<Integer> set1 = new HashSet<>();
        for(int num : nums1) set1.add(num);
        Set<Integer> intersection = new HashSet<>();
        for(int num : nums2) {
            if(set1.contains(num)) intersection.add(num);
        }
        int[] result = new int[intersection.size()];
        int i=0;
        for(int num : intersection) result[i++] = num;
        return result;
    }
    public static void main(String[] args) {
        int[] nums1 = {1,2,2,1};
        int[] nums2 = {2,2};
        int[] res = intersection(nums1, nums2);
        for(int num : res) System.out.print(num + " ");
    }
}
20. Check if Array Contains Duplicates Using HashSet
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ContainsDuplicates {
    public static boolean containsDuplicate(int[] nums) {
        Set<Integer> set = new HashSet<>();
        for(int num : nums) {
            if(set.contains(num)) return true;
            set.add(num);
        }
        return false;
    }
    public static void main(String[] args) {
        int[] nums = {1,2,3,1};
        System.out.println("Contains duplicates? " + containsDuplicate(nums));
    }
}
21. Add All Elements from One Set to Another
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class AddAllSets {
    public static void main(String[] args) {
        Set<String> set1 = new HashSet<>();
        set1.add("A");
        set1.add("B");

        Set<String> set2 = new HashSet<>();
        set2.add("C");
        set2.add("D");

        set1.addAll(set2);
        System.out.println("Merged set: " + set1);
    }
}
22. Remove All Elements from One Set Present in Another
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class RemoveAllSets {
    public static void main(String[] args) {
        Set<Integer> set1 = new HashSet<>();
        set1.add(1);
        set1.add(2);
        set1.add(3);

        Set<Integer> set2 = new HashSet<>();
        set2.add(2);
        set2.add(4);

        set1.removeAll(set2);
        System.out.println("After removal: " + set1);
    }
}
23. Find Symmetric Difference Between Two Sets
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SymmetricDifference {
    public static Set<Integer> symmetricDiff(Set<Integer> set1, Set<Integer> set2) {
        Set<Integer> result = new HashSet<>(set1);
        for(Integer elem : set2) {
            if(!result.add(elem)) {
                result.remove(elem);
            }
        }
        return result;
    }
    public static void main(String[] args) {
        Set<Integer> s1 = Set.of(1,2,3);
        Set<Integer> s2 = Set.of(2,3,4);
        System.out.println("Symmetric difference: " + symmetricDiff(s1, s2));
    }
}
24. Convert Set to List
java
Copy
Edit
import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

public class SetToList {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("X");
        set.add("Y");
        set.add("Z");
        List<String> list = new ArrayList<>(set);
        System.out.println("List: " + list);
    }
}
25. Find Maximum Element in a HashSet of Integers
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class MaxInSet {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>();
        set.add(5);
        set.add(10);
        set.add(3);
        int max = Integer.MIN_VALUE;
        for(int num : set) {
            if(num > max) max = num;
        }
        System.out.println("Max element: " + max);
    }
}
26. Find Minimum Element in a HashSet of Integers
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class MinInSet {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>();
        set.add(5);
        set.add(10);
        set.add(3);
        int min = Integer.MAX_VALUE;
        for(int num : set) {
            if(num < min) min = num;
        }
        System.out.println("Min element: " + min);
    }
}
27. Remove Null from a HashSet (if present)
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class RemoveNullFromSet {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("Hello");
        set.add(null);
        set.add("World");
        set.remove(null);
        System.out.println("Set without null: " + set);
    }
}
28. Count Occurrences of Each Character Using Set and Map
java
Copy
Edit
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;
import java.util.Set;

public class CharCount {
    public static void main(String[] args) {
        String str = "hello world";
        Set<Character> uniqueChars = new HashSet<>();
        Map<Character, Integer> counts = new HashMap<>();

        for(char c : str.toCharArray()) {
            uniqueChars.add(c);
            counts.put(c, counts.getOrDefault(c, 0) + 1);
        }

        System.out.println("Unique chars: " + uniqueChars);
        System.out.println("Counts: " + counts);
    }
}
29. Use Set to Find Palindrome Permutation Possibility
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class PalindromePermutation {
    public static boolean canFormPalindrome(String s) {
        Set<Character> set = new HashSet<>();
        for(char c : s.toCharArray()) {
            if(set.contains(c)) {
                set.remove(c);
            } else {
                set.add(c);
            }
        }
        return set.size() <= 1;
    }

    public static void main(String[] args) {
        System.out.println(canFormPalindrome("carrace")); // true
        System.out.println(canFormPalindrome("hello"));   // false
    }
}
30. Find First Non-Repeated Character Using Set and Map
java
Copy
Edit
import java.util.LinkedHashMap;
import java.util.Map;

public class FirstNonRepeatedChar {
    public static char firstNonRepeated(String s) {
        Map<Character, Integer> countMap = new LinkedHashMap<>();
        for(char c : s.toCharArray()) {
            countMap.put(c, countMap.getOrDefault(c, 0) + 1);
        }
        for(Map.Entry<Character, Integer> entry : countMap.entrySet()) {
            if(entry.getValue() == 1) return entry.getKey();
        }
        return '\0'; // No unique char
    }

    public static void main(String[] args) {
        System.out.println(firstNonRepeated("swiss")); // w
        System.out.println(firstNonRepeated("reappear")); // e
    }
}
31. Create Immutable Set Using Set.of()
java
Copy
Edit
import java.util.Set;

public class ImmutableSet {
    public static void main(String[] args) {
        Set<String> set = Set.of("A", "B", "C");
        System.out.println("Immutable set: " + set);
        // set.add("D"); // Throws UnsupportedOperationException
    }
}
32. Find Common Elements Between Two Lists Using Sets
java
Copy
Edit
import java.util.Arrays;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

public class CommonElements {
    public static void main(String[] args) {
        List<Integer> list1 = Arrays.asList(1, 2, 3, 4);
        List<Integer> list2 = Arrays.asList(3, 4, 5, 6);

        Set<Integer> set1 = new HashSet<>(list1);
        Set<Integer> set2 = new HashSet<>(list2);

        set1.retainAll(set2);
        System.out.println("Common elements: " + set1);
    }
}
33. Remove All Duplicates from a List Using Set
java
Copy
Edit
import java.util.ArrayList;
import java.util.Arrays;
import java.util.LinkedHashSet;
import java.util.List;
import java.util.Set;

public class RemoveDuplicatesFromList {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>(Arrays.asList("apple", "banana", "apple", "orange"));
        Set<String> set = new LinkedHashSet<>(list);
        list.clear();
        list.addAll(set);
        System.out.println("List after removing duplicates: " + list);
    }
}
34. Check If Two Sets Are Equal
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SetEquality {
    public static void main(String[] args) {
        Set<Integer> s1 = new HashSet<>();
        s1.add(1);
        s1.add(2);

        Set<Integer> s2 = new HashSet<>();
        s2.add(2);
        s2.add(1);

        System.out.println("Sets equal? " + s1.equals(s2));
    }
}
35. Create a Set from an ArrayList and Display Unique Elements
java
Copy
Edit
import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

public class UniqueFromList {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("Java");
        list.add("Python");
        list.add("Java");
        Set<String> uniqueSet = new HashSet<>(list);
        System.out.println("Unique elements: " + uniqueSet);
    }
}
36. Use Set to Check if String Has All Unique Characters
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueCharacters {
    public static boolean allUnique(String s) {
        Set<Character> set = new HashSet<>();
        for(char c : s.toCharArray()) {
            if(!set.add(c)) return false;
        }
        return true;
    }
    public static void main(String[] args) {
        System.out.println(allUnique("abcd")); // true
        System.out.println(allUnique("abca")); // false
    }
}
37. Count Distinct Words in a Sentence
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class DistinctWords {
    public static void main(String[] args) {
        String sentence = "hello world hello java";
        String[] words = sentence.split("\\s+");
        Set<String> uniqueWords = new HashSet<>();
        for(String w : words) uniqueWords.add(w);
        System.out.println("Distinct word count: " + uniqueWords.size());
    }
}
38. Find Longest Consecutive Sequence in Array Using Set
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class LongestConsecutiveSequence {
    public static int longestConsecutive(int[] nums) {
        Set<Integer> set = new HashSet<>();
        for(int num : nums) set.add(num);
        int longest = 0;
        for(int num : nums) {
            if(!set.contains(num - 1)) { // start of sequence
                int currentNum = num;
                int length = 1;
                while(set.contains(currentNum + 1)) {
                    currentNum++;
                    length++;
                }
                longest = Math.max(longest, length);
            }
        }
        return longest;
    }
    public static void main(String[] args) {
        int[] arr = {100,4,200,1,3,2};
        System.out.println("Longest consecutive sequence: " + longestConsecutive(arr)); // 4 (1,2,3,4)
    }
}
39. Use Set to Check if Two Strings Are Anagrams
java
Copy
Edit
import java.util.HashMap;
import java.util.Map;

public class AnagramCheck {
    public static boolean areAnagrams(String s1, String s2) {
        if(s1.length() != s2.length()) return false;
        Map<Character, Integer> countMap = new HashMap<>();
        for(char c : s1.toCharArray()) {
            countMap.put(c, countMap.getOrDefault(c, 0) + 1);
        }
        for(char c : s2.toCharArray()) {
            if(!countMap.containsKey(c)) return false;
            countMap.put(c, countMap.get(c) - 1);
            if(countMap.get(c) == 0) countMap.remove(c);
        }
        return countMap.isEmpty();
    }

    public static void main(String[] args) {
        System.out.println(areAnagrams("listen", "silent")); // true
        System.out.println(areAnagrams("hello", "world"));   // false
    }
}
40. Use Set to Remove Common Characters from String
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class RemoveCommonChars {
    public static String removeCommon(String s1, String s2) {
        Set<Character> set2 = new HashSet<>();
        for(char c : s2.toCharArray()) set2.add(c);

        StringBuilder sb = new StringBuilder();
        for(char c : s1.toCharArray()) {
            if(!set2.contains(c)) {
                sb.append(c);
            }
        }
        return sb.toString();
    }

    public static void main(String[] args) {
        System.out.println(removeCommon("abcdef", "bdf")); // ace
    }
}
41. Count Number of Set Bits in an Integer Using Set
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class CountSetBits {
    public static int countSetBits(int n) {
        Set<Integer> set = new HashSet<>();
        int count = 0;
        for(int i=0; i<32; i++) {
            int bit = (n >> i) & 1;
            if(bit == 1) count++;
        }
        return count;
    }

    public static void main(String[] args) {
        System.out.println(countSetBits(9)); // 2 (1001)
    }
}
42. Use Set to Track Visited Nodes in Graph Traversal (DFS example)
java
Copy
Edit
import java.util.*;

public class DFSWithSet {
    static Map<Integer, List<Integer>> graph = new HashMap<>();
    static Set<Integer> visited = new HashSet<>();

    public static void dfs(int node) {
        if(visited.contains(node)) return;
        System.out.print(node + " ");
        visited.add(node);
        for(int neighbor : graph.getOrDefault(node, new ArrayList<>())) {
            dfs(neighbor);
        }
    }

    public static void main(String[] args) {
        graph.put(1, List.of(2,3));
        graph.put(2, List.of(4));
        graph.put(3, List.of());
        graph.put(4, List.of());

        dfs(1); // Output: 1 2 4 3
    }
}
43. Use Set to Detect Cycle in Undirected Graph
java
Copy
Edit
import java.util.*;

public class CycleDetection {
    static Map<Integer, List<Integer>> graph = new HashMap<>();
    static Set<Integer> visited = new HashSet<>();

    public static boolean dfs(int node, int parent) {
        visited.add(node);
        for(int neighbor : graph.getOrDefault(node, new ArrayList<>())) {
            if(!visited.contains(neighbor)) {
                if(dfs(neighbor, node)) return true;
            } else if(neighbor != parent) {
                return true;
            }
        }
        return false;
    }

    public static void main(String[] args) {
        graph.put(1, List.of(2));
        graph.put(2, List.of(1,3));
        graph.put(3, List.of(2,4));
        graph.put(4, List.of(3,1)); // cycle here

        System.out.println("Cycle detected? " + dfs(1, -1)); // true
    }
}
44. Use Set to Track Unique Email Addresses (Ignoring Dots and Plus Sign)
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueEmails {
    public static int numUniqueEmails(String[] emails) {
        Set<String> uniqueEmails = new HashSet<>();
        for(String email : emails) {
            String[] parts = email.split("@");
            String local = parts[0].split("\\+")[0].replace(".", "");
            String domain = parts[1];
            uniqueEmails.add(local + "@" + domain);
        }
        return uniqueEmails.size();
    }

    public static void main(String[] args) {
        String[] emails = {"test.email+alex@leetcode.com", "test.e.mail@leetcode.com", "testemail@lee.tcode.com"};
        System.out.println("Unique emails: " + numUniqueEmails(emails)); // 2
    }
}
45. Use Set to Detect if String Has Any Duplicate Words
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class DuplicateWordsCheck {
    public static boolean hasDuplicateWords(String sentence) {
        String[] words = sentence.split("\\s+");
        Set<String> set = new HashSet<>();
        for(String w : words) {
            if(!set.add(w)) return true;
        }
        return false;
    }

    public static void main(String[] args) {
        System.out.println(hasDuplicateWords("this is a test")); // false
        System.out.println(hasDuplicateWords("this is is a test")); // true
    }
}
46. Use Set to Find Characters Present in Both Strings
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class CommonCharsInStrings {
    public static Set<Character> commonChars(String s1, String s2) {
        Set<Character> set1 = new HashSet<>();
        Set<Character> common = new HashSet<>();

        for(char c : s1.toCharArray()) set1.add(c);
        for(char c : s2.toCharArray()) {
            if(set1.contains(c)) common.add(c);
        }
        return common;
    }

    public static void main(String[] args) {
        System.out.println(commonChars("hello", "world")); // [o, l]
    }
}
47. Use Set to Find Characters Present in One String But Not Other
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueCharsInString {
    public static Set<Character> uniqueChars(String s1, String s2) {
        Set<Character> set1 = new HashSet<>();
        Set<Character> set2 = new HashSet<>();

        for(char c : s1.toCharArray()) set1.add(c);
        for(char c : s2.toCharArray()) set2.add(c);

        set1.removeAll(set2);
        return set1;
    }

    public static void main(String[] args) {
        System.out.println(uniqueChars("hello", "world")); // [h, e]
    }
}
48. Check if a Set is a Subset of Another
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class SubsetCheck {
    public static boolean isSubset(Set<Integer> subset, Set<Integer> superset) {
        return superset.containsAll(subset);
    }

    public static void main(String[] args) {
        Set<Integer> s1 = Set.of(1, 2);
        Set<Integer> s2 = Set.of(1, 2, 3, 4);

        System.out.println("Is subset? " + isSubset(s1, s2)); // true
    }
}
49. Find Union of Multiple Sets
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UnionMultipleSets {
    public static Set<Integer> unionOfSets(Set<Integer>... sets) {
        Set<Integer> union = new HashSet<>();
        for(Set<Integer> s : sets) union.addAll(s);
        return union;
    }

    public static void main(String[] args) {
        Set<Integer> s1 = Set.of(1, 2);
        Set<Integer> s2 = Set.of(3, 4);
        Set<Integer> s3 = Set.of(2, 5);

        System.out.println(unionOfSets(s1, s2, s3)); // [1, 2, 3, 4, 5]
    }
}
50. Use Set to Filter Out Invalid Emails (Simple validation)
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class FilterInvalidEmails {
    public static Set<String> filterValidEmails(Set<String> emails) {
        Set<String> validEmails = new HashSet<>();
        for(String email : emails) {
            if(email.contains("@") && email.indexOf("@") < email.length()-1) {
                validEmails.add(email);
            }
        }
        return validEmails;
    }

    public static void main(String[] args) {
        Set<String> emails = Set.of("abc@domain.com", "xyz@", "noatsign.com");
        System.out.println(filterValidEmails(emails)); // [abc@domain.com]
    }
}
51. Count Unique Words Longer Than a Given Length Using Set
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class CountUniqueLongWords {
    public static int countUniqueLongWords(String sentence, int length) {
        Set<String> set = new HashSet<>();
        for(String w : sentence.split("\\s+")) {
            if(w.length() > length) set.add(w);
        }
        return set.size();
    }

    public static void main(String[] args) {
        String s = "apple banana apple orange pear grape banana";
        System.out.println(countUniqueLongWords(s, 4)); // 4 (apple, banana, orange, grape)
    }
}
52. Check if Set Contains Any Element From Another Set
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ContainsAnyCheck {
    public static boolean containsAny(Set<Integer> s1, Set<Integer> s2) {
        for(int num : s2) {
            if(s1.contains(num)) return true;
        }
        return false;
    }

    public static void main(String[] args) {
        Set<Integer> s1 = Set.of(1, 2, 3);
        Set<Integer> s2 = Set.of(4, 5, 2);
        System.out.println(containsAny(s1, s2)); // true
    }
}
53. Use Set to Count Distinct Integers in a 2D Array
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class DistinctIn2DArray {
    public static int countDistinct(int[][] arr) {
        Set<Integer> set = new HashSet<>();
        for(int[] row : arr) {
            for(int num : row) {
                set.add(num);
            }
        }
        return set.size();
    }

    public static void main(String[] args) {
        int[][] arr = {{1,2,3},{3,4,5},{5,6,1}};
        System.out.println("Distinct count: " + countDistinct(arr)); // 6
    }
}
54. Use Set to Find Intersection Size of Two Arrays
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class IntersectionSize {
    public static int intersectionSize(int[] a, int[] b) {
        Set<Integer> setA = new HashSet<>();
        for(int num : a) setA.add(num);

        Set<Integer> intersection = new HashSet<>();
        for(int num : b) {
            if(setA.contains(num)) intersection.add(num);
        }
        return intersection.size();
    }

    public static void main(String[] args) {
        int[] a = {1,2,3,4};
        int[] b = {3,4,5,6};
        System.out.println("Intersection size: " + intersectionSize(a, b)); // 2
    }
}
55. Use Set to Remove Duplicates from Array of Objects
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

class Person {
    String name;
    Person(String name) { this.name = name; }
    @Override
    public boolean equals(Object o) {
        if(this == o) return true;
        if(!(o instanceof Person)) return false;
        Person p = (Person)o;
        return name.equals(p.name);
    }
    @Override
    public int hashCode() {
        return name.hashCode();
    }
    public String toString() { return name; }
}

public class RemoveDuplicateObjects {
    public static void main(String[] args) {
        Person[] arr = {new Person("Alice"), new Person("Bob"), new Person("Alice")};
        Set<Person> set = new HashSet<>();
        for(Person p : arr) set.add(p);
        System.out.println(set); // [Alice, Bob]
    }
}
56. Use Set to Store Unique Random Numbers
java
Copy
Edit
import java.util.HashSet;
import java.util.Random;
import java.util.Set;

public class UniqueRandomNumbers {
    public static void main(String[] args) {
        Random rand = new Random();
        Set<Integer> set = new HashSet<>();
        while(set.size() < 5) {
            set.add(rand.nextInt(10));
        }
        System.out.println("Unique random numbers: " + set);
    }
}
57. Use Set to Track Unique Visitors (IP addresses)
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueVisitors {
    public static void main(String[] args) {
        String[] ips = {"192.168.0.1", "192.168.0.2", "192.168.0.1"};
        Set<String> uniqueIPs = new HashSet<>();
        for(String ip : ips) uniqueIPs.add(ip);
        System.out.println("Unique visitors: " + uniqueIPs.size());
    }
}
58. Use Set to Track Processed Items in a Loop
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ProcessedItems {
    public static void main(String[] args) {
        int[] items = {1, 2, 3, 2, 1, 4};
        Set<Integer> processed = new HashSet<>();
        for(int item : items) {
            if(processed.contains(item)) {
                System.out.println(item + " already processed");
            } else {
                System.out.println("Processing " + item);
                processed.add(item);
            }
        }
    }
}
59. Use Set to Filter Unique Integers from Mixed List
java
Copy
Edit
import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

public class FilterUniqueIntegers {
    public static void main(String[] args) {
        List<Object> list = List.of(1, "two", 3, 1, "three", 3);
        Set<Integer> uniqueInts = new HashSet<>();
        for(Object o : list) {
            if(o instanceof Integer) uniqueInts.add((Integer)o);
        }
        System.out.println("Unique integers: " + uniqueInts);
    }
}
60. Use Set to Check if Array Contains Any Duplicate
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ContainsDuplicate {
    public static boolean hasDuplicate(int[] arr) {
        Set<Integer> set = new HashSet<>();
        for(int num : arr) {
            if(!set.add(num)) return true;
        }
        return false;
    }

    public static void main(String[] args) {
        int[] arr1 = {1,2,3,4};
        int[] arr2 = {1,2,2,4};
        System.out.println(hasDuplicate(arr1)); // false
        System.out.println(hasDuplicate(arr2)); // true
    }
}
61. Use Set to Keep Track of Visited Coordinates (x,y)
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

class Coord {
    int x, y;
    Coord(int x, int y) { this.x = x; this.y = y; }

    @Override
    public boolean equals(Object o) {
        if(this == o) return true;
        if(!(o instanceof Coord)) return false;
        Coord c = (Coord)o;
        return x == c.x && y == c.y;
    }

    @Override
    public int hashCode() {
        return 31 * x + y;
    }

    @Override
    public String toString() {
        return "(" + x + "," + y + ")";
    }
}

public class VisitedCoordinates {
    public static void main(String[] args) {
        Set<Coord> visited = new HashSet<>();
        visited.add(new Coord(0, 0));
        visited.add(new Coord(1, 0));
        visited.add(new Coord(0, 0)); // duplicate, won't add
        System.out.println("Visited coordinates: " + visited);
    }
}
62. Use Set to Filter Out Duplicate URLs (case insensitive)
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueUrls {
    public static Set<String> uniqueUrls(String[] urls) {
        Set<String> set = new HashSet<>();
        for(String url : urls) {
            set.add(url.toLowerCase());
        }
        return set;
    }

    public static void main(String[] args) {
        String[] urls = {"HTTP://Example.com", "http://example.com", "https://google.com"};
        System.out.println(uniqueUrls(urls)); // [http://example.com, https://google.com]
    }
}
63. Use Set to Store Unique Characters from Multiple Strings
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueCharsFromStrings {
    public static void main(String[] args) {
        String[] strs = {"apple", "banana"};
        Set<Character> set = new HashSet<>();
        for(String s : strs) {
            for(char c : s.toCharArray()) {
                set.add(c);
            }
        }
        System.out.println("Unique chars: " + set);
    }
}
64. Use Set to Count Unique Digits in an Integer
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class UniqueDigitsCount {
    public static int countUniqueDigits(int n) {
        Set<Integer> digits = new HashSet<>();
        while(n > 0) {
            digits.add(n % 10);
            n /= 10;
        }
        return digits.size();
    }

    public static void main(String[] args) {
        System.out.println(countUniqueDigits(112233)); // 3
        System.out.println(countUniqueDigits(987654321)); // 9
    }
}
65. Use Set to Find Words that Appear Only Once in Sentence
java
Copy
Edit
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;
import java.util.Set;

public class WordsAppearingOnce {
    public static Set<String> wordsOnce(String sentence) {
        String[] words = sentence.split("\\s+");
        Map<String, Integer> countMap = new HashMap<>();
        for(String w : words) countMap.put(w, countMap.getOrDefault(w,0)+1);
        Set<String> result = new HashSet<>();
        for(Map.Entry<String, Integer> e : countMap.entrySet()) {
            if(e.getValue() == 1) result.add(e.getKey());
        }
        return result;
    }

    public static void main(String[] args) {
        String s = "apple banana apple orange banana grape";
        System.out.println(wordsOnce(s)); // [orange, grape]
    }
}
66. Use Set to Remove Duplicates from Character Array
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class RemoveDuplicateChars {
    public static void main(String[] args) {
        char[] chars = {'a', 'b', 'a', 'c', 'b'};
        Set<Character> set = new HashSet<>();
        for(char c : chars) set.add(c);
        System.out.println("Unique chars: " + set);
    }
}
67. Use Set to Check if String Has Exactly Two Unique Characters
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class ExactlyTwoUniqueChars {
    public static boolean hasExactlyTwoUnique(String s) {
        Set<Character> set = new HashSet<>();
        for(char c : s.toCharArray()) set.add(c);
        return set.size() == 2;
    }

    public static void main(String[] args) {
        System.out.println(hasExactlyTwoUnique("aabbcc")); // false (3 unique)
        System.out.println(hasExactlyTwoUnique("aabb"));   // true
    }
}
68. Use Set to Find Characters Appearing in At Least Two Strings
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class CharsInAtLeastTwoStrings {
    public static Set<Character> charsInAtLeastTwo(String s1, String s2, String s3) {
        Set<Character> set1 = new HashSet<>();
        for(char c : s1.toCharArray()) set1.add(c);
        Set<Character> set2 = new HashSet<>();
        for(char c : s2.toCharArray()) set2.add(c);
        Set<Character> set3 = new HashSet<>();
        for(char c : s3.toCharArray()) set3.add(c);

        Set<Character> result = new HashSet<>();
        for(char c : set1) {
            int count = 0;
            if(set1.contains(c)) count++;
            if(set2.contains(c)) count++;
            if(set3.contains(c)) count++;
            if(count >= 2) result.add(c);
        }
        for(char c : set2) {
            if(result.contains(c)) continue;
            int count = 0;
            if(set1.contains(c)) count++;
            if(set2.contains(c)) count++;
            if(set3.contains(c)) count++;
            if(count >= 2) result.add(c);
        }
        for(char c : set3) {
            if(result.contains(c)) continue;
            int count = 0;
            if(set1.contains(c)) count++;
            if(set2.contains(c)) count++;
            if(set3.contains(c)) count++;
            if(count >= 2) result.add(c);
        }
        return result;
    }

    public static void main(String[] args) {
        System.out.println(charsInAtLeastTwoStrings("abc", "bcd", "cde")); // [b,c,d]
    }
}
69. Use Set to Find Characters Present in Exactly Two Strings
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class CharsInExactlyTwoStrings {
    public static Set<Character> charsInExactlyTwo(String s1, String s2, String s3) {
        Set<Character> set1 = new HashSet<>();
        for(char c : s1.toCharArray()) set1.add(c);
        Set<Character> set2 = new HashSet<>();
        for(char c : s2.toCharArray()) set2.add(c);
        Set<Character> set3 = new HashSet<>();
        for(char c : s3.toCharArray()) set3.add(c);

        Set<Character> result = new HashSet<>();
        for(char c : set1) {
            int count = 0;
            if(set1.contains(c)) count++;
            if(set2.contains(c)) count++;
            if(set3.contains(c)) count++;
            if(count == 2) result.add(c);
        }
        for(char c : set2) {
            if(result.contains(c)) continue;
            int count = 0;
            if(set1.contains(c)) count++;
            if(set2.contains(c)) count++;
            if(set3.contains(c)) count++;
            if(count == 2) result.add(c);
        }
        for(char c : set3) {
            if(result.contains(c)) continue;
            int count = 0;
            if(set1.contains(c)) count++;
            if(set2.contains(c)) count++;
            if(set3.contains(c)) count++;
            if(count == 2) result.add(c);
        }
        return result;
    }

    public static void main(String[] args) {
        System.out.println(charsInExactlyTwo("abc", "bcd", "cde")); // [b,d]
    }
}
70. Use Set to Find Common Divisors of Two Numbers
java
Copy
Edit
import java.util.HashSet;
import java.util.Set;

public class CommonDivisors {
    public static Set<Integer> commonDivisors(int a, int b) {
        Set<Integer> divisorsA = new HashSet<>();
        for(int i = 1; i <= a; i++) {
            if(a % i == 0) divisorsA.add(i);
        }
        Set<Integer> divisorsB = new HashSet<>();
        for(int i = 1; i <= b; i++) {
            if(b % i == 0) divisorsB.add(i);
        }
        divisorsA.retainAll(divisorsB);
        return divisorsA;
    }

    public static void main(String[] args) {
        System.out.println(commonDivisors(12, 18)); // [1, 2, 3, 6]
    }
}










