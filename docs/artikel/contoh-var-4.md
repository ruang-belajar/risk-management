## Contoh Kasus VaR Metode Monte Carlo
### Skenario Kasus

- **Aset:** Sebuah portofolio perdagangan opsi (derivatif) yang kompleks.
    
- **Nilai Portofolio (Awal):** Rp500.000.000.
    
- **Periode Waktu $(\Delta t)$:** 1 Hari.
    
- **Tingkat Kepercayaan:** 99%.
    
- **Asumsi Input (dari data historis):**
    
    - Rata-rata _return_ harian $(\mu) = 0,05\%$
        
    - Volatilitas (deviasi standar _return_ harian) $(\sigma) = 1,8\%$
        
- **Jumlah Simulasi:** 10.000 skenario (semakin banyak, semakin akurat).
    

### Langkah-Langkah Perhitungan

#### 1. Membangun Model Perubahan Harga

Perubahan harga aset (atau nilai portofolio) dimodelkan menggunakan persamaan pergerakan geometrik Brownian (Geometric Brownian Motion) atau model lain yang sesuai. Untuk periode singkat (1 hari), perubahan harga aset $\Delta S$ dapat disimulasikan sebagai:

$$\Delta S = S_0 \cdot (\mu \Delta t + \sigma \sqrt{\Delta t} Z)$$

Di mana:

- $S_0$ = Nilai portofolio awal (Rp500.000.000).
    
- $\Delta t$ = Periode waktu (1/252 jika 1 hari kerja).
    
- $Z$ = Bilangan acak yang ditarik dari distribusi normal standar (rata-rata 0, deviasi standar 1).
    

#### 2. Melakukan Simulasi (10.000 Kali)

Kita mengulangi perhitungan perubahan nilai portofolio $(\Delta S)$ sebanyak 10.000 kali, menghasilkan 10.000 kemungkinan nilai portofolio pada akhir hari $(S_1 = S_0 + \Delta S)$.

|**Simulasi Ke-**|**Bilangan Acak Z (Contoh)**|**Perubahan Nilai Portofolio ΔS**|**Nilai Portofolio Akhir (S1​)**|
|---|---|---|---|
|1|0,55|Rp4.950.000|Rp504.950.000|
|2|-1,88|-Rp18.750.000|Rp481.250.000|
|...|...|...|...|
|10.000|0,12|Rp1.230.000|Rp501.230.000|

#### 3. Menghitung Kerugian

Dari 10.000 hasil $S_1$, kita hitung kerugian/keuntungan (Profit & Loss / P&L) untuk setiap skenario:

$$\text{P\&L} = S_1 - S_0$$

#### 4. Mengurutkan Hasil dan Menentukan VaR

Urutkan 10.000 hasil P&L dari kerugian terbesar (negatif terbesar) hingga keuntungan terbesar (positif terbesar).

- **Tingkat Kepercayaan 99%** berarti kita mencari persentil ke-$(100\% - 99\%)$ atau **persentil ke-1** dari distribusi kerugian/keuntungan.
    
- Jumlah observasi yang dicari: $10.000 \times 1\% = \text{observasi ke-}100$.
    

Kita mencari nilai P&L yang berada pada posisi ke-100 dari daftar yang diurutkan (mulai dari kerugian terburuk).

- **Asumsi Hasil Simulasi:** Setelah diurutkan, P&L pada posisi ke-100 (persentil ke-1) adalah **-Rp19.500.000**.
    

### Hasil VaR Monte Carlo

$$\text{VaR (99\%, 1 Hari)} = |\text{P\&L pada persentil ke-}1|$$

$$\text{VaR (99\%, 1 Hari)} = \text{Rp19.500.000}$$

### Interpretasi

Dengan menggunakan 10.000 skenario simulasi Monte Carlo, kerugian maksimum yang diperkirakan terjadi pada portofolio derivatif ini dalam satu hari ke depan, dengan tingkat kepercayaan **99%**, adalah **Rp19.500.000**.

Ini berarti, dalam 100 hari (atau skenario), kita hanya memperkirakan 1 hari (atau 1 skenario, yaitu 1%) di mana kerugian portofolio akan melebihi Rp19.500.000.