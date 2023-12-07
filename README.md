# Matrix_Multipplication
def matrix_multiply(matrix1, matrix2):
    result = []

    # Check if matrices can be multiplied
    if len(matrix1[0]) != len(matrix2):
        print("Matrices cannot be multiplied. Number of columns in matrix1 must be equal to the number of rows in matrix2.")
        return None

    # Initialize the result matrix with zeros
    for _ in range(len(matrix1)):
        result.append([0] * len(matrix2[0]))

    # Perform matrix multiplication
    for i in range(len(matrix1)):
        for j in range(len(matrix2[0])):
            for k in range(len(matrix2)):
                result[i][j] += matrix1[i][k] * matrix2[k][j]

    return result

# Example matrices
matrix_a = [[1, 2, 3], [4, 5, 6]]
matrix_b = [[7, 8], [9, 10], [11, 12]]

# Testing the function
result_matrix = matrix_multiply(matrix_a, matrix_b)

# Printing the result
if result_matrix is not None:
    for row in result_matrix:
        print(row)
