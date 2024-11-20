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

Apologies for the confusion! I'll now stick strictly to your original set of questions and provide the solutions exactly as you specified. Here's the corrected version for questions 7 through 24:

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

### Q17: WAJP to find the sum of all elements in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `15`  
  - **Explanation:** The sum of the elements is calculated.  
- **Code:**  
```java
public class SumArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int sum = 0;

        for (int num : arr) {
            sum += num;
        }

        System.out.println("Sum of array elements: " + sum);
    }
}
```

---

### Q18: WAJP to find the average of all elements in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `3.0`  
  - **Explanation:** The average is calculated by dividing the sum by the number of elements.  
- **Code:**  
```java
public class AverageArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int sum = 0;

        for (int num : arr) {
            sum += num;
        }

        double average = (double) sum / arr.length;
        System.out.println("Average of array elements: " + average);
    }
}
```

---

### Q19: WAJP to find the largest number in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `5`  
  - **Explanation:** The largest number in the array is 5.  
- **Code:**  
```java
public class LargestNumber {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int largest = arr[0];

        for (int num : arr) {
            if (num > largest) {
                largest = num;
            }
        }

        System.out.println("Largest number: " + largest);
    }
}
```

---

### Q20: WAJP to find the smallest number in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `1`  
  - **Explanation:** The smallest number in the array is 1.  
- **Code:**  
```java
public class SmallestNumber {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int smallest = arr[0];

        for (int num : arr) {
            if (num < smallest) {
                smallest = num;
            }
        }

        System.out.println("Smallest number: " + smallest);
    }
}
```

---

### Q21: WAJP to print the second largest number in the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `4`  
  - **Explanation:** The second largest number in the array is 4.  
- **Code:**  
```java
public class SecondLargestNumber {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int largest = arr[0];
        int secondLargest = Integer.MIN_VALUE;

        for (int num : arr) {
            if (num > largest) {
                secondLargest = largest;
                largest = num;
            } else if (num > secondLargest && num != largest) {
                secondLargest = num;
            }
        }

        System.out.println("Second largest number: " + secondLargest);
    }
}
```

---

### Q22: WAJP to check if the array is sorted in ascending order.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`  
  - **Output:** `Array is sorted in ascending order`  
  - **Explanation:** The array is checked for ascending order.  
- **Code:**  
```java
public class ArraySortedAscending {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        boolean isSorted = true;

        for (int i = 0; i < arr.length - 1; i++) {
            if (arr[i] > arr[i + 1]) {
                isSorted = false;
                break;
            }
        }

        if (isSorted) {
            System.out.println("Array is sorted in ascending order");
        } else {
            System.out.println("Array is not sorted in ascending order");
        }
    }
}
```

---

### Q23: WAJP to check if the array is sorted in descending order.  
- **Example:**  
  - **Input:** `[5, 4, 3, 2, 1]`  
  - **Output:** `Array is sorted in descending order`  
  - **Explanation:** The array is checked for descending order.  
- **Code:**  
```java
public class ArraySortedDescending {
    public static void main(String[] args) {
        int[] arr = {5, 4, 3, 2, 1};
        boolean isSorted = true;

        for (int i = 0; i < arr.length - 1; i++) {
            if (arr[i] < arr[i + 1]) {
                isSorted = false;
                break;
            }
        }

        if (isSorted) {
            System.out.println("Array is sorted in descending order");
        } else {
            System.out.println("Array is not sorted in descending order");
        }
    }
}
```

---

### Q24: WAJP to remove duplicates from the array.  
- **Example:**  
  - **Input:** `[1, 2, 3, 2, 4, 5, 4]`  
  - **Output:** `[1, 2, 3, 4, 5]`  
  - **Explanation:** The duplicates are removed from the array.  
- **Code:**  
```java
import java.util.HashSet;

public class RemoveDuplicates {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 2, 4, 5, 4};
        HashSet<Integer> set = new HashSet<>();

        for (int num : arr) {
            set.add(num);
        }

        System.out.println("Array after removing duplicates: " + set);
    }
}
```

---

### Q25: WAJP to merge two arrays.  
- **Example:**  
  - **Input:** `[1, 2, 3]`, `[4, 5, 6]`  
  - **Output:** `[1, 2, 3, 4, 5, 6]`  
  - **Explanation:** The two arrays are merged into one.  
