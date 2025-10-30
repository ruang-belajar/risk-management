# METODE ANALISIS RISIKO KUANTITATIF

## 1. Pendahuluan

Jika pada analisis **kualitatif** risiko dinilai dengan deskripsi (low, medium, high), maka pada **analisis kuantitatif** risiko dinilai menggunakan **angka, data statistik, dan model matematis**.  
Metode ini biasanya digunakan pada proyek besar, industri keuangan, kesehatan, energi, atau teknologi yang membutuhkan **akurasi tinggi** dalam pengukuran risiko.

---

## 2. Tujuan Analisis Kuantitatif

1. Mengukur risiko secara **numerik** untuk memperkirakan besarnya kerugian.
    
2. Membandingkan alternatif strategi pengendalian risiko berdasarkan **nilai finansial**.
    
3. Menyediakan dasar kuat untuk **pengambilan keputusan investasi** dan **alokasi sumber daya**.
    
4. Menghitung **eksposur risiko total** organisasi/proyek.
    

---

## 3. Input Data yang Dibutuhkan

1. **Data Historis** → frekuensi kejadian, kerugian sebelumnya.
    
2. **Distribusi Probabilitas** → kemungkinan terjadinya risiko.
    
3. **Nilai Kerugian Potensial** → kerugian finansial atau non-finansial.
    
4. **Model Matematis / Simulasi** → untuk menghitung perkiraan dampak total.
    

---

## 4. Metode Analisis Kuantitatif

### 4.1. Expected Monetary Value (EMV)

**Expected Monetary Value (EMV)** atau **Nilai Harapan Moneter** adalah salah satu teknik kuantitatif yang digunakan dalam **analisis risiko** untuk mengukur **dampak finansial rata-rata** dari suatu keputusan atau kejadian yang memiliki **ketidakpastian**.

Expected Monetary Value adalah **nilai rata-rata tertimbang** dari semua kemungkinan hasil (baik positif maupun negatif), dengan masing-masing hasil dikalikan oleh **probabilitas terjadinya**.

Secara matematis:  
$\text{EMV} = \sum (P_i \times V_i)$

di mana:

- $P_i$ = probabilitas terjadinya hasil ke-i
    
- $V_i$ = nilai moneter (dampak finansial) dari hasil ke-i
    

---

#### Tujuan Penggunaan EMV

1. **Membantu pengambilan keputusan berbasis data**, bukan hanya intuisi.
    
2. **Membandingkan beberapa alternatif keputusan** untuk memilih yang memberikan nilai ekspektasi terbaik.
    
3. **Menilai besarnya risiko finansial** dari suatu proyek atau kejadian.
    
4. Digunakan dalam **analisis keputusan (decision tree)** dan **analisis risiko proyek** seperti di manajemen proyek, investasi, maupun asuransi.
    

---

#### Contoh Perhitungan EMV

Misalkan dalam proyek pengembangan sistem:

- Ada risiko **keterlambatan proyek** dengan probabilitas 30% (0.3).
    
- Jika terjadi, kerugian finansial diperkirakan sebesar **Rp 100 juta**.
    
- Jika tidak terjadi (probabilitas 70% atau 0.7), tidak ada kerugian (Rp 0).
    

Maka:

[  
EMV = (0.3 \times -100.000.000) + (0.7 \times 0) = -30.000.000  
]

👉 **Interpretasi:**  
Nilai EMV sebesar **–Rp 30 juta** menunjukkan bahwa secara rata-rata, risiko keterlambatan ini akan menyebabkan **kerugian ekspektasi Rp 30 juta** terhadap proyek.

---

#### Contoh Penggunaan dalam Decision Tree

