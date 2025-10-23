# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
#include <math.h>

// Function declaration
void calculateEMI(double principal, double rate, int time);

int main() {
    double principal, rate;
    int time;

    // Read loan details from user
    printf("Enter principal amount: ");
    scanf("%lf", &principal);

    printf("Enter annual interest rate (in %%): ");
    scanf("%lf", &rate);

    printf("Enter time period in years: ");
    scanf("%d", &time);

    // Call EMI calculation function
    calculateEMI(principal, rate, time);

    return 0;
}

// Function definition to calculate EMI
void calculateEMI(double principal, double rate, int time) {
    double monthlyRate, emi;
    int months;

    monthlyRate = rate / (12 * 100);   // convert annual rate to monthly fraction
    months = time * 12;                // total number of monthly installments

    // EMI formula: EMI = [P * r * (1+r)^n] / [(1+r)^n - 1]
    emi = (principal * monthlyRate * pow(1 + monthlyRate, months)) / 
          (pow(1 + monthlyRate, months) - 1);

    printf("Your EMI is: %.2lf\n", emi);
}

```


## OUTPUT
<img width="387" height="256" alt="image" src="https://github.com/user-attachments/assets/eb5a5f19-034a-4557-8be0-579e47dba8b8" />






## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

int main() {
    int n = 6;        // number of terms
    int first = 0, second = 1, next;

    printf("Fibonacci series for %d terms:\n", n);

    for (int i = 1; i <= n; i++) {
        if (i == 1) {
            printf("%d ", first);
            continue;
        }
        if (i == 2) {
            printf("%d ", second);
            continue;
        }
        next = first + second;
        printf("%d ", next);
        first = second;
        second = next;
    }

    printf("\n");
    return 0;
}

```

## OUTPUT
<img width="555" height="157" alt="image" src="https://github.com/user-attachments/assets/6fdfe808-2cfb-481c-b6a0-d5516b2881b1" />









## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

int main() {
    int n;

    // Read the number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    // Read array elements
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Print the last element
    printf("The last element is: %d\n", arr[n - 1]);

    return 0;
}

```

## OUTPUT
<img width="402" height="201" alt="image" src="https://github.com/user-attachments/assets/8bdcd4ff-48db-4ebf-878e-2e73eafe9d86" />










## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

int main() {
    int n, count = 0;

    // Read the number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    // Read array elements
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Count positive elements
    for (int i = 0; i < n; i++) {
        if (arr[i] > 0)
            count++;
    }

    printf("Total number of positive elements = %d\n", count);

    return 0;
}

```


## OUTPUT
<img width="375" height="210" alt="image" src="https://github.com/user-attachments/assets/977ce532-0ccb-4892-b7d0-45c7778180bc" />






## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
```c
#include <stdio.h>

int main() {
    int n;

    // Read the number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    // Read array elements
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Replace even elements with 'E'
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0)
            arr[i] = 'E';  // ASCII value of 'E' will replace even number
    }

    // Print the updated array
    printf("Updated array:\n");
    for (int i = 0; i < n; i++) {
        if (arr[i] == 'E')
            printf("%c ", arr[i]);
        else
            printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}

```

## Output:
<img width="349" height="248" alt="image" src="https://github.com/user-attachments/assets/068fd04e-c0a7-4777-b88e-45e661b3d295" />

 


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



