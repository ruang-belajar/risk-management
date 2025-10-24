Berikut contoh **penerapan manajemen risiko dalam bidang _cyber security_**, berdasarkan kerangka **ISO 31000** dan praktik terbaik keamanan informasi (seperti ISO 27005 dan NIST SP 800-30):

---

## 🧩 **1. Konteks dan Tujuan**

Sebuah perusahaan fintech ingin melindungi data nasabah dan menjaga keandalan sistem transaksi digitalnya. Tujuan manajemen risiko adalah **meminimalkan dampak serangan siber dan memastikan kontinuitas layanan.**

---

## ⚙️ **2. Identifikasi Risiko (Risk Identification)**

Beberapa risiko yang diidentifikasi:

| No  | Risiko                        | Penyebab                              | Aset Terdampak          |
| --- | ----------------------------- | ------------------------------------- | ----------------------- |
| 1   | Serangan ransomware           | Email phishing, patch tidak terpasang | Server database nasabah |
| 2   | Pencurian data nasabah        | Kebocoran kredensial, insider threat  | Data pelanggan          |
| 3   | Serangan DDoS                 | Botnet, trafik berlebihan             | Website & API           |
| 4   | Malware di perangkat karyawan | USB tidak aman, antivirus usang       | Jaringan internal       |
| 5   | Kesalahan konfigurasi cloud   | Human error                           | Infrastruktur cloud     |

---

## ⚖️ **3. Analisis Risiko (Risk Analysis)**

Dilakukan analisis _likelihood_ (kemungkinan) dan _impact_ (dampak):

|Risiko|Kemungkinan|Dampak|Level Risiko|
|---|---|---|---|
|Ransomware|Tinggi|Sangat tinggi|**Ekstrem**|
|Data breach|Sedang|Sangat tinggi|**Tinggi**|
|DDoS|Tinggi|Sedang|**Tinggi**|
|Malware|Sedang|Sedang|**Sedang**|
|Cloud misconfiguration|Rendah|Tinggi|**Sedang**|

---

## 🧮 **4. Evaluasi Risiko (Risk Evaluation)**

Risiko dengan tingkat **Tinggi** dan **Ekstrem** menjadi prioritas utama untuk mitigasi.  
Misalnya:

- Ransomware → prioritas 1
    
- Data breach → prioritas 2
    
- DDoS → prioritas 3
    

---

## 🛡️ **5. Penanganan Risiko (Risk Treatment)**

Langkah mitigasi yang diambil:

|Risiko|Strategi|Tindakan Mitigasi|
|---|---|---|
|Ransomware|Mengurangi|Backup harian terenkripsi, patch management, pelatihan anti-phishing|
|Data breach|Menghindari|Multi-factor authentication, enkripsi data, kontrol akses ketat|
|DDoS|Mengurangi|Gunakan CDN & firewall, DDoS protection dari provider|
|Malware|Mengurangi|Endpoint protection, segmentasi jaringan, update rutin|
|Cloud misconfiguration|Mengurangi|Audit konfigurasi, _least privilege access_, _cloud security posture management (CSPM)_|

---

## 📊 **6. Monitoring dan Review**

- Audit keamanan dilakukan tiap 6 bulan.
    
- Uji penetrasi (_penetration test_) tahunan.
    
- _Incident response plan_ diuji dengan simulasi (_table-top exercise_).
    
- Risiko diperbarui sesuai perubahan teknologi dan ancaman baru.
    

---

## 🧠 **7. Komunikasi dan Pelaporan**

- Hasil manajemen risiko dilaporkan ke manajemen dan tim keamanan TI.
    
- Diterapkan kebijakan “security awareness” untuk semua karyawan.
    

---

### 🔐 **Contoh Nyata**

- **Tokopedia (2020)**: kebocoran data pengguna mendorong perusahaan meningkatkan _data encryption_ dan sistem deteksi dini.
    
- **Bank digital** menggunakan framework NIST Cybersecurity Framework untuk memantau risiko real-time pada infrastruktur cloud mereka.
    
