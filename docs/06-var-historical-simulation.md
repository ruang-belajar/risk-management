## 💡 Konsep Dasar Historical Simulation (HS)

Pendekatan **Historical Simulation (HS)** adalah metode **non-parametrik** untuk menghitung _Value at Risk (VaR)_ — artinya, metode ini **tidak mengasumsikan bentuk distribusi tertentu** (seperti normal) atas data return atau kerugian masa lalu.

Dengan HS, kita **menggunakan data historis aktual** untuk memperkirakan kemungkinan kerugian di masa depan, dengan asumsi bahwa **pola risiko masa lalu akan berulang**.

---

## ⚙️ Langkah-langkah Perhitungan VaR dengan Historical Simulation

Berikut tahapan lengkapnya:

### Langkah 1: Kumpulkan data historis

Kumpulkan **data historis nilai aset, portofolio, atau pendapatan** selama periode tertentu (misalnya 1 tahun terakhir, 250 hari kerja).

Dalam konteks proyek IT:

- Data bisa berupa **kerugian harian akibat downtime**, **fluktuasi biaya operasional**, atau **perubahan nilai proyek IT**.
    
- Contoh data: nilai harian pendapatan dari sistem SaaS perusahaan IT selama 250 hari.
    

|Hari|Nilai Pendapatan (Rp)|
|---|---|
|1|1.000.000.000|
|2|995.000.000|
|3|1.010.000.000|
|...|...|

---

### Langkah 2: Hitung _return_ atau _loss_ harian

Dari data historis, hitung perubahan nilai (return atau loss) setiap periode.  
Jika menggunakan _return harian relatif_:

$R_t = \frac{V_t - V_{t-1}}{V_{t-1}}$

atau jika fokusnya pada kerugian absolut:

$L_t = V_{t-1} - V_t$

Contoh (dalam Rp):

|Hari|Pendapatan (Rp)|Loss (Rp)|
|---|---|---|
|1|1.000.000.000|-|
|2|995.000.000|5.000.000|
|3|1.010.000.000|-15.000.000|
|4|980.000.000|30.000.000|
|...|...|...|

---

### Langkah 3: Susun distribusi kerugian historis

Kumpulkan seluruh data kerugian harian (_losses_), lalu **urutkan dari yang terbesar (paling negatif) hingga terkecil** (paling positif).

Contoh urutan kerugian historis (dalam Rp):

|Rank|Loss (Rp)|
|---|---|
|1|70.000.000|
|2|50.000.000|
|3|45.000.000|
|...|...|
|250|-25.000.000|

---

### Langkah 4: Tentukan tingkat kepercayaan (confidence level)

Tentukan tingkat keyakinan (_confidence level_) yang diinginkan, biasanya:

- **95%** → risiko ekstrem 5%
    
- **99%** → risiko ekstrem 1%
    

Untuk data 250 hari (setahun), maka:

- Untuk 95% → ambil persentil ke **5% terburuk**, yaitu data ke-**13** (karena 5% × 250 = 12.5)
    
- Untuk 99% → ambil persentil ke-**3** (karena 1% × 250 = 2.5)
    

---

### Langkah 5: Tentukan nilai VaR

Nilai VaR adalah **nilai kerugian pada persentil tersebut**.

Misal:

- Dari urutan loss, nilai loss ke-13 = **Rp 40.000.000**
    
- Maka **VaR 95% = Rp 40.000.000**
    

Artinya:

> Dengan tingkat keyakinan 95%, kerugian harian **tidak akan melebihi Rp 40 juta**, berdasarkan data historis.

---

### Langkah 6: Interpretasi hasil

VaR tidak menunjukkan kerugian maksimum, melainkan batas probabilistik:

- Ada **5% kemungkinan** kerugian **lebih besar dari Rp 40 juta** (dalam contoh 95% VaR).
    
- Dapat digunakan untuk menetapkan **limit risiko** atau **buffer modal cadangan**.
    

---

## 🔍 Kelebihan & Kelemahan Metode Historical Simulation

|**Kelebihan**|**Kelemahan**|
|---|---|
|Tidak perlu asumsi distribusi|Tidak bisa memprediksi kejadian ekstrem baru|
|Menggunakan data aktual (lebih realistis)|Butuh data historis cukup panjang|
|Mudah diimplementasikan|Tidak responsif terhadap perubahan kondisi pasar atau sistem|


