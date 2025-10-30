# 📱 Laporan Mobile App Development (React Native)

## 🧩 Tugas 1  
**Definisi Mobile Development**  
Proses membuat aplikasi yang berjalan di perangkat seluler atau smartphone, baik untuk sistem operasi **Android** maupun **iOS**.

---

## ⚖️ Tugas 2 – Perbandingan Web vs Mobile Development  

| Aspek | Web Development | Mobile App Development |
|-------|------------------|------------------------|
| **Target Eksekusi** | Browser (multiplatform) | Sistem operasi (Android & iOS) |
| **Distribusi** | Online melalui URL langsung | Melalui Play Store / App Store |
| **Akses Hardware** | Terbatas | Luas dan mendalam (GPS, kamera, penyimpanan) |
| **Implikasi Praktis** | Cepat diakses, mudah di-update | Lebih powerful, bisa offline, tapi butuh instalasi |

---

## 🔍 Tugas 3 – Discovery & Requirement Phase  

Tahap awal pengembangan aplikasi yang bertujuan **memahami masalah, menentukan kebutuhan, dan merancang arah pengembangan** sebelum menulis kode.

### 🔹 Discovery Phase
Menemukan apa yang benar-benar dibutuhkan pengguna dan bisnis.  
**Kegiatan utama:**
- Analisis masalah pengguna  
- Penelitian pasar dan kompetitor  
- Identifikasi target pengguna  
- Studi platform utama (Android/iOS)

### 🔹 Requirement Phase
Mengubah hasil riset menjadi daftar kebutuhan yang jelas untuk developer.  
**Jenis kebutuhan:**
- **Fungsional:** fitur yang harus ada  
- **Non-fungsional:** performa, keamanan, kemudahan penggunaan  

**Menentukan Target Platform:**
1. Dominasi pengguna  
2. Budget dan waktu pengembangan  
3. Tujuan bisnis  

**Menentukan kebutuhan offline/online** berdasarkan kebutuhan pengguna dan kondisi penggunaan.

---

## 🏗️ Tugas 4 – Perancangan Arsitektur & Teknologi  

Tahapan setelah Discovery & Requirement, dengan tujuan **merancang fondasi teknis aplikasi**.

### 🔹 Perancangan Arsitektur
- Menentukan struktur sistem dan alur aplikasi  
- Memilih teknologi, library, dan framework  
- Merancang pemisahan tanggung jawab antar UI  
- Menentukan strategi *state management* dan navigasi

### 🔹 Perancangan Teknologi
Meliputi: UI library, navigasi, state management, data storage, networking, dan authentication.

### 🔹 Pentingnya State Management
- Mengatur dan menyimpan data yang berubah seiring waktu  
- Mempengaruhi alur data, performa, struktur kode, dan dukungan mode offline  

### 🔹 Pentingnya Navigasi
- Menentukan alur pergerakan pengguna dalam aplikasi  
- Berpengaruh pada struktur folder, aliran data antar halaman, dan UX flow  

---

## ⚙️ Tugas 5 – Native vs Hybrid Development  

| Aspek | Native Development | Hybrid Development |
|--------|--------------------|--------------------|
| **Deskripsi** | Menggunakan bahasa & alat resmi untuk Android/iOS | Bisa dibuka di web dan aplikasi |
| **Kelebihan** | Performa tinggi, stabil, UX optimal | Efisien waktu & biaya, fleksibel lintas platform |
| **Kekurangan** | Biaya & waktu besar, butuh 2 tim | Performa lebih rendah, akses hardware terbatas |
| **Pemilihan Berdasarkan:** | Tujuan aplikasi, budget, waktu, kebutuhan pengguna, dan kebutuhan perangkat keras |

---

## 🔄 Tugas 6 – Cross-Platform Native Development  

**Definisi:**  
Pendekatan di mana satu basis kode dapat digunakan untuk membuat aplikasi di berbagai platform (Android & iOS).

| Aspek | Cross-Platform | Native |
|-------|----------------|--------|
| **Basis Kode** | Satu codebase untuk banyak platform | Kode terpisah per OS |
| **Performa** | Hampir sebanding dengan native | Performa optimal |
| **Akses Hardware** | Kadang perlu *bridge* tambahan | Akses langsung |
| **Biaya & Waktu** | Efisien (1 tim, 1 codebase) | Mahal & lama |
| **UI/UX Konsistensi** | Kadang tidak 100% sama | Sesuai guideline OS |
| **Pemeliharaan** | Mudah (1 update untuk semua) | Kompleks (update per OS) |

---

## ⚛️ Tugas 7 – React Native  

| Poin Utama | Penjelasan |
|-------------|------------|
| **React.js** | Library untuk UI berbasis web |
| **React Native** | Framework untuk UI aplikasi mobile native |
| **Sintaks Dasar** | Sama dalam konsep (komponen, props, state), berbeda dalam elemen UI |
| **Styling** | React.js: CSS, React Native: `StyleSheet` berbasis JS |
| **Tujuan Akhir** | React.js → Web, React Native → Mobile |

React Native menempati posisi **“cross-platform framework”** sejajar dengan Flutter (Dart), Xamarin (.NET/C#), dan Kotlin Multiplatform.

---

## 🚧 Tugas 8 – Tantangan & Solusi  

**Tantangan Mobile Development:**  
Lebih rumit dibanding web karena fragmentasi dan perbedaan platform.

**Solusi dengan React Native:**  
Menjembatani kesenjangan tersebut dengan **satu codebase lintas platform** yang tetap menghasilkan aplikasi native dengan efisiensi tinggi.

---

## 🧪 Tugas 9 – Testing, Build, Signing, dan Release  

### 🔹 1. Testing
Menguji fungsi dan tampilan aplikasi:
- **Unit Test:** logika (Jest)  
- **Integration Test:** interaksi antar komponen (Detox/Appium)  
- **UI Test:** di emulator/device nyata  

### 🔹 2. Build
Mengubah kode menjadi aplikasi siap instal:  
- **Android:** `.apk` / `.aab`  
- **iOS:** `.ipa`  
- Perintah:  
  ```bash
  ./gradlew assembleRelease
  # atau melalui Xcode → Product → Archive
### 🔹 3. Signing
Memberi identitas resmi aplikasi:
- **Android:** `file` / `.keystore`
- **iOS:** Apple Developer Certificate & Provisioning Profile
### 🔹 4. Release
Distribusi ke pengguna:
- **Google Play Console:** upload .aab
- **App Store Connect:** upload .ipa
Kesimpulan:
Testing memastikan kualitas → Build menyiapkan paket → Signing membuat resmi → Release mendistribusikan ke publik.

## 🚀 Tugas 10 – Mengapa React Native Populer
React Native populer karena menggabungkan efisiensi lintas platform dengan performa mendekati native.
### 🔹 Keunggulan Utama:
- **Satu Codebase:** Android & iOS sekaligus
- **Performa Tinggi:** menggunakan komponen native
- **Hot Reload:** perubahan kode langsung terlihat
- **Komunitas Kuat:** banyak library dan dukungan
- **Integrasi Modern:** bisa pakai Redux, Firebase, Node.js
- **Mudah Dirawat:** cukup update satu codebase

### 🔹 Kesimpulan:

React Native menawarkan efisiensi, performa, dan fleksibilitas tinggi, cocok untuk startup, tim kecil, dan proyek yang ingin cepat hadir di dua platform tanpa mengorbankan kualitas.