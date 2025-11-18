Menentukan **confidence level (CL)** dalam perhitungan VaR bergantung pada **tujuan analisis**, **konteks regulasi**, dan **kebutuhan manajemen risiko**. Tidak ada satu angka yang “benar untuk semua situasi”, tetapi ada **pedoman jelas** yang dipakai secara umum di industri.

# ⭐ 1. Apa itu Confidence Level?

Confidence Level menunjukkan tingkat keyakinan bahwa kerugian **tidak akan melebihi** nilai VaR dalam satu periode.

Contoh:

- CL 95% → ada 5% kemungkinan kerugian lebih besar dari VaR.
    
- CL 99% → ada 1% kemungkinan kerugian lebih besar dari VaR.
    

Semakin tinggi CL → VaR makin besar (lebih konservatif).

---

# ⭐ 2. **Cara Menentukan Confidence Level**

Ada **4 pendekatan utama**, pilih sesuai kebutuhan.

---

## **A. Berdasarkan Regulasi (Paling Umum)**

Dalam banyak lembaga keuangan, CL sudah ditetapkan oleh regulator:

- **Basel Committee (bank global)**  
    → 99% VaR untuk market risk.  
    → 97.5% Expected Shortfall untuk FRTB.
    
- **OJK / Bank Indonesia**  
    → Biasanya mengikuti pedoman Basel: 99% untuk VaR internal model.
    
- **Perusahaan asuransi / reksa dana**  
    → Umumnya 95% atau 99%.
    

Jika Anda bekerja di lembaga yang regulatif → **ikuti CL yang diwajibkan regulator**.

---

## **B. Berdasarkan Tujuan Penggunaan VaR**

Tujuan yang berbeda membutuhkan CL yang berbeda:

|Tujuan|Confidence Level yang cocok|Alasannya|
|---|---|---|
|Mengukur risiko harian trading desk|**95%**|Agar tidak terlalu konservatif & lebih sensitif terhadap volatilitas|
|Risk limit internal perusahaan|**97.5%–99%**|Untuk mengukur kerugian ekstrem|
|Stress risk / worst-case|**99%–99.9%**|Untuk melihat tail risk|
|Monitoring portofolio retail / investasi|**90–95%**|Untuk edukasi & monitoring ringan|

---

## **C. Berdasarkan Horizon Waktu**

Semakin panjang horizon, sering dipakai CL lebih tinggi.

- **Harian (1-day VaR)** → 95% atau 99%
    
- **Bulanan** → 99%
    
- **Tahunan** → 99%–99.9%
    

---

## **D. Berdasarkan Toleransi Risiko (Risk Appetite)**

Jika organisasi memiliki Risk Appetite Statement, pilih CL berdasarkan:

- seberapa besar kerugian yang bisa diterima,
    
- seberapa sering manajemen siap menerima pelanggaran VaR (_VaR breaches_).
    

Contoh:

- Jika perusahaan tidak ingin loss besar terjadi lebih dari **3 kali setahun**,  
    → gunakan CL **≈ 99%** (karena 1% × 250 hari ≈ 2,5 kali).
    

---

# ⭐ 3. Angka Confidence Level yang Umum di Industri

|Industri = CL Harian Umum|Confidence Level|
|---|---|
|Trading desk (bank)|95%|
|Market risk (perbankan, model internal)|99%|
|Manajer investasi / fund manager|95%|
|Treasury corporate|95%|
|Stress test analis risiko|99%–99.9%|

---

# ⭐ 4. Rule of Thumb untuk Pemula

- **95%** → Analysis ringan, edukasi, laporan internal.
    
- **99%** → Analisis serius, risiko tinggi, compliance ke regulasi.
    
- **99.9%** → Analisis ekstrem, tail risk, stress scenario.
    

---

# ⭐ 5. Jadi… bagaimana memilih yang tepat?

Jawab 3 pertanyaan:

1. **Apa konteksnya?**
    
    - Jika regulasi → ikut aturan.
        
    - Jika internal → lihat risk appetite.
        
2. **Seberapa konservatif laporan yang Anda butuhkan?**
    
    - Sedikit konservatif → CL 95%.
        
    - Sangat konservatif → CL 99%.
        
3. **Seberapa sering Anda ingin VaR dilanggar?**
    
    - 95% CL → pelanggaran ~12x/tahun
        
    - 99% CL → pelanggaran ~2–3x/tahun
        

---

# ⭐ Kesimpulan

Confidence level tidak ditentukan oleh perhitungan matematis, tetapi oleh:

- **kebutuhan analisis**,
    
- **toleransi risiko**,
    
- **konteks regulasi**,
    
- **tujuan VaR**.
    