- **Code:**  
```java
import java.util.Arrays;

public class MergeArrays {
    public static void main(String[] args) {
        int[] arr1 = {1, 2, 3};
        int[] arr2 = {4, 5, 6};

        int[] merged = new int[arr1.length + arr2.length];

        System.arraycopy(arr1, 0, merged, 0, arr1.length);
        System.arraycopy(arr2, 0, merged, arr1.length, arr2.length);

        System.out.println("Merged array: " + Arrays.toString(merged));
    }
}
```

---

### Q26: WAJP to find if an array contains a specific element.  
- **Example:**  
  - **Input:** `[1, 2, 3, 4, 5]`, `element = 3`  
  - **Output:** `Element 3 found in the array`  
  - **Explanation:** The program checks whether the specified element is present in the array.  
- **Code:**  
```java
public class ContainsElement {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int element = 3;
        boolean found = false;

        for (int num : arr) {
            if (num == element) {
                found = true;
                break;
            }
        }

        if (found) {
            System.out.println("Element " + element + " found in the array");
        } else {
            System.out.println("Element " + element + " not found in the array");
        }
    }
}
```

---

### Q27: WAJP to count the occurrences of a specific element in the array.  
- **Example:**  
  - **Input:** `[1, 2, 2, 3, 2, 4, 5]`, `element = 2`  
  - **Output:** `Element 2 occurs 3 times`  
  - **Explanation:** The number 2 appears 3 times in the array.  
- **Code:**  
```java
public class CountOccurrences {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 2, 4, 5};
        int element = 2;
        int count = 0;

        for (int num : arr) {
            if (num == element) {
                count++;
            }
        }

        System.out.println("Element " + element + " occurs " + count + " times");
    }
}
```

---

### Q28: WAJP to find the sum of digits of a given number.  
- **Example:**  
  - **Input:** `12345`  
  - **Output:** `15`  
  - **Explanation:** The sum of the digits 1 + 2 + 3 + 4 + 5

 = 15.  
- **Code:**  
```java
public class SumOfDigits {
    public static void main(String[] args) {
        int num = 12345;
        int sum = 0;

        while (num != 0) {
            sum += num % 10;
            num /= 10;
        }

        System.out.println("Sum of digits: " + sum);
    }
}
```

---

### Q29: WAJP to reverse the digits of a given number.  
- **Example:**  
  - **Input:** `12345`  
  - **Output:** `54321`  
  - **Explanation:** The digits of the number are reversed.  
- **Code:**  
```java
public class ReverseDigits {
    public static void main(String[] args) {
        int num = 12345;
        int reversed = 0;

        while (num != 0) {
            reversed = reversed * 10 + num % 10;
            num /= 10;
        }

        System.out.println("Reversed number: " + reversed);
    }
}
```

---


### Q30: WAJP to check if a number is prime.  
- **Example:**  
  - **Input:** `7`  
  - **Output:** `7 is a prime number`  
  - **Explanation:** The number 7 is prime because it is only divisible by 1 and itself.  
- **Code:**  
```java
public class PrimeNumber {
    public static void main(String[] args) {
        int num = 7;
        boolean isPrime = true;

        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime && num > 1) {
            System.out.println(num + " is a prime number");
        } else {
            System.out.println(num + " is not a prime number");
        }
    }
}
```

---

### Q31: WAJP to find the factorial of a number.  
- **Example:**  
  - **Input:** `5`  
  - **Output:** `120`  
  - **Explanation:** The factorial of 5 is `5 * 4 * 3 * 2 * 1 = 120`.  
- **Code:**  
```java
public class Factorial {
    public static void main(String[] args) {
        int num = 5;
        int factorial = 1;

        for (int i = 1; i <= num; i++) {
            factorial *= i;
        }

        System.out.println("Factorial of " + num + " is: " + factorial);
    }
}
```

---

### Q32: WAJP to print Fibonacci series up to N terms.  
- **Example:**  
  - **Input:** `5`  
  - **Output:** `0, 1, 1, 2, 3`  
  - **Explanation:** The Fibonacci series is generated by summing the two previous numbers.  
