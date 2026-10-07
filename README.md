# Dokumen Proyek

Kumpulan dokumen dari tiga proyek perangkat lunak yang pernah saya kerjakan di Institut Teknologi Del. Setiap proyek disimpan dalam foldernya sendiri dan memuat dokumen kebutuhan, perancangan, pengujian, serta dokumen pendukung.

## Daftar Proyek

| No | Folder | Proyek | Jenis |
|---|---|---|---|
| 1 | `Dokumen_DelPresence` | DelPresence, sistem absensi digital terintegrasi web dan mobile | Proyek Akhir (2025) |
| 2 | `Dokumen_Rancang Bangun Website` | Website SD Negeri 173551 Laguboti | Proyek Akhir 1 (2024) |
| 3 | `Dokumen_SPM(Satuan Penjaminan Mutu IT Del)` | Sistem Informasi Audit Mutu Internal (AMI) SPM IT Del | Proyek |

---

## 1. DelPresence

Sistem absensi digital untuk Institut Teknologi Del yang terdiri dari aplikasi web dan aplikasi mobile. Mahasiswa dapat melakukan absensi menggunakan **scan QR** dan **scan wajah (face recognition)**.

### Dokumen

| Dokumen | Keterangan |
|---|---|
| `BRD_DelPresence.pdf` | Dokumen kebutuhan bisnis |
| `Dokumen_Pengembangan_DelPresence...pdf` | Laporan pengembangan produk (Proyek Akhir) yang terdiri dari 6 bab |
| `Dokumen_Pengembangan_Del...pdf` | Dokumen pengembangan pendukung |

Isi laporan pengembangan produk:

1. Product Requirement Specification: pendahuluan, deskripsi umum produk, kebutuhan produk, environment hardware dan software, metodologi (Agile Scrum)
2. Project Planning: organisasi proyek, WBS, anggaran, tools, risiko dan hambatan
3. Product Design: proses bisnis, use case diagram, karakteristik pengguna, sequence diagram, ERD, CDM, PDM, prototipe antarmuka, arsitektur sistem
4. Product Implementation: IDE, pengujian dan kualitas, aplikasi terdistribusi, komputasi awan (GCP), keamanan, pseudocode
5. Product Testing: butir uji, tools, pengujian fungsional, non-fungsional, integrasi software dan hardware, serta prototipe
6. Product Release: daya guna produk, poster, dan perilisan

### Fitur

**Admin**
- Login dan logout
- Kelola program studi, fakultas, gedung, ruangan, tahun akademik, mata kuliah
- Kelola penugasan dosen dan jadwal perkuliahan
- Impor data dosen, pegawai, dan mahasiswa
- Kelola kelompok mahasiswa
- Melihat dashboard

**Dosen**
- Login dan logout
- Melihat mata kuliah yang ditugaskan dan jadwal mengajar
- Kelola presensi
- Kelola asisten dosen
- Melihat dashboard

**Asisten Dosen**
- Login dan logout
- Melihat jadwal mengajar
- Kelola presensi
- Melihat dashboard

**Mahasiswa**
- Login dan logout
- Pendaftaran wajah
- Absensi dengan scan QR
- Absensi dengan scan wajah
- Melihat jadwal perkuliahan, mata kuliah yang diampu, dan riwayat absensi

### Teknologi

Flutter (mobile), Next.js (web), Golang (backend), PostgreSQL, Docker, Google Cloud Platform.

---

## 2. Website SD Negeri 173551 Laguboti

Website profil dan informasi untuk SD Negeri 173551 Laguboti. Pengunjung (guest) dapat melihat informasi sekolah, sedangkan admin mengelola kontennya.

### Dokumen

