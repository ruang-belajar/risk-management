# Langkah-langkah Perhitungan VaR (Pendekatan Parametric / Variance–Covariance) — Terperinci

Pendekatan **parametric (variance–covariance)** biasanya disebut **Delta-Normal VaR**: diasumsikan return portofolio mendistribusi normal dan perubahan portofolio kira-kira linear terhadap perubahan faktor risiko. Berikut langkah demi langkah, lengkap dengan rumus, catatan praktis, dan contoh numerik yang dihitung **digit-by-digit**.

---

## 1) Definisikan tujuan dan parameter analisis

- **Horizon waktu** (mis. 1 hari, 10 hari).
    
- **Confidence level** (mis. 95% atau 99%).
    
- **Nilai portofolio** atau eksposur finansial (V) (mis. Rp 1.200.000.000).
    
- **Apakah VaR untuk satu aset atau portofolio multi-aset?**
    
- **Sumber data**: gunakan return historis untuk estimasi volatilitas dan korelasi.
    

---

## 2) Pilih nilai Z (z-score) sesuai tingkat kepercayaan

Nilai (Z) adalah z-score dari distribusi normal standar untuk area kumulatif sama dengan confidence level.

Contoh umum:

- 90% → (Z \approx 1{,}282)
    
- 95% → (Z \approx 1{,}645) (sering dibulatkan 1,65)
    
- 99% → (Z \approx 2{,}326) (sering dibulatkan 2,33)
    

(Anda bisa pakai fungsi statistik: `NORM.S.INV(confidence)` di Excel/Sheets atau `scipy.stats.norm.ppf()` di Python.)

---

## 3) Hitung volatilitas (standar deviasi) dari return

- Gunakan return **log** atau **simple** konsisten; parametric biasanya menggunakan return simple jika perubahan kecil.
    
- Hitung standar deviasi harian (\sigma) dari return historis.
    

Contoh: jika (\sigma = 1{,}8% = 0{,}018) per hari.

---

## 4) Jika portofolio multi-aset: buat vektor bobot & matriks kovarians

- Misalkan ada (n) aset, dengan bobot nilai portofolio (w = [w_1, w_2, ..., w_n]) (dalam proporsi, jumlah = 1).
    
- Ambil standar deviasi masing-masing (\sigma_i) dan korelasi (\rho_{ij}).
    
- Matriks kovarians (\Sigma) punya elemen (\Sigma_{ij} = \rho_{ij}\sigma_i\sigma_j).
    

**Rumus volatilitas portofolio (proporsi):**  
[  
\sigma_p = \sqrt{w^\top \Sigma w}  
]

Jika ingin volatilitas dalam nilai uang: (\sigma_{V} = \sigma_p \times V).

---

## 5) Rumus VaR parametric (satu aset, linear)

Untuk satu aset/eksposur linear:  
[  
\text{VaR} = Z \times \sigma \times V  
]  
Di mana:

- (Z) = z-score untuk confidence level
    
- (\sigma) = standar deviasi return per horizon
    
- (V) = nilai portofolio (moneter)
    

Untuk portofolio:  
[  
\text{VaR} = Z \times \sigma_p \times V  
]  
(dengan (\sigma_p) dihitung seperti di atas)

---

## 6) Scaling untuk horizon waktu (jika berbeda dari satu unit)

Jika (\sigma) dihitung per hari dan Anda ingin VaR untuk (t) hari (asumsi return iid dan Brownian scaling):  
[  
\sigma_{t} = \sigma \sqrt{t}  
]  
Sehingga:  
[  
\text{VaR}_{t} = Z \times \sigma \sqrt{t} \times V  
]

Catatan: scaling √t valid untuk jangka pendek bila asumsi independensi & normalitas berlaku; untuk jangka panjang ini sering meleset.

---

## 7) Konversi ke kerugian moneter dan interpretasi tanda

- Rumus di atas memberi **jumlah uang** (positif) yang merepresentasikan _potensi kerugian maksimum_ pada confidence level.
    
- Interpretasi: “Dengan confidence 95%, kerugian tidak akan melebihi VaR dalam horizon yang ditentukan (dalam kondisi normal pasar).”
    

