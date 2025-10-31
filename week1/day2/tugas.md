# 📱 Ringkasan Konsep & Setup React Native CLI v0.80

## 1. Konsep Dasar React Native
React Native adalah framework **cross-platform** yang memungkinkan developer menulis kode **JavaScript/TypeScript** untuk membuat aplikasi **Android dan iOS** dari satu basis kode.  
Berbeda dengan **React untuk web**, yang merender ke DOM melalui HTML dan CSS, React Native menggunakan **komponen native** seperti `<View>`, `<Text>`, dan `<Image>` yang langsung diterjemahkan ke elemen UI asli perangkat.

### 🔹 Peran New Architecture (v0.80)
React Native versi 0.80 memperkenalkan **New Architecture** yang terdiri dari:
- **Fabric Renderer** – Rendering lebih cepat dan sinkron dengan native UI.  
- **TurboModules** – Modul native dimuat secara **lazy loading**, meningkatkan startup time.  
- **JSI (JavaScript Interface)** – Menghubungkan JavaScript dengan kode native tanpa perlu bridge lama.  

💡 Hasilnya: **performa lebih tinggi, latency lebih rendah**, dan integrasi native yang lebih efisien.

---

## 2. React Native CLI vs Expo

| Aspek | React Native CLI | Expo |
|-------|------------------|------|
| **Arsitektur** | Akses penuh ke native modules dan konfigurasi Gradle/Xcode | Menggunakan managed workflow (terkontrol oleh Expo SDK) |
| **Proses Build** | Build langsung dengan Android Studio / Xcode | Build melalui Expo Go atau EAS Build |
| **Kelebihan** | Bebas integrasi library native | Setup sangat cepat dan cocok untuk prototipe |
| **Kekurangan** | Setup lebih kompleks | Terbatas dalam penggunaan native module custom |

**Contoh Skenario:**
- Gunakan **Expo** → untuk aplikasi ringan, edukasi, atau prototipe cepat.  
- Gunakan **React Native CLI** → untuk aplikasi produksi yang butuh akses ke **native module (kamera, Bluetooth, background task, dll.)**.

---

## 3. Komponen Penting Android SDK untuk React Native

| Komponen | Fungsi | Dampak jika tidak ada |
|-----------|---------|-----------------------|
| **SDK Platforms (android-35)** | Berisi API & libraries untuk Android versi tertentu | App tidak bisa dikompilasi karena target platform hilang |
| **Build Tools (35.0.0)** | Menyediakan alat untuk proses build (aapt, dx, zipalign) | Gagal saat `gradlew assembleDebug` |
| **Platform Tools** | Termasuk `adb` (Android Debug Bridge) untuk komunikasi device/emulator | Emulator tidak terdeteksi di VS Code atau terminal |

💡 Semua komponen ini **harus sinkron** dengan versi React Native agar environment stabil.

---

## 4. Prasyarat React Native CLI v0.80

| Tools | Fungsi | Alasan Penting |
|--------|--------|----------------|
| **Node.js** | Menjalankan bundler & runtime JavaScript | Menghubungkan kode JS dengan JSI bridge |
| **Watchman** | Mendeteksi perubahan file | Mempercepat hot reload di development |
| **Yarn** | Package manager alternatif untuk npm | Dependency management yang lebih cepat dan konsisten |

🔗 Kombinasi tiga tools ini memastikan React Native dapat menjalankan JavaScript dengan lancar ke native runtime Android/iOS.

---

## 5. Struktur Folder React Native CLI

myApp/
├── android/ # Proyek native Android (Gradle, build config)
├── ios/ # Proyek native iOS (Xcode project)
├── node_modules/ # Dependency npm/yarn
├── App.js # Entry point utama aplikasi React Native
├── package.json # Informasi dan dependensi proyek
├── metro.config.js # Konfigurasi Metro bundler
└── index.js # File awal yang mendaftarkan root component

markdown
Copy code

### 🧩 Penjelasan:
- **android/** dan **ios/** → Menyimpan konfigurasi & kode native masing-masing platform.  
- **App.js** → Titik masuk React Component utama.  
- **metro.config.js** → Mengatur bagaimana bundler membaca dan meng-compile file JS.  

Struktur ini mendukung **pengembangan lintas platform** — logika aplikasi tetap satu (JavaScript), tetapi tetap bisa memanggil fungsi native lewat `android/` dan `ios/`.

---

## 🏁 Kesimpulan
React Native menjadi pilihan populer karena mampu menggabungkan:
- **Efisiensi pengembangan cross-platform**  
- **Performa native** berkat New Architecture (JSI, Fabric, TurboModules)  
- **Kebebasan arsitektur**, baik melalui **React Native CLI** maupun **Expo**  
- **Integrasi penuh dengan Android SDK tools** untuk proses build dan debugging.