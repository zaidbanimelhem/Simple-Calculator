# Simple Calculator in C

A basic console-based calculator written in C that performs addition, subtraction, multiplication, and division.

## Features
- Performs basic arithmetic operations.
- Handles division by zero errors.
- Simple and easy to use.

## How to run
1. Clone this repository.
2. Compile the code using a C compiler (like GCC): `gcc main.c -o calculator`
3. Run the executable: `./calculator`



#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    printf("--- Simple Calculator ---\n");
    printf("Enter operator (+, -, *, /): ");
    scanf("%c", &operator);

    printf("Enter first number: ");
    scanf("%lf", &num1);
    printf("Enter second number: ");
    scanf("%lf", &num2);

    switch (operator) {
        case '+':
            result = num1 + num2;
            printf("%.2lf + %.2lf = %.2lf\n", num1, num2, result);
            break;
        case '-':
            result = num1 - num2;
            printf("%.2lf - %.2lf = %.2lf\n", num1, num2, result);
            break;
        case '*':
            result = num1 * num2;
            printf("%.2lf * %.2lf = %.2lf\n", num1, num2, result);
            break;
        case '/':
            if (num2 != 0) {
                result = num1 / num2;
                printf("%.2lf / %.2lf = %.2lf\n", num1, num2, result);
            } else {
                printf("Error: Division by zero is not allowed!\n");
            }
            break;
        default:
            printf("Invalid operator.\n");
    }

    return 0;
}
