## 💡 **Konsep Dasar Parametric VaR**

Metode **Parametric (Variance–Covariance)** disebut juga **Analytical VaR** karena menggunakan **distribusi statistik** (biasanya _normal distribution_) untuk memperkirakan potensi kerugian.

Metode ini **tidak memerlukan simulasi data historis** — cukup dengan nilai rata-rata (_mean_) dan simpangan baku (_standard deviation, σ_) dari return aset atau proyek yang dianalisis.


---
## Langkah-langkah Perhitungan VaR (Pendekatan Parametric / Variance–Covariance) 

## 1) Definisikan tujuan dan parameter analisis

- **Horizon waktu** (mis. 1 hari, 10 hari).
    
- **Confidence level** (mis. 95% atau 99%).
    
- **Nilai portofolio** atau eksposur finansial (V) (mis. Rp 1.200.000.000).
    
- **Apakah VaR untuk satu aset atau portofolio multi-aset?**
    
- **Sumber data**: gunakan return historis untuk estimasi volatilitas dan korelasi.
    
---
## 2) Pilih nilai Z (z-score) sesuai tingkat kepercayaan

Nilai $Z$ adalah z-score dari distribusi normal standar untuk area kumulatif sama dengan confidence level.

Contoh umum:

- 90% → $Z \approx 1{,}282$
    
- 95% → $Z \approx 1{,}645$ (sering dibulatkan 1,65)
    
- 99% → $Z \approx 2{,}326$ (sering dibulatkan 2,33)
    

> 💡 EXCEL: Gunakan `NORM.S.INV(confidence)`  
> 💡 Python: Gunakan  `scipy.stats.norm.ppf()` 

---

## 3) Hitung volatilitas (standar deviasi) dari return

### Langkah 1 — Kumpulkan data harga historis

Misalnya, harga harian saham IT perusahaan:

| Tanggal | Harga (Rp) |
| ------- | ---------- |
| 1       | 1.000      |
| 2       | 1.020      |
| 3       | 1.010      |
| 4       | 1.030      |
| 5       | 1.050      |

### Langkah 2 — Hitung return harian

Gunakan simple return:
$$Rt =\frac{P_t - P_{t-1}}{P_{t-1}}$$​

| Hari | Harga | Return                                  |
| ---- | ----- | --------------------------------------- |
| 1    | 1.000 | —                                       |
| 2    | 1.020 | (1020−1000)/1000 = 0.02 = **2%**        |
| 3    | 1.010 | (1010−1020)/1020 = −0.0098 = **−0.98%** |
| 4    | 1.030 | (1030−1010)/1010 = 0.0198 = **1.98%**   |
| 5    | 1.050 | (1050−1030)/1030 = 0.0194 = **1.94%**   |

### Langkah 3 — Hitung rata-rata return

$$R= \frac{0.02+(−0.0098)+0.0198+0.01944}{4} = 0.01235 = 1.235\%$$

### Langkah 4 — Hitung deviasi setiap hari dari rata-rata

$$(Rt−R)^2$$

|Hari|Return|Deviasi dari rata-rata|Kuadrat deviasi|
|---|---|---|---|
|2|0.0200|0.0200−0.01235=0.00765|0.00005852|
|3|−0.0098|−0.0098−0.01235=−0.02215|0.0004906|
|4|0.0198|0.0198−0.01235=0.00745|0.0000555|
|5|0.0194|0.0194−0.01235=0.00705|0.0000497|
### Langkah 5 — Hitung varians dan standar deviasi

$$Varians=\frac{(Rt−Rˉ)^2}{Pn−1}$$$$=\frac{0.00005852+0.0004906+0.0000555+0.0000497}{3}=\frac {0.0006543}{3}=0.0002181$$
$$\sigma = \sqrt{0.0002181} = 0.01477 = 1.477\%$$

**Volatilitas harian = 1.477%**

---

## 4. portofolio multi-aset: buat vektor bobot & matriks kovarians

Untuk volatilitas lebih dari satu aset, check [Volatilitas Multi Aset](artikel/volatilitas-multi-aset.md)

