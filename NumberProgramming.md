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
--- 

### Q8: WAJP to shift all 0’s to the left side and all 1’s to the right side in a binary integer.  
- **Example:**  
  - **Input:**  
    1. `n = 10110010`  
  - **Output:**  
    1. `00001111`  
  - **Explanation:** In the binary number, all zeros are shifted to the left and all ones to the right.  
- **Code:**  
```java
import java.util.Scanner;

public class ShiftZerosOnes {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a binary number: ");
        String binary = sc.next();

        int countZeros = 0;
        for (char ch : binary.toCharArray()) {
            if (ch == '0') countZeros++;
        }

        StringBuilder result = new StringBuilder();
        for (int i = 0; i < countZeros; i++) result.append('0');
        for (int i = 0; i < binary.length() - countZeros; i++) result.append('1');

        System.out.println("Result: " + result);
    }
}
```

---

### Q9: WAJP to shift all even digits to the left side and all odd digits to the right side in a number.  
- **Example:**  
  - **Input:**  
    1. `n = 253687`  
  - **Output:**  
    1. `268537`  
  - **Explanation:** Even digits `2, 6, 8` are moved to the left, and odd digits `5, 3, 7` are on the right, maintaining order.  
- **Code:**  
```java
import java.util.Scanner;

public class ShiftEvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        String num = sc.next();

        StringBuilder even = new StringBuilder();
        StringBuilder odd = new StringBuilder();

        for (char ch : num.toCharArray()) {
            if ((ch - '0') % 2 == 0) even.append(ch);
            else odd.append(ch);
        }

        System.out.println("Result: " + even.toString() + odd.toString());
    }
}
```

---

### Q10: WAJP to shift all 0's to the left and all other digits to the right while maintaining the order of the number.  
- **Example:**  
  - **Input:**  
    1. `n = 2030680`  
  - **Output:**  
    1. `0002368`  
  - **Explanation:** Zeros are moved to the left, maintaining the order of non-zero digits.  
- **Code:**  
```java
import java.util.Scanner;

public class ShiftZerosMaintainOrder {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        String num = sc.next();

        StringBuilder zeros = new StringBuilder();
        StringBuilder others = new StringBuilder();

        for (char ch : num.toCharArray()) {
            if (ch == '0') zeros.append(ch);
            else others.append(ch);
        }

        System.out.println("Result: " + zeros.toString() + others.toString());
    }
}
```

---

### Q11: WAJP to swap two numbers `a` and `b` using a third variable.  
- **Example:**  
  - **Input:**  
    1. `a = 5, b = 10`  
  - **Output:**  
    1. `a = 10, b = 5`  
  - **Explanation:** A third variable temporarily stores one value to facilitate swapping.  
- **Code:**  
```java
public class SwapWithThirdVar {
    public static void main(String[] args) {
        int a = 5, b = 10;

        System.out.println("Before swap: a = " + a + ", b = " + b);
        int temp = a;
        a = b;
        b = temp;

        System.out.println("After swap: a = " + a + ", b = " + b);
    }
}
```

---

### Q12: WAJP to swap two numbers `a` and `b` without using a third variable.  
- **Example:**  
  - **Input:**  
    1. `a = 5, b = 10`  
  - **Output:**  
    1. `a = 10, b = 5`  
  - **Explanation:** Using arithmetic operations for swapping.  
- **Code:**  
```java
public class SwapWithoutThirdVar {
    public static void main(String[] args) {
        int a = 5, b = 10;

        System.out.println("Before swap: a = " + a + ", b = " + b);
        a = a + b;
        b = a - b;
        a = a - b;

        System.out.println("After swap: a = " + a + ", b = " + b);
    }
}
```

---

### Q13: WAJP to take user input and print whether the number is a prime number or not.  
- **Example:**  
  - **Input:**  
    1. `n = 7`  
  - **Output:**  
    1. `7 is a prime number`  
  - **Explanation:** `7` is divisible only by `1` and itself.  
- **Code:**  
```java
import java.util.Scanner;

public class PrimeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        boolean isPrime = n > 1;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime) System.out.println(n + " is a prime number.");
        else System.out.println(n + " is not a prime number.");
    }
}
```

---

### Q14: WAJP to print and count all the prime numbers up to a given range.  
- **Example:**  
  - **Input:**  
    1. `n = 10`  
  - **Output:**  
    1. `2, 3, 5, 7`  
    2. `Count: 4`  
  - **Explanation:** Prime numbers from `1` to `10` are `2, 3, 5, 7`.  
- **Code:**  
```java
import java.util.Scanner;

public class PrimeNumbersRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the range: ");
        int n = sc.nextInt();

        int count = 0;
        for (int i = 2; i <= n; i++) {
            if (isPrime(i)) {
                System.out.print(i + " ");
                count++;
            }
        }

        System.out.println("\nCount: " + count);
    }

    public static boolean isPrime(int n) {
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }
}
```

---

### Q15: WAJP to print and count all prime numbers in a range where the sum of digits is also a prime number.  
- **Example:**  
  - **Input:**  
    1. `n = 20`  
  - **Output:**  
    1. `2, 3, 5, 7, 11`  
    2. `Count: 5`  
  - **Explanation:** Prime numbers whose sum of digits (`11 -> 1+1=2`) is also prime.  
