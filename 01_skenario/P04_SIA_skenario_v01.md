# Tugas Pertemuan 4
## Layanan Hasil Studi

Tugas ini berbeda dari tugas pertemuan sebelumnya. Tugas Pertemuan 2 membahas jadwal kuliah, sedangkan Tugas Pertemuan 3 membahas pengajuan KRS. Tugas Pertemuan 4 membahas layanan hasil studi dengan menggunakan teknik generalization dan collaboration yang sama seperti pada studi kasus sebelumnya, tetapi diterapkan pada skenario baru tanpa contoh jawaban.

### Skenario

Skenario tugas berikut bersifat fiktif untuk praktikum dan berbeda dari tugas Pertemuan 2 (jadwal kuliah) dan Pertemuan 3 (pengajuan KRS).

Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa dapat melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan.

Admin Akademik bertugas mengelola data mahasiswa, yang meliputi menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa.

Dua use case utama, yaitu **Input Nilai Mata Kuliah** dan **Lihat KHS**, ditunjukkan realisasinya melalui collaboration yang bersesuaian.

### Tabel 4.6 Kebutuhan Tugas Pertemuan 4

| ID | Kebutuhan Tugas |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik. |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya. |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan. |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa. |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |

### Batas dan Asumsi

- Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02 (Pertemuan 2), serta SIA-R03 sampai SIA-R06 (Pertemuan 3), tetap mempunyai identitas berbeda.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Kalender akademik pada tugas ini merupakan agenda resmi institusi, seperti awal semester, batas KRS, masa ujian, dan sejenisnya. Kalender akademik tidak boleh disamakan dengan jadwal kuliah pada Pertemuan 2.
- Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai yang diinput belum terpublikasi sebelum dinyatakan resmi sesuai ketentuan tugas ini. KHS hanya menampilkan nilai yang sudah dipublikasikan.
- Hapus Data Mahasiswa hanya diperbolehkan untuk mahasiswa yang tidak memiliki data akademik aktif. Ketentuan ini bersifat fiktif untuk latihan.
- Pengajuan KRS tetap digambar sebagai bagian dari diagram kumulatif Pertemuan 3.
- Pembayaran dan perancangan basis data berada di luar cakupan tugas ini.


Langkah 3: Tetapkan Generalization Aktor
- Mahasiswa adalah bentuk khusus dari Civitas Akademika, dan Dosen adalah bentuk khusus dari Civitas Akademika. Alasannya, keduanya merupakan bagian dari Civitas Akademika dan memiliki fungsi bersama, yaitu melihat kalender akademik.

- Asosiasi ke SIA-UC07 Lihat Kalender Akademik digambar satu kali dari Civitas Akademika. Garis asosiasi tersebut tidak perlu digambar ulang dari Mahasiswa dan Dosen karena kedua aktor mewarisi fungsi dari aktor umum melalui generalization.

- Asosiasi khusus Mahasiswa dan Dosen tetap dipertahankan. Mahasiswa memiliki asosiasi ke SIA-UC09 Lihat KHS, sedangkan Dosen memiliki asosiasi ke SIA-UC08 Input Nilai Mata Kuliah. Fungsi tersebut tidak dipindahkan ke Civitas Akademika karena merupakan fungsi khusus masing-masing aktor.

- Periksa arah panah generalization pada diagram. Ujung segitiga kosong harus mengarah ke Civitas Akademika, bukan ke Mahasiswa atau Dosen. Mahasiswa dan Dosen menjadi aktor khusus yang terhubung ke aktor umum tersebut.

Langkah 4: Tetapkan Generalization Use Case

SIA-UC11 Tambah Data Mahasiswa, SIA-UC12 Ubah Data Mahasiswa, dan SIA-UC13 Hapus Data Mahasiswa adalah bentuk khusus dari SIA-UC10 Kelola Data Mahasiswa. Alasannya, ketiganya merupakan bentuk khusus dari pengelolaan data mahasiswa oleh Admin Akademik.
- SIA-UC11 Tambah Data Mahasiswa: Menghasilkan data mahasiswa baru yang ditambahkan ke dalam sistem.
- SIA-UC12 Ubah Data Mahasiswa: Menghasilkan data mahasiswa yang telah diperbarui sesuai perubahan yang dilakukan.
- SIA-UC13 Hapus Data Mahasiswa: Menghapus data mahasiswa dari sistem dengan syarat mahasiswa tersebut tidak memiliki data akademik aktif, sesuai aturan studi kasus.

Langkah 5: Tetapkan Collaboration dan Realization

### Katalog Collaboration

| ID | Nama Collaboration (Sama dengan Nama Use Case) | Use Case yang Direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08: Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09: Lihat KHS |

Alasan: Kedua use case tersebut merupakan use case utama pada layanan hasil studi. Oleh karena itu, realisasinya ditunjukkan secara eksplisit melalui collaboration yang bersesuaian. SIA-CO01 merealisasikan proses input nilai mata kuliah oleh dosen pengampu, sedangkan SIA-CO02 merealisasikan proses mahasiswa melihat KHS yang nilainya sudah dipublikasikan.

Langkah 6: Susun Use Case Description
A. Deskripsi Use Case SIA-UC08: Input Nilai Mata Kuliah
### Spesifikasi Use Case SIA-UC08: Input Nilai Mata Kuliah