---

## 5. Rumus VaR parametric (satu aset, linear)

Rumus VaR parametric (1 aset)
$$\text{VaR} = Z \times \sigma \times V$$  
Keterangan:
- $Z$ = z-score untuk confidence level
- $\sigma$ = standar deviasi return per horizon
- $V$ = nilai portofolio (moneter)
  
---

## 6. Perhitungan menggunakan program

### Excel

- Return: `=(B3-B2)/B2`
    
- Volatilitas (std dev): `=STDEV(range_return)`
    
- Untuk annualized (250 hari kerja): `=STDEV(range_return)*SQRT(250)`
    

### Python
```python
import numpy as np
returns = np.array([0.02, -0.0098, 0.0198, 0.0194])
volatility = np.std(returns, ddof=1)
```

---

## 6) Scaling untuk horizon waktu (jika berbeda dari satu unit)

Jika $\sigma$ dihitung per hari dan Anda ingin VaR untuk (t) hari (asumsi return iid dan Brownian scaling):  
$$\sigma_{t} = \sigma \sqrt{t}$$  
Sehingga:  
$$\text{VaR}_{t} = Z \times \sigma \sqrt{t} \times V$$

Catatan: scaling √t valid untuk jangka pendek bila asumsi independensi & normalitas berlaku; untuk jangka panjang ini sering meleset.

---

## 7) Konversi ke kerugian moneter dan interpretasi tanda

- Rumus di atas memberi **jumlah uang** (positif) yang merepresentasikan _potensi kerugian maksimum_ pada confidence level.
    
- Interpretasi: “Dengan confidence 95%, kerugian tidak akan melebihi VaR dalam horizon yang ditentukan (dalam kondisi normal pasar).”

---

## 8. Contoh Kasus: Proyek IT

**Kasus:**  
Sebuah perusahaan cloud service memiliki nilai operasional tahunan setara Rp 10 miliar.  
Dari data historis harian pendapatan, diperoleh:

- σ = 1.8%
    
- μ = 0.2%  
    Hitung VaR harian 99%.

**Langkah-langkah:**
Gunakan rumus:
$$\text{VaR} = Z \times \sigma \times V$$

1. Z untuk 99% = 2.33    
2. VaR = 2.33 × 1.8% × 10.000.000.000 = **Rp 399.000.000**
 
**Interpretasi:**  
Dengan keyakinan 99%, kerugian harian akibat fluktuasi pendapatan cloud service **tidak akan melebihi Rp 399 juta**.  
Namun, **ada 1% kemungkinan** kerugian akan lebih besar dari itu.

---

## 9. Rangkuman Rumus Utama

| Simbol     | Keterangan                              | Rumus                                     |
| :--------- | :-------------------------------------- | :---------------------------------------- |
| $R_t$      | Return periode ke-t                     | $\frac{V_t - V_{t-1}}{V_{t-1}}$           |
| $\mu$      | Rata-rata return                        | $\frac{\sum R_t}{n}$                      |
| $\sigma$   | Standar deviasi                         | $\sqrt{\frac{\sum (R_t - \mu)^2}{n - 1}}$ |
| $Z$        | Nilai Z pada tingkat keyakinan tertentu | mis. 1.65 untuk 95%                       |
| $VaR$      | Value at Risk (dalam %)                 | $Z \times \sigma - \mu$                   |
| $VaR_{Rp}$ | Value at Risk (dalam nominal)           | $VaR \times Nilai\ Portofolio$            |

---

## 10. Kelebihan dan Kelemahan Metode Parametric

| **Kelebihan**                | **Kelemahan**                                              |
| ---------------------------- | ---------------------------------------------------------- |
| Cepat dan sederhana          | Asumsi distribusi normal bisa tidak akurat                 |
| Cocok untuk portofolio besar | Kurang baik untuk data yang tidak stabil atau _fat-tailed_ |
| Mudah diotomatisasi          | Tidak menangkap risiko ekstrem/non-linear                  |
