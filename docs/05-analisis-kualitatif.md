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

![](docs/img/matriks-risiko.png)

---

### 4.3. Contoh pengisian risk register

![](risk-register-1.png)

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

1. Buat matrix risiko 4x4
2. Buat _risk register_ untuk kegiatan berikut:
	1. Pengembangan sistem informasi baru
	2. Implementasi jaringan komputer
	3. Peluncuran aplikasi mobile
	4. Proyek infrastruktur TI di kampus
