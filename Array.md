# Array Programming


### Q1: WAJP to print the even index elements of the array.  
- **Example:**  
  - **Input:** `[10, 15, 20, 25, 30, 35]`  
  - **Output:** `[10, 20, 30]`  
  - **Explanation:** The even index elements are at indices 0, 2, and 4, which correspond to the values 10, 20, and 30.  
- **Code:**  
```java
import java.util.Arrays;

public class EvenIndexElements {
    public static void main(String[] args) {
        int[] array = {10, 15, 20, 25, 30, 35};
        System.out.print("Even index elements: ");
        for (int i = 0; i < array.length; i += 2) {
            System.out.print(array[i] + " ");
        }
    }
}
```  

---  

### Q2: WAJP to print the even elements of the array.  
- **Example:**  
  - **Input:** `[10, 15, 20, 25, 30, 35]`  
  - **Output:** `[10, 20, 30]`  
  - **Explanation:** The even elements in the array are those divisible by 2, which are 10, 20, and 30.  
- **Code:**  
```java
import java.util.Arrays;

public class EvenElements {
    public static void main(String[] args) {
        int[] array = {10, 15, 20, 25, 30, 35};
        System.out.print("Even elements: ");
        for (int num : array) {
            if (num % 2 == 0) {
                System.out.print(num + " ");
            }
        }
    }
}
```

---

### Q3: WAJP to count all the even numbers of the array.  
- **Example:**  
  - **Input:** `[10, 15, 20, 25, 30, 35]`  
  - **Output:** `3`  
  - **Explanation:** The even numbers in the array are 10, 20, and 30. The total count is 3.  
- **Code:**  
```java
public class CountEvenNumbers {
    public static void main(String[] args) {
        int[] array = {10, 15, 20, 25, 30, 35};
        int count = 0;
        for (int num : array) {
            if (num % 2 == 0) {
                count++;
            }
        }
        System.out.println("Count of even numbers: " + count);
    }
}
```

---

### Q4: WAJP to print and count all the three-digit numbers of the array.  
- **Example:**  
  - **Input:** `[10, 150, 20, 375, 30, 500]`  
  - **Output:** `150 375 500` and `3`  
  - **Explanation:** The three-digit numbers in the array are 150, 375, and 500. The total count is 3.  
- **Code:**  
```java
public class ThreeDigitNumbers {
    public static void main(String[] args) {
        int[] array = {10, 150, 20, 375, 30, 500};
        int count = 0;
        System.out.print("Three-digit numbers: ");
        for (int num : array) {
            if (num >= 100 && num <= 999) {
                System.out.print(num + " ");
                count++;
            }
        }
        System.out.println("\nCount of three-digit numbers: " + count);
    }
}
```

---

### Q5: WAJP to print sum and average of all the elements of the array.  
- **Example:**  
  - **Input:** `[10, 15, 20, 25, 30]`  
  - **Output:** `Sum: 100, Average: 20.0`  
  - **Explanation:** The sum of the elements is 10+15+20+25+30 = 100. The average is 100 / 5 = 20.0.  
- **Code:**  
```java
public class SumAndAverage {
    public static void main(String[] args) {
        int[] array = {10, 15, 20, 25, 30};
        int sum = 0;
        for (int num : array) {
            sum += num;
        }
        double average = (double) sum / array.length;
        System.out.println("Sum: " + sum);
        System.out.println("Average: " + average);
    }
}
```

---

### Q6: WAJP to print the biggest element, smallest element, and their difference in the array.  
- **Example:**  
  - **Input:** `[10, 15, 20, 25, 30]`  
  - **Output:** `Biggest: 30, Smallest: 10, Difference: 20`  
  - **Explanation:** The largest element is 30, and the smallest is 10. Their difference is 30 - 10 = 20.  
- **Code:**  
```java
import java.util.Arrays;

public class MinMaxDifference {
    public static void main(String[] args) {
        int[] array = {10, 15, 20, 25, 30};
        int max = array[0], min = array[0];
        for (int num : array) {
            if (num > max) max = num;
            if (num < min) min = num;
        }
        System.out.println("Biggest: " + max);
        System.out.println("Smallest: " + min);
        System.out.println("Difference: " + (max - min));
    }
}
```

---

### Q7: For the given array of Strings, print and count all the strings which have even number of characters.  
- **Example:**  
  - **Input:** `["apple", "banana", "pear", "grape"]`  
  - **Output:**  
    ```
    pear
    grape
    Number of strings with even characters: 2
    ```  
  - **Explanation:** "pear" and "grape" both have even character counts (4 and 6, respectively).  
- **Code:**  
```java
public class EvenLengthStrings {
    public static void main(String[] args) {
        String[] arr = {"apple", "banana", "pear", "grape"};
        int count = 0;

        for (String str : arr) {
            if (str.length() % 2 == 0) {
                System.out.println(str);
                count++;
            }
        }

        System.out.println("Number of strings with even characters: " + count);
    }
}
```

---

### Q8: For the given array of Strings, print the largest string and smallest string.  
- **Example:**  
  - **Input:** `["apple", "banana", "pear", "grape"]`  
  - **Output:**  
    ```
    Largest string: banana
    Smallest string: pear
    ```  
  - **Explanation:** "banana" is the largest string and "pear" is the smallest.  
