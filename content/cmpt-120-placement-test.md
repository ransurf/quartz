---
title: cmpt 120 placement test
---
1. true and false
2. looking for 9
3. both a and d
4. int, float, char, boolean
5. all except 7
6. all of the above
7. none of the above
8. none of the above
9. 11.2
10. any int from -10 to -99
11. 16
```
import java.util.Scanner;
import static java.lang.Integer.parseInt;

public class AgeNextYear {
    public static void main (String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("How old are you now? ");
        int age = parseInt(scanner.nextLine());

        System.out.println("Next year, you will be: " + (age + 1));
    }
}


import java.util.ArrayList;
import java.util.Scanner;
import static java.lang.Integer.parseInt;

public class AscendingOrder {
    public static void main (String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter three numbers: ");
        ArrayList<Integer> nums = new ArrayList<Integer>();
        int numOne = parseInt(scanner.nextLine());
        nums.add(numOne);
        int numTwo = parseInt(scanner.nextLine());
        nums.add(numTwo);
        int numThree = parseInt(scanner.nextLine());
        nums.add(numThree);

        System.out.print("Here they are in order: ");
        while (nums.size() > 1) {
            int min = nums.get(0);
            int loc = 0;
            for (int i = 1; i < nums.size(); i++) {
                if (nums.get(i) < min) {
                    min = nums.get(i);
                    loc = i;
                }
                System.out.print(nums.get(loc) + " ");
                nums.remove(loc);
            }

        }
        System.out.print(nums.get(0));
    }
}


import java.util.ArrayList;
import java.util.Scanner;

import static java.lang.Integer.parseInt;

public class AscendingOrder {
    public static void main (String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("How many numbers do you have? ");
        int totalNums = parseInt(scanner.nextLine());
        ArrayList<Integer> nums = new ArrayList<Integer>();
        System.out.println("Enter your " + totalNums + " numbers now: ");
        for (int i = 0; i < totalNums; i++) {
            int num = parseInt(scanner.nextLine());
            nums.add(num);
        }
        int min = nums.get(0);
        int max = nums.get(0);
        for (int i = 1; i < nums.size(); i++) {
            if (nums.get(i) < min) {
                min = nums.get(i);
            }
            if (nums.get(i) > max) {
                max = nums.get(i);
            }
        }

        System.out.println("The smallest number you entered was " + min);
        System.out.println("The largest number you entered was " + max);
    }
}

I would use a value of 2 or larger for `totalNums` for the sorting to actually be tested, and I would make sure the numbers I input are not equal to each other. I would do it again with a different number as `totalNums`, and if it works, I would consider the program to be working properly with the assumption that the program is given appropriate inputs.

import java.util.Scanner;

public class PalindromeChecker {
    public static void main (String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter a word: ");
        String word = scanner.nextLine().toLowerCase();
        boolean isPalindrome = true;

        for(int i = 0; i < word.length(); i++)
        {
            if(word.charAt(i) != word.charAt(word.length()-1-i)) {
                isPalindrome = false;
                break;
            }
        }

        if(isPalindrome) {
            System.out.println("That is a palindrome.");
        } else {
            System.out.println("That is not a palindrome.");
        }
    }
}


1. 
public double transform(double num) {
    return Math.sqrt(Math.abs(num)) + (Math.pow(num, 3) * 5);
 }

2. 
import java.util.Scanner;
import java.lang.Math;

import static java.lang.Double.parseDouble;

public class AscendingOrder {
    public static void main (String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter 5 values: ");
        double[] nums = new double[5];
        for (int i = 0; i < 5; i++) {
            double num = parseDouble(scanner.nextLine());
            nums[i] = num;
        }

        for (int i = 0; i < 5; i++) {
            nums[i] = transform(nums[i]);
        }

        System.out.print("Results in reverse order: ");
        for (int i = 4; i >= 0; i--) {
            System.out.print(nums[i] + " ");
        }
    }
}