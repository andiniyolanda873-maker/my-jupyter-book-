# MATERI KAL

**Definisi 1.1.1. Persamaan Linear.**

_Sebuah ekspresi linear_ dalam _n_ perubah yang tidak diketahui (atau variabel) $x_1, x_2, \ldots, x_n$ adalah suatu bentuk yang dinyatakan sebagai

$$
a_{1}x_{1} + a_{2}x_{2} + \cdots + a_{n}x_{n},
$$

di mana $a_1, a_2, \ldots, a_n$ adalah bilangan real konstan.

Sebuah _persamaan linear_ dalam peubah yang tidak diketahui $x_1, x_2, \ldots, x_n$ adalah persamaan yang dapat disederhanakan, hanya dengan menggunakan operasi penjumlahan dan pengurangan, menjadi bentuk

$$
a_{1}x_{1} + a_{2}x_{2} + \cdots + a_{n}x_{n} = b,
$$

(1.1.1)

yang disebut sebagai _bentuk standar_. Suatu persamaan dalam variabel tak diketahui $x_1, x_2, \ldots, x_n$ disebut _nonlinear_ jika tidak dapat disederhanakan ke bentuk (1.1.1) hanya dengan menggunakan penjumlahan dan pengurangan.

Diberikan sebuah persamaan linear dengan bentuk standar (1.1.1), persamaan tersebut disebut _homogen_ jika \( b = 0 \), dan _nonhomogen_ jika $b \ne 0$.

# Definisi 1.1.3. Sistem persamaan linier

Sistem **persamaan linier** (atau **sistem linier**) adalah sekumpulan persamaan linier.

Sistem linier **homogen** adalah sekumpulan persamaan linier homogen.

Saat menampilkan sistem _m_ persamaan dalam _n_ tidak diketahui $x_1, x_2, \ldots, x_n$,  
kami biasanya menulis setiap persamaan dalam bentuk standar dan menyelaraskan istilah  
yang sesuai dari setiap persamaan ke dalam kolom:

$$
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= b_m
$$

Sistem homogen dengan demikian biasanya ditulis sebagai:

$$
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= 0 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= 0 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= 0
$$

---

# Keterangan 1.1.4

Anda akan ingin merasa nyaman dengan pengindeksan ganda yang digunakan untuk menampilkan sistem linier secepat mungkin.  
Berikut adalah cara yang baik untuk mengarahkan diri Anda:

- Itu $i$ muncul di $a_{ij}$ dan $b_i$ menunjukkan $i$-th dalam sistem yang ditampilkan, atau setara, $i$-persamaan.
- Itu $j$ muncul di $a_{ij}$ menunjukkan $j$-th dalam sistem yang ditampilkan, yang terkait dengan kolom $j$-th, untuk $1 \le j \le n$.

1. Pengertian Sistem Persamaan Linear (SPL)

Sistem Persamaan Linear adalah kumpulan dua atau lebih persamaan linear yang memiliki variabel yang sama dan harus dipenuhi secara bersamaan.

2. Penyelesaian SPL dengan Operasi Baris Elementer (OBE)

Operasi Baris Elementer digunakan pada matriks augmented untuk mencari solusi SPL.
Tiga operasi dasar:

1. Menukar dua baris

2. Mengalikan baris dengan bilangan ≠ 0

3. Menjumlahkan baris dengan kelipatan baris lain

Metode ini dikenal sebagai eliminasi Gauss atau Gauss-Jordan.

# Definisi 1.1.5. Solusi untuk sistem linier

**Solusi untuk persamaan linier**

$a_1x_1 + a_2x_2 + \cdots + a_nx_n = b$

adalah $n$-tuple $(s_1, s_2, \ldots, s_n)$ bilangan real yang penugasan variabel  
$x_1 = s_1, x_2 = s_2, \ldots, x_n = s_n$ membuat persamaan itu benar.  
Kami mengatakan $(s_1, s_2, \ldots, s_n)$ **memecahkan persamaan** dalam kasus ini.

**Solusi untuk sistem persamaan linier**

$$
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= b_m
$$

