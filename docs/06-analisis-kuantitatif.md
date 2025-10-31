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
$$\text{EMV} = \sum (P_i \times V_i)$$

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

$EMV = (0.3 \times -100.000.000) + (0.7 \times 0) = -30.000.000$

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
        $$VaR = Z \times \sigma \times {V}$$
        di mana:        
        - $Z$: nilai dari distribusi normal sesuai tingkat kepercayaan (mis. 1.65 untuk 95%). Di Excel, $Z$ diperoleh menggunakan fungsi `=NORM.S.INV(Conficence level)`
        - $\sigma$: standar deviasi return            
        - $V$: nilai asset
            
3. **Monte Carlo Simulation**
    
    - Menghasilkan ribuan simulasi acak berdasarkan model statistik return.
        
    - Hasil distribusi simulasi digunakan untuk memperkirakan VaR.
        

---

#### Contoh Perhitungan Sederhana

Misalkan portofolio investasi memiliki:

- Nilai = Rp 10 miliar
    
- Standar deviasi return harian = 1.5%
    
- Tingkat kepercayaan = 95%
    
- $Z = 1.65$
    

Maka:  
$VaR = 1.65 \times 1.5\% \times 10.000.000.000 = Rp 247.500.000$

Artinya, ada 95% keyakinan bahwa kerugian **tidak akan melebihi Rp 247,5 juta dalam satu hari**.

---

#### Kelebihan dan Keterbatasan

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

**Analisis Sensitivitas** dalam konteks **metode analisis kuantitatif** adalah teknik yang digunakan untuk **menilai seberapa sensitif hasil suatu model atau keputusan terhadap perubahan variabel input**. Dengan kata lain, analisis ini membantu kita memahami **dampak perubahan kecil pada asumsi atau parameter** terhadap hasil akhir suatu perhitungan atau model risiko.

---

#### Tujuan Analisis Sensitivitas

1. **Mengidentifikasi variabel kunci** yang paling berpengaruh terhadap hasil.
    
2. **Mengukur tingkat ketidakpastian** dalam hasil keputusan atau estimasi.
    
3. **Meningkatkan keandalan keputusan**, dengan mengetahui sejauh mana hasil akan berubah jika asumsi berubah.
    
4. **Mendukung manajemen risiko**, dengan menunjukkan area yang paling rentan terhadap fluktuasi input.
    

---

#### Langkah-langkah Umum Analisis Sensitivitas

1. **Menentukan model atau fungsi matematis** yang digunakan (misal: model biaya, model risiko, model investasi).
    
2. **Mengidentifikasi variabel input utama** (misal: suku bunga, harga bahan baku, permintaan pasar).
    
3. **Menentukan rentang perubahan** untuk setiap variabel (misal: ±10%, ±20%).
    
4. **Menghitung hasil (output)** model untuk setiap perubahan input.
    
5. **Menganalisis perubahan output** dan menentukan seberapa besar sensitivitas hasil terhadap tiap variabel.
    

---

#### Contoh Analisis Sensitivitas
$$NPV = \sum \frac{CF_t}{(1+r)^t} - I$$
- $CF_t​$: arus kas pada tahun ke-t    
- $r$: tingkat diskonto    
- $I$: investasi awal    

Jika tingkat diskonto naik dari **10% menjadi 12%**, maka NPV bisa berubah dari **Rp200 juta menjadi Rp150 juta**.  
Artinya, hasil (NPV) **sangat sensitif terhadap perubahan tingkat diskonto**, dan manajer proyek perlu mewaspadai risiko perubahan suku bunga.

Hasil Analisis Sensitivitas biasanya divisualisasikan dalam bentuk:
- **Tornado chart** → menunjukkan variabel mana yang paling berpengaruh.    
- **Spider chart** → menunjukkan hubungan antara perubahan input dan output.    

![](contoh-tornado-chart-1.png)

---

### 4.4. Analisis Skenario (Scenario Analysis)

#### Pengertian Analisis Skenario

**Analisis Skenario** adalah **metode analisis kuantitatif** yang digunakan untuk mengevaluasi bagaimana hasil suatu proyek, investasi, atau keputusan akan berubah **jika kondisi atau asumsi utama berubah secara signifikan**.

Dengan kata lain, metode ini **menguji dampak dari berbagai skenario kemungkinan masa depan** (misalnya “terbaik”, “terburuk”, dan “paling mungkin”) terhadap hasil numerik seperti **keuntungan, biaya, NPV (Net Present Value), atau tingkat risiko**.

 **Analisis Skenario** adalah alat penting dalam analisis kuantitatif untuk memahami **bagaimana hasil keputusan berubah di bawah kondisi masa depan yang berbeda**.  