| Dokumen | Keterangan |
|---|---|
| `BRD_Website_SD_Negeri_1735...pdf` | Business Requirements Document |
| `ToR-PA1-03-2024.pdf` | Term of Reference |
| `PiP-PA1-03-2024.pdf` | Project Implementation Plan |
| `SRS-PA1-03-2024.pdf` | Software Requirements Specification |
| `SDD-PA1-03-2024.pdf` | Software Design Description |
| `SWTD-PA1-03-2024.pdf` | SW Technical Document (versi 00.01, 13 Mei 2024, 211 halaman) |
| `MoM/` | Notulen rapat |
| `La/` | Dokumen laporan dan lampiran |

Isi SWTD: pendahuluan, gambaran sistem, deskripsi umum perangkat lunak, definisi kebutuhan (antarmuka, deskripsi fungsi, kebutuhan data dan ERD, kebutuhan fungsional dan non-fungsional), desain data (CDM dan PDM), struktur tabel, class diagram, sequence diagram, dan implementasi kode.

### Fitur

**Guest (pengunjung)**
- Melihat visi dan misi, sejarah, prestasi
- Melihat galeri dan pengumuman
- Melihat tenaga kerja dan kontak sekolah
- Melihat dan menambah saran

**Admin**
- Login dan logout
- Kelola visi dan misi (tambah, edit, hapus)
- Edit sejarah sekolah
- Kelola prestasi (tambah, edit, hapus)
- Kelola tenaga kerja (tambah, edit, hapus)
- Kelola galeri (tambah, edit, hapus)
- Kelola pengumuman (tambah, edit, hapus)
- Kelola kontak (tambah, edit, hapus)
- Hapus saran

Total 31 fungsi.

### Teknologi

Laravel 10, PHP 8.2, MySQL 8.0, XAMPP, Visual Studio Code, Figma.

---

## 3. Sistem Informasi Audit Mutu Internal (AMI) SPM IT Del

Sistem berbasis web untuk mengelola proses Audit Mutu Internal di Satuan Penjaminan Mutu IT Del secara terpusat, dari penyusunan standar sampai audit tindak lanjut.

### Dokumen

| Dokumen | Keterangan |
|---|---|
| `BRD_SPM_IT_Del.pdf` | Business Requirements Document (48 halaman) |
| `Dokumen_SPM(Satuan Penjaminan Mutu IT Del).pdf` | Dokumen proyek lengkap sistem SPM |

BRD memuat tujuan bisnis, pemangku kepentingan, proses bisnis, 110 kebutuhan fungsional dalam 16 modul, kebutuhan non-fungsional, aturan bisnis, siklus status dokumen, risiko, dan kriteria penerimaan.

### Fitur

Peran pengguna: **Admin/SPM**, **Auditor**, dan **Auditee** (Ketua dan Anggota).

- Login dan logout (akun CIS dan akun admin lokal)
- Kelola konfigurasi tahun akademik
- Kelola referensi kategori dan kategori detail
- Kelola role dan assign role pengguna (sinkronisasi CIS)
- Kelola standar mutu, termasuk salin dari tahun sebelumnya dan rilis FED
- Kelola indikator dan PIC
- Pembentukan tim auditee
- Pengisian Form Evaluasi Diri (FED) dengan bukti pendukung, simpan, submit, dan unduh
- Verifikasi FED, Daftar Tilik, desk evaluation, pembaruan, dan finalisasi FED
- Form Temuan dan Rencana Tindak Lanjut (temuan positif dan negatif otomatis dari FED)
- Form Audit Tindak Lanjut (ATL)
- Verifikasi status hasil ATL (Open, Toleran, Closed) dan finalisasi
- Monitoring progres AMI melalui dashboard Admin, Auditor, dan Auditee
- Unduh dokumen hasil dalam format PDF atau Word

### Teknologi

Laravel dan MySQL, terintegrasi dengan CIS IT Del untuk autentikasi.

---

## Catatan

- Repositori ini hanya berisi dokumen (PDF), tanpa kode program.
- Setiap folder berdiri sendiri dan tidak saling bergantung.

## Pemilik Repositori

Marshanda Kasih Simangunsong
