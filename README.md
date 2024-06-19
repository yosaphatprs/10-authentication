## Laporan Praktikum

|  | Pemrograman Berbasis Framework 2024 |
|--|--|
| NIM |  2141720031 |
| Nama |  Josafat Pratama Susilo |
| Kelas | TI - 3A |

### Praktikum 1

### Soal 1
Coba running di localhost, capture hasilnya dan buatlah laporan di README.md. Jelaskan apa yang telah Anda pelajari dan bagaimana tampilannya saat ini? Apakah ada error ?

Jangan lupa push dengan pesan commit: "W10: Jawaban soal 1".

### Jawaban Soal 1
Hasil:

![Hasil Soal 1](/assets-report/1.png)

Terdapat error pada acme, karena belum membuat filenya. Yang saya pelajari adalah setup autorisasi pada next.js menggunakan zod dan next-auth.

### Soal 2
Capture hasil form login yang telah dibuat dan buatlah laporan di README.md.

Jangan lupa push dengan pesan commit: "W10: Jawaban soal 2".

### Jawaban Soal 2

Hasil:

![Hasil Soal 2](/assets-report/2.png)

Saat saya mengerjakan praktikum soal 2, saya selalu mendapatkan error mengenai ```ReferenceError: bcrypt is not defined```, saya mencoba mencari solusi di internet dan menemukan bahwa dapat diatasi menggunakan bcryptjs. Saya menginstall dependency bcryptjs dan menggantikan bcrypt dengan bcryptjs pada file auth.js. Saya juga menginstal dev dependency @types/bcryptjs supaya dapat digunakan pada file typescript.

### Soal 3

Silakan save semua dan lakukan running di browser Anda. Capture hasilnya dan buatlah laporan di README.md.

1. Apakah ada error atau fitur yang belum berfungsi ? jika belum, silakan perbaiki!
2. Apakah ketika mengakses path URL root ( / ) dialihkan ke halaman login ? jika belum, silakan perbaiki!

Jangan lupa push dengan pesan commit: "W10: Jawaban soal 3".

### Jawaban Soal 3

Hasil:

Login:

![Hasil Soal 3](/assets-report/3-1.png)

Dashboard:

![Hasil Soal 3](/assets-report/3-2.png)

GIF (Alur Aplikasi):

![Hasil Soal 3](/assets-report/3.gif)

1. Sebelumnya terdapat error dan fungsi yang belum berhasil. Error yang terjadi adalah ```Error: `headers` was called outside a request scope``` hal ini dapat diatasi dengan menambahkan ```'use server'``` pada awal file actions.tsx. Setelah itu, saya memperbaiki beberapa fungsi, diantaranya adalah:
    - Fungsi login yang langsung redirect ke dashboard jika sudah login.
    - Fungsi logout yang langsung redirect ke login jika sudah logout.

2. Ketika mengakses path URL root ( / ) tidak dialihkan ke halaman login sebelumnya. Untuk nomor ini, saya sedikit kesusahan karena middleware seperti tidak berfungsi. Ternyata saya salah dalam menempatkan file auth.config.ts, auth.ts, dan middleware.ts yang berada diluar folder src. Setelah saya memindahkan file tersebut ke dalam folder src, maka aplikasi dapat berjalan dengan baik. Terutama saya merubah sedikit kode program dalam middleware supaya ketika mengakses path URL root ( / ) dialihkan ke halaman login jika tidak terautentikasi.