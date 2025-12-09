# Dokumentasi Lengkap Proyek E-Learning System

> 🌐 **Live Website**: [https://learningsystem.neuraworks.id](https://learningsystem.neuraworks.id)
> 
> 📧 **Kontak**: Jika Anda tertarik dengan proyek ini atau memiliki pertanyaan, silakan hubungi saya melalui email: [athaillah@neuraworks.id](mailto:athaillah@neuraworks.id)

## 📋 Daftar Isi

1. [Overview Proyek](#overview-proyek)
2. [Teknologi yang Digunakan](#teknologi-yang-digunakan)
3. [Struktur Proyek](#struktur-proyek)
4. [Halaman Siswa (Student Pages)](#halaman-siswa-student-pages)
5. [Halaman Instruktur (Instructor Pages)](#halaman-instruktur-instructor-pages)
6. [Halaman Admin (Admin Pages)](#halaman-admin-admin-pages)
7. [Sistem Autentikasi](#sistem-autentikasi)
8. [Learning Path System](#learning-path-system)
9. [Deployment](#deployment)
10. [Pengembangan](#pengembangan)

---

## Overview Proyek

**E-Learning System** adalah platform pembelajaran online yang dirancang khusus untuk sistem pembelajaran terintegrasi di lingkungan manufaktur. Sistem ini mendukung berbagai peran pengguna dengan fitur-fitur khusus untuk masing-masing peran.

🌐 **Akses aplikasi**: [https://learningsystem.neuraworks.id](https://learningsystem.neuraworks.id)

### Fitur Utama

- ✅ Sistem pembelajaran berbasis kursus
- ✅ Learning Path terstruktur berdasarkan cluster dan job level
- ✅ Manajemen tugas dan penilaian
- ✅ Forum diskusi
- ✅ Perpustakaan SOP (Standard Operating Procedure)
- ✅ Jadwal pelatihan
- ✅ Analytics dan pelaporan
- ✅ Sistem sertifikasi bertingkat
- ✅ Audit trail untuk tracking aktivitas

### Target Pengguna

1. **Siswa (Student)** - Karyawan yang mengikuti pelatihan
2. **Instruktur (Instructor)** - Pengajar yang mengelola kursus
3. **Admin** - Administrator sistem
4. **Manager** - Manajer yang memantau tim
5. **HRD** - Divisi HR yang mengelola pelatihan
6. **Supervisor** - Supervisor yang memantau tim

---

## Struktur Proyek

Proyek menggunakan struktur standar React dengan komponen terorganisir berdasarkan role (admin, instructor, student), layout, dan shared components. Konfigurasi deployment menggunakan Docker dan Caddy untuk reverse proxy.

---

## Halaman Siswa (Student Pages)

### 1. Dashboard Siswa (`/dashboard`)

**Fitur:**
- **Welcome Section** dengan informasi user:
  - Cluster (Operator, Leader, Supervisor, Manager, Expatriate)
  - Job Level (Basic, Intermediate, Advanced)
  - Level Sertifikasi (1-5)
  - Progress Learning Path keseluruhan

- **Quick Stats Cards:**
  - Pelatihan Aktif
  - Jam Pelatihan
  - Level Sertifikasi
  - Rata-rata Nilai

- **My Learning Path Section:**
  - Menampilkan Learning Path yang di-assign
  - Progress keseluruhan
  - Progress per track (Technical, Culture, Productivity)
  - Status completion per track

- **My Courses Table:**
  - Daftar kursus yang di-enroll
  - Progress per kursus
  - Status (Belum Dimulai, Berlangsung, Selesai)
  - Aksi untuk melanjutkan/mulai kursus

- **Recent Activity:**
  - Notifikasi terbaru
  - Aktivitas pembelajaran

- **Quick Actions:**
  - Lihat Jadwal
  - Forum Diskusi
  - Sertifikat Saya

### 2. Daftar Kursus (`/courses`)

**Fitur:**
- Grid/list view kursus
- Filter berdasarkan kategori
- Search kursus
- Informasi kursus:
  - Thumbnail
  - Judul dan deskripsi
  - Instruktur
  - Rating
  - Jumlah siswa enrolled
  - Durasi
- Enroll ke kursus

### 3. Detail Kursus (`/courses/:courseId`)

**Fitur:**
- Informasi lengkap kursus
- Daftar modul dan lesson
- Progress tracking per lesson
- Video player untuk video lessons
- Document viewer untuk document lessons
- Quiz interface
- Assignment submission
- Navigasi antar lesson

### 4. Tugas (`/assignments`)

**Fitur:**
- Daftar semua tugas
- Filter berdasarkan:
  - Status (Belum dikerjakan, Sedang dikerjakan, Selesai, Terlambat)
  - Kursus
  - Deadline
- Informasi tugas:
  - Judul dan deskripsi
  - Kursus terkait
  - Deadline
  - Status submission
  - Score (jika sudah dinilai)
- Submit tugas dengan attachment
- View feedback dari instruktur

### 5. Nilai (`/grades`)

**Fitur:**
- Daftar nilai dari semua kursus
- Breakdown nilai per:
  - Assignment
  - Quiz
  - Final exam
- Grafik progress nilai
- Rata-rata nilai keseluruhan
- Sertifikat yang sudah diperoleh
- Download sertifikat

### 6. Jadwal (`/schedule`)

**Fitur:**
- Kalender view jadwal pelatihan
- List view jadwal
- Filter berdasarkan:
  - Tanggal
  - Tipe pelatihan (Classroom, OJT, Practical)
  - Status (Scheduled, Ongoing, Completed)
- Detail jadwal:
  - Waktu dan lokasi
  - Instruktur
  - Materi pelatihan
  - Daftar peserta
- Enroll ke pelatihan
- Absensi

### 7. Forum Diskusi (`/forum`)

**Fitur:**
- Daftar thread diskusi per kursus
- Buat thread baru
- Reply ke thread
- Search dan filter thread
- Like/upvote post
- Notifikasi reply
- Mark as read/unread

### 8. Perpustakaan SOP (`/sop-library`)

**Fitur:**
- Daftar SOP documents
- Filter berdasarkan:
  - Kategori (Production, Quality, Safety, Maintenance, Warehouse, HR)
  - Department
  - Tags
- Search SOP
- Preview SOP
- Download SOP
- Rating dan review SOP
- Versi SOP
- History download

### 9. Profil (`/profile`)

**Fitur:**
- Informasi profil:
  - Nama, email, student ID
  - Department
  - Cluster dan Job Level
  - Level Sertifikasi
  - Avatar
- Edit profil
- Ubah password
- Progress summary
- Achievement badges
- Learning history

### 10. Learning Path Viewer (`/learning-path/:pathId`)

**Fitur:**
- Visualisasi Learning Path
- Tracks dalam Learning Path:
  - Technical Track
  - Culture Track
  - Productivity Track
- Progress per track
- Daftar kursus per track
- Prerequisites
- Estimated duration
- Navigasi ke kursus

---

## Halaman Instruktur (Instructor Pages)

### 1. Dashboard Instruktur (`/dashboard`)

**Fitur:**
- **Welcome Section** dengan quick action "Buat Kursus Baru"

- **Quick Stats:**
  - Total Kursus
  - Total Siswa
  - Rata-rata Rating
  - Diskusi Aktif

- **Readiness Index Tenaga Kerja:**
  - Indeks kesiapan tenaga kerja berdasarkan progress
  - Progress bar dengan status (Siap, Cukup Siap, Perlu Perhatian)
  - Breakdown per cluster (Operator, Leader, Supervisor, Manager, Expatriate)

- **Kompetensi yang Perlu Diperbaiki:**
  - Daftar kompetensi dengan progress rendah
  - Status (Kritis, Perhatian)
  - Jumlah siswa terpengaruh
  - Progress rata-rata

- **Statistik Lulus/Gagal:**
  - Overall statistics (Lulus, Sedang Belajar, Gagal)
  - Breakdown per cluster
  - Persentase per kategori

- **Quick Actions:**
  - Buat Kursus Baru
  - Lihat Analitik Lengkap
  - Kelola Siswa

- **Summary Stats:**
  - Total Kursus
  - Total Siswa
  - Readiness Index
  - Tingkat Kelulusan

### 2. Manajemen Kursus (`/courses`)

**Fitur:**
- Daftar semua kursus yang dibuat instruktur
- Buat kursus baru
- Edit kursus
- Hapus kursus
- Duplicate kursus
- Status kursus (Draft, Active, Archived)
- Statistik per kursus:
  - Jumlah siswa enrolled
  - Rata-rata progress
  - Completion rate
  - Rating

### 3. Detail Kursus Instruktur (`/instructor/courses/:courseId`)

**Fitur:**
- Overview kursus
- Manajemen modul dan lesson:
  - Tambah/edit/hapus modul
  - Tambah/edit/hapus lesson
  - Upload video/document
  - Set durasi
  - Reorder modul/lesson
- Manajemen konten:
  - Video lessons
  - Document lessons
  - Quiz
  - Assignment
- Statistik siswa:
  - Progress per siswa
  - Completion rate
  - Average score
- Settings kursus:
  - Visibility
  - Enrollment settings
  - Prerequisites

### 4. Manajemen Tugas (`/assignments`)

**Fitur:**
- Daftar semua tugas dari semua kursus
- Buat tugas baru
- Edit tugas
- Hapus tugas
- Filter berdasarkan kursus
- View submissions
- Grade assignments
- Berikan feedback
- Export grades

### 5. Detail Tugas (`/assignments/:assignmentId`)

**Fitur:**
- Informasi tugas
- Daftar submissions:
  - Nama siswa
  - Waktu submit
  - Status (Submitted, Graded, Late)
  - Score
- Grade submission:
  - Input score
  - Berikan feedback
  - Download attachment
- Statistics:
  - Submission rate
  - Average score
  - Distribution

### 6. Manajemen Siswa (`/students`)

**Fitur:**
- Daftar semua siswa
- Filter berdasarkan:
  - Cluster
  - Job Level
  - Department
  - Kursus
- View detail siswa:
  - Profil
  - Progress per kursus
  - Assignment submissions
  - Grades
- Export data siswa

### 7. Jadwal Training (`/training-schedule`)

**Fitur:**
- Kalender view jadwal
- Buat jadwal baru:
  - Pilih kursus
  - Set tanggal dan waktu
  - Set lokasi
  - Set tipe (Classroom, OJT, Practical)
  - Set max participants
  - Upload materials
- Edit/hapus jadwal
- View enrolled students
- Take attendance
- Update status (Scheduled, Ongoing, Completed, Cancelled)
- Export jadwal

### 8. Analitik (`/analytics`)

**Fitur:**
- **Overview Analytics:**
  - Total siswa
  - Completion rate
  - Average score
  - Engagement metrics

- **Course Analytics:**
  - Progress per kursus
  - Student engagement
  - Drop-off points
  - Time spent

- **Student Analytics:**
  - Progress per siswa
  - Performance distribution
  - At-risk students
  - Top performers

- **Cluster Analytics:**
  - Performance per cluster
  - Readiness index per cluster
  - Competency gaps

- **Charts & Graphs:**
  - Progress trends
  - Score distribution
  - Completion funnel
  - Engagement heatmap

- **Export Reports:**
  - PDF reports
  - Excel exports
  - Custom date ranges

### 9. Manajemen Forum (`/forum`)

**Fitur:**
- Daftar semua thread dari semua kursus
- Filter berdasarkan kursus
- View thread details
- Reply ke thread
- Pin/unpin thread
- Lock/unlock thread
- Delete thread/reply
- Moderate content
- Analytics:
  - Most active threads
  - Engagement metrics

### 10. Manajemen SOP (`/sop-library`)

**Fitur:**
- Daftar semua SOP
- Buat SOP baru:
  - Upload document
  - Set kategori
  - Set department
  - Add tags
  - Set version
- Edit SOP
- Archive SOP
- Version control
- View download statistics
- Manage reviews

### 11. Learning Paths (`/learning-paths`)

**Fitur:**
- Daftar Learning Paths
- Buat Learning Path baru
- Edit Learning Path
- Assign courses ke tracks
- Set prerequisites
- Assign ke siswa berdasarkan cluster/job level

---

## Halaman Admin (Admin Pages)

### 1. Dashboard Admin (`/dashboard`)

**Fitur:**
- **Welcome Section** dengan quick action "Tambah Pengguna"

- **Main Stats:**
  - Total Siswa (dengan growth percentage)
  - Total Instruktur (dengan growth)
  - Total Kursus (dengan active courses)
  - Revenue Bulan Ini (dengan growth)

- **Status Sistem:**
  - Server Uptime
  - Active Users
  - Storage Used
  - Bandwidth
  - Status indicators (good/warning/error)

- **Overview Kursus:**
  - Daftar semua kursus
  - Jumlah siswa per kursus
  - Rating per kursus

- **Aktivitas Terbaru:**
  - Log aktivitas sistem
  - User actions
  - System events

- **Peringatan:**
  - Storage warnings
  - System alerts
  - Backup status

- **Quick Actions:**
  - Export Data
  - Generate Report
  - System Maintenance

### 2. Manajemen Pengguna (`/users`)

**Fitur:**
- Daftar semua pengguna (Siswa, Instruktur, Admin)
- Filter berdasarkan:
  - Role
  - Position
  - Department
  - Cluster
  - Status
- Tambah pengguna baru:
  - Input data lengkap
  - Set role dan position
  - Set cluster dan job level
  - Assign learning path
- Edit pengguna:
  - Update profil
  - Change role
  - Update cluster/job level
  - Reassign learning path
- Hapus pengguna
- Bulk actions:
  - Bulk assign learning path
  - Bulk update cluster
  - Export users
- View user details:
  - Profil lengkap
  - Activity log
  - Progress summary

### 3. Manajemen Learning Paths (`/learning-paths`)

**Fitur:**
- Daftar semua Learning Paths
- Buat Learning Path baru:
  - Nama dan deskripsi
  - Target cluster
  - Target job level
  - Tracks (Technical, Culture, Productivity)
  - Assign courses ke tracks
  - Set prerequisites
  - Estimated duration
- Edit Learning Path
- Hapus Learning Path
- Duplicate Learning Path
- Assign Learning Path ke siswa:
  - Manual assign
  - Auto assign berdasarkan cluster/job level
  - Bulk assign
- View statistics:
  - Jumlah siswa per Learning Path
  - Average progress
  - Completion rate

### 4. Manajemen Instruktur (`/instructors`)

**Fitur:**
- Daftar semua instruktur
- Tambah instruktur baru
- Edit instruktur
- Hapus instruktur
- Assign kursus ke instruktur
- View instruktur details:
  - Profil
  - Kursus yang diajar
  - Rating
  - Total siswa
  - Performance metrics

### 5. Manajemen Siswa (`/students`)

**Fitur:**
- Daftar semua siswa
- Filter dan search advanced
- Tambah siswa baru
- Edit siswa
- Hapus siswa
- Bulk operations:
  - Bulk assign learning path
  - Bulk update cluster
  - Bulk export
- View detail siswa:
  - Profil lengkap
  - Learning path
  - Progress semua kursus
  - Certification level
  - Activity history
- Assign learning path
- Update certification level

### 6. Manajemen Kursus (`/courses` - Admin view)

**Fitur:**
- Daftar semua kursus dari semua instruktur
- Filter berdasarkan:
  - Instruktur
  - Status
  - Kategori
- View course details
- Approve/reject kursus
- Archive kursus
- Delete kursus
- Statistics per kursus
- Export course data

### 7. Manajemen Tugas & Quiz (`/assignments` - Admin view)

**Fitur:**
- Daftar semua tugas dan quiz
- Filter berdasarkan:
  - Kursus
  - Instruktur
  - Type (Assignment/Quiz)
- View details
- Statistics:
  - Submission rate
  - Average score
  - Distribution
- Export data

### 8. Analitik Admin (`/analytics`)

**Fitur:**
- **System-wide Analytics:**
  - Total users
  - Active users
  - Course completion rates
  - Overall readiness index

- **User Analytics:**
  - Growth trends
  - User distribution by role/cluster
  - Engagement metrics
  - Retention rates

- **Course Analytics:**
  - Popular courses
  - Completion rates
  - Average ratings
  - Revenue per course

- **Learning Path Analytics:**
  - Progress per Learning Path
  - Completion rates
  - Cluster performance
  - Competency gaps

- **Performance Metrics:**
  - System performance
  - Server metrics
  - Storage usage
  - Bandwidth usage

- **Reports:**
  - Generate custom reports
  - Scheduled reports
  - Export options (PDF, Excel, CSV)

### 9. Audit Trail (`/audit-trail`)

**Fitur:**
- Log semua aktivitas sistem
- Filter berdasarkan:
  - User
  - Action type
  - Date range
  - Module/feature
- View detail log:
  - User yang melakukan action
  - Waktu
  - Action details
  - Before/after values
- Search logs
- Export audit logs
- Retention settings

### 10. Pengaturan Sistem (`/settings`)

**Fitur:**
- **General Settings:**
  - Site name
  - Logo
  - Theme settings
  - Language settings

- **User Settings:**
  - Registration settings
  - Role permissions
  - Default settings

- **Course Settings:**
  - Default course settings
  - Enrollment rules
  - Completion criteria

- **Learning Path Settings:**
  - Auto-assignment rules
  - Prerequisites rules
  - Certification rules

- **Notification Settings:**
  - Email notifications
  - In-app notifications
  - Notification templates

- **System Settings:**
  - Storage settings
  - Backup settings
  - Security settings
  - API settings

- **Maintenance:**
  - System maintenance mode
  - Database backup
  - Cache management
  - Log management

---

## Sistem Autentikasi

Sistem autentikasi mendukung login dan register dengan role-based access control. Terdapat 3 role utama: **student** (siswa/karyawan), **instructor** (instruktur), dan **admin** (administrator). Selain itu, terdapat position/jabatan seperti manager, hrd, dan supervisor. Setiap user memiliki atribut seperti cluster, job level, certification level, dan learning path yang di-assign untuk personalisasi pembelajaran.

---

## Learning Path System

### Konsep Learning Path

Learning Path adalah jalur pembelajaran terstruktur yang di-assign ke siswa berdasarkan:
- **Cluster**: Operator, Leader, Supervisor, Manager, Expatriate
- **Job Level**: Basic, Intermediate, Advanced

### Struktur Learning Path

Setiap Learning Path terdiri dari:
1. **Tracks** (Jalur):
   - **Technical Track** - Kompetensi teknis
   - **Culture Track** - Budaya perusahaan
   - **Productivity Track** - Produktivitas

2. **Courses** - Kursus yang di-assign ke setiap track

3. **Prerequisites** - Learning Path yang harus diselesaikan terlebih dahulu

### Auto-Assignment

Sistem dapat auto-assign Learning Path berdasarkan:
- Cluster user
- Job level user
- Department (opsional)

### Progress Tracking

- Progress per track
- Progress keseluruhan Learning Path
- Completion status per course
- Certification level update

---

## Deployment

Aplikasi di-deploy menggunakan Docker dan Caddy sebagai reverse proxy dengan SSL otomatis.

---

## Pengembangan

Proyek menggunakan React dengan TypeScript dan Tailwind CSS. Untuk setup development, install dependencies dan jalankan development server. Struktur proyek terorganisir berdasarkan komponen per role (admin, instructor, student) dan shared components.

---

## Catatan Penting

Saat ini sistem menggunakan mock data untuk development. Untuk production, perlu integrasi dengan backend API, database, dan file storage. Sistem dirancang dengan mempertimbangkan aspek keamanan, performa, dan skalabilitas.

---

## Support & Maintenance

Sistem mendukung logging, backup reguler, dan update berkala untuk memastikan keamanan dan performa optimal.

---

## Kontak & Dokumentasi Tambahan

- **🌐 Live Website**: [https://learningsystem.neuraworks.id](https://learningsystem.neuraworks.id)
- **📧 Email**: [athaillah@neuraworks.id](mailto:athaillah@neuraworks.id)
- **🔑 Demo Credentials**: `DEMO_CREDENTIALS.md`

---

**Dokumentasi ini dibuat untuk memberikan overview lengkap tentang sistem E-Learning.**

**Jika Anda tertarik dengan proyek ini atau memiliki pertanyaan, silakan hubungi saya melalui email: [athaillah@neuraworks.id](mailto:athaillah@neuraworks.id)**