- **Code:**  
```java
import java.util.Scanner;

public class PrimeWithPrimeDigitSum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the range: ");
        int n = sc.nextInt();

        int count = 0;
        for (int i = 2; i <= n; i++) {
            if (isPrime(i) && isPrime(sumOfDigits(i))) {
                System.out.print(i + " ");
                count++;
            }
        }

        System.out.println("\nCount: " + count);
    }

    public static boolean isPrime(int n) {
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static int sumOfDigits(int n) {
        int sum = 0;
        while (n > 0) {
            sum += n % 10;
            n /= 10;
        }
        return sum;
    }
}
```

---

### Q16: WAJP to take user input and check whether the number is a palindrome.  
- **Example:**  
  - **Input:**  
    1. `n = 121`  
  - **Output:**  
    1. `121 is a palindrome`  
  - **Explanation:** The number `121` reads the same forward and backward.  
- **Code:**  
```java
import java.util.Scanner;

public class PalindromeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        int original = n, reverse = 0;
        while (n > 0) {
            reverse = reverse * 10 + n % 10;
            n /= 10;
        }

        if (original == reverse) System.out.println(original + " is a palindrome.");
        else System.out.println(original + " is not a palindrome.");
    }
}
```

---

### Q17: [Palindrome Number - LeetCode](https://leetcode.com/problems/palindrome-number/)  
- **Link:** [Palindrome Number - LeetCode](https://leetcode.com/problems/palindrome-number/)  
- **Example:**  
  - **Input:**  
    1. `n = 121`  
  - **Output:**  
    1. `true`  
  - **Explanation:** The number `121` reads the same forward and backward.  
- **Code:**  
```java
public class PalindromeNumber {
    public boolean isPalindrome(int x) {
        if (x < 0) return false;
        int original = x, reverse = 0;
        while (x > 0) {
            reverse = reverse * 10 + x % 10;
            x /= 10;
        }
        return original == reverse;
    }
}
```

---

### Q18: WAJP to print all palindrome numbers in a range which are also prime numbers.  
- **Example:**  
  - **Input:**  
    1. `Range: 1 to 100`  
  - **Output:**  
    1. `2, 3, 5, 7, 11, 101`  
  - **Explanation:** Palindrome numbers from `1 to 100` which are also prime.  
- **Code:**  
```java
public class PrimePalindrome {
    public static void main(String[] args) {
        int range = 100;

        for (int i = 2; i <= range; i++) {
            if (isPalindrome(i) && isPrime(i)) {
                System.out.print(i + " ");
            }
        }
    }

    public static boolean isPalindrome(int n) {
        int original = n, reverse = 0;
        while (n > 0) {
            reverse = reverse * 10 + n % 10;
            n /= 10;
        }
        return original == reverse;
    }

    public static boolean isPrime(int n) {
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }
}
```

---

### Q19: [Prime Palindrome - LeetCode](https://leetcode.com/problems/prime-palindrome/)  
- **Link:** [Prime Palindrome - LeetCode](https://leetcode.com/problems/prime-palindrome/)  
- **Example:**  
  - **Input:**  
    1. `n = 6`  
  - **Output:**  
    1. `7`  
  - **Explanation:** The smallest palindrome prime greater than `6` is `7`.  
- **Code:**  
```java
public class PrimePalindromeLeetCode {
    public int primePalindrome(int n) {
        while (true) {
            if (n == reverse(n) && isPrime(n)) return n;
            n++;
        }
    }

    public boolean isPrime(int n) {
        if (n < 2) return false;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public int reverse(int n) {
        int rev = 0;
        while (n > 0) {
            rev = rev * 10 + n % 10;
            n /= 10;
        }
        return rev;
    }
}
```

---

### Q20: WAJP to take user input and check if the number is a perfect number.  
- **Example:**  
  - **Input:**  
    1. `n = 28`  
  - **Output:**  
    1. `28 is a perfect number`  
  - **Explanation:** The divisors of `28` (`1, 2, 4, 7, 14`) sum to `28`.  
- **Code:**  
```java
public class PerfectNumber {
    public static void main(String[] args) {
        int n = 28;
        int sum = 0;

        for (int i = 1; i < n; i++) {
            if (n % i == 0) sum += i;
        }

        if (sum == n) System.out.println(n + " is a perfect number.");
        else System.out.println(n + " is not a perfect number.");
    }
}
```

---

### Q21: WAJP to print and count all perfect numbers up to 100.  
- **Example:**  
  - **Input:**  
    1. `Range: 1 to 100`  
  - **Output:**  
    1. `6, 28`  
    2. `Count: 2`  
  - **Explanation:** Perfect numbers from `1 to 100` are `6` and `28`.  
- **Code:**  
```java
public class PerfectNumbersRange {
    public static void main(String[] args) {
        int range = 100, count = 0;

        for (int n = 1; n <= range; n++) {
            int sum = 0;
            for (int i = 1; i < n; i++) {
                if (n % i == 0) sum += i;
            }
            if (sum == n) {
                System.out.print(n + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }
}
```

---

### Q22: [507. Perfect Number - LeetCode](https://leetcode.com/problems/perfect-number/)  
- **Link:** [507. Perfect Number - LeetCode](https://leetcode.com/problems/perfect-number/)  
- **Example:**  
  - **Input:**  
    1. `n = 28`  
  - **Output:**  
    1. `true`  
  - **Explanation:** The divisors of `28` sum to `28`.  
- **Code:**  
```java
public class PerfectNumberLeetCode {
    public boolean checkPerfectNumber(int num) {
        if (num <= 1) return false;
        int sum = 1;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                sum += i + num / i;
            }
        }
        return sum == num;
    }
}
```

---

### Q23: WAJP to check if a number is a Disarium number.  
- **Example:**  
  - **Input:**  
    1. `n = 89`  
  - **Output:**  
    1. `89 is a Disarium number`  
  - **Explanation:** `8^1 + 9^2 = 89`.  
- **Code:**  
```java
public class DisariumNumber {
    public static void main(String[] args) {
        int n = 89;
        int sum = 0, num = n, len = String.valueOf(n).length();

        while (num > 0) {
            sum += Math.pow(num % 10, len--);
            num /= 10;
        }

        if (sum == n) System.out.println(n + " is a Disarium number.");
        else System.out.println(n + " is not a Disarium number.");
    }
}
```

---

### Q24: WAJP to print and count all Disarium numbers up to 1000.  
- **Example:**  
  - **Input:**  
    1. `Range: 1 to 1000`  
  - **Output:**  
    1. `1, 2, 3, 4, 5, 6, 7, 8, 9, 89, 135, 175, 518, 598`  
    2. `Count: 14`  
  - **Explanation:** Disarium numbers up to `1000`.  
- **Code:**  
```java
public class DisariumNumbersRange {
    public static void main(String[] args) {
        int range = 1000, count = 0;

        for (int n = 1; n <= range; n++) {
            int sum = 0, num = n, len = String.valueOf(n).length();
            while (num > 0) {
                sum += Math.pow(num % 10, len--);
                num /= 10;
            }
            if (sum == n) {
                System.out.print(n + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }
}
```

---


### Q25: [202. Happy Number - LeetCode](https://leetcode.com/problems/happy-number/)  
- **Link:** [202. Happy Number - LeetCode](https://leetcode.com/problems/happy-number/)  
- **Example:**  
  - **Input:**  
    1. `n = 19`  
  - **Output:**  
    1. `true`  
  - **Explanation:** `19 -> 1^2 + 9^2 = 82 -> ... -> 1`.  
- **Code:**  
```java
public class HappyNumber {
    public boolean isHappy(int n) {
        int slow = n, fast = n;
        do {
            slow = sumOfSquares(slow);
            fast = sumOfSquares(sumOfSquares(fast));
        } while (slow != fast);

        return slow == 1;
    }

    public int sumOfSquares(int n) {
        int sum = 0;
        while (n > 0) {
            int digit = n % 10;
            sum += digit * digit;
            n /= 10;
        }
        return sum;
    }
}
```

---

### Q26: WAJP to print and count all the Happy numbers up to 100.  
- **Example:**  
  - **Input:**  
    1. `Range: 1 to 100`  
  - **Output:**  
    1. `1, 7, 10, 13, 19, 23, 28, 31, 32, 44, 49, 68, 70, 79, 82, 86, 91, 94, 97, 100`  
    2. `Count: 20`  
  - **Explanation:** Happy numbers up to `100`.  
- **Code:**  
```java
import java.util.HashSet;

public class HappyNumbersRange {
    public static void main(String[] args) {
        int range = 100, count = 0;

        for (int i = 1; i <= range; i++) {
            if (isHappy(i)) {
                System.out.print(i + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }

    public static boolean isHappy(int n) {
        HashSet<Integer> seen = new HashSet<>();
        while (n != 1 && !seen.contains(n)) {
            seen.add(n);
            n = sumOfSquares(n);
        }
        return n == 1;
    }

    public static int sumOfSquares(int n) {
        int sum = 0;
        while (n > 0) {
            int digit = n % 10;
            sum += digit * digit;
            n /= 10;
        }
        return sum;
    }
}
```

---

### Q27: WAJP to take user input and print whether the number is an Automorphic number.  
- **Example:**  
  - **Input:**  
    1. `n = 76`  
  - **Output:**  
    1. `76 is an Automorphic number.`  
  - **Explanation:** The square of `76` is `5776`, which ends with `76`.  
- **Code:**  
```java
public class AutomorphicNumber {
    public static void main(String[] args) {
        int n = 76;
        int square = n * n;

        if (String.valueOf(square).endsWith(String.valueOf(n))) {
            System.out.println(n + " is an Automorphic number.");
        } else {
            System.out.println(n + " is not an Automorphic number.");
        }
    }
}
```

---

### Q28: WAJP to print and count all the Automorphic numbers up to 100.  
- **Example:**  
  - **Input:**  
    1. `Range: 1 to 100`  
  - **Output:**  
    1. `1, 5, 6, 25, 76`  
    2. `Count: 5`  
  - **Explanation:** Automorphic numbers up to `100`.  
- **Code:**  
```java
public class AutomorphicNumbersRange {
    public static void main(String[] args) {
        int range = 100, count = 0;

        for (int i = 1; i <= range; i++) {
            int square = i * i;
            if (String.valueOf(square).endsWith(String.valueOf(i))) {
                System.out.print(i + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }
}
```

---

### Q29: [Check if The Number is Fascinating - LeetCode](https://leetcode.com/problems/check-if-the-number-is-fascinating/)  
- **Link:** [Check if The Number is Fascinating - LeetCode](https://leetcode.com/problems/check-if-the-number-is-fascinating/)  
- **Example:**  
  - **Input:**  
    1. `n = 192`  
  - **Output:**  
    1. `true`  
  - **Explanation:** Concatenating `192`, `192*2`, and `192*3` gives `192384576`, which contains all digits from `1` to `9` exactly once.  
- **Code:**  
```java
public class FascinatingNumberLeetCode {
    public boolean isFascinating(int n) {
        String concat = n + "" + (n * 2) + "" + (n * 3);
        if (concat.length() != 9) return false;

        int[] digits = new int[10];
        for (char c : concat.toCharArray()) {
            int digit = c - '0';
            if (digit == 0 || digits[digit] > 0) return false;
            digits[digit]++;
        }
        return true;
    }
}
```

---

### Q30: WAJP to print and count all the Fascinating numbers up to 10000.  
- **Example:**  
  - **Input:**  
    1. `Range: 1 to 10000`  
  - **Output:**  
    1. `192, 219`  
    2. `Count: 2`  
  - **Explanation:** Fascinating numbers in the range `1 to 10000`.  
- **Code:**  
```java
public class FascinatingNumbersRange {
    public static void main(String[] args) {
        int range = 10000, count = 0;

        for (int n = 1; n <= range; n++) {
            if (isFascinating(n)) {
                System.out.print(n + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }

    public static boolean isFascinating(int n) {
        String concat = n + "" + (n * 2) + "" + (n * 3);
        if (concat.length() != 9) return false;

        int[] digits = new int[10];
        for (char c : concat.toCharArray()) {
            int digit = c - '0';
            if (digit == 0 || digits[digit] > 0) return false;
            digits[digit]++;
        }
        return true;
    }
}
```

---

### Q31: WAJP to take user input and print whether the number is a Strong number or not.  
- **Example:**  
  - **Input:**  
    145  
  - **Output:**  
    Strong Number  
  - **Explanation:**  
    A Strong number is a number whose sum of the factorials of its digits equals the number itself. For example, \(145 = 1! + 4! + 5! = 145\).  

- **Code:**  
```java
import java.util.Scanner;

public class StrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number:");
        int num = sc.nextInt();
        if (isStrongNumber(num)) {
            System.out.println(num + " is a Strong Number");
        } else {
            System.out.println(num + " is not a Strong Number");
        }
    }

    public static boolean isStrongNumber(int num) {
        int sum = 0, temp = num;
        while (temp > 0) {
            sum += factorial(temp % 10);
            temp /= 10;
        }
        return sum == num;
    }

    public static int factorial(int n) {
        int fact = 1;
        for (int i = 2; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }
}
```

---

### Q32: WAJP to print and count all the Strong numbers up to 100.  
- **Example:**  
  - **Input:**  
    Range: 1 to 100  
  - **Output:**  
    Strong Numbers: 1, 2, 145  
    Count: 3  
  - **Explanation:**  
    All numbers within the range are checked for the Strong number property.  

- **Code:**  
```java
public class StrongNumbersUpTo100 {
    public static void main(String[] args) {
        int count = 0;
        System.out.println("Strong Numbers up to 100 are:");
        for (int i = 1; i <= 100; i++) {
            if (isStrongNumber(i)) {
                System.out.print(i + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }

    public static boolean isStrongNumber(int num) {
        int sum = 0, temp = num;
        while (temp > 0) {
            sum += factorial(temp % 10);
            temp /= 10;
        }
        return sum == num;
    }

    public static int factorial(int n) {
        int fact = 1;
        for (int i = 2; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }
}
```

---

### Q33: WAJP to take user input and print whether the number is an Armstrong number or not.  
- **Example:**  
  - **Input:**  
    153  
  - **Output:**  
    Armstrong Number  
  - **Explanation:**  
    An Armstrong number is a number where the sum of the digits raised to the power of their count equals the number itself. For example, \(153 = 1^3 + 5^3 + 3^3 = 153\).  

- **Code:**  
```java
import java.util.Scanner;

public class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number:");
        int num = sc.nextInt();
        if (isArmstrong(num)) {
            System.out.println(num + " is an Armstrong Number");
        } else {
            System.out.println(num + " is not an Armstrong Number");
        }
    }

    public static boolean isArmstrong(int num) {
        int sum = 0, temp = num, digits = String.valueOf(num).length();
        while (temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }
        return sum == num;
    }
}
```

---

### Q34: WAJP to print and count all the Armstrong numbers up to 100.  
- **Example:**  
  - **Input:**  
    Range: 1 to 100  
  - **Output:**  
    Armstrong Numbers: 1, 2, ..., 153  
    Count: 5  
  - **Explanation:**  
    Iterate through the range and check for the Armstrong number property.  

- **Code:**  
```java
public class ArmstrongNumbersUpTo100 {
    public static void main(String[] args) {
        int count = 0;
        System.out.println("Armstrong Numbers up to 100 are:");
        for (int i = 1; i <= 100; i++) {
            if (isArmstrong(i)) {
                System.out.print(i + " ");
                count++;
            }
        }
        System.out.println("\nCount: " + count);
    }

    public static boolean isArmstrong(int num) {
        int sum = 0, temp = num, digits = String.valueOf(num).length();
        while (temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }
        return sum == num;
    }
}
```

---

### Q35: Count the Digits That Divide a Number - LeetCode  
- **Link:** [Count the Digits That Divide a Number - LeetCode](https://leetcode.com/problems/count-the-digits-that-divide-a-number/)  
- **Example:**  
  - **Input:**  
    `num = 121`  
  - **Output:**  
    `2`  
  - **Explanation:**  
    The digits of `121` are `1`, `2`, and `1`. Digits `1` and `1` divide `121` evenly.  

- **Code:**  
```java
public class CountDigits {
    public static void main(String[] args) {
        int num = 121;
        System.out.println("Count of digits that divide " + num + ": " + countDigits(num));
    }

    public static int countDigits(int num) {
        int count = 0, temp = num;
        while (temp > 0) {
            int digit = temp % 10;
            if (digit != 0 && num % digit == 0) {
                count++;
            }
            temp /= 10;
        }
        return count;
    }
}
```

---

### Q36: Number of Steps to Reduce a Number to Zero - LeetCode  
- **Link:** [Number of Steps to Reduce a Number to Zero - LeetCode](https://leetcode.com/problems/number-of-steps-to-reduce-a-number-to-zero/)  
- **Example:**  
  - **Input:**  
    `num = 14`  
  - **Output:**  
    `6`  
  - **Explanation:**  
    Steps:  
    1. Subtract 1 (odd), 13  
    2. Divide by 2 (even), 6  
    3. Divide by 2 (even), 3  
    4. Subtract 1 (odd), 2  
    5. Divide by 2 (even), 1  
    6. Subtract 1 (odd), 0  

- **Code:**  
```java
public class StepsToReduceNumber {
    public static void main(String[] args) {
        int num = 14;
        System.out.println("Number of steps to reduce " + num + " to zero: " + numberOfSteps(num));
    }

    public static int numberOfSteps(int num) {
        int steps = 0;
        while (num > 0) {
            if (num % 2 == 0) {
                num /= 2;
            } else {
                num -= 1;
            }
            steps++;
        }
        return steps;
    }
}
```

---

### Q37: [Valid Perfect Square - LeetCode](https://leetcode.com/problems/valid-perfect-square/)  
- **Link:** [Valid Perfect Square - LeetCode](https://leetcode.com/problems/valid-perfect-square/)  
- **Example:**  
  - **Input:**  
    `num = 16`  
  - **Output:**  
    `true`  
  - **Explanation:**  
    \(16 = 4^2\), so it's a perfect square.  

- **Code:**  
```java
public class ValidPerfectSquare {
    public static void main(String[] args) {
        int num = 16;
        System.out.println(num + " is a perfect square: " + isPerfectSquare(num));
    }

    public static boolean isPerfectSquare(int num) {
        if (num < 1) return false;
        long left = 1, right = num;
        while (left <= right) {
            long mid = left + (right - left) / 2;
            long square = mid * mid;
            if (square == num) return true;
            else if (square < num) left = mid + 1;
            else right = mid - 1;
        }
        return false;
    }
}
```

---

### Q38: WAJP to take two user inputs and print GCD/HCF of the two numbers.  
- **Example:**  
  - **Input:**  
    `num1 = 12, num2 = 18`  
  - **Output:**  
    `GCD = 6`  
  - **Explanation:**  
    The greatest common divisor (GCD) of `12` and `18` is `6`.  

- **Code:**  
```java
import java.util.Scanner;

public class GCDOfTwoNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter two numbers:");
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        System.out.println("GCD of " + num1 + " and " + num2 + ": " + gcd(num1, num2));
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

### Q39: WAJP to take three user inputs and print LCM of the three numbers.  
- **Example:**  
  - **Input:**  
    `num1 = 2, num2 = 3, num3 = 5`  
  - **Output:**  
    `LCM = 30`  
  - **Explanation:**  
    The least common multiple (LCM) of `2`, `3`, and `5` is `30`.  

- **Code:**  
```java
import java.util.Scanner;

public class LCMOfThreeNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter three numbers:");
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        int num3 = sc.nextInt();
        System.out.println("LCM of " + num1 + ", " + num2 + ", " + num3 + ": " + lcm(num1, lcm(num2, num3)));
    }

    public static int gcd(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }

    public static int lcm(int a, int b) {
        return (a * b) / gcd(a, b);
    }
}
```

---

### Q40: WAJP to convert a decimal number into binary number.  
- **Example:**  
  - **Input:**  
    `num = 28`  
  - **Output:**  
    `Binary = 11100`  
  - **Explanation:**  
    Converting decimal `28` to binary results in `11100`.  

- **Code:**  
```java
import java.util.Scanner;

public class DecimalToBinary {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a decimal number:");
        int num = sc.nextInt();
        System.out.println("Binary representation of " + num + ": " + decimalToBinary(num));
    }

    public static String decimalToBinary(int num) {
        return Integer.toBinaryString(num);
    }
}
```

---

### Q41: WAJP to convert a binary number into a decimal number  
- **Example:**  
  - **Input:**  
    `101101`  
  - **Output:**  
    `45`  
  - **Explanation:**  
    Binary `101101` equals \(1×2^5 + 0×2^4 + 1×2^3 + 1×2^2 + 0×2^1 + 1×2^0 = 45\).  

- **Code:**  
```java
import java.util.Scanner;

public class BinaryToDecimal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a binary number:");
        String binary = sc.nextLine();
        int decimal = Integer.parseInt(binary, 2);
        System.out.println("Decimal representation: " + decimal);
    }
}
```

---

### Q42: WAJP to convert a decimal number into an octal number  
- **Example:**  
  - **Input:**  
    `235`  
  - **Output:**  
    `353`  
  - **Explanation:**  
    Decimal `235` converts to octal as `353`.  

- **Code:**  
```java
import java.util.Scanner;

public class DecimalToOctal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a decimal number:");
        int decimal = sc.nextInt();
        String octal = Integer.toOctalString(decimal);
        System.out.println("Octal representation: " + octal);
    }
}
```

---

### Q43: WAJP to convert an octal number into a decimal number  
- **Example:**  
  - **Input:**  
    `353`  
  - **Output:**  
    `235`  
  - **Explanation:**  
    Octal `353` equals \(3×8^2 + 5×8^1 + 3×8^0 = 235\).  

- **Code:**  
```java
import java.util.Scanner;

public class OctalToDecimal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter an octal number:");
        String octal = sc.nextLine();
        int decimal = Integer.parseInt(octal, 8);
        System.out.println("Decimal representation: " + decimal);
    }
}
```

---

### Q44: WAJP to convert a decimal number into a hexadecimal number  
- **Example:**  
  - **Input:**  
    `255`  
  - **Output:**  
    `FF`  
  - **Explanation:**  
    Decimal `255` converts to hexadecimal as `FF`.  

- **Code:**  
```java
import java.util.Scanner;

