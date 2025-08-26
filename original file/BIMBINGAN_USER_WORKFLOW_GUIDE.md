# Bimbingan Mahasiswa User Workflow Guide

## Overview

Panduan lengkap untuk menggunakan sistem bimbingan mahasiswa yang mencakup semua fitur dan alur kerja untuk mahasiswa, dosen, dan kemahasiswaan.

## Daftar Isi

1. [Login dan Autentikasi](#login-dan-autentikasi)
2. [Workflow Mahasiswa](#workflow-mahasiswa)
3. [Workflow Dosen](#workflow-dosen)
4. [Workflow Kemahasiswaan](#workflow-kemahasiswaan)
5. [Dashboard dan Analytics](#dashboard-dan-analytics)
6. [File Management](#file-management)
7. [Notifikasi](#notifikasi)
8. [Troubleshooting](#troubleshooting)

## Login dan Autentikasi

### Langkah-langkah Login
1. Buka aplikasi Sikemas
2. Masukkan username dan password
3. Klik tombol "Login"
4. Sistem akan memvalidasi kredensial
5. Jika berhasil, user akan diarahkan ke dashboard sesuai role

### Role-based Access
- **Mahasiswa**: Akses ke bimbingan sendiri dan fungsi request
- **Dosen**: Akses ke bimbingan yang ditangani dan fungsi penjadwalan
- **Kemahasiswaan**: Akses penuh ke semua data dan fungsi management

## Workflow Mahasiswa

### 1. Melihat Dashboard Mahasiswa

**Langkah-langkah:**
1. Login sebagai mahasiswa
2. Klik menu "Bimbingan" di sidebar
3. Dashboard akan menampilkan:
   - Periode aktif
   - Total bimbingan yang diajukan
   - Bimbingan dalam semester aktif
   - Bimbingan yang sudah dijadwalkan
   - Minimal requirement dan fulfillment status

### 2. Mengajukan Request Bimbingan

**Langkah-langkah:**
1. Dari dashboard, klik tombol "Ajukan Bimbingan Baru"
2. Isi form bimbingan:
   - **Dosen Pembimbing**: Pilih dosen dari dropdown
   - **Kategori**: Pilih Akademik atau Non-Akademik
   - **Jenis Bimbingan**: 
     - Akademik: KRS, Nilai, Tugas Akhir, Magang/PKL
     - Non-Akademik: Karir, Pribadi, Beasiswa, Lainnya
   - **Topik**: Masukkan topik bimbingan
   - **Deskripsi**: Jelaskan detail bimbingan
   - **Dokumen**: Upload dokumen pendukung (opsional)
3. Klik "Simpan" untuk menyimpan sebagai draft
4. Klik "Submit" untuk mengajukan ke dosen

**Tips:**
- Pastikan semua field wajib terisi
- Upload dokumen yang relevan untuk membantu dosen memahami kebutuhan
- Berikan deskripsi yang jelas dan detail

### 3. Melihat Jadwal Bimbingan

**Langkah-langkah:**
1. Klik menu "Jadwal Bimbingan"
2. Sistem menampilkan daftar bimbingan yang sudah dijadwalkan
3. Klik pada bimbingan untuk melihat detail:
   - Tanggal dan waktu
   - Link meeting
   - Topik bimbingan
   - Status bimbingan

### 4. Menambah Komentar

**Langkah-langkah:**
1. Buka detail bimbingan
2. Scroll ke bagian "Komentar"
3. Klik "Tambah Komentar"
4. Masukkan komentar
5. Klik "Kirim"

### 5. Upload Dokumen

**Langkah-langkah:**
1. Buka detail bimbingan
2. Klik "Upload Dokumen"
3. Pilih file (PDF, JPG, JPEG, PNG)
4. Klik "Upload"
5. Sistem akan memvalidasi dan menyimpan file

## Workflow Dosen

### 1. Melihat Dashboard Dosen

**Langkah-langkah:**
1. Login sebagai dosen
2. Klik menu "Bimbingan" di sidebar
3. Dashboard menampilkan:
   - Total bimbingan yang ditangani
   - Bimbingan yang pending
   - Bimbingan yang completed
   - Bimbingan yang need revision
   - Distribusi berdasarkan kategori

### 2. Review Request Bimbingan

**Langkah-langkah:**
1. Dari dashboard, klik "Request Pending"
2. Pilih bimbingan yang akan direview
3. Baca detail bimbingan dan dokumen pendukung
4. Pilih aksi:
   - **Setujui**: Klik "Setujui" untuk lanjut ke penjadwalan
   - **Revisi**: Klik "Perlu Revisi", berikan catatan
   - **Tolak**: Klik "Tolak", berikan alasan

### 3. Menjadwalkan Bimbingan

**Langkah-langkah:**
1. Dari daftar bimbingan yang disetujui, pilih bimbingan
2. Klik "Jadwalkan"
3. Isi form penjadwalan:
   - **Tanggal**: Pilih tanggal bimbingan
   - **Waktu**: Pilih waktu bimbingan
   - **Link Meeting**: Masukkan link meeting (untuk online)
4. Klik "Simpan Jadwal"
5. Sistem akan mengirim notifikasi ke mahasiswa

### 4. Bulk Scheduling

**Langkah-langkah:**
1. Klik menu "Bulk Scheduling"
2. Pilih beberapa bimbingan yang akan dijadwalkan
3. Isi jadwal yang sama untuk semua bimbingan
4. Klik "Jadwalkan Massal"
5. Sistem akan mengupdate semua bimbingan sekaligus

### 5. Melakukan Bimbingan

**Langkah-langkah:**
1. Bergabung ke meeting sesuai jadwal
2. Lakukan bimbingan sesuai topik
3. Setelah selesai, update status:
   - Klik "Selesai" untuk set status completed
   - Tambahkan catatan bimbingan
4. Klik "Simpan"

### 6. Mengelola Template Saran

**Langkah-langkah:**
1. Klik menu "Template Saran"
2. Untuk membuat template baru:
   - Klik "Tambah Template"
   - Isi judul dan isi template
   - Klik "Simpan"
3. Untuk mengedit template:
   - Pilih template yang akan diedit
   - Klik "Edit"
   - Ubah isi template
   - Klik "Simpan"

## Workflow Kemahasiswaan

### 1. Manajemen Periode Bimbingan

**Langkah-langkah:**
1. Login sebagai kemahasiswaan
2. Klik menu "Manajemen Periode"
3. Untuk membuat periode baru:
   - Klik "Tambah Periode"
   - Isi nama periode
   - Klik "Simpan"
4. Untuk mengaktifkan periode:
   - Pilih periode yang akan diaktifkan
   - Klik "Aktifkan"
   - Sistem otomatis menonaktifkan periode lain

### 2. Monitoring Bimbingan

**Langkah-langkah:**
1. Klik menu "Monitoring Bimbingan"
2. Sistem menampilkan:
   - Total bimbingan per periode
   - Status distribution
   - Performance metrics
3. Klik pada statistik untuk melihat detail

## Dashboard dan Analytics

### Dashboard Mahasiswa

**Informasi yang Ditampilkan:**
- Periode aktif saat ini
- Total bimbingan yang diajukan
- Bimbingan dalam semester aktif
- Bimbingan yang sudah dijadwalkan
- Minimal requirement (3 bimbingan per semester)
- Fulfillment status (apakah sudah memenuhi requirement)

### Dashboard Dosen

**Informasi yang Ditampilkan:**
- Total bimbingan yang ditangani
- Bimbingan yang pending review
- Bimbingan yang completed
- Bimbingan yang need revision
- Distribusi berdasarkan kategori (akademik vs non-akademik)
- Performance metrics

### Analytics

**Metrics yang Tersedia:**
- Response time dosen
- Completion rate
- Kategori bimbingan yang paling sering
- Trend bimbingan per periode

## File Management

### Format File yang Didukung
- **PDF**: Dokumen, laporan, proposal
- **JPG/JPEG**: Screenshot, foto
- **PNG**: Gambar dengan transparansi

### Ukuran File
- Maksimal 10MB per file
- Total storage per user: 100MB

### Upload Guidelines
1. Pastikan file tidak corrupt
2. Gunakan nama file yang deskriptif
3. Kompres file jika terlalu besar
4. Scan dokumen dengan resolusi yang baik

## Notifikasi

### Jenis Notifikasi
- **Request Baru**: Ketika mahasiswa mengajukan bimbingan
- **Jadwal Diupdate**: Ketika dosen menjadwalkan bimbingan
- **Status Berubah**: Ketika status bimbingan berubah
- **Komentar Baru**: Ketika ada komentar baru
- **Reminder**: Pengingat jadwal bimbingan

### Mengelola Notifikasi
1. Klik icon notifikasi di header
2. Lihat daftar notifikasi
3. Klik notifikasi untuk melihat detail
4. Klik "Mark as Read" untuk menandai sudah dibaca
5. Klik "Mark All as Read" untuk menandai semua sudah dibaca

## Troubleshooting

### Masalah Umum

#### 1. Tidak Bisa Login
**Penyebab:**
- Username/password salah
- Akun belum terdaftar
- Akun dinonaktifkan

**Solusi:**
- Periksa username dan password
- Hubungi admin untuk registrasi
- Hubungi admin untuk aktivasi akun

#### 2. Tidak Bisa Upload File
**Penyebab:**
- Format file tidak didukung
- Ukuran file terlalu besar
- Koneksi internet lambat

**Solusi:**
- Pastikan format file sesuai (PDF, JPG, JPEG, PNG)
- Kompres file jika terlalu besar
- Coba upload ulang dengan koneksi yang stabil

#### 3. Tidak Ada Periode Aktif
**Penyebab:**
- Belum ada periode yang diaktifkan
- Periode sudah berakhir

**Solusi:**
- Hubungi kemahasiswaan untuk aktivasi periode
- Tunggu periode baru

#### 4. Status Bimbingan Tidak Berubah
**Penyebab:**
- Transisi status tidak valid
- Tidak memiliki permission

**Solusi:**
- Pastikan transisi status sesuai workflow
- Hubungi admin jika ada masalah permission

#### 5. Notifikasi Tidak Muncul
**Penyebab:**
- Browser notification dinonaktifkan
- Notifikasi sudah dibaca

**Solusi:**
- Aktifkan notification di browser
- Refresh halaman untuk melihat notifikasi baru

### Error Messages

#### "Periode bimbingan tidak aktif"
- Hubungi kemahasiswaan untuk aktivasi periode

#### "Invalid status transition"
- Pastikan perubahan status sesuai workflow
- Hubungi admin jika diperlukan

#### "File format not supported"
- Pastikan format file sesuai (PDF, JPG, JPEG, PNG)
- Convert file ke format yang didukung

#### "File size too large"
- Kompres file atau gunakan file yang lebih kecil
- Maksimal ukuran file 10MB

#### "Access denied"
- Pastikan login dengan akun yang benar
- Hubungi admin jika ada masalah permission

### Best Practices

#### Untuk Mahasiswa
1. **Persiapkan dokumen** sebelum mengajukan bimbingan
2. **Berikan deskripsi yang jelas** untuk membantu dosen
3. **Ikuti jadwal** yang sudah ditentukan
4. **Aktif berkomunikasi** melalui komentar
5. **Upload dokumen pendukung** yang relevan

#### Untuk Dosen
1. **Review request dengan cepat** untuk efisiensi
2. **Berikan feedback yang konstruktif** melalui komentar
3. **Gunakan template saran** untuk konsistensi
4. **Jadwalkan bimbingan dengan tepat** untuk menghindari konflik
5. **Update status secara berkala** untuk tracking

#### Untuk Kemahasiswaan
1. **Aktifkan periode tepat waktu** untuk kelancaran
2. **Monitor performance** secara berkala
3. **Berikan support** kepada user yang mengalami masalah
4. **Backup data** secara regular
5. **Update sistem** sesuai kebutuhan

## Support dan Kontak

### Technical Support
- Unit IT

### Office Hours
- **Senin - Jumat**: 08:00 - 17:00 WIB
- **Sabtu**: 08:00 - 12:00 WIB
- **Minggu**: Tutup

### Documentation
- **User Manual**: Tersedia di help.sikemas.ac.id
- **Video Tutorial**: Tersedia di YouTube channel Sikemas
- **FAQ**: Tersedia di help.sikemas.ac.id/faq

## Conclusion

Panduan ini memberikan informasi lengkap untuk menggunakan sistem bimbingan mahasiswa. Pastikan untuk membaca dan memahami setiap bagian sebelum menggunakan sistem. Jika ada pertanyaan atau masalah, jangan ragu untuk menghubungi technical support.
