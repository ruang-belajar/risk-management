# PASTA

PASTA (**Process for Attack Simulation and Threat Analysis**) adalah **metodologi terstruktur untuk analisis risiko keamanan** yang berfokus pada **ancaman (threats)** terhadap sistem informasi atau aplikasi. Metode ini banyak digunakan dalam **cyber risk management** dan **threat modeling**, karena membantu organisasi memahami bagaimana serangan bisa terjadi dan bagaimana cara menguranginya secara efektif.

---

## 🧩 Pengertian PASTA

PASTA dikembangkan oleh **Tony UcedaVélez dan Marco Morana**.  
Tujuan utamanya adalah untuk **menyelaraskan analisis risiko keamanan dengan tujuan bisnis**, bukan hanya sekadar menemukan kerentanan teknis.

Dengan kata lain, PASTA membantu menjawab pertanyaan:

> “Bagaimana potensi serangan terhadap sistem ini bisa berdampak pada tujuan bisnis organisasi?”

---

## ⚙️ Tahapan PASTA (7 Langkah Utama)

PASTA terdiri dari **tujuh tahap** yang terstruktur secara berurutan — dari pemahaman konteks bisnis hingga penentuan mitigasi risiko:

|**Tahap**|**Nama Tahapan**|**Tujuan Utama**|
|---|---|---|
|**1. Definition of the Objectives (Define Business Objectives)**|Menetapkan tujuan bisnis dan keamanan sistem.|Memahami _apa yang dilindungi_ dan _mengapa_ penting.|
|**2. Definition of the Technical Scope**|Mengidentifikasi lingkungan teknis (aplikasi, jaringan, API, dll.).|Menentukan batas sistem yang akan dianalisis.|
|**3. Application Decomposition and Analysis**|Memecah sistem menjadi komponen (modul, proses data, entitas pengguna).|Memahami bagaimana sistem bekerja dan di mana potensi titik serangan.|
|**4. Threat Analysis**|Mengidentifikasi potensi ancaman yang relevan terhadap sistem.|Menggunakan model seperti STRIDE, CAPEC, atau OWASP.|
|**5. Vulnerability & Weakness Analysis**|Menilai kerentanan teknis yang mungkin dieksploitasi oleh ancaman.|Menghubungkan ancaman dengan titik lemah nyata di sistem.|
|**6. Attack Modeling & Simulation**|Membuat simulasi serangan (attack trees, event trees, dsb).|Menilai bagaimana ancaman dapat direalisasikan.|
|**7. Risk & Impact Analysis**|Menentukan tingkat risiko (probabilitas × dampak) dan rekomendasi mitigasi.|Memberikan dasar keputusan bagi manajemen risiko.|

---

## 🧠 Fokus PASTA

- **Pendekatan berbasis risiko:** PASTA tidak hanya mencari bug, tapi mengukur risiko terhadap aset bisnis.
    
- **Threat-centric:** Fokus pada _threat actor_, _attack vector_, dan _potential impact_.
    
- **Berorientasi bisnis:** Setiap ancaman dikaitkan dengan dampaknya pada tujuan organisasi.
    
- **Terukur:** Menggunakan simulasi serangan dan skoring risiko.
    

---

## 🔐 Manfaat PASTA dalam Risk Management

1. **Menyediakan pandangan end-to-end** terhadap ancaman dan risiko.
    
2. **Menghubungkan tim teknis dan manajemen bisnis**, karena hasilnya dapat diterjemahkan dalam bahasa risiko (bukan hanya teknis).
    
3. **Membantu prioritisasi mitigasi**, karena risiko dihitung berdasarkan dampak terhadap bisnis.
    
4. **Meningkatkan keamanan desain sistem (secure by design)** sejak tahap awal pengembangan.
    

---

## 📘 Contoh Singkat

**Kasus:** Aplikasi e-commerce.  
PASTA digunakan untuk:

- Menentukan aset utama: data pelanggan, transaksi, sistem pembayaran.
    
- Menganalisis ancaman: serangan SQL injection, pencurian token autentikasi.
    
- Mensimulasikan serangan: attacker mencoba bypass login dan mengakses database.
    
- Menilai risiko: kemungkinan tinggi, dampak finansial besar.
    
- Rekomendasi: penerapan _input validation_, _parameterized queries_, dan _WAF_.
    

---

## 🧾 **Referensi**

- UcedaVélez, T. & Morana, M. (2015). _Risk Centric Threat Modeling: Process for Attack Simulation and Threat Analysis (PASTA)_. Wiley.
    
- OWASP Threat Modeling Methodologies.
    
- NIST SP 800-30 Rev.1: _Guide for Conducting Risk Assessments_.
    

---

Apakah Anda ingin saya buatkan **contoh diagram PASTA** (misalnya alur 7 tahap dalam konteks sistem informasi)? Itu bisa membantu memvisualkan prosesnya.