public class DecimalToHexadecimal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a decimal number:");
        int decimal = sc.nextInt();
        String hex = Integer.toHexString(decimal).toUpperCase();
        System.out.println("Hexadecimal representation: " + hex);
    }
}
```

---

### Q45: WAJP to convert a hexadecimal number into a decimal number  
- **Example:**  
  - **Input:**  
    `FF`  
  - **Output:**  
    `255`  
  - **Explanation:**  
    Hexadecimal `FF` equals \(15×16^1 + 15×16^0 = 255\).  

- **Code:**  
```java
import java.util.Scanner;

public class HexadecimalToDecimal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a hexadecimal number:");
        String hex = sc.nextLine();
        int decimal = Integer.parseInt(hex, 16);
        System.out.println("Decimal representation: " + decimal);
    }
}
```

---

### Q46: WAJP to generate random numbers in Java  
- **Example:**  
  - **Output:**  
    `Random number: 67`  

- **Code:**  
```java
import java.util.Random;

public class RandomNumberGenerator {
    public static void main(String[] args) {
        Random random = new Random();
        int randomNumber = random.nextInt(100); // Generate a number between 0 and 99
        System.out.println("Random number: " + randomNumber);
    }
}
```

---

### Q47: WAJP to calculate permutations  
- **Example:**  
  - **Input:**  
    `Total seats = 12, Boys = 8`  
  - **Output:**  
    `Permutation = 19958400`  

- **Code:**  
```java
public class Permutations {
    public static void main(String[] args) {
        int totalSeats = 12;
        int boys = 8;
        System.out.println("Permutation: " + permutation(totalSeats, boys));
    }

