# PROSES RISK AUDIT

## Contoh Skenario pada Perusahaan E-Commerce

---

## 1. Gambaran Umum Skenario

**Perusahaan**  
PT DigitalMart Indonesia – platform e-commerce nasional (marketplace)

**Model Bisnis**  
Marketplace yang menghubungkan penjual dan pembeli, dengan sistem pembayaran digital dan layanan logistik terintegrasi.

**Tujuan Strategis**

- Menjaga keandalan platform (high availability),
    
- Melindungi data pelanggan,
    
- Menjamin kepercayaan pengguna dan kepatuhan regulasi,
    
- Mendukung pertumbuhan transaksi secara berkelanjutan.
    

**Pendekatan Audit**  
Internal Audit menggunakan **Risk-Based Audit (RBA)**.

---

## 2. Tahap 1 – Penetapan Konteks dan Tujuan Audit

### Aktivitas Auditor

- Menelaah strategi bisnis e-commerce (growth, promo, scaling),
    
- Memahami **risk appetite** (misalnya: zero tolerance untuk data breach),
    
- Mengkaji kerangka manajemen risiko berbasis ISO 31000,
    
- Mengidentifikasi regulasi relevan (UU PDP, PCI-DSS, peraturan fintech).
    

### Tujuan Audit

Memberikan assurance atas efektivitas pengelolaan **risiko teknologi, keamanan data, dan operasional transaksi** pada platform e-commerce.

---

## 3. Tahap 2 – Identifikasi dan Penilaian Risiko Audit

### Aktivitas

Auditor:

- Menelaah **risk register perusahaan**,
    
- Melakukan workshop dengan IT, security, operations, dan compliance,
    
- Mengidentifikasi risiko dengan **residual risk tertinggi**.
    

### Contoh Risiko Utama E-Commerce

|Risiko|Likelihood|Impact|Level Risiko|
|---|---|---|---|
|Data breach pelanggan|Sedang|Sangat tinggi|Ekstrem|
|Downtime sistem saat peak sale|Tinggi|Tinggi|Tinggi|
|Fraud transaksi (fake order, refund abuse)|Tinggi|Sedang|Tinggi|
|Kegagalan settlement pembayaran|Rendah|Tinggi|Sedang|

### Hasil

Audit memprioritaskan:

- Risiko kebocoran data,
    
- Risiko downtime platform,
    
- Risiko fraud transaksi.
    

---

## 4. Tahap 3 – Penyusunan Risk-Based Audit Plan

### Ruang Lingkup Audit

- Infrastruktur IT & cloud,
    
- Sistem keamanan informasi,
    
- Proses pembayaran dan antifraud,
    
- Incident management & business continuity.
    

### Contoh Tujuan Audit

- Menilai efektivitas kontrol keamanan data pelanggan,
    
- Mengevaluasi kesiapan sistem menghadapi lonjakan transaksi,
    
- Menilai kecukupan kontrol pencegahan dan deteksi fraud.
    

### Kriteria Audit

- Kebijakan internal IT & security,
    
- ISO/IEC 27001,
    
- PCI-DSS,
    
- Best practice e-commerce.
    

---

## 5. Tahap 4 – Pelaksanaan Risk Audit

### 5.1 Evaluasi Desain Pengendalian Risiko

Auditor menilai apakah kontrol telah **dirancang memadai**.

**Contoh**

- Enkripsi data pelanggan tersedia,
    
- Sistem antifraud berbasis rule dan machine learning,
    
- Disaster Recovery Plan (DRP) terdokumentasi.
    

**Catatan**

- DRP belum diuji secara rutin.
    

---

### 5.2 Pengujian Efektivitas Pengendalian

Auditor melakukan:

- Review log keamanan dan incident ticket,
    
- Uji akses user (access control testing),
    
- Analisis data transaksi anomali,
    
- Observasi simulasi peak sale.
    

**Contoh Temuan**

- MFA belum diterapkan untuk seluruh admin,
    
- Fraud detection terlambat mengenali pola baru,
    
- Uji DRP terakhir dilakukan dua tahun lalu.
    

---

### 5.3 Penilaian Residual Risk

Auditor menilai apakah risiko setelah kontrol:

- Masih di atas risk tolerance,
    
- Memerlukan perbaikan segera.
    

**Hasil**

- Residual risk data breach masih tinggi,
    
- Risiko downtime meningkat saat event promo besar.
    

---

## 6. Tahap 5 – Pelaporan Hasil Risk Audit

### Contoh Struktur Temuan Audit Berbasis Risiko

**Risiko**  
Kebocoran data pelanggan

**Temuan**  
MFA tidak diterapkan pada seluruh akun privileged.

**Dampak**  
Potensi akses tidak sah dan pelanggaran UU PDP.

**Level Residual Risk**  
Tinggi

**Rekomendasi**

- Implementasi MFA mandatory untuk semua admin,
    
- Pengetesan penetrasi berkala,
    
- Peningkatan monitoring SIEM berbasis KRI.
    

---

## 7. Tahap 6 – Tindak Lanjut dan Risk Monitoring

### Aktivitas

- Manajemen menyusun action plan,
    
- Unit IT dan security melaksanakan perbaikan,
    
- Internal audit memantau implementasi.
    

### Contoh Indikator Monitoring

- Jumlah security incident,
    
- Persentase akun privileged dengan MFA,
    
- System uptime saat peak sale,
    
- Rasio fraud transaksi.
    

### Hasil

- Penurunan risiko data breach,
    
- Peningkatan stabilitas sistem saat campaign besar.
    

---

## 8. Ringkasan Alur Risk Audit pada E-Commerce

1. Memahami konteks bisnis digital,
    
2. Mengidentifikasi risiko teknologi dan transaksi,
    
3. Menyusun audit plan berbasis risiko,
    
4. Menguji desain dan efektivitas kontrol,
    
5. Menilai residual risk,
    
6. Melaporkan temuan berbasis risiko,
    
7. Memantau tindak lanjut secara berkelanjutan.
    

---

## 9. Nilai Pembelajaran dari Skenario

- Risk audit e-commerce sangat **technology-driven**,
    
- Fokus audit bergeser dari kepatuhan ke **keandalan platform dan trust pelanggan**,
    
- Risk-Based Audit memastikan area kritikal digital mendapat prioritas audit.
    

---

Jika Anda ingin, saya dapat:

- Mengubah skenario ini menjadi **studi kasus diskusi kelas**,
    
- Menyusun **contoh soal analisis risk audit e-commerce**, atau
    
- Membuat **pemetaan risiko–kontrol–audit test** khusus untuk platform digital.