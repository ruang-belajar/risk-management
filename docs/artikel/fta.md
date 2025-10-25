# Fault Tree Analysis

**Fault Tree Analysis (FTA)** adalah **metode analisis risiko dan keandalan sistem** yang digunakan untuk **mengidentifikasi penyebab potensial dari suatu kegagalan sistem** secara logis dan sistematis. Metode ini menelusuri **hubungan sebab-akibat antara kegagalan komponen dan kegagalan sistem secara keseluruhan**, dengan menggunakan **diagram berbentuk pohon terbalik (tree diagram)**.

---

## 🔹 Tujuan Fault Tree Analysis

FTA bertujuan untuk:

1. **Menemukan akar penyebab (root cause)** dari suatu kejadian atau kegagalan sistem.
    
2. **Menganalisis kemungkinan terjadinya kegagalan sistem** melalui kombinasi kegagalan komponen.
    
3. **Membantu pengambilan keputusan** dalam desain, operasi, dan pemeliharaan sistem agar lebih andal.
    
4. **Menentukan prioritas perbaikan** berdasarkan tingkat risiko dan probabilitas kegagalan.
    

---

## 🔹 Struktur Dasar FTA

FTA digambarkan sebagai **pohon logika terbalik**, di mana:

- **Top Event**: Kegagalan utama atau kejadian yang ingin dianalisis (misalnya: sistem tidak berfungsi).
    
- **Intermediate Events**: Peristiwa antara yang menjelaskan bagaimana top event dapat terjadi.
    
- **Basic Events**: Kegagalan dasar (komponen atau kesalahan manusia) yang menjadi akar penyebab.
    
- **Gate (Gerbang Logika)**: Simbol yang menghubungkan peristiwa-peristiwa, biasanya berupa:
    
    - **AND Gate (∧)** → Top event terjadi **jika semua** penyebab di bawahnya terjadi.
        
    - **OR Gate (∨)** → Top event terjadi **jika salah satu** penyebab di bawahnya terjadi.
        
![](img/Pasted%20image%2020251024223934.png)

---

## 🔹 Langkah-langkah Melakukan FTA

1. **Identifikasi top event**  
    Tentukan kejadian atau kegagalan sistem yang akan dianalisis.
    
2. **Bangun struktur pohon kesalahan**  
    Turunkan top event menjadi penyebab-penyebabnya menggunakan logika AND/OR.
    
3. **Identifikasi basic events**  
    Tentukan kejadian dasar yang menyebabkan intermediate event.
    
4. **Kuantifikasi probabilitas**  
    Jika data tersedia, hitung probabilitas terjadinya top event berdasarkan probabilitas setiap basic event.
    
5. **Evaluasi dan interpretasi hasil**  
    Gunakan hasil analisis untuk menentukan langkah mitigasi atau desain ulang sistem.
    

---

## 🔹 Contoh Diagram FTA

![](Pasted%20image%2020251024224912.png)

![](img/Pasted%20image%2020251024225207.png)

---

## 🔹 Kelebihan dan Kekurangan

|**Kelebihan**|**Kekurangan**|
|---|---|
|Memudahkan identifikasi penyebab kegagalan kompleks|Tidak cocok untuk sistem dengan banyak ketidakpastian|
|Dapat digunakan untuk analisis kuantitatif maupun kualitatif|Pembuatan pohon bisa rumit dan memakan waktu|
|Membantu prioritas mitigasi risiko|Membutuhkan data kegagalan yang akurat|

---
## 🔹 Kapan Menggunakan FTA

- **Industri Berisiko Tinggi** : Sempurna untuk sektor yang konsekuensi kegagalannya parah, seperti industri kedirgantaraan, tenaga nuklir, dan petrokimia.
    
- **Sistem Kompleks dengan Saling Ketergantungan** : Berguna untuk menganalisis sistem dengan banyak bagian yang saling berhubungan, di mana satu kegagalan dapat menyebabkan kegagalan lainnya.
    
- **Analisis Risiko Kuantitatif** : Ideal ketika pendekatan berbasis data diperlukan untuk menghitung probabilitas kegagalan menggunakan pohon kesalahan dan gerbang logika.
    
- **Kesalahan Manusia atau Peristiwa Eksternal** : Efektif untuk sistem yang terdampak oleh kesalahan manusia atau faktor eksternal, membantu memahami pengaruhnya terhadap keandalan sistem.

---

## 🔹 **Referensi**

- Ericson, C. A. (2005). _Hazard Analysis Techniques for System Safety._ Wiley.
    
- Vesely, W. E., Goldberg, F. F., Roberts, N. H., & Haasl, D. F. (1981). _Fault Tree Handbook (NUREG-0492)._ U.S. Nuclear Regulatory Commission.
    
- ISO 31010:2019 — _Risk Management — Risk Assessment Techniques._

- https://mahasiswaindonesia.id/metode-fault-tree-analysis-fta/
- https://creately-com.translate.goog/guides/fta-vs-fmea/
    
