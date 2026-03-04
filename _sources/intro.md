# Materi KAL

## Pengertian sistem persamaan linear

Sistem persamaan linear merupakan serangkaian persamaan linear yang terdiri dari satu atau lebih variabel yang tidak diketahui. Tujuan utama dari sistem persamaan linear adalah menyelesaikan masalah menggunakan aljabar linear elementer.Metode penyelesaian utamanya meliputi substitusi, eliminasi, grafik, dan matriks (invers/determinan). Dan SPL sering digunakan untuk mencari nilai variabel yang memenuhi persamaan, contohnya dalam pemodelan matematika dalam kesehariaan. Saya akan menjelaskan metode apa itu Penyelesaian Sistem Persamaan Linear ?

**1. Metode substitusi**

Metode substitusi adalah cara menyelesaikan sistem persamaan linear dengan mencari satu variabel dari salah satu persamaan, lalu menggantinya ke persamaan lain. Langkahnya: pilih persamaan yang paling mudah diselesaikan untuk satu variabel, substitusikan hasilnya ke persamaan kedua hingga menjadi satu variabel, selesaikan, lalu masukkan kembali nilainya untuk mendapatkan variabel lainnya. Terakhir, lakukan pengecekan dengan memasukkan kedua nilai ke persamaan awal.

**2. Metode Eliminasi**

Metode eliminasi menyelesaikan sistem persamaan linear dengan menghilangkan satu variabel melalui penjumlahan atau pengurangan persamaan. Caranya, samakan atau buat berlawanan koefisien salah satu variabel dengan mengalikan persamaan jika perlu, lalu jumlahkan atau kurangkan hingga variabel tersebut hilang. Selesaikan persamaan satu variabel yang diperoleh, kemudian substitusikan nilainya ke persamaan awal untuk mendapatkan variabel lainnya.

**3. Metode Grafik**

Metode grafik adalah cara visual untuk menyelesaikan sistem persamaan linear dua variabel dengan menggambar setiap persamaan sebagai garis di bidang Cartesius. Solusinya adalah titik potong kedua garis. Biasanya persamaan diubah ke bentuk ( y = mx + b ) agar mudah digambar menggunakan intersep dan kemiringan. Metode ini membantu memahami konsep, tetapi kurang akurat untuk perhitungan yang membutuhkan presisi tinggi.

**4. Metode matriks (invers/determinan)**

Metode matriks merupakan pendekatan aljabar yang sangat bagus untuk menyelesaikan sistem persamaan linier, terutama untuk sistem dengan banyak variabel. Dengan cara ini mengubah persamaan linear ke dalam bentuk matriks dan menggunakan operasi-operasi matriks untuk menemukan solusi.

## Definisi Persamaan Liner

Persamaan yang variabelnya hanya berpangkat satu.

**Bentuk umum:**

1 variabel : **ax + b = 0** solusi berupa angka
2 variabel : **ax + by + c =** grafiknya garis lurus di bidang.
3 variabel : **ax + by + cz + d = 0** grafiknya bidang datar di ruang 3D.

Ciri utama: tidak ada pangkat lebih dari 1, tidak ada perkalian antar variabel.

Solusinya adalah semua nilai variabel yang membuat persamaan benar.

## Bentuk Matriks

Matriks adalah susunan bilangan ril .Contoh persamaan liner dalam dua variabel adalah 2x - y+3 sedangkan matriks adalah gabungan bilangaan dalam bentuk tabel yang terdiri dari baris dan kolom di suatu bilangan dalam matriks di sebut elemen matriks.

kedua konsep ini dapat dihubungkan dalam bentuk persamaan liner. sebuah sistem linier dapat dilakukan dalam bentuk matriks yaitu sebagai berikut.

$$
\begin{cases}
2x + y = 5 \\
x - y = 1
\end{cases}
$$

dapat ditulis bentuk matriks seperti ini :

$$
\left[
\begin{array}{cc|c}
2 & 1 & 5 \\
1 & -1 & 1
\end{array}
\right]
$$

Bentuk ini disebut bentuk matriks dan sistem persamaan liner yang secara umum dapat ditulis sebagai

$$
AX=B
$$

Dimana :

1. A adalah matriks konfesien
2. X adalah matriks variabel
3. B adalah matriks konstansta

Dengan bentuk inipenyelesaiaan sistem dapat dilakukan dengan cara mengunakaan operasi matriks seperti invers matriks atau operasi barisan elementer.

## Konsep Operasi Baris Elementer (OBE)

Operasi Baris Elementer (OBE) adalah cara untuk mengubah bentuk matriks tanpa mengubah hasil atau solusi dari sistem persamaan linear. Biasanya digunakan untuk menyederhanakan matriks menjadi bentuk eselon atau eselon baris tereduksi agar lebih mudah diselesaikan.