- **Code:**  
```java
public class FibonacciSeries {
    public static void main(String[] args) {
        int N = 5;
        int first = 0, second = 1;

        System.out.print("Fibonacci series: ");
        for (int i = 0; i < N; i++) {
            System.out.print(first + " ");
            int next = first + second;
            first = second;
            second = next;
        }
    }
}
```

---

### Q33: WAJP to find the GCD (Greatest Common Divisor) of two numbers.  
- **Example:**  
  - **Input:** `12, 18`  
  - **Output:** `6`  
  - **Explanation:** The GCD of 12 and 18 is 6, as it's the largest number that divides both.  
- **Code:**  
```java
public class GCD {
    public static void main(String[] args) {
        int num1 = 12, num2 = 18;
        int gcd = 1;

        for (int i = 1; i <= Math.min(num1, num2); i++) {
            if (num1 % i == 0 && num2 % i == 0) {
                gcd = i;
            }
        }

        System.out.println("GCD of " + num1 + " and " + num2 + " is: " + gcd);
    }
}
```

---

### Q34: WAJP to find the LCM (Least Common Multiple) of two numbers.  
- **Example:**  
  - **Input:** `12, 18`  
  - **Output:** `36`  
  - **Explanation:** The LCM of 12 and 18 is 36, as it's the smallest number that both divide evenly into.  
- **Code:**  
```java
public class LCM {
    public static void main(String[] args) {
        int num1 = 12, num2 = 18;
        int lcm = (num1 * num2) / gcd(num1, num2);

        System.out.println("LCM of " + num1 + " and " + num2 + " is: " + lcm);
    }

    public static int gcd(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }
}
```

---

### Q35: WAJP to convert a decimal number to binary.  
- **Example:**  
  - **Input:** `10`  
  - **Output:** `1010`  
  - **Explanation:** The binary representation of 10 is `1010`.  
- **Code:**  
```java
public class DecimalToBinary {
    public static void main(String[] args) {
        int num = 10;
        String binary = Integer.toBinaryString(num);

        System.out.println("Binary of " + num + " is: " + binary);
    }
}
```

---

### Q36: WAJP to convert a binary number to decimal.  
- **Example:**  
  - **Input:** `1010`  
  - **Output:** `10`  
  - **Explanation:** The decimal equivalent of the binary number `1010` is 10.  
- **Code:**  
```java
public class BinaryToDecimal {
    public static void main(String[] args) {
        String binary = "1010";
        int decimal = Integer.parseInt(binary, 2);

        System.out.println("Decimal of " + binary + " is: " + decimal);
    }
}
```

---

### Q37: WAJP to find the square root of a number.  
- **Example:**  
  - **Input:** `16`  
  - **Output:** `4.0`  
  - **Explanation:** The square root of 16 is 4.0.  
- **Code:**  
```java
public class SquareRoot {
    public static void main(String[] args) {
        double num = 16;
        double sqrt = Math.sqrt(num);

        System.out.println("Square root of " + num + " is: " + sqrt);
    }
}
```

---

### Q38: WAJP to calculate the power of a number (x raised to the power of y).  
- **Example:**  
  - **Input:** `2, 3`  
  - **Output:** `8`  
  - **Explanation:** `2^3 = 8`  
- **Code:**  
```java
public class PowerOfNumber {
    public static void main(String[] args) {
        int x = 2, y = 3;
        double result = Math.pow(x, y);

        System.out.println(x + " raised to the power of " + y + " is: " + result);
    }
}
```

---

### Q39: WAJP to check if a number is an Armstrong number.  
- **Example:**  
  - **Input:** `153`  
  - **Output:** `153 is an Armstrong number`  
  - **Explanation:** An Armstrong number is a number that is equal to the sum of its own digits each raised to the power of the number of digits.  
- **Code:**  
```java
public class ArmstrongNumber {
    public static void main(String[] args) {
        int num = 153;
        int originalNum = num;
        int sum = 0;
        int digits = String.valueOf(num).length();

        while (num != 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        if (sum == originalNum) {
            System.out.println(originalNum + " is an Armstrong number");
        } else {
            System.out.println(originalNum + " is not an Armstrong number");
        }
    }
}
```

---

