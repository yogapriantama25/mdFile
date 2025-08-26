# Bimbingan Mahasiswa Use Case Specification

## Overview

Dokumen ini menjelaskan use case lengkap untuk sistem bimbingan mahasiswa yang mencakup semua skenario penggunaan, aktor, dan alur kerja yang diperlukan untuk mengelola bimbingan akademik dan non-akademik.

## Actors (Aktor)

### Primary Actors
1. **Mahasiswa** - Pengguna utama yang mengajukan dan mengikuti bimbingan
2. **Dosen** - Pengguna yang memberikan bimbingan dan mengelola jadwal
3. **Kemahasiswaan** - Administrator yang mengelola sistem dan periode

### Secondary Actors
1. **Sistem** - Sistem otomatis yang mengirim notifikasi dan validasi
2. **File System** - Sistem penyimpanan dokumen

## Use Cases

## Business Rules

### BR-BIM-001: Periode Aktif
- Hanya satu periode yang dapat aktif pada satu waktu
- Bimbingan baru otomatis ter-assign ke periode aktif

### BR-BIM-002: Status Transitions
- Status bimbingan hanya dapat berubah sesuai workflow yang ditentukan
- Mahasiswa hanya dapat mengubah status dari "submitted" ke "completed"
- Dosen dapat mengubah semua status

### BR-BIM-003: Access Control
- Mahasiswa hanya dapat mengakses bimbingan sendiri
- Dosen hanya dapat mengakses bimbingan yang ditangani
- Kemahasiswaan dapat mengakses semua data

### BR-BIM-004: File Validation
- Dokumen bimbingan hanya dapat berformat PDF, JPG, JPEG, PNG
- Ukuran file maksimal 10MB
- File harus valid dan tidak corrupt

### BR-BIM-005: Scheduling Rules
- Jadwal bimbingan tidak boleh di masa lalu
- Link meeting harus valid URL
- Bulk scheduling hanya untuk bimbingan yang pending

## Exception Handling

### EX-BIM-001: Periode Tidak Aktif
**Condition:** Tidak ada periode bimbingan yang aktif
**Action:** Sistem menampilkan pesan error dan mencegah pembuatan bimbingan baru

### EX-BIM-002: Invalid Status Transition
**Condition:** User mencoba mengubah status yang tidak valid
**Action:** Sistem menampilkan pesan error dan tidak mengubah status

### EX-BIM-003: File Upload Error
**Condition:** File yang diupload tidak valid
**Action:** Sistem menampilkan pesan error dan tidak menyimpan file

### EX-BIM-004: Access Denied
**Condition:** User mencoba mengakses data yang tidak diizinkan
**Action:** Sistem menampilkan pesan error dan redirect ke halaman yang sesuai

### EX-BIM-005: Scheduling Conflict
**Condition:** Jadwal bimbingan bertabrakan dengan jadwal lain
**Action:** Sistem menampilkan warning dan meminta konfirmasi

## Performance Requirements

### PR-BIM-001: Response Time
- Dashboard loading: < 2 detik
- API response: < 1 detik
- File upload: < 30 detik untuk file 10MB

### PR-BIM-002: Concurrent Users
- Sistem harus dapat menangani 100+ concurrent users
- Database harus dapat menangani 1000+ bimbingan

### PR-BIM-003: Data Storage
- File storage harus dapat menangani 1GB+ dokumen
- Database harus dapat menangani 10,000+ records

## Security Requirements

### SR-BIM-001: Authentication
- Semua akses harus melalui token authentication
- Token harus expire setelah 24 jam

### SR-BIM-002: Authorization
- Access control berdasarkan role dan kepemilikan data
- Validasi keanggotaan untuk setiap request

### SR-BIM-003: Data Protection
- Data bimbingan harus dienkripsi
- File dokumen harus disimpan dengan aman
- Audit trail untuk semua perubahan

## Integration Points

### IP-BIM-001: Notification System
- Integrasi dengan sistem notifikasi untuk mengirim alert
- Support untuk email dan push notification

### IP-BIM-002: File System
- Integrasi dengan file storage system
- Support untuk CDN untuk file serving

### IP-BIM-003: Academic System
- Integrasi dengan sistem akademik untuk data mahasiswa dan dosen
- Sync data biodata mahasiswa

## Monitoring & Logging

### ML-BIM-001: Activity Logging
- Log semua aktivitas bimbingan
- Log semua perubahan status
- Log semua file upload

### ML-BIM-002: Performance Monitoring
- Monitor response time API
- Monitor database performance
- Monitor file storage usage

### ML-BIM-003: Error Tracking
- Track semua error dan exception
- Alert untuk critical errors
- Error reporting untuk debugging

## Testing Scenarios

### TS-BIM-001: Happy Path Testing
1. Mahasiswa ajukan bimbingan
2. Dosen review dan jadwalkan
3. Bimbingan dilaksanakan
4. Status diupdate ke completed

### TS-BIM-002: Error Handling Testing
1. Test invalid status transition
2. Test file upload dengan format invalid
3. Test access control untuk unauthorized user
4. Test scheduling conflict

### TS-BIM-003: Performance Testing
1. Test dengan 100+ concurrent users
2. Test file upload dengan file besar
3. Test database dengan 10,000+ records
4. Test API response time

### TS-BIM-004: Security Testing
1. Test authentication bypass
2. Test authorization bypass
3. Test file upload security
4. Test data encryption

## Conclusion

Dokumen use case specification ini memberikan panduan lengkap untuk implementasi dan testing sistem bimbingan mahasiswa. Semua skenario penggunaan telah diidentifikasi dan didokumentasikan dengan detail yang diperlukan untuk pengembangan yang sukses.