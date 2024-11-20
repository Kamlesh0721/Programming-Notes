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

