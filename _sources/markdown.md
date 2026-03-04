# Coding Python

## Sistem Persamaan Linier

**Mencari Variabel ke-2**

```python
import sympy as sp

# Membuat matriks augmented
A = sp.Matrix([
    [1, 1, 1, 6],
    [2, 1, 1, 9],
    [1, 2, 1, 8]
])

# Ubah ke RREF
rref_matrix, pivot = A.rref()

# Ambil variabel ke-2 (y)
y = rref_matrix[1, 3]

print("Nilai variabel ke-2 (y) adalah =", y)
```

**Hasil Penyelesaiaan**

Hasil Penyelesaian:
x = 2
y = 1

## Sistem Persamaan Linier

**Mencari Variabel ke-3**

```python
import sympy as sp

# Membuat matriks augmented
A = sp.Matrix([
    [1, 1, 1, 6],
    [2, 1, 1, 9],
    [1, 2, 1, 8]
])

# Mengubah ke bentuk RREF
rref_matrix, pivot = A.rref()

print("Bentuk RREF:")
print(rref_matrix)

# Mengambil solusi dari kolom terakhir
x = rref_matrix[0, 3]
y = rref_matrix[1, 3]
z = rref_matrix[2, 3]

print("\nSolusi:")
print("x =", x)
print("y =", y)
print("z =", z)
```

**Hasilnya Penyelesaian :**

x = 3
y = 2
z = 1