| Elemen | Keterangan |
|---|---|
| ID dan Nama | SIA-UC08: Input Nilai Mata Kuliah |
| Sumber Kebutuhan | SIA-R08 dan SIA-R12 |
| Tujuan | Nilai mahasiswa untuk mata kuliah yang diampu dosen berhasil dimasukkan dan disimpan ke dalam sistem. |
| Aktor Utama | Dosen |
| Pemicu | Dosen memilih fungsi input nilai dan menentukan mata kuliah yang akan diinput nilainya. |
| Prasyarat | Dosen telah terautentikasi, memiliki hak akses sesuai perannya, dan merupakan dosen pengampu mata kuliah yang dipilih. Masa perkuliahan untuk mata kuliah tersebut telah berakhir. |
| Pascakondisi Berhasil | Nilai mahasiswa berhasil disimpan dalam sistem, tetapi belum dianggap dipublikasikan sebelum dinyatakan resmi sesuai ketentuan tugas. |
| Pascakondisi Gagal | Nilai tidak tersimpan atau tidak mengalami perubahan. Sistem menampilkan informasi kegagalan. |
| Include | Tidak ada. |
| Collaboration | SIA-CO01: Input Nilai Mata Kuliah |

### Alur Utama SIA-UC08: Input Nilai Mata Kuliah

| Langkah | Tindakan Dosen | Respons Sistem |
|---|---|---|
| 1 | Memilih fungsi input nilai mata kuliah. | Menampilkan daftar mata kuliah yang dapat diinput nilainya oleh dosen. |
| 2 | Memilih mata kuliah yang akan diinput nilainya. | Menampilkan data mata kuliah dan daftar mahasiswa yang mengikuti mata kuliah tersebut. |
| 3 | Tidak ada. | Memeriksa apakah dosen merupakan pengampu mata kuliah yang dipilih. |
| 4 | Memasukkan nilai mahasiswa. | Menerima dan memvalidasi nilai yang dimasukkan. |
| 5 | Mengonfirmasi penyimpanan nilai. | Memeriksa apakah nilai berada dalam rentang yang sah. |
| 6 | Melihat hasil penyimpanan. | Menyimpan nilai yang valid dan menampilkan konfirmasi bahwa nilai berhasil disimpan. |

Alur alternatif atau pengecualian
- A1: Dosen bukan pengampu mata kuliah (pada langkah 3). Sistem menolak akses untuk menginput nilai dan menampilkan pesan bahwa dosen tidak memiliki hak untuk menginput nilai mata kuliah tersebut. Pascakondisi gagal berlaku; tidak ada nilai yang disimpan.
- A2: Nilai berada di luar rentang yang sah (pada langkah 5). Sistem menolak nilai yang dimasukkan dan menampilkan pesan kesalahan agar dosen memperbaiki nilai tersebut. Nilai yang tidak sah tidak disimpan. Pascakondisi gagal berlaku apabila proses berakhir tanpa penyimpanan yang berhasil.
- A3: Terjadi kegagalan penyimpanan. Sistem menampilkan informasi bahwa nilai gagal disimpan. Data nilai tidak berubah dan pascakondisi gagal berlaku.

B. Deskripsi Ringkas Use Case SIA-UC09: Lihat KHS

### Spesifikasi Use Case SIA-UC09: Lihat KHS

| Elemen | Keterangan |
|---|---|
| ID dan Nama | SIA-UC09: Lihat KHS |
| Sumber Kebutuhan | SIA-R09 dan SIA-R12 |
| Tujuan | Mahasiswa dapat melihat Kartu Hasil Studi (KHS) untuk semester yang dipilih. |
| Aktor Utama | Mahasiswa |
| Pemicu | Mahasiswa memilih menu KHS dan menentukan semester yang ingin dilihat. |
| Prasyarat | Mahasiswa telah terautentikasi dan memiliki hak akses sesuai perannya. |
| Pascakondisi Berhasil | KHS ditampilkan dengan hanya memuat nilai yang sudah dipublikasikan. |
| Pascakondisi Gagal | KHS tidak berhasil ditampilkan dan sistem memberikan informasi yang sesuai. |
| Include | Tidak ada. |
| Collaboration | SIA-CO02: Lihat KHS |

### Alur Utama SIA-UC08: Input Nilai Mata Kuliah

| Langkah | Tindakan Dosen | Respons Sistem |
|---|---|---|
| 1 | Memilih fungsi input nilai mata kuliah. | Menampilkan daftar mata kuliah yang dapat diinput nilainya oleh dosen. |
| 2 | Memilih mata kuliah yang akan diinput nilainya. | Menampilkan data mata kuliah dan daftar mahasiswa yang mengikuti mata kuliah tersebut. |
| 3 | Tidak ada. | Memeriksa apakah dosen merupakan pengampu mata kuliah yang dipilih. |
| 4 | Memasukkan nilai mahasiswa. | Menerima dan memvalidasi nilai yang dimasukkan. |
| 5 | Mengonfirmasi penyimpanan nilai. | Memeriksa apakah nilai berada dalam rentang yang sah. |
| 6 | Melihat hasil penyimpanan. | Menyimpan nilai yang valid dan menampilkan konfirmasi bahwa nilai berhasil disimpan. |

Alur alternatif atau pengecualian
- A1: Belum ada nilai yang dipublikasikan. Sistem tidak menampilkan nilai yang belum dipublikasikan. Jika belum ada nilai yang dapat ditampilkan, sistem memberikan informasi bahwa hasil studi belum tersedia.
- A2: KHS gagal dimuat. Sistem menampilkan pesan bahwa KHS tidak dapat ditampilkan. Pascakondisi gagal berlaku.