Dengan metode ini, organisasi dapat menilai **ketahanan strategi**, **mengantisipasi risiko ekstrem**, dan **membuat keputusan yang lebih adaptif** terhadap ketidakpastian.

**Monte Carlo Simulation** membantu manajer risiko memahami **variasi kemungkinan hasil dan probabilitasnya**, sehingga dapat mengambil keputusan yang lebih informasional dan mengantisipasi potensi kerugian atau keterlambatan sejak dini.

---

#### Tujuan Analisis Skenario

1. **Menilai ketahanan (robustness)** keputusan terhadap perubahan variabel eksternal.
    
2. **Mengidentifikasi risiko dan peluang** yang mungkin terjadi di bawah kondisi berbeda.
    
3. **Mendukung pengambilan keputusan** berbasis data dan bukan asumsi tunggal.
    
4. **Meningkatkan kesiapan manajemen risiko** dengan memahami hasil ekstrem (worst case / best case).
    

---

#### Langkah-Langkah Analisis Skenario (Kuantitatif)

1. **Tentukan variabel kunci**  
    Misalnya: biaya bahan baku, tingkat inflasi, suku bunga, durasi proyek, permintaan pasar.
    
2. **Tentukan skenario**  
    Biasanya dibagi menjadi:
    
    - **Skenario optimis (best case)**
        
    - **Skenario pesimis (worst case)**
        
    - **Skenario realistis (most likely)**
        
3. **Tentukan nilai numerik untuk tiap variabel di setiap skenario**  
    Contoh:
    
    - Inflasi best case = 2%,
        
    - Most likely = 5%,
        
    - Worst case = 10%.
        
4. **Hitung hasil akhir** untuk masing-masing skenario menggunakan model perhitungan (misalnya model keuangan proyek atau EMV).
    
5. **Bandingkan hasil** antar skenario untuk menilai sensitivitas hasil terhadap perubahan variabel.
    

---

#### Contoh Tabel Analisis Skenario

|Skenario|Inflasi (%)|Biaya Bahan (Rp juta)|Permintaan (unit)|NPV (Rp juta)|Keterangan|
|---|---|---|---|---|---|
|Optimis (Best)|2|400|1200|800|Hasil terbaik|
|Realistis|5|450|1000|500|Hasil normal|
|Pesimis (Worst)|10|500|700|200|Hasil terendah|

Dari tabel di atas, kita bisa melihat bahwa jika inflasi dan biaya meningkat (skenario pesimis), NPV proyek turun drastis dari Rp 800 juta menjadi Rp 200 juta.

---

#### Perbedaan dengan Analisis Sensitivitas

|Aspek|Analisis Sensitivitas|Analisis Skenario|
|---|---|---|
|Fokus|Mengubah **satu variabel** saja|Mengubah **beberapa variabel sekaligus**|
|Tujuan|Melihat seberapa sensitif hasil terhadap satu faktor|Melihat dampak kombinasi perubahan kondisi|
|Output|Tornado chart / garis hubungan|Tabel atau grafik perbandingan hasil skenario|


Apakah Anda ingin saya bantu **buatkan contoh grafik (bar chart)** dari tabel skenario di atas agar bisa langsung digunakan untuk presentasi atau laporan manajemen risiko proyek?
    

---

### 4.5. Monte Carlo Simulation

**Monte Carlo Simulation (Simulasi Monte Carlo)** adalah salah satu **metode analisis kuantitatif** yang digunakan dalam **manajemen risiko** untuk memperkirakan kemungkinan hasil dari suatu proyek, investasi, atau keputusan yang mengandung ketidakpastian.

Metode ini **menggunakan pendekatan statistik dan komputasi** dengan **melakukan ribuan hingga jutaan percobaan acak (random sampling)** untuk mensimulasikan berbagai kemungkinan hasil dari variabel-variabel risiko.

---

#### Konsep Dasar Monte Carlo Simulation

Monte Carlo bekerja dengan prinsip **“pengulangan acak terhadap variabel input yang tidak pasti”** untuk melihat bagaimana ketidakpastian tersebut memengaruhi hasil akhir.

Langkah-langkah umumnya:

1. **Identifikasi variabel input yang tidak pasti**  
    Misalnya: biaya proyek, durasi kegiatan, harga bahan baku, atau nilai tukar.
    
