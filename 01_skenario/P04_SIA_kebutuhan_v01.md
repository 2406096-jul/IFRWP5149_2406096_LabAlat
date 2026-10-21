### Tabel 4.6 Kebutuhan Tugas Pertemuan 4

| ID | Kebutuhan Tugas |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik. |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya. |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan. |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa. |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |


## Katalog Use Case Gabungan Pertemuan 2, 3, dan 4

| ID | Nama Use Case | Peran dalam Model | Sumber Kebutuhan |
|--- |---            |---                |---               |
| SIA-UC01 | Lihat Jadwal Kuliah | Tetap dari Pertemuan 2; fungsi lama untuk melihat jadwal kuliah. | SIA-R01 |
| SIA-UC02 | Kelola Jadwal Kuliah | Tetap dari Pertemuan 2; fungsi lama untuk mengelola jadwal kuliah. | SIA-R02 |
| SIA-UC03 | Ajukan KRS | Tetap dari Pertemuan 3; fungsi lama pengajuan KRS. | SIA-R03 |
| SIA-UC04 | Validasi KRS | Tetap dari Pertemuan 3; perilaku validasi KRS sesuai relasi pada diagram sebelumnya. | SIA-R03 |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Tetap dari Pertemuan 3; tambahan bersyarat pada pengajuan KRS melalui `«extend»` jika sesuai diagram sebelumnya. | SIA-R04 |
| SIA-UC06 | Proses Keputusan KRS | Tetap dari Pertemuan 3; fungsi lama pemrosesan keputusan KRS. | SIA-R05, SIA-R06 |
| SIA-UC07 | Lihat Kalender Akademik | Baru pada Pertemuan 4; fungsi aktor umum Civitas Akademika. | SIA-R07 |
| SIA-UC08 | Input Nilai Mata Kuliah | Baru pada Pertemuan 4; fungsi utama Dosen dan direalisasikan oleh SIA-CO01. | SIA-R08, SIA-R12 |
| SIA-UC09 | Lihat KHS | Baru pada Pertemuan 4; fungsi utama Mahasiswa dan direalisasikan oleh SIA-CO02. | SIA-R09, SIA-R12 |
| SIA-UC10 | Kelola Data Mahasiswa | Baru pada Pertemuan 4; use case umum bagi SIA-UC11, SIA-UC12, dan SIA-UC13. | SIA-R10, SIA-R11 |
| SIA-UC11 | Tambah Data Mahasiswa | Baru pada Pertemuan 4; use case khusus dari SIA-UC10. | SIA-R11 |
| SIA-UC12 | Ubah Data Mahasiswa | Baru pada Pertemuan 4; use case khusus dari SIA-UC10. | SIA-R11 |
| SIA-UC13 | Hapus Data Mahasiswa | Baru pada Pertemuan 4; use case khusus dari SIA-UC10. | SIA-R11 |

### Identifikasi Aktor

| Nama Aktor | Peran dalam Model | Sumber |
|---         |---                |--     -|
| Civitas Akademika | Aktor umum yang memiliki fungsi melihat kalender akademik. | SIA-R07 |
| Mahasiswa | Aktor khusus dari Civitas Akademika; dapat melihat kalender akademik dan KHS. | SIA-R07, SIA-R09 |
| Dosen | Aktor khusus dari Civitas Akademika; dapat melihat kalender akademik dan menginput nilai mata kuliah yang diampunya. | SIA-R07, SIA-R08 |
| Admin Akademik | Aktor yang mengelola data mahasiswa. | SIA-R10, SIA-R11 |
| Dosen Wali | Aktor yang tetap dipertahankan dari pertemuan sebelumnya. | Kebutuhan Pertemuan 2 dan 3 |