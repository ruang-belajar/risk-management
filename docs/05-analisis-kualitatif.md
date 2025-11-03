# METODE ANALISIS RISIKO KUALITATIF

## 1. Pendahuluan

Setelah risiko diidentifikasi, langkah berikutnya adalah **analisis risiko**. Analisis bertujuan untuk menilai **tingkat risiko** berdasarkan dua faktor utama:
1. **Probabilitas (Likelihood)** → seberapa besar kemungkinan risiko terjadi.    
2. **Dampak (Impact/Consequence)** → seberapa besar konsekuensi yang ditimbulkan jika risiko terjadi.
    
Analisis risiko bisa dilakukan dengan dua pendekatan:
- **Kualitatif** → menggunakan penilaian deskriptif (low, medium, high).    
- **Kuantitatif** → menggunakan data numerik, probabilitas statistik, simulasi.
    
Pada bab ini dibahas pendekatan **kualitatif** karena paling sering digunakan di banyak organisasi.

---
## 2. Tujuan Analisis Kualitatif

1. Menentukan **tingkat prioritas** risiko.    
2. Memberikan gambaran cepat tanpa membutuhkan data numerik yang rumit.    
3. Membantu manajemen dalam pengambilan keputusan awal.    
4. Menjadi dasar untuk analisis kuantitatif (jika diperlukan).
    
---
## 3. Skala Penilaian Risiko
### 3.1 Probabilitas (Likelihood)

Menggambarkan seberapa besar peluang terjadinya suatu risiko. Biasanya dinilai dalam 5 tingkat, misalnya:

| Skor | Deskripsi     | Contoh                             |
| ---- | ------------- | ---------------------------------- |
| 1    | Sangat Jarang | Terjadi sekali dalam 10 tahun      |
| 2    | Jarang        | Terjadi sekali dalam 5 tahun       |
| 3    | Mungkin       | Terjadi sekali per tahun           |
| 4    | Sering        | Terjadi beberapa kali per tahun    |
| 5    | Sangat Sering | Terjadi hampir setiap bulan/minggu |

### 3.2. Dampak (Consequence/Impact)

Menunjukkan tingkat konsekuensi jika risiko benar-benar terjadi:

| Skor | Deskripsi        | Contoh                                 |
| ---- | ---------------- | -------------------------------------- |
| 1    | Tidak Signifikan | Gangguan kecil, tidak berdampak serius |
| 2    | Minor            | Kerugian kecil, perbaikan cepat        |
| 3    | Moderat          | Kerugian sedang, gangguan operasional  |
| 4    | Major            | Kerugian besar, downtime panjang       |
| 5    | Katastropik      | Cedera fatal, kerugian sangat besar    |

> Baik *likelihood* ataupun *impact*, batasan-batasannya ini tentu adalah sesuatu yang ditentukan dan disepakati sesuai dengan konteks, sehingga setiap orang membaca dan membuat dokumen _risk register_ bisa memiliki pemahaman yang sama.

---

## 4. Risk Matrix (Matriks Risiko)

Matriks risiko adalah alat visual untuk mengkombinasikan **probabilitas** dan **dampak**, lalu menentukan tingkat risiko:
### 4.1. Langkah-langkah Membuat Matrik Risiko

1. **Tentukan tujuan** — untuk proyek, unit, atau organisasi? (mis. proyek IT, operasional pabrik).
    
2. **Pilih ukuran matriks** — umum: **3×3**, **4×4**, atau **5×5**. (5×5 memberi detail paling baik).
    
3. **Definisikan skala untuk Likelihood & Impact**  
    Contoh 5-level:
    
    - 1 = Sangat kecil / sangat tidak mungkin
        
    - 2 = Kecil / jarang
        
    - 3 = Sedang / mungkin
        
    - 4 = Besar / sering
        
    - 5 = Sangat besar / hampir pasti  
        Beri definisi konkret tiap level (frekuensi, contoh).
        
4. **Beri skor**: risiko diberi dua skor: `L` (likelihood) dan `I` (impact).
    
5. **Hitung skor risiko**: biasanya `Skor = L × I` (atau gunakan matriks warna langsung).
    
6. **Buat threshold / zona warna**: tentukan rentang skor untuk Hijau / Kuning / Oranye / Merah.
    
7. **Tentukan tindakan** berdasarkan zona (terima, monitor, mitigasi, hindari).
    
8. **Catat mitigasi, pemilik, dan tenggat** dalam risk register.
    
9. **Tinjau berkala** dan update setelah mitigasi atau perubahan konteks.
    

---

### 4.2. Contoh matriks 5×5 (skor = L × I)

![](matriks-risiko-4.png)

| range   | indikator           |
| ------- | ------------------- |
| 1 - 4   | 🔵 Prioritas rendah |
| 5 - 8   | 🟡 Prioritas sedang |
| 9 - 16  | 🟠 Prioritas Tinggi |
| 20 - 25 | 🔴 Kritis           |