---

## Menentukan Nilai Kuartil

Perbedaan **metode interpolasi** dan **tanpa interpolasi (empiris)** dalam perhitungan VaR pada Historical Simulation terletak pada **cara menentukan nilai kuantil (percentile)** dari data kerugian historis.  
Penjelasan berikut fokus pada konteks Excel karena proses VaR biasanya dihitung menggunakan `PERCENTILE.INC` / `PERCENTILE.EXC` (interpolasi) dan vs **sorted empirical percentile** (tanpa interpolasi).

### ⭐ 1. Metode **Interpolasi**

#### Bagaimana cara kerjanya?

- Menghitung kuantil (misalnya 5% atau 1%) dengan **menginterpolasi** nilai antara dua observasi terdekat.
    
- Digunakan oleh fungsi Excel seperti:
    
    - `PERCENTILE.INC`
        
    - `PERCENTILE.EXC`
        
- Hasil kuantil bisa **berada di antara dua data** — artinya bukan angka yang benar-benar ada di dataset.
    
#### Contoh:

Misalkan data P&L yang sudah diurutkan (ascending):

```
[-30.000, -20.000, -12.000, -8.000, -5.000, ...]
```

Jika ingin kuantil 5%, Excel menghitung posisi:

$$pos = (n-1) \times p + 1 = 9 \times 0.05 + 1 = 1.45$$

Artinya nilai kuantil ada **45% di antara nilai pertama & kedua**.  
Maka kuantil =  
$$-30.000 + 0.45 \times (-20.000 + 30.000) = -25.500$$

→ **Hasil kuantil = -25.500**, padahal angka ini tidak ada di dataset.

#### Kelebihan:

- Lebih **halus**, tidak sensitif terhadap ukuran sampel kecil.
    
- Digunakan pada banyak software statistik, konsisten secara matematis.
    
- Cocok ketika dataset besar (250–1000 observasi).
    

#### Kekurangan:

- Hasilnya **bukan nilai historis nyata**.
    
- Bagi sebagian risk manager/regulator, ini dianggap “kurang murni” karena historical VaR seharusnya memakai data sebenarnya.
    

---

### ⭐ 2. Metode **Tanpa Interpolasi** (Empirical / Non-parametric)

#### Bagaimana cara kerjanya?

- Menentukan kuantil dengan **memilih langsung** observasi ke-k pada data yang sudah diurutkan, **tanpa menghitung titik di antaranya**.
    
- Dikenal sebagai _Order Statistic_ atau _Empirical Quantile_.
    
- Ini adalah metode VaR yang dianggap paling “murni” untuk Historical Simulation.
    

#### Rumus posisi umum:

$$k = \lceil n \times p \rceil$$

Contoh 10 data & 5% quantile:

- $10 \times 0.05 = 0.5$
    
- Round up → k = 1
    

→ Kuantil = **observasi pertama** (nilai terendah) = −30.000  
**Tidak ada interpolasi.**

#### Kelebihan:

- Menggunakan **nilai historis 100% apa adanya**.
    
- Lebih mudah dijelaskan dan dipahami.
    
- Sesuai dengan konsep VaR historis klasik:  
    _“What was the worst X% of actual losses in history?”_
    

#### Kekurangan:

- Hasil dapat berubah drastis jika dataset kecil (sensitif terhadap sampel).
    
- Bisa tidak stabil untuk 1% VaR jika observasi sedikit.
    

---

### ⭐ 3. Perbedaan Inti (Ringkas)

|Aspek|Interpolasi|Tanpa Interpolasi (Empiris)|
|---|---|---|
|Dasar metode|Mengambil nilai di antara dua data (linear interpolation)|Mengambil data apa adanya (order statistic)|
|Hasil kuantil|Bisa nilai baru yang tidak ada di dataset|Selalu nilai yang benar-benar ada di dataset|
|Stabilitas|Lebih halus, lebih stabil|Bisa loncat-loncat pada dataset kecil|
|Digunakan Excel?|Ya (`PERCENTILE.INC`, `PERCENTILE.EXC`)|Tidak langsung, harus sorting + pilih observasi ke-k|
|Cocok untuk|Dataset besar atau kebutuhan analisis statistik|VaR historis murnih / backtesting|
|Regulasi|Beberapa regulator prefer empirical (contohnya Basel untuk backtesting)|Umumnya diterima dalam praktik konservatif|


