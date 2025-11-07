## 💹 **Contoh Soal – Metode Historical Simulation**

### **Soal:**

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

---

### **Langkah Penyelesaian:**

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

---

### ✅ **Jawaban:**

Value at Risk (VaR) harian pada tingkat kepercayaan 90% adalah **Rp 30 juta**.  
Artinya, dengan keyakinan 90%, kerugian tidak akan melebihi **Rp 30 juta** dalam 1 hari.
