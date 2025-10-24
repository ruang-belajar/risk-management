# OCTAVE
## Pengertian OCTAVE dalam Manajemen Risiko

**OCTAVE (Operationally Critical Threat, Asset, and Vulnerability Evaluation)**  
adalah **kerangka kerja (framework)** untuk **manajemen risiko keamanan informasi** yang berfokus pada **identifikasi aset-aset penting organisasi, ancaman terhadapnya, dan kerentanan yang ada**.

Metode ini **dikembangkan oleh CERT Coordination Center (CERT/CC)** di Carnegie Mellon University pada akhir 1990-an dan digunakan secara luas untuk **penilaian risiko TI dan keamanan informasi.**

---

## 🧩 Tujuan OCTAVE

Tujuan utama dari OCTAVE adalah:

- Mengidentifikasi **aset informasi kritikal** organisasi.
    
- Menentukan **ancaman dan kerentanan** yang dapat mempengaruhi aset tersebut.
    
- Menilai **tingkat risiko** terhadap aset informasi.
    
- Menyusun **strategi mitigasi dan rencana keamanan informasi** yang terukur.
    

---

## ⚙️ Tiga Fase Utama OCTAVE

1. **Phase 1: Identifikasi Aset dan Ancaman (Build Asset-Based Threat Profiles)**
    
    - Identifikasi aset penting (data, sistem, proses bisnis).
        
    - Tentukan ancaman terhadap aset-aset tersebut.
        
    - Klasifikasikan dampak jika ancaman terjadi (misalnya: finansial, reputasi, hukum).
        
2. **Phase 2: Identifikasi Kerentanan (Identify Infrastructure Vulnerabilities)**
    
    - Lakukan analisis terhadap sistem TI dan infrastruktur.
        
    - Temukan kelemahan pada kebijakan, proses, atau kontrol teknis.
        
    - Dokumentasikan risiko yang muncul akibat kelemahan ini.
        
3. **Phase 3: Analisis Risiko dan Strategi Mitigasi (Develop Security Strategy and Plans)**
    
    - Menilai tingkat risiko berdasarkan probabilitas dan dampaknya.
        
    - Prioritaskan risiko yang paling signifikan.
        
    - Rancang strategi pengendalian (control measures) dan rencana aksi mitigasi.
        

---

## 📊 Hasil (Output) dari OCTAVE

- **Profil risiko organisasi**, yang menggambarkan risiko terbesar bagi aset informasi.
    
- **Rencana mitigasi risiko**, lengkap dengan tindakan pencegahan dan respons.
    
- **Strategi keamanan informasi organisasi** yang disesuaikan dengan konteks bisnis.
    

---

## 💡 Keunggulan OCTAVE

- Pendekatan **berbasis organisasi**, bukan hanya teknis.
    
- Dapat diterapkan oleh **tim internal organisasi**, tanpa perlu konsultan eksternal.
    
- Menyelaraskan **kebutuhan bisnis** dengan **pengamanan informasi**.
    

---

## 🧠 Versi dan Varian OCTAVE

1. **OCTAVE Original** – untuk organisasi besar dengan sumber daya lengkap.
    
2. **OCTAVE-S (Simplified)** – versi lebih sederhana untuk organisasi kecil/menengah.
    
3. **OCTAVE Allegro** – versi terbaru dan lebih ringan, fokus pada **informasi dan konteks risiko**, bukan infrastruktur.
    

---

## 📘 Contoh Penerapan Singkat

Misalnya pada perusahaan pengembang perangkat lunak:

1. **Phase 1:** Identifikasi bahwa _source code repository_ adalah aset penting.
    
2. **Phase 2:** Temukan bahwa akses ke repository tidak menggunakan MFA → kerentanan.
    
3. **Phase 3:** Risiko pencurian kode sumber tinggi → mitigasi dengan penerapan MFA, audit log, dan pelatihan keamanan.
    
---

## 🧱 Kasus Studi: Proyek Pengembangan Aplikasi E-Commerce PT DigitalMart

### 📌 Latar Belakang

PT DigitalMart sedang mengembangkan aplikasi e-commerce berbasis web dan mobile.  
Tujuannya adalah untuk menyediakan layanan jual beli online dengan transaksi kartu kredit, dompet digital, dan integrasi API pihak ketiga.

Manajemen ingin menilai **risiko keamanan informasi** agar proyek berjalan aman dan sesuai standar ISO 27001.

