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