|Alternatif Keputusan|Skenario|Probabilitas|Nilai (Rp)|EMV (Rp)|
|---|---|---|---|---|
|Menggunakan Vendor A|Sukses|0.8|+200.000.000|160.000.000|
||Gagal|0.2|–100.000.000|–20.000.000|
|**Total EMV Vendor A**||||**140.000.000**|
|Menggunakan Vendor B|Sukses|0.6|+250.000.000|150.000.000|
||Gagal|0.4|–150.000.000|–60.000.000|
|**Total EMV Vendor B**||||**90.000.000**|

➡️ **Kesimpulan:** Pilih **Vendor A** karena memiliki **EMV lebih tinggi (Rp 140 juta)**.

---

#### Kelebihan dan Keterbatasan EMV

**Kelebihan:**

- Memberikan **dasar kuantitatif** untuk pengambilan keputusan.
    
- Mudah digunakan dalam **model probabilistik dan decision tree**.
    

**Keterbatasan:**

- Bergantung pada **akurasi estimasi probabilitas dan dampak**.
    
- Tidak mempertimbangkan **faktor non-finansial** (seperti reputasi, moral tim, dll).
    
- Tidak menggambarkan **variabilitas risiko ekstrem (outlier)**.
    
---
### 4.2. Value at Risk (VaR)

**Value at Risk (VaR)** adalah suatu **metode pengukuran risiko keuangan** yang digunakan untuk **menilai potensi kerugian maksimum** yang mungkin dialami oleh suatu portofolio investasi, perusahaan, atau proyek dalam periode waktu tertentu **dengan tingkat kepercayaan tertentu**.

Secara sederhana, **VaR menjawab pertanyaan:**

> “Berapa besar kerugian maksimum yang mungkin terjadi dalam kondisi pasar normal, selama periode tertentu, dengan tingkat keyakinan tertentu?”

Contoh:

> Sebuah portofolio memiliki VaR sebesar **Rp 1 miliar pada tingkat kepercayaan 95% selama 1 hari.**  
> Artinya, ada **95% kemungkinan** bahwa kerugian **tidak akan melebihi Rp 1 miliar** dalam satu hari ke depan,  
> dan **5% kemungkinan** kerugian akan lebih besar dari itu.

#### Komponen Utama dalam VaR

1. **Horizon Waktu (Time Horizon)**  
    Periode analisis risiko, misalnya 1 hari, 10 hari, 1 bulan, dll.  
    → Semakin panjang periode, semakin besar potensi risiko.
    
2. **Tingkat Kepercayaan (Confidence Level)**  
    Biasanya 95%, 97.5%, atau 99%.  
    → Semakin tinggi tingkat kepercayaan, semakin besar nilai VaR.
    
3. **Nilai Potensial Kerugian (Loss Amount)**  
    Hasil akhir pengukuran VaR dalam satuan uang (misalnya rupiah atau dolar).
    
#### Metode Perhitungan VaR

Terdapat tiga pendekatan utama:

1. **Historical Simulation**
    
    - Berdasarkan data historis harga aset.
        
    - Tidak mengasumsikan distribusi tertentu.
        
    - Contoh: melihat kerugian yang benar-benar terjadi dalam 250 hari terakhir dan mengambil persentil ke-5.
        
2. **Variance–Covariance (Parametric)**
    
    - Mengasumsikan bahwa return mengikuti **distribusi normal**.
        
    - Menghitung VaR dengan formula:  
        $VaR = Z \times \sigma \times \sqrt{t}$  
        di mana:
        
        - $Z$: nilai dari distribusi normal sesuai tingkat kepercayaan (mis. 1.65 untuk 95%)
            
        - $\sigma$: standar deviasi return
            
        - $t$: periode waktu (hari)
            
3. **Monte Carlo Simulation**
    
    - Menghasilkan ribuan simulasi acak berdasarkan model statistik return.
        
    - Hasil distribusi simulasi digunakan untuk memperkirakan VaR.
        

---

#### 🧮 Contoh Perhitungan Sederhana

Misalkan portofolio investasi memiliki:

- Nilai = Rp 10 miliar
    
- Standar deviasi return harian = 1.5%
    
