---
title: "Assignment 1: Matrix Multiplication"
date: 2025-06-06
---
## Matrix Multiplication Project Report

**Student Name**: Ivonne Andrea Anave Zenteno  
**Student ID**: LS2408221  
**Submission Date**: 26/03/2025  

---

## System Configuration

| **Parameter**               | **Value**                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| **CPU Model**               | Intel(R) Core(TM) i7-14650HX                                              |
| **Memory Size**             | total 15Gi, used 500Mi                                                    |
| **Operating System Version**| Linux WSL2 - Ubuntu 22.04                                                 |
| **Compiler Version**        | gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0                                 |
| **Python Version**          | Python 3.12.9                                                             |

---

## Implementation Details
### C Language Implementation
{% raw %}
```c
#include <stdio.h>
#include <stdlib.h>

#define SIZE 2

void printMatrix(int mat[SIZE][SIZE]) {
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            printf("%d ", mat[i][j]);
        }
        printf("\n");
    }
}

void multiplyMatrices(int mat1[SIZE][SIZE], int mat2[SIZE][SIZE], int result[SIZE][SIZE]) {
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            result[i][j] = 0;
            for (int k = 0; k < SIZE; k++) {
                result[i][j] += mat1[i][k] * mat2[k][j];
            }
        }
    }
}

int main() {
int mat1[SIZE][SIZE] = { {1, 2}, {3, 4} };
int mat2[SIZE][SIZE] = { {5, 6}, {7, 8} };

    int result[SIZE][SIZE];

    multiplyMatrices(mat1, mat2, result);

    printf("Matrix 1:\n");
    printMatrix(mat1);
    printf("Matrix 2:\n");
    printMatrix(mat2);
    printf("Result:\n");
    printMatrix(result);

    return 0;
}
```
{% endraw %}
### Python Language Implementation
{% raw %}
```python
def print_matrix(matrix):
    for row in matrix:
        print(" ".join(str(val) for val in row))

def multiply_matrices(mat1, mat2):
    result = [[0, 0], [0, 0]]
    for i in range(2):
        for j in range(2):
            for k in range(2):
                result[i][j] += mat1[i][k] * mat2[k][j]
    return result

mat1 = [[1, 2], [3, 4]]
mat2 = [[5, 6], [7, 8]]

print("Matrix 1:")
print_matrix(mat1)
print("Matrix 2:")
print_matrix(mat2)
print("Result:")
result = multiply_matrices(mat1, mat2)
print_matrix(result)
```
{% endraw %}
### 2. Algorithm Verification

- **Correctness**: To verify the correctness of the matrix multiplication algorithm, I manually calculated the results for small matrices (2x2) and compared them with the output of the programs.


- **Analysis**: The C implementation is faster due to its compiled nature, which allows for more efficient execution. Python, being an interpreted language, has a higher overhead due to its dynamic nature and the use of the NumPy library for matrix operations.
## Conclusion

This project provided valuable insights into Unix/Linux command line operations, Markdown documentation, and the differences between compiled and interpreted languages. The C implementation demonstrated superior performance, while the Python implementation showcased the ease of use and readability of high-level languages.
## References

- [C Programming Language Documentation](https://gcc.gnu.org/)
- [Python Documentation](https://docs.python.org/3/)
- [NumPy Documentation](https://numpy.org/doc/stable/)
> Written with [StackEdit](https://stackedit.io/).