### Q40: WAJP to find the sum of the first N natural numbers.  
- **Example:**  
  - **Input:** `5`  
  - **Output:** `15`  
  - **Explanation:** The sum of the first 5 natural numbers is `1 + 2 + 3 + 4 + 5 = 15`.  
- **Code:**  
```java
public class SumOfNaturalNumbers {
    public static void main(String[] args) {
        int N = 5;
        int sum = N * (N + 1) / 2;

        System.out.println("Sum of first " + N + " natural numbers is: " + sum);
    }
}
```

---

### Q41: WAJP to calculate the area of a circle.  
- **Example:**  
  - **Input:** `radius = 7`  
  - **Output:** `153.93804002589985`  
  - **Explanation:** The area of a circle is calculated as π * r^2.  
- **Code:**  
```java
public class CircleArea {
    public static void main(String[] args) {
        double radius = 7;
        double area = Math.PI * Math.pow(radius, 2);

        System.out.println("Area of circle with radius " + radius + " is: " + area);
    }
}
```

---

### Q42: WAJP to calculate the perimeter of a rectangle.  
- **Example:**  
  - **Input:** `length = 5, width = 3`  
  - **Output:** `16`  
  - **Explanation:** The perimeter of a rectangle is calculated as 2 * (length + width).  
- **Code:**  
```java
public class RectanglePerimeter {


    public static void main(String[] args) {
        double length = 5, width = 3;
        double perimeter = 2 * (length + width);

        System.out.println("Perimeter of rectangle is: " + perimeter);
    }
}
```

---

### Q43: WAJP to find the area of a triangle using Heron's formula.  
- **Example:**  
  - **Input:** `a = 5, b = 6, c = 7`  
  - **Output:** `14.7`  
  - **Explanation:** The area of the triangle is calculated using Heron's formula:  
    \( A = \sqrt{s(s - a)(s - b)(s - c)} \)  
    where \( s = \frac{a + b + c}{2} \).  
- **Code:**  
```java
public class TriangleArea {
    public static void main(String[] args) {
        double a = 5, b = 6, c = 7;
        double s = (a + b + c) / 2;
        double area = Math.sqrt(s * (s - a) * (s - b) * (s - c));

        System.out.println("Area of triangle is: " + area);
    }
}
```

---

### Q44: WAJP to check if a number is a perfect number.  
- **Example:**  
  - **Input:** `28`  
  - **Output:** `28 is a perfect number`  
  - **Explanation:** A perfect number is a positive integer that is equal to the sum of its proper divisors, excluding itself.  
- **Code:**  
```java
public class PerfectNumber {
    public static void main(String[] args) {
        int num = 28;
        int sum = 0;

        for (int i = 1; i <= num / 2; i++) {
            if (num % i == 0) {
                sum += i;
            }
        }

        if (sum == num) {
            System.out.println(num + " is a perfect number");
        } else {
            System.out.println(num + " is not a perfect number");
        }
    }
}
```

---

### Q45: WAJP to find the sum of the squares of the first N natural numbers.  
- **Example:**  
  - **Input:** `5`  
  - **Output:** `55`  
  - **Explanation:** The sum of the squares of the first 5 natural numbers is \(1^2 + 2^2 + 3^2 + 4^2 + 5^2 = 55\).  
- **Code:**  
```java
public class SumOfSquares {
    public static void main(String[] args) {
        int N = 5;
        int sum = 0;

        for (int i = 1; i <= N; i++) {
            sum += i * i;
        }

        System.out.println("Sum of squares of first " + N + " natural numbers is: " + sum);
    }
}
```

---


### Q46: WAJP to check if a number is a palindrome.  
- **Example:**  
  - **Input:** `121`  
  - **Output:** `121 is a palindrome`  
  - **Explanation:** A number is a palindrome if it reads the same forward and backward.  
- **Code:**  
```java
public class PalindromeNumber {
    public static void main(String[] args) {
        int num = 121;
        int originalNum = num;
        int reversed = 0;

        while (num != 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num /= 10;
        }

        if (originalNum == reversed) {
            System.out.println(originalNum + " is a palindrome");
        } else {
            System.out.println(originalNum + " is not a palindrome");
        }
    }
}
```

---

### Q47: WAJP to count the number of vowels in a string.  
- **Example:**  
  - **Input:** `"hello"`  
  - **Output:** `2`  
  - **Explanation:** The vowels in "hello" are 'e' and 'o', so there are 2 vowels.  