---

## 8) Validasi & backtesting

- Bandingkan VaR yang dihitung dengan kerugian aktual dalam periode uji (hit frequency).
    
- Untuk confidence 95%, rata-rata pelanggaran (loss > VaR) seharusnya ~5%.
    
- Lakukan uji statistik (Kupiec, Christoffersen) jika perlu.
    

---

## 9) Catatan tentang asumsi dan keterbatasan

- Mengasumsikan **normalitas** return (mengabaikan ekor tebal) → meremehkan risiko ekstrem.
    
- Asumsi **linearitas** (delta) — non-linear instrument (opsional) butuh modifikasi.
    
- Parameter estimasi (σ, ρ) sensitif terhadap window data dan outlier.
    
- Gunakan VaR bersama metrik lain (CVaR/ES, stress testing, scenario analysis).
    

---

## 10) Contoh numerik — Satu Aset (langkah terperinci, digit-by-digit)

**Parameter:**

- Nilai portofolio (V =) Rp **1.200.000.000**
    
- Standar deviasi harian (\sigma = 1{,}8% = 0{,}018)
    
- Confidence = 95% → (Z = 1{,}645) (sering dibulatkan 1,65; di sini gunakan 1,645 untuk akurasi)
    

**Rumus:**  
[  
\text{VaR} = Z \times \sigma \times V  
]

**Hitung digit-by-digit:**

1. Hitung (Z \times \sigma):  
    (1{,}645 \times 0{,}018)
    
    - (1{,}645 \times 18 = 29{,}610) (karena 1,645×18 = 1,645×(20−2) = 32,9 − 3,29 = 29,61)
        
    - Karena 18 berarti 18/1000 (0,018), bagi 29,610 dengan 1000 → (29{,}610/1000 = 0{,}02961)
        
2. Kalikan dengan (V):  
    (0{,}02961 \times 1.200.000.000)
    
    - 1% dari V = (0{,}01 \times 1.200.000.000 = 12.000.000)
        
    - 2% dari V = (24.000.000)
        
    - 0{,}00961 × V = 1.200.000.000 × 9{,}61/1000 = (1.200.000.000 × 9{,}61)/1000
        
        - (1.200.000.000 × 9{,}61 = 1.200.000.000 × (10 − 0{,}39) = 12.000.000.000 − 468.000.000 = 11.532.000.000)
            
        - Bagi 1000 → (11.532.000.000 / 1000 = 11.532.000)
            
    - Jadi (0{,}02961 = 0{,}02 + 0{,}00961): (24.000.000 + 11.532.000 = 35.532.000)
        

[  
\boxed{\text{VaR}_{\text{harian, 95%}} \approx Rp\ 35.532.000}  
]

(Interpretasi: 95% confidence bahwa kerugian harian tidak akan melebihi ~Rp 35,5 juta.)

---

## 11) Contoh numerik — Dua Aset (portofolio) — ringkas & terperinci

**Asumsi:**

- Nilai portofolio (V = Rp\ 2.000.000.000).
    
- Dua aset A dan B dengan bobot nilai (proporsi) (w = [0{,}6,\ 0{,}4]). (60% di A, 40% di B)
    
- Standar deviasi harian: (\sigma_A = 2{,}0% = 0{,}02); (\sigma_B = 1{,}2% = 0{,}012).
    
- Korelasi (\rho_{AB} = 0{,}5).
    
- Confidence 95% → (Z = 1{,}645).
    

**Langkah:**

1. Buat matriks kovarians (\Sigma):
    
    - (\Sigma_{AA} = \sigma_A^2 = 0{,}02^2 = 0{,}0004)
        
    - (\Sigma_{BB} = \sigma_B^2 = 0{,}012^2 = 0{,}000144)
        
    - (\Sigma_{AB} = \rho_{AB}\sigma_A\sigma_B = 0{,}5 \times 0{,}02 \times 0{,}012)
        
        - (0{,}02 \times 0{,}012 = 0{,}00024)
            
        - Dikalikan 0{,}5 → (0{,}00024 \times 0{,}5 = 0{,}00012)
            
    
    Jadi:  
    [  
    \Sigma = \begin{pmatrix}  
    0{,}0004 & 0{,}00012 \  
    0{,}00012 & 0{,}000144  
    \end{pmatrix}  
    ]
    
