# Demo Credentials - SKEMA LMS

Dokumen ini berisi daftar lengkap email dan password untuk semua user demo dalam sistem SKEMA LMS.

## Informasi Login

**Password untuk semua user:** `password`

**Catatan:** 
- Pilih role yang sesuai saat login (Student/Instructor/Admin)
- Email dan role harus match untuk bisa login
- Position (Manager/HRD/Supervisor) diatur oleh Admin dan tidak mempengaruhi login

---

## 📋 Daftar User Demo

### 🔵 ADMIN & INSTRUCTOR

| No | Nama | Email | Role | Password | Keterangan |
|---|---|---|---|---|---|
| 1 | Budi Santoso | `budi.santoso@admin.com` | Admin | `password` | Admin utama - akses penuh |
| 2 | Li Wei Ming | `li.weiming@instructor.com` | Instructor | `password` | Instruktur Training & Development |

---

### 👷 OPERATOR (Basic Level)

| No | Nama | Email | Role | Password | Cluster | Cert Level | Learning Path | Department |
|---|---|---|---|---|---|---|---|---|
| 1 | Ahmad Putra | `ahmad.putra@student.com` | Student | `password` | Operator | 1 | lp-operator-basic | Produksi |
| 2 | Operator Baru | `operator.new@factory.com` | Student | `password` | Operator | 0 | lp-operator-basic | Produksi |
| 3 | Rudi Hartono | `rudi.hartono@factory.com` | Student | `password` | Operator | 1 | lp-operator-basic | Produksi Line 1 |
| 4 | Sari Indah | `sari.indah@factory.com` | Student | `password` | Operator | 0 | lp-operator-basic | Produksi Line 2 |
| 5 | Bambang Surya | `bambang.surya@factory.com` | Student | `password` | Operator | 2 | lp-operator-basic | Quality Control |
| 6 | Dedi Kurniawan | `dedi.kurniawan@factory.com` | Student | `password` | Operator | 1 | lp-operator-basic | Produksi Line 3 |
| 7 | Indah Permata | `indah.permata@factory.com` | Student | `password` | Operator | 0 | lp-operator-basic | Assembly |

**Testing Skenario:**
- ✅ User baru (Cert Level 0) - belum mulai belajar
- ✅ User sedang belajar (Cert Level 1-2)
- ✅ Progress tracking per track

---

### 👔 LEADER / FOREMAN (Intermediate Level)

| No | Nama | Email | Role | Password | Cluster | Cert Level | Learning Path | Department |
|---|---|---|---|---|---|---|---|---|
| 1 | Bambang Wijaya | `leader1@factory.com` | Student | `password` | Leader | 3 | lp-leader-intermediate | Production Line A |
| 2 | Dewi Sari | `leader2@factory.com` | Student | `password` | Leader | 2 | lp-leader-intermediate | Production Line B |
| 3 | Ahmad Fauzi | `ahmad.fauzi@factory.com` | Student | `password` | Leader | 3 | lp-leader-intermediate | Production Line C |
| 4 | Maya Sari | `maya.sari@factory.com` | Student | `password` | Leader | 2 | lp-leader-intermediate | Packaging |

**Testing Skenario:**
- ✅ Intermediate level learning path
- ✅ Technical + Culture + Productivity tracks
- ✅ Certification progress tracking

---

### 👨‍💼 SUPERVISOR / PIC TEKNIS (Advanced Level)

| No | Nama | Email | Role | Password | Position | Cluster | Cert Level | Learning Path | Department |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Supervisor Production A | `supervisor1@factory.com` | Student | `password` | Supervisor | Supervisor | 4 | lp-supervisor-advanced | Production Line A |
| 2 | Supervisor Production B | `supervisor2@factory.com` | Student | `password` | Supervisor | Supervisor | 4 | lp-supervisor-advanced | Production Line B |
| 3 | Supervisor Quality Control | `supervisor3@factory.com` | Student | `password` | Supervisor | Supervisor | 4 | lp-supervisor-advanced | Quality Control |
| 4 | Agus Prasetyo | `agus.prasetyo@factory.com` | Student | `password` | Supervisor | Supervisor | 4 | lp-supervisor-advanced | Maintenance |
| 5 | Ratna Dewi | `ratna.dewi@factory.com` | Student | `password` | Supervisor | Supervisor | 5 | lp-supervisor-advanced | Warehouse |

**Testing Skenario:**
- ✅ Advanced level learning path
- ✅ Supervisor dashboard
- ✅ Team management features
- ✅ Certification Level 5 (expert)

---

### 🎯 MANAGER / HEAD DEPT