adalah $n$-tuple $(s_1, s_2, \ldots, s_n)$ itu adalah solusi untuk masing-masing sistem _m_ persamaan.  
Kami mengatakan $(s_1, s_2, \ldots, s_n)$ **memecahkan sistem** dalam hal ini.

Mengingat sistem linier, kita akan berusaha untuk menemukan kumpulan semuasolusi untuk sistem. Seperti yang akan segera kita lihat, serangkaian solusi ini akan mengambil salah satu dari tiga bentuk kualitatif:

1. Set solusi kosong; yaitu, tidak ada solusi. Kami mengatakan sistem tidak konsistendalam kasus ini. Jika tidak, sistem disebut konsisten.
2. Set solusi berisi satu elemen; yaitu, ada satu solusi.
3. Set larutan berisi banyak unsur; yaitu, ada solusi tak terbatas.

_kode python untuk OBE(operasi baris elementer)_

```python
import numpy as np

# Jumlah variabel
n = int(input("Masukkan jumlah variabel: "))

print("\nMasukkan persamaan (format: a1 a2 ... an b)")
print("Contoh x + y = 5 → 1 1 5\n")

A = []

# Input matriks augmented
for i in range(n):
    row = list(map(float, input(f"Persamaan {i+1}: ").split()))
    A.append(row)

A = np.array(A, dtype=float)

# ===== Menampilkan soal =====
print("\nSistem Persamaan Linear yang dimasukkan:")
for i in range(n):
    pers = ""
    for j in range(n):
        pers += f"{A[i,j]}x{j+1} "
        if j < n-1:
            pers += "+ "
    pers += f"= {A[i,n]}"
    print(pers)

print("\nMatriks awal:")
print(A)

# ===== OBE Gauss-Jordan =====
for i in range(n):

    # Jika pivot 0 → tukar baris
    if A[i][i] == 0:
        for k in range(i+1, n):
            if A[k][i] != 0:
                A[[i,k]] = A[[k,i]]
                break

    pivot = A[i][i]

    # Jika pivot 0 dan baris nol → lewati
    if pivot == 0:
      print(f"\nBaris {i+1} adalah baris nol → kemungkinan solusi tak hingga")
      continue

    print(f"\nMembagi baris {i+1} dengan {pivot}")
    A[i] = A[i] / pivot
    print(A)

    # Eliminasi
    for j in range(n):
        if i != j:
            A[j] = A[j] - A[j][i] * A[i]

    print(f"\nLangkah OBE ke-{i+1}:")
    print(A)

# ===== MENENTUKAN JENIS SOLUSI =====
tidak_ada = False
baris_nol = 0

for i in range(n):
    if np.allclose(A[i,:n], 0) and not np.isclose(A[i,n], 0):
        tidak_ada = True
    if np.allclose(A[i], 0):
        baris_nol += 1

print("Hasil akhir matriks:")
print(A)

if tidak_ada:
    print("Sistem tidak memiliki solusi")

elif baris_nol > 0:
    print("Sistem memiliki solusi tak hingga")
    print("Gunakan parameter bebas")

else:
    print("Solusi tunggal:")
    for i in range(n):
        print(f"x{i+1} =", A[i,n])
```

# contoh hasil untuk solusi tak hingga

Masukkan jumlah variabel: 2

Masukkan persamaan (format: a1 a2 ... an b)
Contoh x + y = 5 → 1 1 5

Persamaan 1: 1 1 2
Persamaan 2: 2 2 4

Sistem Persamaan Linear yang dimasukkan:

$$
1.0x1 + 1.0x2 = 2.0
$$

$$
2.0x1 + 2.0x2 = 4.0
$$

**Matriks awal:**

$$
\begin{bmatrix}
1 & 1 & 2 \\
2 & 2 & 4
\end{bmatrix}
$$

**Membagi baris 1 dengan 1.0**

$$
\begin{bmatrix}
1 & 1 & 2 \\
2 & 2 & 4
\end{bmatrix}
$$

**Langkah OBE ke-1:**

$$
\begin{bmatrix}
1 & 1 & 2 \\
0 & 0 & 0
\end{bmatrix}
$$

Baris 2 adalah baris nol $\rightarrow$ kemungkinan solusi tak hingga.