    public static int permutation(int n, int r) {
        return factorial(n) / factorial(n - r);
    }

    public static int factorial(int num) {
        if (num <= 1) return 1;
        return num * factorial(num - 1);
    }
}
```

---

### Q48: WAJP to calculate combinations  
- **Example:**  
  - **Input:**  
    `Total players = 15, Team size = 11`  
  - **Output:**  
    `Combination = 1365`  

- **Code:**  
```java
public class Combinations {
    public static void main(String[] args) {
        int totalPlayers = 15;
        int teamSize = 11;
        System.out.println("Combination: " + combination(totalPlayers, teamSize));
    }

    public static int combination(int n, int r) {
        return factorial(n) / (factorial(r) * factorial(n - r));
    }

    public static int factorial(int num) {
        if (num <= 1) return 1;
        return num * factorial(num - 1);
    }
}
```

---

### Q49: WAJP to print the nth row of Pascal's Triangle  
- **Example:**  
  - **Input:**  
    `n = 4`  
  - **Output:**  
    `1 4 6 4 1`  

- **Code:**  
```java
public class PascalTriangle {
    public static void main(String[] args) {
        int n = 4;
        for (int i = 0; i <= n; i++) {
            System.out.print(combination(n, i) + " ");
        }
    }

    public static int combination(int n, int r) {
        return factorial(n) / (factorial(r) * factorial(n - r));
    }

