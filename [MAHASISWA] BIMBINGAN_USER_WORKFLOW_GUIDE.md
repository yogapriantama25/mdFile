# Bimbingan Mahasiswa Use Case Specification

### Actors
**Mahasiswa** - Pengguna utama yang mengajukan dan mengikuti bimbingan

## Overview

Dokumen ini menjelaskan use case lengkap untuk sistem bimbingan mahasiswa yang mencakup semua skenario penggunaan, aktor, dan alur kerja yang diperlukan untuk mengelola bimbingan akademik dan non-akademik.

### UC-BIM-002: Ajukan Request Bimbingan

**Actor:** Mahasiswa

**Precondition:** 
- Mahasiswa sudah login ke sistem
- Ada periode bimbingan yang aktif

**Main Flow:**
1. Mahasiswa membuka halaman bimbingan
2. Mahasiswa memilih "Ajukan Bimbingan Baru"
3. Mahasiswa mengisi form bimbingan:
   - Memilih dosen pembimbing
   - Memilih kategori (akademik/non-akademik)
   - Memilih jenis bimbingan
   - Mengisi topik bimbingan
   - Mengisi deskripsi
   - Upload dokumen pendukung (opsional)
4. Mahasiswa menyimpan request bimbingan
5. Sistem otomatis mengassign periode aktif
6. Sistem mengirim notifikasi ke dosen
7. Status bimbingan menjadi "submitted"

**Postcondition:** Request bimbingan berhasil diajukan

**Alternative Flow:**
- Jika tidak ada periode aktif, sistem menampilkan pesan error
- Jika form tidak lengkap, sistem menampilkan validasi error

### UC-BIM-006: Lakukan Bimbingan

**Actor:** Mahasiswa

**Precondition:** 
- Bimbingan sudah dijadwalkan
- Waktu bimbingan sudah tiba

**Main Flow:**
1. Mahasiswa dan dosen bergabung ke meeting sesuai jadwal
2. Bimbingan dilaksanakan sesuai topik yang diajukan
3. Dosen memberikan feedback dan catatan
4. Setelah bimbingan selesai:
   - Dosen mengupdate status menjadi "completed"
   - Dosen menambahkan catatan bimbingan
5. Sistem mengirim notifikasi ke mahasiswa

**Postcondition:** Bimbingan berhasil dilaksanakan

### UC-BIM-007: Tambah Komentar

**Actor:** Mahasiswa

**Precondition:** 
- User sudah login ke sistem
- Ada bimbingan yang aktif

**Main Flow:**
1. User membuka detail bimbingan
2. User melihat daftar komentar yang ada
3. User menambahkan komentar baru
4. User menyimpan komentar
5. Sistem mengirim notifikasi ke user lain

**Postcondition:** Komentar berhasil ditambahkan

### UC-BIM-010: Lihat Dashboard Mahasiswa

**Actor:** Mahasiswa

**Precondition:** Mahasiswa sudah login ke sistem

**Main Flow:**
1. Mahasiswa membuka dashboard
2. Sistem menampilkan informasi:
   - Periode aktif
   - Total bimbingan yang diajukan
   - Bimbingan dalam semester aktif
   - Bimbingan yang sudah dijadwalkan
   - Minimal requirement dan fulfillment status
3. Mahasiswa dapat melihat detail untuk setiap informasi

**Postcondition:** Dashboard berhasil ditampilkan

### UC-BIM-011: Lihat Jadwal Bimbingan

**Actor:** Mahasiswa

**Precondition:** Mahasiswa sudah login ke sistem

**Main Flow:**
1. Mahasiswa membuka halaman jadwal bimbingan
2. Sistem menampilkan daftar bimbingan yang sudah dijadwalkan
3. Sistem mengurutkan berdasarkan tanggal dan waktu
4. Mahasiswa dapat melihat detail setiap jadwal

**Postcondition:** Jadwal bimbingan berhasil ditampilkan

### UC-BIM-012: Upload Dokumen Bimbingan

**Actor:** Mahasiswa

**Precondition:** 
- Mahasiswa sudah login ke sistem
- Ada bimbingan yang aktif

**Main Flow:**
1. Mahasiswa membuka detail bimbingan
2. Mahasiswa memilih "Upload Dokumen"
3. Mahasiswa memilih file dokumen (PDF, JPG, JPEG, PNG)
4. Mahasiswa mengupload dokumen
5. Sistem memvalidasi format dan ukuran file
6. Sistem menyimpan dokumen
7. Sistem mengupdate bimbingan dengan dokumen

**Postcondition:** Dokumen berhasil diupload

**Alternative Flow:**
- Jika format file tidak valid, sistem menampilkan error
- Jika ukuran file terlalu besar, sistem menampilkan error