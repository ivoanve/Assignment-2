# Matrix Multiplication Project Report

**Student Name**: Ivonne Andrea Anave Zenteno
**Student ID**: LS2408221
**Submission Date**: 26/03/2025

## System Configuration

| **Parameter**               | **Value**                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| **CPU Model**               |  Intel(R) Core(TM) i7-14650HX                                |
| **Memory Size**             |  total    15Gi   used  500Mi|
| **Operating System Version**| Linux DESKTOP-VDV6BM1 5.15.167.4-microsoft-standard-WSL2 #1 SMP Tue Nov 5 00:21:55 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux                                                 |
| **Compiler Version**        | gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0                                            |
| **Python Version**          | Python 3.12.9                                     |

## Implementation Details

### C Language Implementation

- **Source Code**:
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
      int mat1[SIZE][SIZE] = {{1, 2}, {3, 4}};
      int mat2[SIZE][SIZE] = {{5, 6}, {7, 8}};
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
  
#### Python Language Implementation
- **Source Code**: Include the Python script with comments explaining key sections.
- **Execution Command**: Describes how to run the script.

```markdown
### Python Language Implementation

- **Source Code**:
  ```python
  import numpy as np

  def multiply_matrices(mat1, mat2):
      return np.dot(mat1, mat2)

  mat1 = np.array([[1, 2], [3, 4]])
  mat2 = np.array([[5, 6], [7, 8]])

  result = multiply_matrices(mat1, mat2)

  print("Matrix 1:")
  print(mat1)
  print("Matrix 2:")
  print(mat2)
  print("Result:")
  print(result)
  
### 2. Algorithm Verification

```markdown
## Algorithm Verification

- **Correctness**: To verify the correctness of the matrix multiplication algorithm, we manually calculated the results for small matrices (2x2) and compared them with the output of the programs.


- **Analysis**: The C implementation is faster due to its compiled nature, which allows for more efficient execution. Python, being an interpreted language, has a higher overhead due to its dynamic nature and the use of the NumPy library for matrix operations.
## Conclusion

This project provided valuable insights into Unix/Linux command line operations, Markdown documentation, and the differences between compiled and interpreted languages. The C implementation demonstrated superior performance, while the Python implementation showcased the ease of use and readability of high-level languages.
## References

- [C Programming Language Documentation](https://gcc.gnu.org/)
- [Python Documentation](https://docs.python.org/3/)
- [NumPy Documentation](https://numpy.org/doc/stable/)
> Written with [StackEdit](https://stackedit.io/).