    public static int factorial(int num) {
        if (num <= 1) return 1;
        return num * factorial(num - 1);
    }
}
```

---

### Q50: WAJP to replace all `0`s by `1` in a number  
- **Example:**  
  - **Input:**  
    `41022005`  
  - **Output:**  
    `41122115`  

- **Code:**  
```java
import java.util.Scanner;

public class ReplaceZerosWithOnes {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number:");
        String number = sc.nextLine();
        String result = number.replace('0', '1');
        System.out.println("Result: " + result);
    }
}
```

---

### Q51: WAJP to replace all `7`s by `0` in a number  
- **Example:**  
  - **Input:**  
    `41072707`  
  - **Output:**  
    `41002000`  
  - **Explanation:**  
    Replace all occurrences of the digit `7` with `0`.  

- **Code:**  
```java
import java.util.Scanner;

public class ReplaceSevensWithZeros {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a number:");
        String number = sc.nextLine();
        String result = number.replace('7', '0');
        System.out.println("Result: " + result);
    }
}
```

---

### Q52: WAJP to use `BigInteger` and `BigDecimal` classes to perform arithmetic operations  
- **Example:**  
  - **Input:**  
    `BigInteger: 123456789123456789`, `BigDecimal: 12345.6789`  
  - **Output:**  
    - Addition: `BigInteger + BigInteger: 246913578246913578`  
    - Multiplication: `BigDecimal × BigDecimal: 152415787.50190521`  

- **Code:**  
```java
import java.math.BigInteger;
import java.math.BigDecimal;

