# Bimbingan Mahasiswa Use Case Specification

### Actor
**Kemahasiswaan** - Administrator yang mengelola sistem dan periode

## Overview

Dokumen ini menjelaskan use case lengkap untuk sistem bimbingan mahasiswa yang mencakup semua skenario penggunaan, aktor, dan alur kerja yang diperlukan untuk mengelola bimbingan akademik dan non-akademik.

### UC-BIM-001: Manajemen Periode Bimbingan

**Actor:** Kemahasiswaan

**Precondition:** Kemahasiswaan sudah login ke sistem

**Main Flow:**
1. Kemahasiswaan membuka halaman manajemen periode
2. Sistem menampilkan daftar periode yang ada
3. Kemahasiswaan memilih untuk membuat periode baru atau mengaktifkan periode yang ada
4. Jika membuat periode baru:
   - Kemahasiswaan mengisi nama periode
   - Kemahasiswaan menyimpan periode
5. Jika mengaktifkan periode:
   - Kemahasiswaan memilih periode yang akan diaktifkan
   - Sistem otomatis menonaktifkan periode lain yang sedang aktif
   - Sistem mengaktifkan periode yang dipilih

**Postcondition:** Periode bimbingan berhasil dikelola

**Alternative Flow:**
- Jika periode sudah ada, sistem menampilkan pesan error