**Hasil akhir matriks:**

$$
\begin{bmatrix}
1 & 1 & 2 \\
0 & 0 & 0
\end{bmatrix}
$$

Sistem memiliki solusi tak hingga.  
Gunakan parameter bebas.

# cintoh hasil untuk solusi tunggal

masukkan jumlah variabel: 2

Masukkan persamaan (format: a1 a2 ... an b)
Contoh x + y = 5 → 1 1 5

Persamaan 1: 1 1 5
Persamaan 2: 2 -1 1

Sistem Persamaan Linear yang dimasukkan:

$$
1.0x1 + 1.0x2 = 5.0
$$

$$
2.0x1 + -1.0x2 = 1.0
$$

**Matriks awal:**

$$
\begin{bmatrix}
1 & 1 & 5 \\
2 & -1 & 1
\end{bmatrix}
$$

**Membagi baris 1 dengan 1.0**

$$
\begin{bmatrix}
1 & 1 & 5 \\
2 & -1 & 1
\end{bmatrix}
$$

**Langkah OBE ke-1:**

$$
\begin{bmatrix}
1 & 1 & 5 \\
0 & -3 & -9
\end{bmatrix}
$$

**Membagi baris 2 dengan -3.0**

$$
\begin{bmatrix}
1 & 1 & 5 \\
0 & 1 & 3
\end{bmatrix}
$$

**Langkah OBE ke-2:**

$$
\begin{bmatrix}
1 & 0 & 2 \\
0 & 1 & 3
\end{bmatrix}
$$

**Hasil akhir matriks:**

$$
\begin{bmatrix}
1 & 0 & 2 \\
0 & 1 & 3
\end{bmatrix}
$$

**Solusi tunggal:**

$$
x_1 = 2
$$

$$
x_2 = 3
$$

# contoh hasil untuk tidak ada solusi

Masukkan jumlah variabel: 2

Masukkan persamaan (format: a1 a2 ... an b)
Contoh x + y = 5 → 1 1 5

Persamaan 1: 1 1 2
Persamaan 2: 1 1 5

Sistem Persamaan Linear yang dimasukkan:

$$
1x_1 + 1x_2 = 2
$$

$$
1x_1 + 1x_2 = 5
$$

**Matriks awal:**

$$
\begin{bmatrix}
1 & 1 & 2 \\
1 & 1 & 5
\end{bmatrix}
$$

**Membagi baris 1 dengan 1.0**

$$
\begin{bmatrix}
1 & 1 & 2 \\
1 & 1 & 5
\end{bmatrix}
$$

**Langkah OBE ke-1:**

$$
\begin{bmatrix}
1 & 1 & 2 \\
0 & 0 & 3
\end{bmatrix}
$$

Baris kedua menghasilkan persamaan:

$$
0x_1 + 0x_2 = 3
$$

Karena persamaan tersebut tidak mungkin terpenuhi, sistem **tidak memiliki solusi (inkonsisten)**.
Sistem tidak memiliki solusi

# penjelasan geometri menggunakan geogebra

Geometri adalah cabang matematika yang mempelajari bentuk, ukuran, posisi, dan hubungan antar objek di ruang seperti titik, garis, sudut, bidang, dan bangun ruang.

unsur dasar geometri ada 5 yaitu:

1. titik = tidak punya ukuran, hanya posisi
2. garis = kumpulan titik yang memanjang
3. sudut = pertemuan dua garis
4. bidang = permukaan datar
5. ruang = tempat objek 3D berada

ada 4 jenis geometri yaitu:

1. geometri datar(2D) - mempelajari mengenai bangun pada bidang datar
2. geometri ruang(3D) - mempelajari bangun yang punya volume
3. geometri analitik - menggabungkan geometri dengan aljabar menggunakan koordinat(grafik x-y)
4. geometri transformasi - mempelajari perubahan bntuk tanpa mengubah sifat dasar

<iframe src="https://www.geogebra.org/calculator/y3tgyaaw?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

_bentuk bidang dengan geogebra_

<iframe src="https://www.geogebra.org/calculator/uma5kx87?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>