2. **Tentukan distribusi probabilitas** untuk setiap variabel  
    Contoh:
    
    - Biaya bahan baku ~ Distribusi Normal (mean = 100, sd = 10)
        
    - Durasi proyek ~ Distribusi Triangular (min = 5, most likely = 7, max = 10)
        
3. **Lakukan simulasi acak (random sampling)** terhadap tiap variabel input ribuan kali.
    
4. **Hitung hasil output** (misalnya total biaya atau waktu proyek) untuk setiap percobaan.
    
5. **Analisis hasil simulasi** dalam bentuk distribusi output — seperti nilai rata-rata, standar deviasi, dan probabilitas terjadinya skenario tertentu.
    

---

#### Contoh dalam Konteks Manajemen Risiko Proyek

Misalnya, manajer risiko ingin mengetahui **kemungkinan proyek terlambat atau melebihi anggaran**.

|Variabel Risiko|Distribusi|Minimum|Most Likely|Maksimum|
|---|---|---|---|---|
|Durasi Aktivitas A (hari)|Triangular|5|7|10|
|Biaya Material (juta Rp)|Normal|90|100|110|
|Produktivitas Tim (%)|Uniform|80|-|100|

Setelah dilakukan 10.000 kali simulasi:

- Rata-rata total biaya proyek: **Rp 1,2 miliar**
    
- Probabilitas proyek melebihi Rp 1,3 miliar: **25%**
    
- Probabilitas proyek selesai lebih dari 40 hari: **18%**
    

---

#### Output yang Umum Dihasilkan

- **Histogram distribusi hasil** (misal total biaya atau durasi)
    
- **Cumulative Probability Chart (S-curve)** untuk melihat peluang suatu hasil tercapai
    
- **Sensitivity Chart (Tornado Chart)** untuk mengidentifikasi variabel paling berpengaruh terhadap hasil
    

---

#### Kelebihan Monte Carlo Simulation

✅ Menggambarkan **ketidakpastian secara realistis**  
✅ Memberikan **beragam kemungkinan hasil**, bukan satu estimasi saja  
✅ Dapat **mengukur probabilitas risiko** secara kuantitatif  
✅ Memudahkan **pengambilan keputusan berbasis data**

---

#### Keterbatasan

❌ Membutuhkan **data yang cukup akurat** untuk menentukan distribusi probabilitas  
❌ Memerlukan **alat bantu perangkat lunak** (misalnya @RISK, Crystal Ball, Python, atau Excel Add-in)  
❌ Interpretasi hasil harus hati-hati agar tidak menyesatkan

---

Apakah Anda ingin saya buatkan **contoh grafik hasil Monte Carlo Simulation** (misalnya histogram probabilitas total biaya proyek) agar bisa langsung digunakan dalam laporan atau presentasi manajemen risiko?
    

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

## 💼 Diskusi & Tugas

### Menghitung EMV

#### Soal 1 — Risiko Proyek Teknologi Informasi

Sebuah perusahaan sedang mengembangkan aplikasi e-commerce baru.  
Terdapat dua risiko utama yang diidentifikasi:

|Risiko|Probabilitas|Dampak Finansial|
|---|---|---|
|Keterlambatan pengembangan|0,25|–Rp 80.000.000|
|Kegagalan uji coba sistem|0,10|–Rp 120.000.000|
|Tidak terjadi risiko apa pun|?|Rp 0|

**Pertanyaan:**

1. Hitunglah probabilitas untuk kondisi “tidak terjadi risiko apa pun”!
    
2. Hitung **Expected Monetary Value (EMV)** dari keseluruhan proyek!
    
3. Apa interpretasi dari nilai EMV yang diperoleh?
    

---

#### Soal 2 — Analisis Alternatif Investasi Sistem Informasi

Sebuah perusahaan sedang mempertimbangkan dua alternatif sistem baru:

|Alternatif|Kondisi|Probabilitas|Nilai Finansial (Rp)|
|---|---|---|---|
|Sistem A|Berhasil|0,7|+250.000.000|
|Sistem A|Gagal|0,3|–100.000.000|
|Sistem B|Berhasil|0,6|+300.000.000|
|Sistem B|Gagal|0,4|–150.000.000|

**Pertanyaan:**
1. Hitunglah EMV untuk masing-masing sistem (A dan B)!    
2. Berdasarkan hasil EMV, sistem mana yang sebaiknya dipilih?
3. Jelaskan alasan pemilihan berdasarkan konsep EMV.  

---


