## 1. Write a program to input two numbers(A & B) from user and print the maximum element among A & B in each line.

- Input Format

- First line is a single integer A. Second line is a single integer B.

- Constraints

  - 1 <= A <= 1000000

  - 1 <= B <= 1000000

- Output Format

- One line containing the greater integer A or B.

- Sample Input 
-  5
-  6

- Sample Output
-  6
```
 import java.util.Scanner;
 
 public class num {
    public static void main(String[]arg){
        Scanner Value = new Scanner(System.in);
        
        int A = Value.nextInt();
        int B = Value.nextInt();
        
        int max = Math.max(A,B);
        
        System.out.println(max);
    }    
 }
```
## 2.Write a program to input three numbers(A, B & C) from user and print the maximum element among A, B & C in each line.

= Input Format

- First line is a single integer A. Second line is a single integer B. Third line is a single integer C.

- Constraints

   - 1 <= A <= 1000000

   - 1 <= B <= 1000000

- 1 <= C <= 1000000

- Output Format

- One line containing an integer as per the question.

- Sample Input
- 0
- 5 
- 6 
- 7
- Sample Output
- 0
- 7

 ```
import java.util.Scanner;

public class MaximumNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int A = scanner.nextInt();

        int B = scanner.nextInt();

        int C = scanner.nextInt();

        int max = Math.max(A, Math.max(B, C));
        System.out.println(max);
    }
}
```
## 3.Write a program to calculate the percentage (according to marks of a student) and grade (according to the percentage of a student). Five numbers(A, B, C, D & E) represent the marks of a student in 5 subjects which are out of 100. Print the percentage and the grade of the student.

- If percentage >= 90% : Grade A If percentage >= 80% but <90 : Grade B If percentage >= 70% but <80: Grade C If percentage >= 60% but <70: Grade D If percentage >= 40% but <60: Grade E If percentage < 40%: Grade F

- NOTE: You have to take the lowest integer of the percentage. E.g. 90.8% will be treated as 90%.

- Input Format

- There will be five lines of inputs as following: The five lines contain the 5 subject marks of the student in numerical format.

- Constraints

    - NA

- Output Format

- The first line indicates the percentage in integer format. The next line displays the grade in string format.

- Sample Input 0
- 50
- 60
- 70
- 80
- 90
- Sample Output 0
- 70
- C
 ```
import java.util.Scanner;
public class maxi{
    public static void main(String[]arg){
        Scanner scan = new Scanner(System.in);
         {
            int A = scan.nextInt();
            int B = scan.nextInt();
            int C = scan.nextInt();
            int D = scan.nextInt();
            int E = scan.nextInt();

            int total = A + B + C + D + E;
            int precentage = total / 5;

            String grade;
            
            if(precentage>=90){
                grade = "A";
            }
            else if(precentage>=80){
                grade = "B";
            }
            else if (precentage>=70){
                grade = "C";
            }
            else if (precentage>=60){
                grade = "D";
            }
            else if(precentage>=40){
                grade = "E";
            }
            else{
                grade = "F";
            }
            
            System.out.println(precentage);
            System.out.println(grade);
        }
    }
}
```

## 4.Write a program to input an integer(A) from user and print the Ath month of the year.

- Months list: {January, February, March, April, May, June, July, August, September, October, November, December}

- Input Format

- One line containing an integer integer A.

- Constraints

   - 1 <= A <= 12

- Output Format

- One line containing the Ath month of the year.

- Sample Input 0
- 1
- Sample Output 0
- January
```
import java.util.Scanner;

public class MonthOfYear {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input for the integer A
        int A = scanner.nextInt();

        // Array representing the months of the year
        String[] months = {"January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"};

        // Print the Ath month of the year
        System.out.println(months[A - 1]);
    }
}
```
## 5.You are given 3 integer angles(in degrees) A, B and C of a triangle. You have to tell whether the triangle is valid or not.

- A triangle is valid if sum of its angles equals to 180.

- Input Format

- First line of the input contains an integer A.

- Second line of the input contains an integer B.

- Third line of the input contains an integer C.

- Constraints

   - 1 <= A, B, C <= 180

- Output Format

- Print 1 if the triangle having given sides is valid, else print 0.

- Sample Input 0

 - 60
 - 60
 - 60
- Sample Output 0
- 1
- Explanation 0

