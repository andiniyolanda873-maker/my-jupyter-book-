# Coding Phyton (Jupyter)

## Pembuktian Python (Jupyter) variabel 3

```python
import sympy as sp

def with_added_multiple_of_row(M, i, j, k):
    M2 = M.copy()
    M2.row_op(i, lambda v, col: v + k*M[j, col])
    return M2

M0 = sp.Matrix([
    [1,1,1,6],
    [2,-1,1,3],
    [1,2,-1,3]
])

M1 = with_added_multiple_of_row(M0,1,0,-2)
M2 = with_added_multiple_of_row(M1,2,0,-1)
M3 = with_added_multiple_of_row(M2,2,1,sp.Rational(1,3))

M3.rref()
```

## Pembuktian Python (Jupyter) variabel 4

```python
B = sp.Matrix([
    [1,1,1,1,10],
    [2,-1,1,1,8],
    [1,2,-1,1,7],
    [1,1,1,-1,4]
])

B.rref()
```

## Pembuktian di web gaussian sage variabel 3

![Gauss Variabel 3](images/gasuan-variabel-2.png)
<img src="images/gasuan-variabel-2.png" width="500">

## Pembuktian di web gaussian sage variabel 4

![Gauss 4](images/gasuan-variabel-4.png)
<img src="images/gasuan-variabel-4.png" width="500">
