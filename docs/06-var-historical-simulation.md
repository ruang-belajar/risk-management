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

## 💹 Contoh Soal – Metode Historical Simulation

### Soal:

Sebuah portofolio memiliki data return harian selama 10 hari terakhir (dalam %):

|Hari|Return (%)|
|---|---|
|1|0.8|
|2|-0.3|
|3|0.5|
|4|-1.2|
|5|-0.8|
|6|0.2|
|7|-0.6|
|8|0.9|
|9|-1.5|
|10|-0.4|

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