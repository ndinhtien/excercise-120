import numpy as np

def generate_matrix(N, M):
    return np.random.randint(-100, 101, (N, M))

def calculate_determinant(matrix):
    if matrix.shape[0] == matrix.shape[1]:
        return np.linalg.det(matrix)
    return "Determinant not defined for non-square matrices"

def inverse_matrix(matrix):
    if matrix.shape[0] == matrix.shape[1]:
        try:
            return np.linalg.inv(matrix)
        except np.linalg.LinAlgError:
            return "Matrix is singular and cannot be inverted"
    return "Inverse not defined for non-square matrices"

def sort_by_row(matrix):
    return np.sort(matrix, axis=1)

def sort_by_column(matrix):
    return np.sort(matrix, axis=0)

def sort_by_row_avg(matrix):
    return matrix[np.argsort(np.mean(matrix, axis=1))]

def change_element(matrix, row, col, new_value):
    matrix[row, col] = new_value
    return matrix

def change_column(matrix, col):
    matrix[:, col] += 2
    return matrix

def add_vector(matrix):
    vector = np.random.randint(-10, 11, matrix.shape[1])
    return matrix + vector

def calculate_rank(matrix):
    return np.linalg.matrix_rank(matrix)

def calculate_svd(matrix):
    U, S, Vt = np.linalg.svd(matrix)
    return U, S, Vt

# Example usage
N, M = 4, 4  # Adjust dimensions as needed
matrix = generate_matrix(N, M)
print("Original Matrix:")
print(matrix)
print("Determinant:", calculate_determinant(matrix))
print("Inverse Matrix:", inverse_matrix(matrix))
print("Sorted by row:")
print(sort_by_row(matrix))
print("Sorted by column:")
print(sort_by_column(matrix))
print("Sorted by row averages:")
print(sort_by_row_avg(matrix))
print("Rank of matrix:", calculate_rank(matrix))
U, S, Vt = calculate_svd(matrix)
print("SVD - U:")
print(U)
print("SVD - S:")
print(S)
print("SVD - Vt:")
print(Vt)
