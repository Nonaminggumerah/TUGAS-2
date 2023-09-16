# TUGAS-2

Tugas 2 mengharuskan kami untuk membuat jawaban terkait konvolusi 2D.

Konvolusi 2D adalah operasi matematis yang sering digunakan dalam pemrosesan citra, pengolahan sinyal, dan bidang-bidang lainnya dalam ilmu komputer dan matematika. Operasi ini melibatkan penggunaan sebuah matriks kecil yang disebut "kernel" untuk memindai (bergeser) sebuah matriks sumber (input) yang lebih besar, dan pada setiap langkah pergeseran, melakukan perhitungan untuk menghasilkan matriks keluaran yang baru. Mari kita bahas beberapa konsep dasar terkait konvolusi 2D:

### Matriks Kernel

- Kernel adalah matriks kecil dengan ukuran tertentu yang digunakan untuk melakukan konvolusi. Kernel berisi bobot (atau koefisien) yang akan diterapkan pada elemen-elemen yang bersesuaian dalam matriks input.

- Kernel digunakan untuk menentukan bagaimana informasi dalam matriks input akan "difilter" atau "disaring" untuk menghasilkan matriks keluaran.

### Proses Pergeseran

- Konvolusi 2D melibatkan pergeseran kernel di atas matriks input. Pada setiap langkah pergeseran, kernel ditempatkan di atas sekelompok elemen yang bersesuaian dalam matriks input.

- Setelah kernel ditempatkan, produk titik antara elemen-elemen kernel dan elemen-elemen matriks input yang bersesuaian dihitung.

- Hasil dari produk ini kemudian dijumlahkan untuk membentuk elemen matriks keluaran pada posisi yang sesuai.

- Proses pergeseran ini berlanjut hingga seluruh matriks keluaran terbentuk.

### Aplikasi Umum Konvolusi 2D

Konvolusi 2D memiliki banyak aplikasi, termasuk:

1. **Pemrosesan Citra**: Dalam pemrosesan citra, konvolusi 2D digunakan untuk berbagai tugas seperti penyaringan citra (misalnya, menghilangkan noise), deteksi tepi, dan ekstraksi fitur.

2. **Pengolahan Sinyal**: Dalam pengolahan sinyal, konvolusi digunakan untuk operasi seperti konvolusi dalam domain frekuensi untuk filter sinyal atau ekstraksi fitur.

3. **Pengenalan Pola**: Dalam pengenalan pola, konvolusi digunakan untuk mencocokkan pola dalam citra dengan pola yang diinginkan.

### Implementasi dalam Python

Konvolusi 2D dapat diimplementasikan dalam Python dengan menggunakan pustaka seperti NumPy. Fungsi-fungsi khusus seperti `convolve2d` dalam NumPy atau berbagai pustaka pemrosesan citra dapat digunakan untuk melakukan konvolusi dengan mudah.

Contoh implementasi sederhana konvolusi 2D dalam Python dengan NumPy adalah seperti ini:

```python
import numpy as np

def convolution2d(input_matrix, kernel):
    result = np.zeros_like(input_matrix)
    kernel = np.flipud(np.fliplr(kernel))  # Melakukan flip kernel secara vertikal dan horizontal
    kernel_height, kernel_width = kernel.shape
    for i in range(input_matrix.shape[0] - kernel_height + 1):
        for j in range(input_matrix.shape[1] - kernel_width + 1):
            result[i, j] = np.sum(input_matrix[i:i+kernel_height, j:j+kernel_width] * kernel)
    return result
```

Inilah dasar-dasar konvolusi 2D. Ini adalah operasi penting yang memungkinkan kita untuk melakukan berbagai tugas dalam pemrosesan citra, pengolahan sinyal, dan analisis data lainnya. Dengan pemahaman tentang konsep dasar ini, Anda dapat menjelajahi berbagai aplikasi yang lebih kompleks.


## Tugas 2 Contoh Konvolusi 2D

Adapun tugas 2 hasilnya adalah dalam link berikut :

https://github.com/Nonaminggumerah/TUGAS-2/blob/master/5009211079_Nadya%20Putri%20Arisni_Tugas%20SPO%202.pdf