[🔗 source](https://docs.google.com/spreadsheets/d/1u3VsuAn9e7nHdj1DmC_8OVCZnQJzaphFahNaya_77G8/edit)

---

### 4.3. Contoh pengisian risk register

![](risk-register-2.png)

[🔗 source](https://docs.google.com/spreadsheets/d/1u3VsuAn9e7nHdj1DmC_8OVCZnQJzaphFahNaya_77G8/edit)

---

### 4.4. Tips praktis & best practices

- **Definisikan kriteria impact** (keuangan, reputasi, keselamatan) secara terukur (mis. kerugian Rp, downtime jam, jumlah pelanggan terdampak).
    
- **Gunakan kombinasi kuantitatif & kualitatif** bila data detail tidak tersedia.
    
- **Tetapkan pemilik risiko** untuk tiap risiko dan langkah mitigasi.
    
- **Sertakan *Key Risk Indicator* (KRI)** untuk memantau perubahan likelihood.
    
- **Sederhana lebih baik** pada awalnya — mulai 3×3 kalau tim belum familiar, lalu tingkatkan ke 5×5.
    
- **Dokumentasikan asumsi** (mengapa L=4, I=5) supaya penilaian bisa ditinjau ulang.
    
---

## 💼 Diskusi & Tugas

Kerjakan soal-soal berikut, gunakan matriks 4x4 untuk skala penilaian risiko
### Soal 1 — Proyek Pengembangan Aplikasi Mobile Kampus

Sebuah tim IT kampus sedang mengembangkan **aplikasi mobile untuk sistem informasi akademik**, yang memungkinkan mahasiswa mengakses KRS, nilai, dan jadwal kuliah.  
Namun, proyek sering tertunda karena koordinasi antar divisi tidak berjalan baik dan server uji sering bermasalah.

**Tugas:**  
Buat _risk register_ minimal 8 risiko yang mungkin muncul selama proyek berlangsung, termasuk risiko teknis, manajerial, dan operasional. Tentukan tingkat risiko dan strategi mitigasinya.

---

#### Soal 2 — Proyek Implementasi ERP (Enterprise Resource Planning) di Perusahaan Manufaktur

Perusahaan “PT Mekatronik Jaya” memutuskan untuk menerapkan sistem ERP untuk mengintegrasikan data produksi, keuangan, dan logistik.  
Namun, beberapa karyawan menolak perubahan sistem dan pelatihan berjalan lambat. Vendor ERP juga mengalami keterlambatan dalam pengiriman modul.

**Tugas:**  
Susun _risk register_ untuk proyek ERP ini dengan memperhatikan risiko:

- Perubahan budaya kerja,
    
- Kesiapan sumber daya manusia,
    
- Keterlambatan vendor,
    
- Risiko integrasi sistem lama dan baru.
    

---

#### Soal 3 — Proyek Migrasi Data ke Cloud

Sebuah organisasi pemerintahan sedang memigrasikan seluruh data dari server lokal ke **cloud server** agar lebih efisien.  
Selama proses, muncul kekhawatiran tentang keamanan data, downtime saat pemindahan, dan keterbatasan bandwidth internet di kantor daerah.

**Tugas:**  
Buat _risk register_ proyek migrasi ini dengan mengidentifikasi risiko teknis, keamanan, dan operasional. Tentukan kemungkinan, dampak, dan rencana mitigasi yang realistis.

---

#### Soal 4 — Proyek Pembangunan Data Center Baru

Sebuah perusahaan e-commerce membangun **data center baru** untuk mendukung lonjakan transaksi online.  
Proyek melibatkan banyak kontraktor eksternal dan bergantung pada pengiriman perangkat keras dari luar negeri. Pandemi dan perubahan kebijakan impor memperlambat jadwal proyek.

**Tugas:**  
Susun _risk register_ dengan mempertimbangkan risiko-risiko seperti:

- Gangguan rantai pasok,
    
- Keterlambatan konstruksi,
    
- Kegagalan sistem pendingin,
    
- Kelebihan anggaran,
    
- Risiko keselamatan kerja.
    

---

#### Soal 5 — Proyek Implementasi Sistem Keamanan Informasi (ISO 27001)

PT DigitalMart ingin memperoleh sertifikasi **ISO 27001** untuk meningkatkan kepercayaan pelanggan terhadap keamanan datanya.  
Namun, ditemukan masalah berupa ketidaklengkapan dokumen kebijakan keamanan, kurangnya kesadaran karyawan, dan ketidaksesuaian beberapa sistem lama terhadap standar ISO.

**Tugas:**  
Buat _risk register_ untuk proyek implementasi ISO 27001 ini dengan mengidentifikasi risiko terkait kepatuhan, SDM, teknologi, dan manajemen. Tentukan nilai risiko dan strategi mitigasinya.