- **Code:**  
```java
public class VowelCount {
    public static void main(String[] args) {
        String str = "hello";
        int count = 0;

        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
                ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
                count++;
            }
        }

        System.out.println("Number of vowels: " + count);
    }
}
```

---

### Q48: WAJP to count the number of words in a string.  
- **Example:**  
  - **Input:** `"This is a test"`  
  - **Output:** `4`  
  - **Explanation:** There are 4 words in the string "This is a test".  
- **Code:**  
```java
public class WordCount {
    public static void main(String[] args) {
        String str = "This is a test";
        String[] words = str.split("\\s+");
        
        System.out.println("Number of words: " + words.length);
    }
}
```

---

### Q49: WAJP to reverse a string.  
- **Example:**  
  - **Input:** `"hello"`  
  - **Output:** `"olleh"`  
  - **Explanation:** The reverse of the string "hello" is "olleh".  
- **Code:**  
```java
public class ReverseString {
    public static void main(String[] args) {
        String str = "hello";
        String reversed = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }

        System.out.println("Reversed string: " + reversed);
    }
}
```

---

### Q50: WAJP to check if a string is a palindrome.  
- **Example:**  
  - **Input:** `"madam"`  
  - **Output:** `"madam is a palindrome"`  
  - **Explanation:** A string is a palindrome if it reads the same forward and backward.  
- **Code:**  
```java
public class StringPalindrome {
    public static void main(String[] args) {
        String str = "madam";
        String reversed = new StringBuilder(str).reverse().toString();

        if (str.equals(reversed)) {
            System.out.println(str + " is a palindrome");
        } else {
            System.out.println(str + " is not a palindrome");
        }
    }
}
```

---

### Q51: WAJP to find the largest word in a string.  
- **Example:**  
  - **Input:** `"The quick brown fox jumps over the lazy dog"`  
  - **Output:** `"jumps"`  
  - **Explanation:** The largest word in the string is "jumps".  
- **Code:**  
```java
public class LargestWord {
    public static void main(String[] args) {
        String str = "The quick brown fox jumps over the lazy dog";
        String[] words = str.split("\\s+");

        String largestWord = words[0];
        for (String word : words) {
            if (word.length() > largestWord.length()) {
                largestWord = word;
            }
        }

        System.out.println("Largest word is: " + largestWord);
    }
}
```

---

### Q52: WAJP to check if a string is an anagram of another string.  
- **Example:**  
  - **Input:** `"listen", "silent"`  
  - **Output:** `"listen and silent are anagrams"`  
  - **Explanation:** Two strings are anagrams if they contain the same characters in a different order.  
- **Code:**  
```java
import java.util.Arrays;

public class AnagramCheck {
    public static void main(String[] args) {
        String str1 = "listen";
        String str2 = "silent";

        char[] str1Array = str1.toCharArray();
        char[] str2Array = str2.toCharArray();

        Arrays.sort(str1Array);
        Arrays.sort(str2Array);

        if (Arrays.equals(str1Array, str2Array)) {
            System.out.println(str1 + " and " + str2 + " are anagrams");
        } else {
            System.out.println(str1 + " and " + str2 + " are not anagrams");
        }
    }
}
```

---

### Q53: WAJP to convert all characters in a string to uppercase.  
- **Example:**  
  - **Input:** `"hello"`  
  - **Output:** `"HELLO"`  
  - **Explanation:** The string "hello" is converted to uppercase as "HELLO".  
- **Code:**  
```java
public class UppercaseString {
    public static void main(String[] args) {
        String str = "hello";
        String upperStr = str.toUpperCase();

        System.out.println("Uppercase string: " + upperStr);
    }
}
```

---

### Q54: WAJP to convert all characters in a string to lowercase.  
- **Example:**  
  - **Input:** `"HELLO"`  
  - **Output:** `"hello"`  
  - **Explanation:** The string "HELLO" is converted to lowercase as "hello".  
- **Code:**  
```java
public class LowercaseString {
    public static void main(String[] args) {
        String str = "HELLO";
        String lowerStr = str.toLowerCase();

        System.out.println("Lowercase string: " + lowerStr);
    }
}
```

