# Penyelesaian sistem persamaan liner dengan menggunakan metode Gaussian

## Contoh SPL 3 Variabel (Eliminasi Gauss)

**Soal**

$$
\begin{cases}
x + y + z = 6 \\
2x - y + z = 3 \\
x + 2y - z = 3
\end{cases}
$$

**Langkah 1: Ubah ke bentuk matriks augmented**

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 3
\end{array}
\right]
$$

**Langkah 2: Hilangkan angka di bawah pivot pertama**

Pivot pertama = 1 (baris 1 kolom 1)

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -3
\end{array}
\right]
$$

Matriks Menjadi:

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 0 & -\frac{7}{3} & -6
\end{array}
\right]
$$

**Langkah 4: Substitusi balik**
Dari baris 3:

$$
-\frac{7}{3}z = -6
$$

$$
z = \frac{-6}{-\frac{7}{3}}
$$

$$
z = -6 \times \left(-\frac{3}{7}\right)
$$

$$
z = \frac{18}{7}
$$

Masukkan ke baris 2:

$$
-3y - z = -9
$$

$$
-3y - \frac{18}{7} = -9
$$

$$
-3y = -9 + \frac{18}{7}
$$

$$
-3y = -\frac{45}{7}
$$

$$
y = \frac{15}{7}
$$

Masukkan ke baris 1:

$$
x + y + z = 6
$$

$$
x + \frac{15}{7} + \frac{18}{7} = 6
$$

$$
x + \frac{33}{7} = 6
$$

$$
x = 6 - \frac{33}{7}
$$

$$
x = \frac{9}{7}
$$

**Jawaban SPL 3 Variabel**

$$
x = \frac{9}{7}, \quad
y = \frac{15}{7}, \quad
z = \frac{18}{7}
$$

## Contoh SPL 4 Variabel (Eliminasi Gauss)

**Soal**

$$
\begin{cases}
x + y + z + w = 10 \\
2x - y + z + w = 8 \\
x + 2y - z + w = 7 \\
x + y + z - w = 4
\end{cases}
$$

**Langkah 1: Matriks Augmented**

$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
2 & -1 & 1 & 1 & 8 \\
1 & 2 & -1 & 1 & 7 \\
1 & 1 & 1 & -1 & 4
\end{array}
\right]
$$

**Langkah 2: Nolkan bawah pivot pertama**
Hasil:

$$
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \\
0 & -3 & -1 & -1 & -12 \\
0 & 1 & -2 & 0 & -3 \\
0 & 0 & 0 & -2 & -6
\end{array}
\right]
$$

**Langkah 3: Dari baris terakhir**

$$
-2w = -6
$$

$$
w = 3
$$

**Langkah 4: Substitusi balik**
Baris 3

$$
y - 2z= 3
$$

Baris 2

$$
-3y - z - 3 = -12
$$

Masukkan w = 3

$$
-3y - z - 3 = -12
$$

$$
-3y - z = -9
$$

Selesaikan sistem 2 variabel

$$
\begin{cases}
y - 2z = -3 \\
-3y - z = -9
\end{cases}
$$

Hasil:

$$
z = 3
$$

$$
y = 3
$$

Masukkan ke baris 1:

$$
x + 3 + 3 + 3 = 10
$$

$$
x = 1
$$

**Jawaban SPL 4 Variabel**

$$
x = 1,\quad y = 3,\quad z = 3,\quad w = 3
$$
