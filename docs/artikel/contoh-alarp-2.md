# **Contoh Kasus Evaluasi Risiko (ALARP) – Pembangunan Sistem E-Commerce**

## **Latar Belakang**

Sebuah perusahaan retail sedang membangun **platform e-commerce baru** untuk memperluas penjualan online. Selama fase pengembangan, tim manajemen risiko mengidentifikasi risiko utama terkait keamanan data dan kelancaran operasional.

Salah satu risiko kritis adalah:

### **Risiko: Kebocoran Data Pelanggan (Data Breach)**

Termasuk:

- Nama, alamat, nomor telepon
    
- Riwayat transaksi
    
- Informasi pembayaran (tokenized, bukan raw card data)
    

### **Informasi Risiko Awal**

- Probabilitas terjadinya serangan yang berhasil: **P = 1×10⁻³ per bulan**
    
- Dampak jika terjadi:
    
    - Kerugian finansial: **Rp 5.000.000.000** (biaya pemulihan, kompensasi, downtime)
        
    - Hilangnya reputasi → pelanggan berkurang 10–20%
        
    - Potensi denda regulasi (misalnya karena pelanggaran PDP)
        

### **Kategori Risiko Awal**

- Level: **High / Unacceptable**
    

---

# **Alternatif Pengendalian Risiko**

|Opsi|Deskripsi Mitigasi|Dampak pada Probabilitas / Dampak|Biaya Implementasi|
|---|---|---|---|
|A|Implementasi Web Application Firewall (WAF) + patch rutin|Mengurangi probabilitas menjadi 1×10⁻⁴|Rp 300.000.000|
|B|Penerapan **Zero-Trust Architecture** pada seluruh layanan|Menurunkan probabilitas menjadi 1×10⁻⁵|Rp 2.000.000.000|
|C|Enkripsi data pelanggan menggunakan AES-256 + tokenisasi penuh|Tidak mengubah probabilitas; tetapi mengurangi kerusakan (kerugian finansial turun 60%)|Rp 700.000.000|

---

## **Batas ALARP Perusahaan (Monthly Risk Criteria)**

|Kategori|Probabilitas|
|---|---|
|Unacceptable|> 1×10⁻⁴|
|ALARP region|1×10⁻⁵ – 1×10⁻⁴|
|Acceptable|< 1×10⁻⁵|

---

# **Pertanyaan**

1. Tentukan posisi **risiko awal** dalam matriks ALARP berdasarkan probabilitas yang diberikan.
    
2. Untuk setiap opsi mitigasi (A, B, C):  
    a. Tentukan apakah risiko setelah mitigasi berada pada kategori **Unacceptable**, **ALARP**, atau **Acceptable**.  
    b. Nilai apakah biaya mitigasi **reasonable** menurut prinsip ALARP (gunakan analisis sederhana proporsionalitas _biaya vs penurunan risiko_).
    
3. Rekomendasikan mitigasi terbaik berdasarkan prinsip ALARP dan jelaskan alasan Anda.
    

---

# **KUNCI JAWABAN / PEMBAHASAN**

## **1. Kategori Risiko Awal**

- Probabilitas = 1×10⁻³
    
- Batas unacceptable = >1×10⁻⁴  
    → **1×10⁻³ > 1×10⁻⁴ → Risiko berada pada kategori UNACCEPTABLE**
    

---

## **2. Evaluasi Setiap Opsi Mitigasi**

### **Opsi A: Web Application Firewall (WAF)**

- Probabilitas baru = 1×10⁻⁴  
    → Masuk **ALARP region**
    
- Penurunan risiko = dari 10⁻³ → 10⁻⁴ (10× lebih kecil)
    
- Biaya = Rp 300 juta (relatif rendah untuk risk reduction signifikan)
    

**Kesimpulan:**  
→ Cost-effective → **wajar secara ALARP**

---

### **Opsi B: Zero-Trust Architecture**

- Probabilitas baru = 1×10⁻⁵  
    → Masuk **Acceptable region**
    
- Penurunan risiko sangat besar (dari 10⁻³ → 10⁻⁵)
    
- Biaya = Rp 2 miliar (sangat tinggi)
    
- _Marginal improvement_ dari 10⁻⁴ → 10⁻⁵ kecil dibanding selisih biaya (dibanding jika sudah menerapkan Opsi A)
    

**Kesimpulan:**  
→ Walau hasilnya sangat baik, biaya mungkin **tidak proporsional**  
→ ALARP tidak mewajibkan mitigasi ini, kecuali regulasi atau strategi jangka panjang membutuhkannya

---

### **Opsi C: Enkripsi + Tokenisasi**

- Probabilitas tidak berubah (tetap 10⁻³ tanpa mitigasi lain → tetap unacceptable)
    
- _Namun_, kerugian ketika breach turun 60%
    
- Probabilitas masih unacceptable → risiko tetap tinggi
    
- Biaya = Rp 700 juta  
    → Dampak berkurang signifikan, tetapi tidak menggeser probabilitas ke zona ALARP/acceptable
    

**Kesimpulan:**  
→ Tidak memindahkan risiko ke level ALARP → **tidak memadai sebagai mitigasi utama**  
→ Namun penting sebagai _complementary control_, bukan mitigasi utama probabilitas.

---

## **3. Rekomendasi Opsi Terbaik (Pendekatan ALARP)**

### **Mitigasi yang direkomendasikan:**

### **➡ Opsi A (WAF + patching)**

**Alasan:**

- Menggeser risiko dari **unacceptable → ALARP region**
    
- Biaya paling rendah di antara opsi
    
- Pengurangan risiko signifikan (90%)
    
- Sesuai prinsip ALARP: penurunan risiko yang besar dengan biaya yang wajar
    

### Opsi B dapat dipertimbangkan:

- Jika perusahaan ingin mencapai risiko acceptable
    
- Jika platform e-commerce diproyeksikan menangani data sensitif dalam jumlah sangat besar
    
- Jika ada regulasi ketat terkait keamanan data
    

### Opsi C bukan mitigasi utama ALARP:

- Cocok sebagai kontrol tambahan setelah risiko berada pada wilayah ALARP/acceptable.
    