---
## 💹 Contoh Soal – Metode Historical Simulation

### Soal:

Sebuah portofolio memiliki data return harian selama 10 hari terakhir (dalam %):

| Hari | Return (%) |
| ---- | ---------- |
| 1    | 0.8        |
| 2    | -0.3       |
| 3    | 0.5        |
| 4    | -1.2       |
| 5    | -0.8       |
| 6    | 0.2        |
| 7    | -0.6       |
| 8    | 0.9        |
| 9    | -1.5       |
| 10   | -0.4       |

Nilai portofolio saat ini = **Rp 2.000.000.000**.  
Hitung **VaR harian** dengan tingkat kepercayaan **90%** menggunakan **Historical Simulation Method**.

### Langkah Penyelesaian:

1. **Urutkan return dari yang paling kecil hingga terbesar:**
    

|Urutan|Return (%)|
|---|---|
|1|-1.5|
|2|-1.2|
|3|-0.8|
|4|-0.6|
|5|-0.4|
|6|-0.3|
|7|0.2|
|8|0.5|
|9|0.8|
|10|0.9|

2. **Tentukan persentil ke-10 (karena confidence 90% → 10% sisi kiri).**  
    Dari 10 data, nilai ke-1 (10%) adalah **-1.5%**.
    
3. **Hitung nilai kerugian maksimum:**      $$VaR = 1.5\% \times 2.000.000.000 = 0.015 \times 2.000.000.000$$
$$\boxed{VaR = Rp 30.000.000}$$

### ✅ Jawaban:

Value at Risk (VaR) harian pada tingkat kepercayaan 90% adalah **Rp 30 juta**.  
Artinya, dengan keyakinan 90%, kerugian tidak akan melebihi **Rp 30 juta** dalam 1 hari.


---

## 📊 Contoh sederhana — proyek IT

**Kasus:**  
Perusahaan IT ingin menghitung VaR harian dari potensi kehilangan pendapatan akibat _downtime sistem online store_.

**Data 10 hari terakhir (kerugian harian, Rp):**

|Hari|Loss (Rp)|
|---|---|
|1|1.000.000|
|2|2.500.000|
|3|0|
|4|10.000.000|
|5|5.000.000|
|6|2.000.000|
|7|15.000.000|
|8|8.000.000|
|9|0|
|10|12.000.000|

**Langkah:**

1. Urutkan dari besar ke kecil:  
    [15.000.000, 12.000.000, 10.000.000, 8.000.000, 5.000.000, 2.500.000, 2.000.000, 1.000.000, 0, 0]
    
2. Tentukan tingkat kepercayaan 95% (5% * 10 data = 0,5 → ambil data ke-1)
    
3. Maka:  
    **VaR 95% = Rp 15.000.000**
    

**Interpretasi:**  
Ada kemungkinan 5% bahwa kerugian harian melebihi Rp 15 juta akibat downtime sistem.

---

## 💼 Diskusi & Tugas

### Soal 1 - VaR Historical Simulation

| Hari Ke-       | Pendapatan Harian |
| -------------- | ----------------- |
| investasi awal | **100000000**     |
| 1              | 100800000         |
| 2              | 99300000          |
| 3              | 100500000         |
| 4              | 100100000         |
| 5              | 100200000         |
| 6              | 102300000         |
| 7              | 101400000         |
| 8              | 101900000         |
| 9              | 100000000         |
| 10             | 100200000         |
| 11             | 100050000         |
| 12             | 101850000         |
| 13             | 102450000         |
| 14             | 101700000         |
| 15             | 102000000         |
| 16             | 99500000          |
| 17             | 100900000         |
| 18             | 100850000         |
| 19             | 101550000         |
| 20             | 102550000         |

Buat template Excel untuk menghitung VaR menggunakan pendekatan Historical Simulation.

Asumsi, investasi awal adalah **Rp. 100.000.000**