public class BigIntegerBigDecimalOps {
    public static void main(String[] args) {
        BigInteger bigInt1 = new BigInteger("123456789123456789");
        BigInteger bigInt2 = new BigInteger("123456789123456789");
        BigDecimal bigDec1 = new BigDecimal("12345.6789");
        BigDecimal bigDec2 = new BigDecimal("12345.6789");

        System.out.println("Addition of BigInteger: " + bigInt1.add(bigInt2));
        System.out.println("Multiplication of BigDecimal: " + bigDec1.multiply(bigDec2));
    }
}
```

---

### Q53: WAJP to calculate factorial using `BigInteger`  
- **Example:**  
  - **Input:**  
    `5`  
  - **Output:**  
    `120`  

- **Code:**  
```java
import java.math.BigInteger;

public class FactorialBigInteger {
    public static void main(String[] args) {
        int num = 20; // Example input
        System.out.println("Factorial: " + factorial(num));
    }

    public static BigInteger factorial(int n) {
        BigInteger result = BigInteger.ONE;
        for (int i = 1; i <= n; i++) {
            result = result.multiply(BigInteger.valueOf(i));
        }
        return result;
    }
}
```

---

### Q54: [Ugly Number - LeetCode](https://leetcode.com/problems/ugly-number/)  
- **Example:**  
  - **Input:**  
    `6`  
  - **Output:**  
    `true`  
  - **Explanation:**  
    \(6 = 2×3\), and it only has prime factors `2`, `3`, or `5`.  

- **Code:**  
```java
class UglyNumber {
    public boolean isUgly(int n) {
        if (n <= 0) return false;
        int[] factors = {2, 3, 5};
        for (int factor : factors) {
            while (n % factor == 0) {
                n /= factor;
            }
        }
        return n == 1;
    }
}
```

---

### Q55: [Ugly Number II - LeetCode](https://leetcode.com/problems/ugly-number-ii/)  
- **Example:**  
  - **Input:**  
    `10`  
  - **Output:**  
    `12`  
  - **Explanation:**  
    The 10th ugly number is `12`.  

- **Code:**  
```java
import java.util.PriorityQueue;

