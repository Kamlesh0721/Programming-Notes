# Number Programming


### Q1: WAJP to take user input and count the number of bits in that number.  
- **Example:**  
  - **Input:**  
    1. `n = 13`  
  - **Output:**  
    1. `Bits: 4`  
  - **Explanation:** Binary representation of `13` is `1101`, which has `4` bits.  
- **Code:**  
```java
import java.util.Scanner;

public class CountBits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        System.out.println("Bits: " + Integer.toBinaryString(n).length());
    }
}
```

---

### Q2: WAJP to take user input and count the number of 0’s bits and 1’s bits in that number.  
- **Example:**  
  - **Input:**  
    1. `n = 13`  
  - **Output:**  
    1. `1’s: 3, 0’s: 1`  
  - **Explanation:** Binary representation of `13` is `1101`, which has `3` ones and `1` zero.  
- **Code:**  
```java
import java.util.Scanner;

public class CountZeroesAndOnes {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        String binary = Integer.toBinaryString(n);

        int countOnes = 0, countZeroes = 0;
        for (char bit : binary.toCharArray()) {
            if (bit == '1') countOnes++;
            else countZeroes++;
        }

        System.out.println("1’s: " + countOnes + ", 0’s: " + countZeroes);
    }
}
```

---

### Q3: [191. Number of 1 Bits - LeetCode](https://leetcode.com/problems/number-of-1-bits/)  
- **Example:**  
  - **Input:**  
    1. `n = 11`  
  - **Output:**  
    1. `3`  
  - **Explanation:** Binary representation of `11` is `1011`, which has `3` ones.  
- **Code:**  
```java
public class NumberOf1Bits {
    public static void main(String[] args) {
        int n = 11; // Example input
        System.out.println(hammingWeight(n));
    }

    public static int hammingWeight(int n) {
        int count = 0;
        while (n != 0) {
            count += n & 1;
            n >>= 1;
        }
        return count;
    }
}
```

---

### Q4: [Counting Bits - LeetCode](https://leetcode.com/problems/counting-bits/)  
- **Example:**  
  - **Input:**  
    1. `n = 5`  
  - **Output:**  
    1. `[0, 1, 1, 2, 1, 2]`  
  - **Explanation:** Count of 1’s in binary representation for `0 to 5` are:  
    `0 -> 0, 1 -> 1, 2 -> 1, 3 -> 2, 4 -> 1, 5 -> 2`.  
- **Code:**  
```java
import java.util.Arrays;

public class CountingBits {
    public static void main(String[] args) {
        int n = 5; // Example input
        System.out.println(Arrays.toString(countBits(n)));
    }

    public static int[] countBits(int n) {
        int[] result = new int[n + 1];
        for (int i = 1; i <= n; i++) {
            result[i] = result[i >> 1] + (i & 1);
        }
        return result;
    }
}
```

---

### Q5: [762. Prime Number of Set Bits in Binary Representation](https://leetcode.com/problems/prime-number-of-set-bits-in-binary-representation/)  
- **Example:**  
  - **Input:**  
    1. `L = 6, R = 10`  
  - **Output:**  
    1. `4`  
  - **Explanation:** Numbers `6, 7, 8, 9, 10` have set bits: `[2, 3, 1, 2, 2]`. Primes: `2, 3`. Count: `4`.  
- **Code:**  
```java
import java.util.Set;
import java.util.HashSet;

public class PrimeSetBits {
    public static void main(String[] args) {
        int L = 6, R = 10;
        System.out.println(countPrimeSetBits(L, R));
    }

    public static int countPrimeSetBits(int L, int R) {
        Set<Integer> primes = Set.of(2, 3, 5, 7, 11, 13, 17, 19);
        int count = 0;

        for (int i = L; i <= R; i++) {
            int bits = Integer.bitCount(i);
            if (primes.contains(bits)) {
                count++;
            }
        }
        return count;
    }
}
```

---

### Q6: [2595. Number of Even and Odd Bits](https://leetcode.com/problems/number-of-even-and-odd-bits/)  
- **Example:**  
  - **Input:**  
    1. `n = 17`  
  - **Output:**  
    1. `Even Bits: 1, Odd Bits: 1`  
  - **Explanation:** Binary of `17` is `10001`, even-position bits: `1`, odd-position bits: `1`.  
- **Code:**  
```java
public class EvenOddBits {
    public static void main(String[] args) {
        int n = 17;
        countEvenOddBits(n);
    }

    public static void countEvenOddBits(int n) {
        int even = 0, odd = 0, position = 0;

        while (n > 0) {
            if ((n & 1) == 1) {
                if (position % 2 == 0) even++;
                else odd++;
            }
            position++;
            n >>= 1;
        }

        System.out.println("Even Bits: " + even + ", Odd Bits: " + odd);
    }
}
```

---

### Q7: [Binary Number with Alternating Bits - LeetCode](https://leetcode.com/problems/binary-number-with-alternating-bits/)  
- **Example:**  
  - **Input:**  
    1. `n = 5`  
  - **Output:**  
    1. `true`  
  - **Explanation:** Binary of `5` is `101`, alternating bits are present.  
- **Code:**  
```java
public class AlternatingBits {
    public static void main(String[] args) {
        int n = 5;
        System.out.println(hasAlternatingBits(n));
    }

    public static boolean hasAlternatingBits(int n) {
        int prev = n & 1;
        n >>= 1;

        while (n > 0) {
            int current = n & 1;
            if (current == prev) return false;
            prev = current;
            n >>= 1;
        }
        return true;
    }
}
```