- **Code:**  
```java
public class LargestSmallestString {
    public static void main(String[] args) {
        String[] arr = {"apple", "banana", "pear", "grape"};
        String largest = arr[0];
        String smallest = arr[0];

        for (String str : arr) {
            if (str.compareTo(largest) > 0) {
                largest = str;
            }
            if (str.compareTo(smallest) < 0) {
                smallest = str;
            }
        }

        System.out.println("Largest string: " + largest);
        System.out.println("Smallest string: " + smallest);
    }
}
```

---

### Q9: WAJP to print each element of the array in reverse order.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `[5, 4, 3, 2, 1]`  
  - **Explanation:** The array is printed in reverse order.  
- **Code:**  
```java
public class ReverseArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        
        for (int i = arr.length - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

---

### Q10: WAJP to print alternate elements of the array from the end.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `[5, 3, 1]`  
  - **Explanation:** The alternate elements starting from the end are printed.  
- **Code:**  
```java
public class AlternateFromEnd {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        
        for (int i = arr.length - 1; i >= 0; i -= 2) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

---

### Q11: WAJP to swap two index values of the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`, `index1 = 1`, `index2 = 3`  
  - **Output:** `[1, 4, 3, 2, 5]`  
  - **Explanation:** The elements at index 1 and index 3 are swapped.  
- **Code:**  
```java
public class SwapArrayElements {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int index1 = 1, index2 = 3;

        // Swapping elements
        int temp = arr[index1];
        arr[index1] = arr[index2];
        arr[index2] = temp;

        // Printing swapped array
        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

### Q12: WAJP to insert an element at a certain position in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`, `element = 6`, `position = 2`  
  - **Output:** `[1, 2, 6, 3, 4, 5]`  
  - **Explanation:** The element 6 is inserted at index 2.  
- **Code:**  
```java
public class InsertElement {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int element = 6;
        int position = 2;

        for (int i = arr.length - 1; i > position; i--) {
            arr[i] = arr[i - 1];
        }

        arr[position] = element;

        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

### Q13: WAJP to remove an element from a certain position in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`, `position = 2`  
  - **Output:** `[1, 2, 4, 5]`  
  - **Explanation:** The element at index 2 (value 3) is removed.  
- **Code:**  
```java
public class RemoveElement {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int position = 2;

        for (int i = position; i < arr.length - 1; i++) {
            arr[i] = arr[i + 1];
        }

        // Printing the new array
        for (int i = 0; i < arr.length - 1; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

---

### Q14: WAJP to check if a number is even or odd without using if else/conditional operator statement.  
- **Example:**  
  - **Input:** `4`  
  - **Output:** `Even`  
  - **Explanation:** The program checks the number using bitwise operations.  
- **Code:**  
```java
public class EvenOddWithoutIf {
    public static void main(String[] args) {
        int number = 4;

        // Check if the number is even or odd
        String result = (number & 1) == 0 ? "Even" : "Odd";
        System.out.println(result);
    }
}
```

---

### Q15: WAJP to print and count all the prime numbers of the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`  
  - **Output:**  
    ```
    Prime numbers: 2 3 5 7
    Count of prime numbers: 4
    ```  
  - **Explanation:** The prime numbers in the array are 2, 3, 5, and 7.  
- **Code:**  
```java
public class PrimeNumbers {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
        int count = 0;

        for (int num : arr) {
            if (isPrime(num)) {
                System.out.print(num + " ");
                count++;
            }
        }

        System.out.println("\nCount of prime numbers: " + count);
    }

    public static boolean isPrime(int num) {
        if (num <= 1) {
            return false;
        }

        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }

        return true;
    }
}
```

---

### Q16: WAJP to rotate each element of an array by one position to the right side.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `[5, 1, 2, 3, 4]`  
  - **Explanation:** All elements are shifted to the right, and the last element moves to the first position.  
- **Code:**  
```java
public class RotateArrayRight {
    public static void main(String[] args) {
        int[] arr = {1, 2, 

3, 4, 5};
        int lastElement = arr[arr.length - 1];

        // Shift elements to the right
        for (int i = arr.length - 1; i > 0; i--) {
            arr[i] = arr[i - 1];
        }

        // Set the last element at the first position
        arr[0] = lastElement;

        // Print rotated array
        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

### Q17: WAJP to rotate all the elements of the array k positions to its right.

- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5, 6, 7}`  
    2. `k = 2`  
  - **Output:** `{6, 7, 1, 2, 3, 4, 5}`  
  - **Explanation:** The array is rotated 2 positions to the right. The last 2 elements (`6, 7`) move to the front, and the rest of the elements shift right.  
- **Code:**  
```java
import java.util.Arrays;

public class RotateArrayRight {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5, 6, 7};
        int k = 2;
        rotateRight(array, k);
        System.out.println(Arrays.toString(array));
    }

    public static void rotateRight(int[] array, int k) {
        int n = array.length;
        k = k % n;  // Handle case when k > n
        reverse(array, 0, n - 1);  
        reverse(array, 0, k - 1);
        reverse(array, k, n - 1);
    }

    public static void reverse(int[] array, int start, int end) {
        while (start < end) {
            int temp = array[start];
            array[start] = array[end];
            array[end] = temp;
            start++;
            end--;
        }
    }
}
```

---

### Q18: WAJP to rotate each element of an array by one position to the left side.

- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5, 6, 7}`  
  - **Output:** `{2, 3, 4, 5, 6, 7, 1}`  
  - **Explanation:** All elements shift left by one position, and the first element (`1`) moves to the end.  
- **Code:**  
```java
import java.util.Arrays;