Tiga Operasi Baris Elementer:

1. Menukar dua baris :Posisi dua baris ditukar.

2. Mengalikan satu baris dengan konstanta ≠ 0
   Semua elemen dalam satu baris dikalikan dengan suatu bilangan selain nol.

3. Menambahkan kelipatan suatu baris ke baris lain
   Satu baris ditambah dengan hasil perkalian baris lain dengan suatu bilangan.

Intinya: OBE dipakai untuk menyederhanakan matriks supaya mudah mencari solusi sistem persamaan linear atau mencari invers matriks.

## Contoh Penyelesaian OBE Variable 2

**Contoh Soal**

$$
\begin{cases}
2x + y = 5 \\
x - y = 1
\end{cases}
$$

1. Bentuk Matriks

$$
\left[
\begin{array}{cc|c}
2 & 1 & 5 \\
1 & -1 & 1
\end{array}
\right]
$$

2. Nolkan angka di bawah 2 Baris kedua − ½ × baris pertama

$$
\xrightarrow{R_2 \to R_2 - \frac{1}{2}R_1}
\left[
\begin{array}{cc|c}
2 & 1 & 5 \\
0 & -\frac{3}{2} & -\frac{3}{2}
\end{array}
\right]
$$

3. Substitusi Balik
   Dari baris kedua:

$$
-\frac{3}{2}y = -\frac{3}{2}
$$

$$
y = 1
$$

4. Masukkan ke baris pertama:

$$
2x + 1 = 5
$$

$$
2x = 4
$$

$$
x = 2
$$

5. Jawabaan Akhir

$$
x = 2,\quad y = 1
$$

## Contoh Penyelesaian OBE Variable 3

**Contoh Soal :**

$$
\begin{cases}
x + y + z = 6 \\
2x + y + z = 9 \\
x + 2y + z = 8
\end{cases}
$$

1. Bentuk Matriks

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & 1 & 1 & 9 \\
1 & 2 & 1 & 8
\end{array}
\right]
$$

2. Nolkan bawah kolom pertama
   Baris kedua − 2×baris pertama
   Baris ketiga − baris pertama

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -1 & -1 & -3 \\
0 & 1 & 0 & 2
\end{array}
\right]
$$

3. Substitusi Balik

$$
-z = -1
$$

$$
z = 1
$$

4. Masukkan ke baris kedua:

$$
-y - 1 = -3
$$

$$
-y = -2
$$

$$
y = 2
$$

5. Masukkan ke baris pertama:

$$
x + 2 + 1 = 6
$$

$$
x = 3
$$

6. Jawabaan Akhir

$$
\boxed{x = 3,\; y = 2,\; z = 1}
$$

## Penjelasan Geometri SPL Variabel 2

Setiap persamaan linier 2 variabel merepresentasikan garis.

Persamaan pertama:

$$
2x+y=5
$$

Persamaan Kedua :

$$
x-y=1
$$

Dua garis ini:

1. Jika berpotongan → satu solusi
2. Jika sejajar → tidak ada solusi
3. Jika berhimpit → tak hingga solusi

Pada contoh kita, garis berpotongan di titik:

$$
(2,1)
$$

## Visualisasi dengan GeoGebra

<iframe src="https://www.geogebra.org/calculator/rejuvuqd?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

## Penjelasaan geometri SPL Variabel ke 3

Setiap persamaan linier 2 variabel bidang ruang.

$$
\begin{cases}
x + y + z = 6 \\
2x + y + z = 9 \\
x + 2y + z = 8
\end{cases}
$$

jika ada 3 persamaan berarti ada 3 bidang kemungkinan yang akan terjadi:

1. Jika ketiga bidang berpotongan di satu titik - satu solusi
2. Jika berpotongan membentuk 1 garis -tak hingga solusi
3. Jika tidak bertemu di satu titik - tidak ada solusi

## Visualisasi dengan GeoGebra

<iframe src="https://www.geogebra.org/calculator/erkwf6nm?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

## Sumber Referensi

1. “Wikipedia. (2023). System of linear equations. Wikipedia.
   https://en.wikipedia.org/wiki/System_of_linear_equations”

2. “Ruangguru. (n.d.). Mengenal matriks dalam matematika: Pengertian, jenis, dan transpose.
   https://www.ruangguru.com/blog/mengenal-matriks-dalam-matematika-pengertian-jenis-dan-transpose”

3. “Konsep Matematika. (2015, September). Operasi baris elementer (OBE) dan penerapannya.
   https://konsep-matematika.com/2015/09/operasi-baris-elementer-obe-dan-penerapannya.html”

4. “Scribd. (n.d.). 2-SPL-OBE.
   https://www.scribd.com/document/596092219/2-SPL-OBE”
