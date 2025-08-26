# Bimbingan Mahasiswa Use Case Specification

### Actors
**Dosen** - Pengguna yang memberikan bimbingan dan mengelola jadwal

## Overview

Dokumen ini menjelaskan use case lengkap untuk sistem bimbingan mahasiswa yang mencakup semua skenario penggunaan, aktor, dan alur kerja yang diperlukan untuk mengelola bimbingan akademik dan non-akademik.


### UC-BIM-003: Review Request Bimbingan

**Actor:** Dosen

**Precondition:** 
- Dosen sudah login ke sistem
- Ada request bimbingan yang pending

**Main Flow:**
1. Dosen membuka dashboard bimbingan
2. Dosen melihat daftar request bimbingan yang pending
3. Dosen memilih request bimbingan untuk direview
4. Dosen melihat detail request bimbingan
5. Dosen memutuskan:
   - Jika disetujui: lanjut ke penjadwalan
   - Jika perlu revisi: berikan catatan dan set status "need_revision"
   - Jika ditolak: berikan alasan dan set status "rejected"

**Postcondition:** Request bimbingan berhasil direview

### UC-BIM-004: Jadwalkan Bimbingan

**Actor:** Dosen

**Precondition:** 
- Dosen sudah login ke sistem
- Ada request bimbingan dengan status "submitted" atau "reviewed"

**Main Flow:**
1. Dosen membuka halaman penjadwalan
2. Dosen memilih bimbingan yang akan dijadwalkan
3. Dosen mengisi jadwal:
   - Tanggal dan waktu bimbingan
   - Link meeting (untuk bimbingan online)
4. Dosen menyimpan jadwal
5. Sistem mengupdate status bimbingan menjadi "reviewed"
6. Sistem mengirim notifikasi ke mahasiswa

**Postcondition:** Bimbingan berhasil dijadwalkan

**Alternative Flow:**
- Jika jadwal bertabrakan, sistem menampilkan warning
- Jika link meeting tidak valid, sistem menampilkan error

### UC-BIM-005: Bulk Scheduling

**Actor:** Dosen

**Precondition:** 
- Dosen sudah login ke sistem
- Ada beberapa request bimbingan yang pending

**Main Flow:**
1. Dosen membuka halaman bulk scheduling
2. Dosen memilih beberapa bimbingan yang akan dijadwalkan
3. Dosen mengisi jadwal yang sama untuk semua bimbingan:
   - Tanggal dan waktu bimbingan
   - Link meeting
4. Dosen menyimpan jadwal massal
5. Sistem mengupdate status semua bimbingan menjadi "reviewed"
6. Sistem mengirim notifikasi ke semua mahasiswa terkait

**Postcondition:** Semua bimbingan berhasil dijadwalkan

### UC-BIM-006: Lakukan Bimbingan

**Actor:** Dosen

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

**Actor:** Dosen

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

### UC-BIM-008: Kelola Template Saran

**Actor:** Dosen

**Precondition:** Dosen sudah login ke sistem

**Main Flow:**
1. Dosen membuka halaman template saran
2. Dosen melihat daftar template yang sudah ada
3. Dosen memilih untuk membuat template baru atau mengedit yang ada
4. Jika membuat template baru:
   - Dosen mengisi judul template
   - Dosen mengisi isi template
   - Dosen menyimpan template
5. Jika mengedit template:
   - Dosen mengubah isi template
   - Dosen menyimpan perubahan

**Postcondition:** Template saran berhasil dikelola

### UC-BIM-009: Lihat Dashboard Dosen

**Actor:** Dosen

**Precondition:** Dosen sudah login ke sistem

**Main Flow:**
1. Dosen membuka dashboard
2. Sistem menampilkan statistik:
   - Total bimbingan yang ditangani
   - Bimbingan yang pending
   - Bimbingan yang completed
   - Bimbingan yang need revision
3. Sistem menampilkan distribusi berdasarkan kategori
4. Dosen dapat melihat detail untuk setiap statistik

**Postcondition:** Dashboard berhasil ditampilkan