- Tingkat kepercayaan = 95%
    
- $Z = 1.65$
    

Maka:  
$VaR = 1.65 \times 1.5\% \times 10.000.000.000 = Rp 247.500.000$

Artinya, ada 95% keyakinan bahwa kerugian **tidak akan melebihi Rp 247,5 juta dalam satu hari**.

---

#### 📉 Kelebihan dan Keterbatasan

**Kelebihan:**

- Memberikan ukuran risiko yang jelas dalam satuan uang.
    
- Dapat dibandingkan antar aset atau portofolio.
    
- Digunakan secara luas oleh lembaga keuangan dan regulator (misal: Basel II).
    

**Keterbatasan:**

- Tidak menunjukkan **kerugian di luar batas VaR** (extreme loss).
    
- Bergantung pada asumsi distribusi return (terutama pada metode parametric).
    
- Kurang akurat dalam kondisi pasar ekstrem atau krisis.
    

---

### 4.3. Analisis Sensitivitas

- Mengukur seberapa sensitif suatu hasil terhadap perubahan variabel risiko.
    
- **Contoh**: Jika harga bahan baku naik 10%, maka biaya produksi naik 15%.
    

---

### 4.4. Analisis Skenario (Scenario Analysis)

- Menilai risiko dengan membandingkan skenario: **optimis, moderat, pesimis**.
    
- Membantu manajemen melihat potensi dampak dalam kondisi berbeda.
    

---

### 4.5. Monte Carlo Simulation

- Menggunakan **komputer dan model probabilistik** untuk menghasilkan ribuan simulasi hasil.
    
- Menunjukkan distribusi kemungkinan kerugian/keuntungan.
    
- Banyak digunakan dalam **proyek besar, energi, investasi, asuransi**.
    

---

## 5. Perbandingan Analisis Kualitatif vs Kuantitatif

| Aspek          | Kualitatif               | Kuantitatif                              |
| -------------- | ------------------------ | ---------------------------------------- |
| **Tujuan**     | Prioritas risiko         | Nilai risiko numerik                     |
| **Data**       | Subjektif, opini         | Data historis, statistik                 |
| **Hasil**      | Low, Medium, High        | Nilai rupiah, probabilitas               |
| **Kelebihan**  | Mudah, cepat, murah      | Lebih akurat, bisa perhitungan finansial |
| **Kekurangan** | Kurang akurat, subjektif | Rumit, butuh data lengkap, mahal         |

---

## 6. Contoh Kasus Sederhana

**Kasus: Proyek Konstruksi**

- Risiko keterlambatan: Probabilitas 40%, kerugian Rp 200 juta → EMV = Rp 80 juta.
    
- Risiko kecelakaan kerja: Probabilitas 10%, kerugian Rp 500 juta → EMV = Rp 50 juta.
    
- Risiko kenaikan harga material: Probabilitas 30%, kerugian Rp 150 juta → EMV = Rp 45 juta.
    

📌 **Total Eksposur Risiko (EMV Total) = Rp 175 juta**

Manajemen bisa menggunakan nilai ini untuk **menyediakan cadangan biaya risiko (contingency fund)**.

---

## 7. Ringkasan

- Analisis kuantitatif memberikan gambaran **finansial dan probabilistik** risiko.
    
- Metode populer: **EMV, VaR, Analisis Sensitivitas, Analisis Skenario, Monte Carlo**.
    
- Membutuhkan **data valid** agar hasil akurat.
    
- Biasanya digunakan bersama analisis kualitatif untuk keputusan strategis.
    

---

## 💼 Diskusi & Tugas

1. Ambil 3 risiko dari Risk Register (Bab 4).
    
2. Berikan nilai probabilitas (%) dan dampak finansial (Rp).
    
3. Hitung **EMV (Expected Monetary Value)** masing-masing risiko.
    
4. Tentukan total cadangan biaya risiko (Contingency Reserve).
    