public class RotateArrayLeft {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5, 6, 7};
        rotateLeft(array);
        System.out.println(Arrays.toString(array));
    }

    public static void rotateLeft(int[] array) {
        int first = array[0];
        for (int i = 0; i < array.length - 1; i++) {
            array[i] = array[i + 1];
        }
        array[array.length - 1] = first;
    }
}
```

---

### Q19: WAJP to rotate all the elements of the array k positions to its left.

- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5, 6, 7}`  
    2. `k = 2`  
  - **Output:** `{3, 4, 5, 6, 7, 1, 2}`  
  - **Explanation:** The array is rotated 2 positions to the left. The first 2 elements (`1, 2`) move to the end, and the rest shift left.  
- **Code:**  
```java
import java.util.Arrays;

public class RotateArrayLeftByK {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5, 6, 7};
        int k = 2;
        rotateLeftByK(array, k);
        System.out.println(Arrays.toString(array));
    }

    public static void rotateLeftByK(int[] array, int k) {
        int n = array.length;
        k = k % n;  // Handle case when k > n
        reverse(array, 0, n - 1);
        reverse(array, 0, n - k - 1);
        reverse(array, n - k, n - 1);
    }

    public static void reverse(int[] array, int start, int end) {
        while (start < end) {
            int temp = array[start];
            array[start] = array[end];
            array[end] = temp;
            start++;
            end--;
        }
    }
}
```

---

### Q20: Rotate Array - LeetCode