- Sum of angles = A + B + C = 60 + 60 + 60 = 180 Hence, the given triangle is valid.
 ```
import java.util.Scanner;
public class fun{
    public static void main(String[]arg){
        Scanner value = new Scanner(System.in);

        int A = value.nextInt();
        int B = value.nextInt();
        int C = value.nextInt();

        int sum = A + B + C;

        if(sum==180){
            System.out.println("1");
        }
        else{
            System.out.println("0");
        }
    }
}
```
## 6.You are given a Bank account having N amount and you are asked to perform ADD(credit) or SUBTRACT(debit) operation of an amount X.

- After the operation print the amount left in the Bank account. If the debit amount is greater than current balance print "Insufficient Funds"(without quotes) and the operation is skipped.

- Input Format

- First line contains a single integer N denoting the balance in bank account.

- Next line contains two space separated integers Type and Amount(X).

- If Type == 1, Perform ADD operation. If Type == 2, Perform SUBTRACT operation.

- Constraints

    - 1 <= N, X <= 10^5

- Output Format

- Print Amount in the bank balance after the operation.

- Sample Input 0

- 1000
- 1 500
- Sample Output 0

- 1500
- Explanation 0

- Initially bank balance is 1000. ADD 500, bank balance becomes 1500, print it.
 ```
import java.util.Scanner;

public class BankAccount {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input for the initial balance
        int balance = scanner.nextInt();

        // Input for the operation type and amount
        int type = scanner.nextInt();
        int amount = scanner.nextInt();

        // Perform the operation based on the type
        if (type == 1) {
            // ADD operation
            balance += amount;
        } else if (type == 2) {
            // SUBTRACT operation
            if (amount > balance) {
                System.out.println("Insufficient Funds");
                return;
            }
            balance -= amount;
        }

        // Print the updated balance
        System.out.println(balance);
    }
}
```
## 7.Take an integer A as input. You have to tell whether A is divible by both 5 and 11 or not.

- Input Format

- The input contains a single integer A.

- Constraints

   - 1 <= A <= 10^9

- Output Format

- Print 1 if A is divisible by both 5 and 11, else print 0.
 ```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int A = scanner.nextInt();

        if (A % 5 == 0 && A % 11 == 0) {
            System.out.println(1);  
        } else {
            System.out.println(0);   
        }
    }
}
```
## 8.Write a program to input from user three numbers(A, B & C) representing side lengths of a triangle.

- You have to print if the traingle is "equilateral", "scalene" or "isosceles".

- Input Format

- One line containing three space separated integers A, B & C.

- Constraints

   - 1 <= A <= 100000

   - 1 <= B <= 100000

   - 1 <= C <= 100000

- Output Format

- One string either "equilateral", "scalene" or "isosceles".

- Sample Input 0

- 5
- 6
- 7
- Sample Output 0

- scalene
- Explanation 0

- Since all sides are different, hence it's a scalene triangle.
 ```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int A = scanner.nextInt();
        int B = scanner.nextInt();
        int C = scanner.nextInt();

        if (A == B && B == C) {
            System.out.println("equilateral");
        } else if (A == B || B == C || A == C) {
            System.out.println("isosceles");
        } else {
            System.out.println("scalene");
        }
    }
}
```
## 9.Write a program to input a number(A) from user and print 1 if it is positive, -1 if it is negative, 0 if it's neither positive nor negative.

- Input Format

- One line containing an integer A.

- Constraints

    - 1 <= A <= 1000000

- Output Format

- One line each 0/1/-1 as per the question.

- Sample Input 0
- 50
- Sample Output
- 0
- 1
 ```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int A = scanner.nextInt();

        if (A > 0) {
            System.out.println(1);  // A is positive
        } else if (A < 0) {
            System.out.println(-1);  // A is negative
        } else {
            System.out.println(0);  // A is neither positive nor negative
        }
    }
}
```
## 10.Given two numbers A and B. Print the floor of A/B.

- Input Format

- There are two input lines The first line has a single integer A. The second line has a single integer B.

- Constraints

    - 1 <= A, B <= 10^4

- Output Format

- Print the floor of A/B in a single line.

- Sample Input
- 0
- 4
- 5
- Sample Output 0
- 0
- Explanation 0
- floor(4/5) = 0
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int A = scanner.nextInt();
        int B = scanner.nextInt();
        int floor = A / B; // Integer division
        System.out.println(floor);
    }
}
```
