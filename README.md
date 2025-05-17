# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
```
#include <stdio.h>
int main() 
{
    int m, n;
    scanf("%d %d", &m, &n);
    if (m % 2 != 0) { 
        m++;
    }

    for (int i = m; i <= n; i += 2) {
        printf("%d ", i);
    }
    printf("\n");

    return 0;
}
```
## OUTPUT:

![image](https://github.com/user-attachments/assets/c0f113db-7709-442b-b23d-4871980bf1c7)









## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
```
#include <stdio.h>

int main() 
{
    int rows, i, j, space;
    scanf("%d", &rows);
    for (i = 1; i <= rows; ++i)
    {
        for (space = 1; space <= rows - i; ++space) 
        {
            printf(" ");
        }

        for (j = 1; j <= 2 * i - 1; ++j) {
            printf("X");
        }

        printf("\n");
    }

    return 0;
}
```

## OUTPUT:



![image](https://github.com/user-attachments/assets/ded16472-cf7e-4920-a172-5734b29f9ca5)


## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
```
#include <stdio.h>
int add(int a, int b);
int subtract(int a, int b);

int main() {
    int num1, num2;
    scanf("%d", &num1);
    scanf("%d", &num2);

    
    printf("Addition: %d\n", add(num1, num2));
    printf("Subtraction: %d\n", subtract(num1, num2));

    return 0;
}
int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) { 
    return a - b;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/16fb019f-cdde-451c-b08e-1ac7d14bd4c3)






## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int number, sum_odd = 0;
    
    printf("Enter a number: ");
    scanf("%d", &number);
    
    if (number < 0) {
        number = -number;
    }
    
    for (; number > 0; number /= 10) {
        int digit = number % 10;
        if (digit % 2 != 0) {
            sum_odd += digit;
        }
    }
    
    printf("Sum of odd digits: %d\n", sum_odd);
    
    return 0;
}

```
## OUTPUT:
![image](https://github.com/user-attachments/assets/1ea361c1-41d9-4247-8805-e7cf8d4a7f03)




## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
```
#include <stdio.h>

void fact() {
    int i, N;
    long long fact = 1; // Using long long to handle larger factorials
    
    printf("Enter a number: ");
    scanf("%d", &N);
    
    // Handle negative input
    if (N < 0) {
        printf("Factorial is not defined for negative numbers.\n");
        return;
    }
    
    for (i = 1; i <= N; i++) {
        fact *= i;
    }
    
    printf("Factorial of %d is: %lld\n", N, fact);
}

int main() {
    fact();
    return 0;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/81df83c8-b28b-4997-a68b-3ed955aa12f1)

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.

 
