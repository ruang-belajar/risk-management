## 💡 **Konsep Dasar Parametric VaR**

Metode **Parametric (Variance–Covariance)** disebut juga **Analytical VaR** karena menggunakan **distribusi statistik** (biasanya _normal distribution_) untuk memperkirakan potensi kerugian.

Metode ini **tidak memerlukan simulasi data historis** — cukup dengan nilai rata-rata (_mean_) dan simpangan baku (_standard deviation, σ_) dari return aset atau proyek yang dianalisis.

---

## ⚙️ **Langkah-langkah Perhitungan VaR Parametric**

### **Langkah 1: Tentukan periode dan data historis return**

Kumpulkan data **return harian** (atau mingguan, bulanan, tergantung horizon risiko) dari portofolio, aset, atau proyek IT.

Misalnya:

- Untuk proyek cloud service → data “perubahan pendapatan harian”.
    
- Untuk startup → data “fluktuasi valuasi harian”.
    

**Rumus return harian:**  
$$R_t = \frac{V_t - V_{t-1}}{V_{t-1}}$$

Contoh:

|Hari|Nilai Portofolio (Rp)|Return (%)|
|---|---|---|
|1|1.000.000.000|-|
|2|980.000.000|-2.0|
|3|1.010.000.000|+3.1|
|4|995.000.000|-1.5|
|5|1.005.000.000|+1.0|

---

### **Langkah 2: Hitung rata-rata dan standar deviasi return**

Hitung:

- **Rata-rata (μ)** → menggambarkan _expected return_
    
- **Standar deviasi (σ)** → menggambarkan _volatilitas risiko_
    

**Rumus:**  
$$\mu = \frac{\sum R_t}{n}$$ $$\sigma = \sqrt{\frac{\sum (R_t - \mu)^2}{n - 1}}$$

Contoh hasil perhitungan:

- μ = 0.001 (0,1%)
    
- σ = 0.02 (2%)
    

---

### **Langkah 3: Tentukan tingkat kepercayaan (confidence level)**

Umumnya digunakan:

- **90%** → Z = 1.28
    
- **95%** → Z = 1.65
    
- **99%** → Z = 2.33
    

> Nilai **Z** berasal dari _Z-table (distribusi normal baku)_.  
> Z menyatakan jarak dalam satuan standar deviasi dari mean pada tingkat keyakinan tertentu.

---

### **Langkah 4: Hitung VaR dalam bentuk persentase return**

Jika asumsi return terdistribusi normal, maka VaR dihitung dengan:

$$VaR = Z \times \sigma - \mu$$

Namun dalam praktik sederhana (terutama untuk portofolio besar atau proyek IT di mana return harian kecil), μ sering dianggap ≈ 0, sehingga:

$$VaR = Z \times \sigma$$

Contoh:  

$$VaR = 1.65 \times 0.02 = 0.033$$  
Artinya potensi kerugian **3,3%** dari nilai portofolio pada tingkat keyakinan 95%.

---

### **Langkah 5: Konversi VaR ke nilai nominal (Rp)**

Kalikan hasil VaR (persentase) dengan **nilai total portofolio/proyek (V):**

$$VaR_{Rp} = VaR_{\%} \times Nilai\ Portofolio$$

Contoh:  
$$VaR_{Rp} = 0.033 \times 5.000.000.000 = Rp 165.000.000$$

---

### **Langkah 6: Interpretasi Hasil**

- VaR 95% = Rp 165 juta  
    → berarti:  
    “Dengan keyakinan 95%, kerugian harian **tidak akan melebihi Rp 165 juta**.”
    
- Namun, **ada 5% kemungkinan** bahwa kerugian akan lebih besar dari nilai tersebut.
    

---

## 📊 **Contoh Kasus: Proyek IT**

**Kasus:**  
Sebuah perusahaan cloud service memiliki nilai operasional tahunan setara Rp 10 miliar.  
Dari data historis harian pendapatan, diperoleh:

- σ = 1.8%
    
- μ = 0.2%  
    Hitung VaR harian 99%.
    

---

**Langkah-langkah:**

1. Z untuk 99% = 2.33
    
2. VaR (%) = (2.33 × 1.8%) - 0.2% = 4.19% - 0.2% = **3.99%**
    
3. VaR (Rp) = 3.99% × 10.000.000.000 = **Rp 399.000.000**
    

---

**Interpretasi:**  
Dengan keyakinan 99%, kerugian harian akibat fluktuasi pendapatan cloud service **tidak akan melebihi Rp 399 juta**.  
Namun, **ada 1% kemungkinan** kerugian akan lebih besar dari itu.

---

## 🧮 **Rangkuman Rumus Utama**

| Simbol     | Keterangan                              | Rumus                                     |
| :--------- | :-------------------------------------- | :---------------------------------------- |
| $R_t$      | Return periode ke-t                     | $\frac{V_t - V_{t-1}}{V_{t-1}}$           |
| $\mu$      | Rata-rata return                        | $\frac{\sum R_t}{n}$                      |
| $\sigma$   | Standar deviasi                         | $\sqrt{\frac{\sum (R_t - \mu)^2}{n - 1}}$ |
| $Z$        | Nilai Z pada tingkat keyakinan tertentu | $mis. 1.65 untuk 95\%$                    |
| $VaR$      | Value at Risk (dalam %)                 | $Z \times \sigma - \mu$                   |
| $VaR_{Rp}$ | Value at Risk (dalam nominal)           | $VaR \times Nilai\ Portofolio$            |

---

## ⚖️ **Kelebihan dan Kelemahan Metode Parametric**

|**Kelebihan**|**Kelemahan**|
|---|---|
|Cepat dan sederhana|Asumsi distribusi normal bisa tidak akurat|
|Cocok untuk portofolio besar|Kurang baik untuk data yang tidak stabil atau _fat-tailed_|
|Mudah diotomatisasi|Tidak menangkap risiko ekstrem/non-linear|