| No | Nama | Email | Role | Password | Position | Cluster | Cert Level | Learning Path | Department |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Zhang Wei | `manager@factory.com` | Student | `password` | Manager | Manager | 5 | lp-manager-advanced | Production Management |
| 2 | Siti Nurhaliza | `hrd@factory.com` | Student | `password` | HRD | Manager | 4 | lp-manager-advanced | Human Resources |
| 3 | Joko Widodo | `joko.widodo@factory.com` | Student | `password` | Manager | Manager | 5 | lp-manager-advanced | Operations |
| 4 | Sri Mulyani | `sri.mulyani@factory.com` | Student | `password` | HRD | Manager | 4 | lp-manager-advanced | Human Resources |

**Testing Skenario:**
- ✅ Manager dashboard
- ✅ HRD dashboard
- ✅ Advanced learning path
- ✅ Workforce analytics

---

### 🌏 EXPATRIATE (China Engineers)

| No | Nama | Email | Role | Password | Cluster | Cert Level | Learning Path | Department |
|---|---|---|---|---|---|---|---|---|
| 1 | Wang Li | `wang.li@expatriate.com` | Student | `password` | Expatriate | 3 | lp-expatriate | Engineering |
| 2 | Chen Wei | `chen.wei@expatriate.com` | Student | `password` | Expatriate | 2 | lp-expatriate | Engineering |
| 3 | Liu Fang | `liu.fang@expatriate.com` | Student | `password` | Expatriate | 4 | lp-expatriate | Technical Support |
| 4 | Zhang Ming | `zhang.ming@expatriate.com` | Student | `password` | Expatriate | 1 | lp-expatriate | Quality Assurance |

**Testing Skenario:**
- ✅ Expatriate learning path (Culture Track khusus)
- ✅ Multi-language support (Mandarin/English)
- ✅ Cross-cultural training modules

---

## 🎯 Quick Testing Guide

### Testing Learning Path per Cluster

1. **Operator Basic**
   - Email: `ahmad.putra@student.com`
   - Role: Student
   - Expected: Learning Path Operator (Basic) dengan 3 tracks

2. **Leader Intermediate**
   - Email: `leader1@factory.com`
   - Role: Student
   - Expected: Learning Path Leader/Foreman (Intermediate)

3. **Supervisor Advanced**
   - Email: `supervisor1@factory.com`
   - Role: Student
   - Expected: Learning Path Supervisor/PIC (Advanced)

4. **Manager Advanced**
   - Email: `manager@factory.com`
   - Role: Student
   - Expected: Learning Path Manager/Head Dept (Advanced)

5. **Expatriate**
   - Email: `wang.li@expatriate.com`
   - Role: Student
   - Expected: Learning Path Expatriate dengan Culture Track khusus

### Testing Admin Features

1. **Admin Login**
   - Email: `budi.santoso@admin.com`
   - Role: Admin
   - Features: User Management, Learning Path Management, Analytics

2. **User Management Testing**
   - Filter by Cluster (Operator, Leader, Supervisor, Manager, Expatriate)
   - Filter by Certification Level (0-5)
   - Assign Learning Path to users
   - Edit user properties (cluster, job level, expatriate status)

### Testing Dashboard Features

1. **Student Dashboard**
   - Login sebagai student → Lihat Learning Path section
   - Progress tracking per track
   - Courses dari learning path

2. **Manager Dashboard**
   - Login sebagai manager → Manager-specific dashboard
   - Workforce analytics

3. **HRD Dashboard**
   - Login sebagai HRD → HRD-specific dashboard
   - Training management

4. **Supervisor Dashboard**
   - Login sebagai supervisor → Supervisor dashboard
   - Team management

---

## 📊 Summary Statistics

| Cluster | Total Users | Certification Levels |
|---|---|---|
| **Operator** | 7 users | Level 0-2 |
| **Leader/Foreman** | 4 users | Level 2-3 |
| **Supervisor** | 5 users | Level 4-5 |
| **Manager** | 4 users | Level 4-5 |
| **Expatriate** | 4 users | Level 1-4 |
| **Admin** | 1 user | - |
| **Instructor** | 1 user | - |
| **TOTAL** | **26 users** | - |

---

## 🔐 Security Note

**⚠️ IMPORTANT:** 
- Ini adalah credentials untuk **DEMO/TESTING** saja
- Jangan gunakan credentials ini di production
- Password sama untuk semua user untuk kemudahan testing
- Di production, setiap user harus memiliki password yang unik dan aman

---

## 📝 Notes

- Semua user memiliki learning path yang sesuai dengan cluster mereka
- Certification level menunjukkan progress user dalam learning path
- Position (Manager/HRD/Supervisor) menentukan dashboard yang ditampilkan
- Expatriate users memiliki learning path khusus dengan Culture Track berbeda

---

**Last Updated:** 2024-03-18
**Version:** 1.0