---

## ⚙️ Langkah-Langkah Penerapan OCTAVE

---

### 🧩 Phase 1 – Identifikasi Aset dan Ancaman

**Tujuan:** Mengetahui aset informasi penting dan ancaman terhadapnya.

#### 🔹 1. Identifikasi Aset Kritis

|No|Aset Informasi|Kepemilikan|Nilai/Kritisitas|
|---|---|---|---|
|1|Database pengguna (data pribadi & transaksi)|Tim Database|Sangat tinggi|
|2|Source code aplikasi e-commerce|Tim Developer|Tinggi|
|3|Server API pembayaran|Tim Infrastruktur|Sangat tinggi|
|4|Kredensial admin (username & password)|Tim Keamanan|Tinggi|
|5|Dokumentasi proyek dan repositori Git|Tim Project|Sedang|

#### 🔹 2. Identifikasi Ancaman

|Aset|Ancaman|Dampak|
|---|---|---|
|Database pengguna|Serangan SQL injection, pencurian data|Pelanggaran privasi, sanksi hukum, reputasi buruk|
|Source code|Akses tidak sah atau kebocoran|Kehilangan keunggulan kompetitif|
|Server API|DDoS, spoofing transaksi|Gangguan operasional, kerugian finansial|
|Kredensial admin|Phishing, brute force|Eskalasi hak akses|
|Dokumentasi proyek|Kebocoran perencanaan|Risiko keamanan proyek|

---

### 🧠 Phase 2 – Identifikasi Kerentanan

**Tujuan:** Menemukan kelemahan yang dapat dieksploitasi ancaman.

#### 🔹 1. Temuan Kerentanan

|Area|Kerentanan yang Ditemukan|Penyebab|
|---|---|---|
|Database|Tidak ada input validation pada beberapa modul|Kurangnya uji keamanan (security testing)|
|Source code|Tidak ada mekanisme version control terproteksi (Git publik)|Konfigurasi repositori salah|
|Server|Tidak ada IDS/IPS|Infrastruktur belum lengkap|
|Kredensial|Password disimpan plaintext di file konfigurasi|Tidak ada kebijakan keamanan developer|
|Dokumentasi|File dibagikan via email tanpa enkripsi|Tidak ada kebijakan kontrol dokumen|

---

### 📊 Phase 3 – Analisis Risiko dan Strategi Mitigasi

**Tujuan:** Mengukur risiko dan menentukan langkah mitigasi.

#### 🔹 1. Penilaian Risiko

|Aset|Dampak|Probabilitas|Level Risiko|Prioritas|
|---|---|---|---|---|
|Database pengguna|5 (sangat tinggi)|4 (tinggi)|**20 (Ekstrem)**|1|
|Source code|4|3|12 (Tinggi)|2|
|Server API|4|3|12 (Tinggi)|3|
|Kredensial admin|4|2|8 (Sedang)|4|
|Dokumentasi|3|2|6 (Sedang)|5|

#### 🔹 2. Rencana Mitigasi

|Risiko|Strategi Mitigasi|Tanggung Jawab|
|---|---|---|
|Kebocoran database|Implementasi _input validation_, _parameterized query_, enkripsi data sensitif|Tim Developer|
|Pencurian source code|Gunakan repositori privat dengan _access control list_|Tim DevOps|
|Serangan API|Tambah WAF, rate-limiting, dan autentikasi API key|Tim Infrastruktur|
|Penyalahgunaan kredensial|Terapkan MFA dan rotasi password|Tim Keamanan|
|Kebocoran dokumen proyek|Gunakan sistem file sharing terenkripsi (mis. SharePoint)|Tim Project|

---

### 📈 Output Akhir (Deliverables OCTAVE)

1. **Dokumen Profil Risiko Keamanan Informasi PT DigitalMart.**
    
2. **Daftar prioritas mitigasi risiko dan rencana implementasi keamanan.**
    
3. **Rencana pelatihan kesadaran keamanan (security awareness) bagi developer.**
    
4. **Kebijakan pengelolaan aset informasi dan kontrol akses.**
    

---

### 🧭 Ringkasan Hasil

- Ditemukan 5 aset kritikal.
    
- 3 risiko dikategorikan **tinggi sampai ekstrem**, terutama terkait database dan source code.
    
- Strategi mitigasi fokus pada **kontrol akses, enkripsi, dan pengamanan proses pengembangan software**.
    
