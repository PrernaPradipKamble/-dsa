import java.util.*;

public class SecondLargestUnique {
    public static int findSecondLargest(int[] nums) {
       
        TreeSet<Integer> uniqueNumbers = new TreeSet<>();

        for (int num : nums) {
            uniqueNumbers.add(num);
        }

        
        if (uniqueNumbers.size() < 2) {
            return -1;
        }

        
        uniqueNumbers.pollLast();

        
        return uniqueNumbers.last();
    }

    public static void main(String[] args) {
        int[] arr1 = {3, 5, 2, 5, 6, 6, 1};
        int[] arr2 = {7, 7, 7};

        System.out.println("Input: [3, 5, 2, 5, 6, 6, 1]");
        System.out.println("Output: " + findSecondLargest(arr1)); 

        System.out.println("\nInput: [7, 7, 7]");
        System.out.println("Output: " + findSecondLargest(arr2)); 
    }
}

