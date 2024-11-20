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

Would you like me to proceed with the next one or continue working on all in sequence? 