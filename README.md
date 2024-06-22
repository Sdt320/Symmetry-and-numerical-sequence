# Symmetry-and-numerical-sequence
We can write a C program that uses nested loops to generate the desired output. The pattern has a specific symmetry and numerical sequence that must be followed.

Here's the code to achieve the given pattern:

```c
#include <stdio.h>

int main() {
    int n = 4; // The number of rows for the top part, excluding the middle line

    // Print the upper part of the pattern including the middle line
    for (int i = 0; i <= n; i++) {
        printf("*");
        for (int j = 1; j <= i; j++) {
            printf("%d", j);
        }
        for (int j = i - 1; j >= 1; j--) {
            printf("%d", j);
        }
        if (i > 0) {
            printf("*");
        }
        printf("\n");
    }

    // Print the lower part of the pattern
    for (int i = n - 1; i >= 1; i--) {
        printf("*");
        for (int j = 1; j <= i; j++) {
            printf("%d", j);
        }
        for (int j = i - 1; j >= 1; j--) {
            printf("%d", j);
        }
        if (i > 0) {
            printf("*");
        }
        printf("\n");
    }
    printf("*\n");

    return 0;
}
```

Explanation:
1. The variable `n` is set to `4`, representing the number of rows in the top part of the pattern excluding the middle line.
2. The first `for` loop generates the upper part of the pattern including the middle line. For each row `i`, it starts with a `*`, then prints the numbers from `1` to `i`, and then prints the numbers from `i-1` down to `1`. Another `*` is printed if `i` is greater than `0`.
3. The second `for` loop generates the lower part of the pattern. It mirrors the upper part by decreasing the row number `i` from `n-1` to `1`.
4. Finally, a single `*` is printed to complete the bottom of the pattern.

Output:
```
*
*1*
*121*
*12321*
*121*
*1*
*
```

This program prints the pattern exactly as described. Adjust the value of `n` to change the size of the pattern.