2. Hitung (\sigma_p = \sqrt{w^\top \Sigma w}) dengan (w = \begin{pmatrix}0{,}6\0{,}4\end{pmatrix}).
    
    - Hitung vektor menengah (u = \Sigma w):
        
        - Baris 1: (0{,}0004 \times 0{,}6 + 0{,}00012 \times 0{,}4)
            
            - (0{,}0004 \times 0{,}6 = 0{,}00024)
                
            - (0{,}00012 \times 0{,}4 = 0{,}000048)
                
            - Jumlah = (0{,}00024 + 0{,}000048 = 0{,}000288)
                
        - Baris 2: (0{,}00012 \times 0{,}6 + 0{,}000144 \times 0{,}4)
            
            - (0{,}00012 \times 0{,}6 = 0{,}000072)
                
            - (0{,}000144 \times 0{,}4 = 0{,}0000576)
                
            - Jumlah = (0{,}000072 + 0{,}0000576 = 0{,}0001296)
                
        
        Jadi (u = \begin{pmatrix}0{,}000288\0{,}0001296\end{pmatrix}).
        
    - Sekarang (w^\top u = 0{,}6 \times 0{,}000288 + 0{,}4 \times 0{,}0001296)
        
        - (0{,}6 \times 0{,}000288 = 0{,}0001728)
            
        - (0{,}4 \times 0{,}0001296 = 0{,}00005184)
            
        - Jumlah = (0{,}0001728 + 0{,}00005184 = 0{,}00022464)
            
    - Jadi (\sigma_p = \sqrt{0{,}00022464}).
        
        - (\sqrt{0{,}00022464} \approx 0{,}015) (karena (0{,}015^2 = 0{,}000225) sangat dekat)
            
    
    → (\sigma_p \approx 0{,}015 = 1{,}5%) per hari.
    
3. VaR:  
    [  
    \text{VaR} = Z \times \sigma_p \times V = 1{,}645 \times 0{,}015 \times 2.000.000.000  
    ]
    
    - (1{,}645 \times 0{,}015 = 1{,}645 \times 15/1000 = (1{,}645 \times 15)/1000)
        
        - (1{,}645 \times 15 = 24{,}675)
            
        - Dibagi 1000 → (24{,}675/1000 = 0{,}024675)
            
    - (0{,}024675 \times 2.000.000.000)
        
        - 1% dari V = 20.000.000 (karena 0,01×2.000.000.000 = 20.000.000)
            
        - 2% = 40.000.000
            
        - 0{,}004675 × V = 2.000.000.000 × 4{,}675/1000 = (2.000.000.000 × 4{,}675)/1000
            
            - (2.000.000.000 × 4{,}675 = 9.350.000.000)
                
            - Dibagi 1000 → (9.350.000.000/1000 = 9.350.000)
                
        - Jadi (0{,}024675 = 0{,}02 + 0{,}004675) → (40.000.000 + 9.350.000 = 49.350.000)
            

[  
\boxed{\text{VaR}_{\text{harian, 95%}} \approx Rp\ 49.350.000}  
]

---

## 12) Praktik terbaik & pemeriksaan akhir

- **Gunakan window data** yang tepat (tradeoff recency vs sample size).
    
- **Periksa normalitas** (histogram, skewness, kurtosis). Jika ada ekor tebal, pertimbangkan Historical VaR atau Monte Carlo.
    
- **Backtest** model dan lakukan stress testing (skenario ekstrem).
    
- **Laporkan bersama CVaR/ES** agar memberi informasi pada kerugian di luar VaR.
    
- **Catat asumsi** (normalitas, linearitas, independensi).
    

---

Kalau kamu mau, aku bisa:

- Terapkan langkah-langkah ini ke **data historismu** (beri return series / volatilitas & korelasi) dan aku hitung VaR-nya.
    
- Atau buat **template Excel** yang otomatis menghitung VaR parametric dan portofolio VaR. Mau yang mana?