class UglyNumberII {
    public int nthUglyNumber(int n) {
        int[] primes = {2, 3, 5};
        PriorityQueue<Long> pq = new PriorityQueue<>();
        pq.add(1L);
        long ugly = 1;
        for (int i = 0; i < n; i++) {
            ugly = pq.poll();
            for (int prime : primes) {
                pq.add(ugly * prime);
            }
            while (!pq.isEmpty() && pq.peek() == ugly) {
                pq.poll();
            }
        }
        return (int) ugly;
    }
}
```

---

### Q56: [Ugly Number III - LeetCode](https://leetcode.com/problems/ugly-number-iii/)  
- **Example:**  
  - **Input:**  
    `n = 4, a = 2, b = 3, c = 4`  
  - **Output:**  
    `6`  
  - **Explanation:**  
    The 4th ugly number that is divisible by \(2\), \(3\), or \(4\) is `6`.  

- **Code:**  
```java
class UglyNumberIII {
    public int nthUglyNumber(int n, int a, int b, int c) {
        long low = 1, high = (long) 2e9, result = -1;
        while (low <= high) {
            long mid = low + (high - low) / 2;
            if (count(mid, a, b, c) >= n) {
                result = mid;
                high = mid - 1;
            } else {
                low = mid + 1;
            }
        }
        return (int) result;
    }

