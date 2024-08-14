
Here are the C programs for the specified tasks without comments:

### Task 1: Save Student Details to `output.txt`
```c
#include <stdio.h>

int main() {
    FILE *file;
    file = fopen("output.txt", "w");

    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    int student_number;
    char name[50];
    int age;
    char address[100];

    printf("Enter your student number: ");
    scanf("%d", &student_number);

    printf("Enter your name: ");
    scanf(" %[^\n]", name);

    printf("Enter your age: ");
    scanf("%d", &age);

    printf("Enter your address: ");
    scanf(" %[^\n]", address);

    fprintf(file, "Student Number: %d\n", student_number);
    fprintf(file, "Name: %s\n", name);
    fprintf(file, "Age: %d\n", age);
    fprintf(file, "Address: %s\n", address);

    fclose(file);

    printf("Data successfully written to output.txt\n");

    return 0;
}
```

### Task 2: Perform Mathematical Operations
```c
#include <stdio.h>
#include <math.h>

int main() {
    float value;

    printf("Please enter your number: ");
    scanf("%f", &value);

    printf("Cosine value: %f\n", cos(value));
    printf("Sine value: %f\n", sin(value));
    printf("Value raised to the third power: %f\n", pow(value, 3));
    printf("Smallest integer greater than or equal to the input: %f\n", ceil(value));
    printf("Largest integer less than or equal to the input: %f\n", floor(value));
    printf("Natural log(e) of the input: %f\n", log(value));
    printf("Log base 10 of the input: %f\n", log10(value));

    return 0;
}
```

### Task 3: Print Personal Information
```c
#include <stdio.h>

void personal_info();

int main() {
    personal_info();
    return 0;
}

void personal_info() {
    printf("Name: John Doe\n");
    printf("Student ID: 12345678\n");
    printf("Address: 123 Main St.\n");
}
```

### Task 4: Find the Largest of Three Numbers
```c
#include <stdio.h>

int largest(int a, int b, int c) {
    int max = a;

    if (b > max)
        max = b;
    if (c > max)
        max = c;

    return max;
}

int main() {
    int num1, num2, num3;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &num1, &num2, &num3);

    printf("The largest number is: %d\n", largest(num1, num2, num3));

    return 0;
}
```

### Task 5: Simple Calculator
```c
#include <stdio.h>

float add(float a, float b) {
    return a + b;
}

float subtract(float a, float b) {
    return a - b;
}

float multiply(float a, float b) {
    return a * b;
}

float divide(float a, float b) {
    if (b != 0)
        return a / b;
    else {
        printf("Error: Division by zero!\n");
        return 0;
    }
}

int main() {
    float num1, num2;
    char operator;

    printf("Enter first number: ");
    scanf("%f", &num1);

    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);

    printf("Enter second number: ");
    scanf("%f", &num2);

    switch (operator) {
        case '+':
            printf("Result: %.2f\n", add(num1, num2));
            break;
        case '-':
            printf("Result: %.2f\n", subtract(num1, num2));
            break;
        case '*':
            printf("Result: %.2f\n", multiply(num1, num2));
            break;
        case '/':
            printf("Result: %.2f\n", divide(num1, num2));
            break;
        default:
            printf("Invalid operator!\n");
    }

    return 0;
}
```

### Task 6: Factorial Function
```c
#include <stdio.h>

unsigned long long factorial(int n) {
    if (n == 0 || n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    int num;

    printf("Enter a number to calculate its factorial: ");
    scanf("%d", &num);

    if (num < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        printf("Factorial of %d is %llu\n", num, factorial(num));
    }

    return 0;
}
```

### Task 7: Find the Leading Digit
```c
#include <stdio.h>

int leading_digit(int n) {
    while (n >= 10) {
        n /= 10;
    }
    return n;
}

int main() {
    int num;

    printf("Enter a positive integer: ");
    scanf("%d", &num);

    if (num <= 0) {
        printf("Please enter a positive integer.\n");
    } else {
        printf("The leading digit of %d is %d\n", num, leading_digit(num));
    }

    return 0;
}
```

These are the C programs you requested, without comments. Let me know if you need any further assistance!
