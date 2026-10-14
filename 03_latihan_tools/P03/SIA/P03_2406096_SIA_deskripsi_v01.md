Elemen                  SIA-UC03 — Ajukan KRS
Tujuan                  Menghasilkan pengajuan KRS yang tersimpan
Aktor utama             Mahasiswa
Sumber kebutuhan        SIA-R03 dan SIA-R04
Pemicu                  Mahasiswa memilih fungsi pengajuan KRS
Prasyarat               Mahasiswa telah terautentikasi; data mata kuliah,
                        prasyarat, dan jadwal tersedia
Pascakondisi berhasil   Pengajuan KRS tersimpan dengan status
                        Menunggu persetujuan dosen wali
Pascakondisi gagal      Tidak ada pengajuan baru yang berhasil tersimpan
Include                 SIA-UC04 — Validasi KRS
Extension point         Konfirmasi penyimpanan pengajuan, pada langkah 6
Extend                  SIA-UC05 jika [mahasiswa memilih unduh bukti]


Elemen                  SIA-UC04 — Validasi KRS
Tujuan                  Memastikan pengajuan KRS memenuhi aturan validasi
Aktor utama             Mahasiswa (pemicu melalui pengajuan KRS)
Sumber kebutuhan        SIA-R04
Pemicu                  SIA-UC03 menjalankan validasi KRS
Prasyarat               Mahasiswa telah memilih mata kuliah untuk diajukan;
                        data mata kuliah, prasyarat, dan jadwal tersedia
Pascakondisi berhasil   KRS dinyatakan valid dan dapat diproses untuk
                        penyimpanan
Pascakondisi gagal      KRS dinyatakan tidak valid dan pengajuan belum
                        berhasil tersimpan
Include                 Tidak ada
Extend                  Tidak ada


Elemen                  SIA-UC05 — Unduh bukti pengajuan KRS
Tujuan                  Menyediakan bukti pengajuan KRS yang dapat diunduh
Aktor utama             Mahasiswa
Sumber kebutuhan        SIA-R05
Pemicu                  Mahasiswa memilih unduh bukti pada konfirmasi
                        penyimpanan pengajuan
Prasyarat               Pengajuan KRS berhasil tersimpan
Pascakondisi berhasil   Bukti pengajuan berhasil diunduh oleh mahasiswa
Pascakondisi gagal      Bukti tidak berhasil diunduh; pengajuan KRS tetap
                        tersimpan
Include                 Tidak ada
Extend                  SIA-UC03 — Ajukan KRS
Kondisi                 [mahasiswa memilih unduh bukti]


Elemen                  SIA-UC06 — Proses keputusan KRS
Tujuan                  Menghasilkan keputusan persetujuan atau penolakan KRS
Aktor utama             Dosen wali
Sumber kebutuhan        SIA-R06
Pemicu                  Dosen wali memilih pengajuan KRS untuk diproses
Prasyarat               Pengajuan KRS telah tersimpan dengan status
                        Menunggu persetujuan dosen wali
Pascakondisi berhasil   Keputusan tersimpan dengan status Disetujui atau
                        Ditolak beserta catatan keputusan
Pascakondisi gagal      Keputusan belum berhasil diproses atau disimpan
Include                 Tidak ada
Extend                  Tidak ada