- **Link:** [Rotate Array - LeetCode](https://leetcode.com/problems/rotate-array/)  

- **Example:**  
  - **Input:**  
    1. `array = [-1, -100, 3, 99]`  
    2. `k = 2`  
  - **Output:** `[3, 99, -1, -100]`  
  - **Explanation:** The array is rotated 2 positions to the right. The last 2 elements (`99, -100`) move to the front, and the rest shift right.  
- **Code:**  
```java
import java.util.Arrays;

public class RotateArrayLeetCode {
    public static void main(String[] args) {
        int[] nums = {-1, -100, 3, 99};
        int k = 2;
        rotate(nums, k);
        System.out.println(Arrays.toString(nums));
    }

    public static void rotate(int[] nums, int k) {
        int n = nums.length;
        k = k % n;  // Handle case when k > n
        reverse(nums, 0, n - 1);
        reverse(nums, 0, k - 1);
        reverse(nums, k, n - 1);
    }

    public static void reverse(int[] nums, int start, int end) {
        while (start < end) {
            int temp = nums[start];
            nums[start] = nums[end];
            nums[end] = temp;
            start++;
            end--;
        }
    }
}

```

### Q21: Move Zeroes - LeetCode  
**Link:** [Move Zeroes - LeetCode](https://leetcode.com/problems/move-zeroes/)

- **Example:**  
  - **Input:**  
    1. `nums = [0, 1, 0, 3, 12]`  
  - **Output:** `[1, 3, 12, 0, 0]`  
  - **Explanation:** All zeroes are moved to the end of the array while maintaining the relative order of the non-zero elements.  
- **Code:**  
```java
import java.util.Arrays;

public class MoveZeroes {
    public static void main(String[] args) {
        int[] nums = {0, 1, 0, 3, 12};
        moveZeroes(nums);
        System.out.println(Arrays.toString(nums));
    }

    public static void moveZeroes(int[] nums) {
        int nonZeroIndex = 0;
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] != 0) {
                nums[nonZeroIndex] = nums[i];
                if (i != nonZeroIndex) {
                    nums[i] = 0;
                }
                nonZeroIndex++;
            }
        }
    }
}

```

### Q22: WAJP to move all zeroes of an array to the end.  
- **Example:**  
  - **Input:**  
    1. `array[] = [7, 0, 2, 6, 0, 4]`  
  - **Output:** `[7, 2, 6, 4, 0, 0]`  
  - **Explanation:** All zeroes are moved to the end of the array while keeping the non-zero elements in the same order.  
- **Code:**  
```java
import java.util.Arrays;

public class MoveZeroesToEnd {
    public static void main(String[] args) {
        int[] array = {7, 0, 2, 6, 0, 4};
        moveZeroes(array);
        System.out.println(Arrays.toString(array));
    }

    public static void moveZeroes(int[] array) {
        int nonZeroIndex = 0;
        for (int i = 0; i < array.length; i++) {
            if (array[i] != 0) {
                array[nonZeroIndex] = array[i];
                if (i != nonZeroIndex) {
                    array[i] = 0;
                }
                nonZeroIndex++;
            }
        }
    }
}
```

---

### Q23: WAJP to shift all 0’s to the left and all 1’s to the right (without sorting).  
- **Example:**  
  - **Input:**  
    1. `array[] = [0, 1, 1, 0, 0, 1, 0, 0]`  
  - **Output:** `[0, 0, 0, 0, 0, 1, 1, 1]`  
  - **Explanation:** All the zeroes are moved to the left and all the ones are moved to the right without sorting.  
- **Code:**  
```java
import java.util.Arrays;

public class ShiftZeroesAndOnes {
    public static void main(String[] args) {
        int[] array = {0, 1, 1, 0, 0, 1, 0, 0};
        shiftZeroesAndOnes(array);
        System.out.println(Arrays.toString(array));
    }

    public static void shiftZeroesAndOnes(int[] array) {
        int left = 0, right = array.length - 1;
        while (left < right) {
            if (array[left] == 0) {
                left++;
            } else if (array[right] == 1) {
                right--;
            } else {
                int temp = array[left];
                array[left] = array[right];
                array[right] = temp;
                left++;
                right--;
            }
        }
    }
}
```

---

### Q24: For the given array of 0’s, 1’s, and 2’s  
1. Sort the elements (without sorting).  
- **Example:**  
  - **Input:**  
    1. `array[] = [0, 2, 0, 1, 2, 1, 0, 2]`  
  - **Output:** `[0, 0, 0, 1, 1, 2, 2, 2]`  
  - **Explanation:** The array is rearranged so that all 0's are first, followed by all 1's, and then all 2's.  
- **Code:**  
```java
import java.util.Arrays;

public class Sort012 {
    public static void main(String[] args) {
        int[] array = {0, 2, 0, 1, 2, 1, 0, 2};
        sort012(array);
        System.out.println(Arrays.toString(array));
    }

    public static void sort012(int[] array) {
        int low = 0, mid = 0, high = array.length - 1;
        while (mid <= high) {
            if (array[mid] == 0) {
                swap(array, low, mid);
                low++;
                mid++;
            } else if (array[mid] == 1) {
                mid++;
            } else {
                swap(array, mid, high);
                high--;
            }
        }
    }

    public static void swap(int[] array, int i, int j) {
        int temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }
}
```

---

### Q25: [Sort Colors - LeetCode](https://leetcode.com/problems/sort-colors/)  
**Link:** [Sort Colors - LeetCode](https://leetcode.com/problems/sort-colors/)

- **Example:**  
  - **Input:**  
    1. `array[] = [2, 0, 2, 1, 1, 0]`  
  - **Output:** `[0, 0, 1, 1, 2, 2]`  
  - **Explanation:** The array is rearranged in a way that all 0's come first, followed by 1's, and then 2's.  
- **Code:**  
```java
import java.util.Arrays;

public class SortColors {
    public static void main(String[] args) {
        int[] nums = {2, 0, 2, 1, 1, 0};
        sortColors(nums);
        System.out.println(Arrays.toString(nums));
    }

    public static void sortColors(int[] nums) {
        int low = 0, mid = 0, high = nums.length - 1;
        while (mid <= high) {
            if (nums[mid] == 0) {
                swap(nums, low, mid);
                low++;
                mid++;
            } else if (nums[mid] == 1) {
                mid++;
            } else {
                swap(nums, mid, high);
                high--;
            }
        }
    }

    public static void swap(int[] nums, int i, int j) {
        int temp = nums[i];
        nums[i] = nums[j];
        nums[j] = temp;
    }
}

```

### Q26: WAJP to print the frequency of each element of the array if all given elements are in the range from 0 to 1000.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 2, 3, 3, 3, 4}`  
  - **Output:**  
    1. `1 appears 1 time`  
    2. `2 appears 2 times`  
    3. `3 appears 3 times`  
    4. `4 appears 1 time`  
  - **Explanation:** The elements are counted and printed along with their frequency.  
- **Code:**  
```java
import java.util.Arrays;

public class FrequencyInRange {
    public static void main(String[] args) {
        int[] array = {1, 2, 2, 3, 3, 3, 4};
        printFrequency(array);
    }

    public static void printFrequency(int[] array) {
        int[] frequency = new int[1001]; // Range from 0 to 1000
        for (int num : array) {
            frequency[num]++;
        }

        for (int i = 0; i < frequency.length; i++) {
            if (frequency[i] > 0) {
                System.out.println(i + " appears " + frequency[i] + " time(s)");
            }
        }
    }
}
```

---

### Q27: WAJP to print the frequency of each element of the array when elements provided are in any range.  
- **Example:**  
  - **Input:**  
    1. `array[] = {3, 1, 3, 2, 4, 2, 1, 5}`  
  - **Output:**  
    1. `3 appears 2 times`  
    2. `1 appears 2 times`  
    3. `2 appears 2 times`  
    4. `4 appears 1 time`  
    5. `5 appears 1 time`  
  - **Explanation:** The elements are counted and printed along with their frequency.  
- **Code:**  
```java
import java.util.HashMap;
import java.util.Map;

public class FrequencyAnyRange {
    public static void main(String[] args) {
        int[] array = {3, 1, 3, 2, 4, 2, 1, 5};
        printFrequency(array);
    }

    public static void printFrequency(int[] array) {
        Map<Integer, Integer> frequencyMap = new HashMap<>();
        
        for (int num : array) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
        }
        
        for (Map.Entry<Integer, Integer> entry : frequencyMap.entrySet()) {
            System.out.println(entry.getKey() + " appears " + entry.getValue() + " time(s)");
        }
    }
}
```

---

### Q28: WAJP to print each element of the array which has appeared only once in the array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 2, 3, 3, 3, 4}`  
  - **Output:**  
    `1 4`  
  - **Explanation:** Only `1` and `4` appear once in the array.  
- **Code:**  
```java
import java.util.HashMap;
import java.util.Map;

public class UniqueElements {
    public static void main(String[] args) {
        int[] array = {1, 2, 2, 3, 3, 3, 4};
        printUniqueElements(array);
    }

    public static void printUniqueElements(int[] array) {
        Map<Integer, Integer> frequencyMap = new HashMap<>();
        
        for (int num : array) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
        }
        
        for (Map.Entry<Integer, Integer> entry : frequencyMap.entrySet()) {
            if (entry.getValue() == 1) {
                System.out.print(entry.getKey() + " ");
            }
        }
    }
}
```

---

### Q29: WAJP to print each element of the array which has appeared more than once/which has duplicate values in the array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 2, 3, 3, 3, 4}`  
  - **Output:**  
    `2 3`  
  - **Explanation:** `2` and `3` appear more than once in the array.  
- **Code:**  
```java
import java.util.HashMap;
import java.util.Map;

public class DuplicateElements {
    public static void main(String[] args) {
        int[] array = {1, 2, 2, 3, 3, 3, 4};
        printDuplicateElements(array);
    }

    public static void printDuplicateElements(int[] array) {
        Map<Integer, Integer> frequencyMap = new HashMap<>();
        
        for (int num : array) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
        }
        
        for (Map.Entry<Integer, Integer> entry : frequencyMap.entrySet()) {
            if (entry.getValue() > 1) {
                System.out.print(entry.getKey() + " ");
            }
        }
    }
}
```

---

### Q30: WAJP to print all the elements of the array whose frequency is odd.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 2, 3, 3, 3, 4, 4, 4, 4}`  
  - **Output:**  
    `1 3`  
  - **Explanation:** Only `1` and `3` have odd frequencies in the array.  
- **Code:**  
```java
import java.util.HashMap;
import java.util.Map;

public class OddFrequencyElements {
    public static void main(String[] args) {
        int[] array = {1, 2, 2, 3, 3, 3, 4, 4, 4, 4};
        printOddFrequencyElements(array);
    }

    public static void printOddFrequencyElements(int[] array) {
        Map<Integer, Integer> frequencyMap = new HashMap<>();
        
        for (int num : array) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
        }
        
        for (Map.Entry<Integer, Integer> entry : frequencyMap.entrySet()) {
            if (entry.getValue() % 2 != 0) {
                System.out.print(entry.getKey() + " ");
            }
        }
    }
}
```

---

### Q31: WAJP to print the element and its frequency which has appeared for the maximum time in the array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 3, 4, 2, 2, 3}`  
  - **Output:**  
    `3 appears 3 time(s)`  
  - **Explanation:** `3` has appeared the maximum number of times (3 times).  
- **Code:**  
```java
import java.util.HashMap;
import java.util.Map;

public class MaxFrequencyElement {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 3, 4, 2, 2, 3};
        printMaxFrequencyElement(array);
    }

    public static void printMaxFrequencyElement(int[] array) {
        Map<Integer, Integer> frequencyMap = new HashMap<>();
        
        for (int num : array) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
        }
        
        int maxCount = 0;
        int maxElement = -1;
        
        for (Map.Entry<Integer, Integer> entry : frequencyMap.entrySet()) {
            if (entry.getValue() > maxCount) {
                maxCount = entry.getValue();
                maxElement = entry.getKey();
            }
        }
        
        System.out.println(maxElement + " appears " + maxCount + " time(s)");
    }
}
```

---

### Q32: WAJP to print the index and the value of the first non-repeating element in an array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 2, 3, 3, 3, 4}`  
  - **Output:**  
    `Index: 0, Value: 1`  
  - **Explanation:** `1` is the first non-repeating element in the array at index `0`.  
- **Code:**  
```java
import java.util.HashMap;
import java.util.Map;

public class FirstNonRepeatingElement {
    public static void main(String[] args) {
        int[] array = {1, 2, 2, 3, 3, 3, 4};
        printFirstNonRepeatingElement(array);
    }

    public static void printFirstNonRepeatingElement(int[] array) {
        Map<Integer, Integer> frequencyMap = new HashMap<>();
        
        for (int num : array) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num,

 0) + 1);
        }
        
        for (int i = 0; i < array.length; i++) {
            if (frequencyMap.get(array[i]) == 1) {
                System.out.println("Index: " + i + ", Value: " + array[i]);
                return;
            }
        }
        
        System.out.println("No non-repeating elements found");
    }
}
```

---

### Q33: WAJP to remove the duplicate values from the array and store all unique elements in a new array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 2, 3, 4, 4, 5}`  
  - **Output:**  
    `[1, 2, 3, 4, 5]`  
  - **Explanation:** The duplicates are removed, and only the unique elements are stored in the new array.  
- **Code:**  
```java
import java.util.Arrays;
import java.util.HashSet;

public class RemoveDuplicates {
    public static void main(String[] args) {
        int[] array = {1, 2, 2, 3, 4, 4, 5};
        int[] uniqueArray = removeDuplicates(array);
        System.out.println(Arrays.toString(uniqueArray));
    }

    public static int[] removeDuplicates(int[] array) {
        HashSet<Integer> set = new HashSet<>();
        
        for (int num : array) {
            set.add(num);
        }
        
        int[] uniqueArray = new int[set.size()];
        int i = 0;
        for (int num : set) {
            uniqueArray[i++] = num;
        }
        
        return uniqueArray;
    }
}
```

---

### Q34: WAJP to print true if all the elements in the array are unique.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5}`  
  - **Output:**  
    `true`  
  - **Explanation:** All elements in the array are unique.  
- **Code:**  
```java
import java.util.HashSet;

public class AllUniqueElements {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};
        System.out.println(areAllUnique(array));
    }

    public static boolean areAllUnique(int[] array) {
        HashSet<Integer> set = new HashSet<>();
        for (int num : array) {
            if (!set.add(num)) {
                return false;
            }
        }
        return true;
    }
}
```

---

### Q35: WAJP to print the biggest and second biggest element of the array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5}`  
  - **Output:**  
    `Biggest: 5, Second Biggest: 4`  
  - **Explanation:** `5` is the biggest element and `4` is the second biggest.  
- **Code:**  
```java
public class BiggestSecondBiggest {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};
        findBiggestAndSecondBiggest(array);
    }

    public static void findBiggestAndSecondBiggest(int[] array) {
        int biggest = Integer.MIN_VALUE;
        int secondBiggest = Integer.MIN_VALUE;
        
        for (int num : array) {
            if (num > biggest) {
                secondBiggest = biggest;
                biggest = num;
            } else if (num > secondBiggest && num != biggest) {
                secondBiggest = num;
            }
        }
        
        System.out.println("Biggest: " + biggest + ", Second Biggest: " + secondBiggest);
    }
}
```

---

### Q36: WAJP to print the smallest and second smallest element of the array.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5}`  
  - **Output:**  
    `Smallest: 1, Second Smallest: 2`  
  - **Explanation:** `1` is the smallest element and `2` is the second smallest.  
- **Code:**  
```java
public class SmallestSecondSmallest {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};
        findSmallestAndSecondSmallest(array);
    }

    public static void findSmallestAndSecondSmallest(int[] array) {
        int smallest = Integer.MAX_VALUE;
        int secondSmallest = Integer.MAX_VALUE;
        
        for (int num : array) {
            if (num < smallest) {
                secondSmallest = smallest;
                smallest = num;
            } else if (num < secondSmallest && num != smallest) {
                secondSmallest = num;
            }
        }
        
        System.out.println("Smallest: " + smallest + ", Second Smallest: " + secondSmallest);
    }
}

```

### Q37: WAJP to find the maximum product of two integers in a given array of positive integers.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5}`  
  - **Output:**  
    1. `Product: 20`  
  - **Explanation:** The maximum product comes from multiplying `4` and `5`, i.e., `4 * 5 = 20`.  
- **Code:**  
```java
public class MaxProduct {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};
        System.out.println("Product: " + findMaxProduct(array));
    }

    public static int findMaxProduct(int[] array) {
        int max1 = Integer.MIN_VALUE;
        int max2 = Integer.MIN_VALUE;

        for (int num : array) {
            if (num > max1) {
                max2 = max1;
                max1 = num;
            } else if (num > max2) {
                max2 = num;
            }
        }

        return max1 * max2;
    }
}
```

---

### Q38: WAJP to sort the array elements in ascending order.  
- **Example:**  
  - **Input:**  
    1. `array[] = {5, 2, 8, 3, 1}`  
  - **Output:**  
    1. `[1, 2, 3, 5, 8]`  
  - **Explanation:** The elements are arranged in ascending order.  
- **Code:**  
```java
import java.util.Arrays;

public class AscendingSort {
    public static void main(String[] args) {
        int[] array = {5, 2, 8, 3, 1};
        Arrays.sort(array);
        System.out.println(Arrays.toString(array));
    }
}
```

---

### Q39: WAJP to sort the array elements in descending order.  
- **Example:**  
  - **Input:**  
    1. `array[] = {5, 2, 8, 3, 1}`  
  - **Output:**  
    1. `[8, 5, 3, 2, 1]`  
  - **Explanation:** The elements are arranged in descending order.  
- **Code:**  
```java
import java.util.Arrays;
import java.util.Collections;

public class DescendingSort {
    public static void main(String[] args) {
        Integer[] array = {5, 2, 8, 3, 1};
        Arrays.sort(array, Collections.reverseOrder());
        System.out.println(Arrays.toString(array));
    }
}
```

---

### Q40: WAJP to print the first half of the array elements in ascending order and the second half of the elements in descending order.  
- **Example:**  
  - **Input:**  
    1. `array[] = {25, 34, 12, 45, 23, 28}`  
  - **Output:**  
    1. `[12, 25, 34, 45, 28, 23]`  
  - **Explanation:** The first half `[25, 34, 12]` is sorted in ascending order, and the second half `[45, 23, 28]` is sorted in descending order.  
- **Code:**  
```java
import java.util.Arrays;
import java.util.Collections;

public class HalfAscendingHalfDescending {
    public static void main(String[] args) {
        int[] array = {25, 34, 12, 45, 23, 28};
        printSortedHalves(array);
    }

    public static void printSortedHalves(int[] array) {
        int mid = array.length / 2;

        int[] firstHalf = Arrays.copyOfRange(array, 0, mid);
        int[] secondHalf = Arrays.copyOfRange(array, mid, array.length);

        Arrays.sort(firstHalf);
        Arrays.sort(secondHalf);

        System.out.println(Arrays.toString(firstHalf));
        Integer[] secondHalfDesc = Arrays.stream(secondHalf)
                                         .boxed()
                                         .toArray(Integer[]::new);
        Arrays.sort(secondHalfDesc, Collections.reverseOrder());
        System.out.println(Arrays.toString(secondHalfDesc));
    }
}
```

---

### Q41: WAJP to print the first half of the array in ascending order and the second half in descending order.  
- **Example:**  
  - **Input:**  
    1. `array[] = {25, 34, 12, 45, 23, 28}`  
  - **Output:**  
    1. `[12, 23, 25, 45, 34, 28]`  
  - **Explanation:** The first half `[25, 34, 12]` is sorted in ascending order, and the second half `[45, 23, 28]` is sorted in descending order.  
- **Code:**  
```java
import java.util.Arrays;
import java.util.Collections;

public class HalfAscendingHalfDescending2 {
    public static void main(String[] args) {
        int[] array = {25, 34, 12, 45, 23, 28};
        printSortedHalves(array);
    }

    public static void printSortedHalves(int[] array) {
        int mid = array.length / 2;

        int[] firstHalf = Arrays.copyOfRange(array, 0, mid);
        int[] secondHalf = Arrays.copyOfRange(array, mid, array.length);

        Arrays.sort(firstHalf);
        Arrays.sort(secondHalf);

        Integer[] secondHalfDesc = Arrays.stream(secondHalf)
                                         .boxed()
                                         .toArray(Integer[]::new);
        Arrays.sort(secondHalfDesc, Collections.reverseOrder());
        
        System.out.println(Arrays.toString(firstHalf));
        System.out.println(Arrays.toString(secondHalfDesc));
    }
}
```

---

### Q42: WAJP to print true if elements of an array are the same when read from front or from back; otherwise, print false.  
- **Example:**  
  - **Input:**  
    1. `array[] = {12, 23, 15, 15, 23, 12}`  
  - **Output:**  
    1. `true`  
  - **Explanation:** The array is the same when read from front to back or back to front.  
- **Code:**  
```java
public class PalindromeArray {
    public static void main(String[] args) {
        int[] array = {12, 23, 15, 15, 23, 12};
        System.out.println(isPalindrome(array));
    }

    public static boolean isPalindrome(int[] array) {
        int start = 0;
        int end = array.length - 1;

        while (start < end) {
            if (array[start] != array[end]) {
                return false;
            }
            start++;
            end--;
        }

        return true;
    }
}
```

---

### Q43: WAJP to find the missing element.  
- **Example:**  
  - **Input:**  
    1. `array[] = {7, 4, 3, 5, 1, 6}`  
  - **Output:**  
    1. `2`  
  - **Explanation:** The missing element between 1 and 7 is `2`.  
- **Code:**  
```java
public class MissingElement {
    public static void main(String[] args) {
        int[] array = {7, 4, 3, 5, 1, 6};
        System.out.println("Missing element: " + findMissingElement(array));
    }

    public static int findMissingElement(int[] array) {
        int n = array.length + 1;
        int totalSum = n * (n + 1) / 2;
        int arraySum = 0;

        for (int num : array) {
            arraySum += num;
        }

        return totalSum - arraySum;
    }
}
```

---

### Q44: WAJP to check if an array is strictly increasing.  
- **Example:**  
  - **Input:**  
    1. `array[] = {2, 3, 7, 8, 9}`  
  - **Output:**  
    1. `Array is strictly increasing`  
  - **Explanation:** The array elements are strictly increasing.  
- **Code:**  
```java
public class StrictlyIncreasing {
    public static void main(String[] args) {
        int[] array = {2, 3, 7, 8, 9};
        System.out.println(isStrictlyIncreasing(array));
    }

    public static boolean isStrictlyIncreasing(int[] array) {
        for (int i = 1; i < array.length; i++) {
            if (array[i] <= array[i - 1]) {
                return false;
            }
        }
        return true;
    }
}
```

---

### Q45: WAJP to check whether a given array is in sorted order or not.  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5}`  
  - **Output:**  
    1. `Array is sorted`  
  - **Explanation:** The array is in sorted order (ascending).  
- **Code:**  
```java
public class SortedArray {
    public static void main(String[] args) {
        int[] array = {1

, 2, 3, 4, 5};
        System.out.println(isSorted(array));
    }

    public static boolean isSorted(int[] array) {
        for (int i = 1; i < array.length; i++) {
            if (array[i] < array[i - 1]) {
                return false;
            }
        }
        return true;
    }
}
```
---

### Q46: [Migratory Birds - Hackerrank](https://www.hackerrank.com/challenges/migratory-birds/problem)  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 1, 2, 2, 3}`  
  - **Output:**  
    1. `1`  
  - **Explanation:** The most frequent bird is `1` (appears 2 times).  
- **Code:**  
```java
import java.util.*;

public class MigratoryBirds {
    public static void main(String[] args) {
        int[] birds = {1, 1, 2, 2, 3};
        System.out.println(mostFrequentBird(birds));
    }

    public static int mostFrequentBird(int[] birds) {
        Map<Integer, Integer> birdCount = new HashMap<>();
        for (int bird : birds) {
            birdCount.put(bird, birdCount.getOrDefault(bird, 0) + 1);
        }

        int mostFrequent = birds[0];
        int maxCount = birdCount.get(mostFrequent);

        for (Map.Entry<Integer, Integer> entry : birdCount.entrySet()) {
            if (entry.getValue() > maxCount) {
                mostFrequent = entry.getKey();
                maxCount = entry.getValue();
            } else if (entry.getValue() == maxCount && entry.getKey() < mostFrequent) {
                mostFrequent = entry.getKey();
            }
        }

        return mostFrequent;
    }
}
```

---

### Q47: [Implement binary search algorithm](https://www.geeksforgeeks.org/binary-search/)  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}, target = 5`  
  - **Output:**  
    1. `Index: 4`  
  - **Explanation:** The target `5` is found at index `4`.  
- **Code:**  
```java
public class BinarySearch {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
        int target = 5;
        System.out.println("Index: " + binarySearch(array, target));
    }

    public static int binarySearch(int[] array, int target) {
        int left = 0;
        int right = array.length - 1;

        while (left <= right) {
            int mid = left + (right - left) / 2;

            if (array[mid] == target) {
                return mid;
            } else if (array[mid] < target) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }

        return -1;  // Target not found
    }
}
```

---

### Q48: [First Missing Positive - LeetCode](https://leetcode.com/problems/first-missing-positive/)  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 2, 0}`  
  - **Output:**  
    1. `3`  
  - **Explanation:** The first missing positive integer is `3`.  
- **Code:**  
```java
public class FirstMissingPositive {
    public static void main(String[] args) {
        int[] array = {1, 2, 0};
        System.out.println(firstMissingPositive(array));
    }

    public static int firstMissingPositive(int[] nums) {
        int n = nums.length;

        for (int i = 0; i < n; i++) {
            while (nums[i] > 0 && nums[i] <= n && nums[nums[i] - 1] != nums[i]) {
                int temp = nums[i];
                nums[i] = nums[nums[i] - 1];
                nums[temp - 1] = temp;
            }
        }

        for (int i = 0; i < n; i++) {
            if (nums[i] != i + 1) {
                return i + 1;
            }
        }

        return n + 1;
    }
}
```

---

### Q49: [Remove Duplicates from Sorted Array - LeetCode](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)  
- **Example:**  
  - **Input:**  
    1. `array[] = {1, 1, 2, 3, 3}`  
  - **Output:**  
    1. `array[] = {1, 2, 3}`  
  - **Explanation:** Duplicates are removed from the sorted array.  
- **Code:**  
```java
public class RemoveDuplicates {
    public static void main(String[] args) {
        int[] array = {1, 1, 2, 3, 3};
        System.out.println(removeDuplicates(array));
    }

    public static int removeDuplicates(int[] nums) {
        if (nums.length == 0) {
            return 0;
        }

        int index = 1;
        for (int i = 1; i < nums.length; i++) {
            if (nums[i] != nums[i - 1]) {
                nums[index++] = nums[i];
            }
        }

        return index;
    }
}
```

---

### Q50: [Count Primes - LeetCode](https://leetcode.com/problems/count-primes/)  
- **Example:**  
  - **Input:**  
    1. `n = 10`  
  - **Output:**  
    1. `4`  
  - **Explanation:** The prime numbers less than 10 are 2, 3, 5, and 7.  
- **Code:**  
```java
public class CountPrimes {
    public static void main(String[] args) {
        int n = 10;
        System.out.println(countPrimes(n));
    }

    public static int countPrimes(int n) {
        boolean[] isPrime = new boolean[n];
        int count = 0;

        for (int i = 2; i < n; i++) {
            if (!isPrime[i]) {
                count++;
                for (int j = 2 * i; j < n; j += i) {
                    isPrime[j] = true;
                }
            }
        }

        return count;
    }
}
```

---

### Q51: [Third Maximum Number - LeetCode](https://leetcode.com/problems/third-maximum-number/)  
- **Example:**  
  - **Input:**  
    1. `array[] = {3, 2, 1}`  
  - **Output:**  
    1. `1`  
  - **Explanation:** The third maximum number is `1`.  
- **Code:**  
```java
import java.util.*;

public class ThirdMaximumNumber {
    public static void main(String[] args) {
        int[] array = {3, 2, 1};
        System.out.println(thirdMax(array));
    }

    public static int thirdMax(int[] nums) {
        TreeSet<Integer> set = new TreeSet<>();
        for (int num : nums) {
            set.add(num);
            if (set.size() > 3) {
                set.pollFirst();
            }
        }

        if (set.size() == 3) {
            return set.first();
        }

        return set.last();
    }
}
```

---