    private long count(long num, long a, long b, long c) {
        return num / a + num / b + num / c 
             - num / lcm(a, b) - num / lcm(b, c) - num / lcm(a, c) 
             + num / lcm(a, lcm(b, c));
    }

    private long gcd(long x, long y) {
        return y == 0 ? x : gcd(y, x % y);
    }

    private long lcm(long x, long y) {
        return x * (y / gcd(x, y));
    }
}
```

---

### Q57: [Three Divisors - LeetCode](https://leetcode.com/problems/three-divisors/)  
- **Example:**  
  - **Input:**  
    `9`  
  - **Output:**  
    `true`  
  - **Explanation:**  
    The number \(9\) has exactly three divisors: \(1, 3, 9\).  

- **Code:**  
```java
class ThreeDivisors {
    public boolean isThree(int n) {
        int count = 0;
        for (int i = 1; i * i <= n; i++) {
            if (n % i == 0) {
                count++;
                if (i != n / i) count++;
            }
        }
        return count == 3;
    }
}
```

---

Here are the solutions for the remaining questions:

---

### Q58: [Smallest Even Multiple - LeetCode](https://leetcode.com/problems/smallest-even-multiple/)  
- **Example:**  
  - **Input:**  
    `3`  
  - **Output:**  
    `6`  
  - **Explanation:**  
    The smallest multiple of `3` that is even is `6`.  

- **Code:**  
```java
class SmallestEvenMultiple {
    public int smallestEvenMultiple(int n) {
        return n % 2 == 0 ? n : n * 2;
    }
}
```

---

### Q59: [Number of Common Factors - LeetCode](https://leetcode.com/problems/number-of-common-factors/)  
- **Example:**  
  - **Input:**  
    `12`, `6`  
  - **Output:**  
    `4`  
  - **Explanation:**  
    The common factors of `12` and `6` are `1, 2, 3, 6`.  

- **Code:**  
```java
class NumberOfCommonFactors {
    public int commonFactors(int a, int b) {
        int count = 0;
        for (int i = 1; i <= Math.min(a, b); i++) {
            if (a % i == 0 && b % i == 0) {
                count++;
            }
        }
        return count;
    }
}
```

---

### Q60: [Sqrt(x) - LeetCode](https://leetcode.com/problems/sqrtx/)  
- **Example:**  
  - **Input:**  
    `8`  
  - **Output:**  
    `2`  
  - **Explanation:**  
    The square root of `8` is `2.828...`, but the floor of this value is `2`.  

- **Code:**  
```java
class SqrtX {
    public int mySqrt(int x) {
        int left = 0, right = x;
        while (left <= right) {
            int mid = left + (right - left) / 2;
            if (mid * mid == x) {
                return mid;
            } else if (mid * mid < x) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }
        return right;
    }
}
```

---

### Q61: [Factorial Trailing Zeroes](https://leetcode.com/problems/factorial-trailing-zeroes/)  
- **Example:**  
  - **Input:**  
    `5`  
  - **Output:**  
    `1`  
  - **Explanation:**  
    The factorial of `5` is `120`, which has one trailing zero.  

- **Code:**  
```java
class FactorialTrailingZeroes {
    public int trailingZeroes(int n) {
        int count = 0;
        while (n >= 5) {
            n /= 5;
            count += n;
        }
        return count;
    }
}
```

---

### Q62: [Number of Digit One - LeetCode](https://leetcode.com/problems/number-of-digit-one/)  
- **Example:**  
  - **Input:**  
    `13`  
  - **Output:**  
    `6`  
  - **Explanation:**  
    The numbers from `1` to `13` that contain the digit `1` are: `1, 10, 11, 12, 13`. There are 6 occurrences of the digit `1`.  

- **Code:**  
```java
class NumberOfDigitOne {
    public int countDigitOne(int n) {
        int count = 0, factor = 1;
        while (n >= factor) {
            int digit = (n / factor) % 10;
            int higher = n / (factor * 10);
            int lower = n % factor;
            
            if (digit == 0) {
                count += higher * factor;
            } else if (digit == 1) {
                count += higher * factor + lower + 1;
            } else {
                count += (higher + 1) * factor;
            }
            factor *= 10;
        }
        return count;
    }
}
```

---

### Q63: [Add Digits](https://leetcode.com/problems/add-digits/)  
- **Example:**  
  - **Input:**  
    `38`  
  - **Output:**  
    `2`  
  - **Explanation:**  
    The sum of digits of `38` is `3 + 8 = 11`. Then, `1 + 1 = 2`.  

- **Code:**  
```java
class AddDigits {
    public int addDigits(int num) {
        while (num >= 10) {
            int sum = 0;
            while (num > 0) {
                sum += num % 10;
                num /= 10;
            }
            num = sum;
        }
        return num;
    }
}
```

---
