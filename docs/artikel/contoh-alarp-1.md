
# **Contoh Kasus Evaluasi Risiko dengan Pendekatan ALARP - Kebocoran Gas**

## **Latar Belakang Kasus**

Sebuah perusahaan manufaktur kimia memiliki fasilitas penyimpanan gas bertekanan. Salah satu risiko utama adalah **kebocoran gas** yang dapat menyebabkan **ledakan** atau **paparan toksik**. Tim manajemen risiko melakukan analisis kuantitatif awal dan mendapatkan informasi berikut:

### **Data Risiko**

- Potensi kejadian: **Kebocoran gas dari tangki utama**
    
- Frekuensi estimasi: **1 kali dalam 10.000 jam operasi** (probabilitas = 1×10⁻⁴ per jam)
    
- Dampak jika terjadi:
    
    - Cedera serius pada pekerja
        
    - Potensi kematian (fatality)
        
    - Kerusakan aset hingga **Rp 2.000.000.000**
        
- Tingkat risiko awal: **High**
    

### **Opsi Pengendalian**

Tim teknis mengusulkan tiga alternatif perbaikan:

|Opsi Mitigasi|Deskripsi|Efektivitas Penurunan Risiko|Biaya Implementasi|
|---|---|---|---|
|A|Pemasangan _gas detection system_|Mengurangi frekuensi kejadian menjadi 1×10⁻⁵|Rp 150.000.000|
|B|Penggantian material tangki dengan stainless steel grade tinggi|Mengurangi frekuensi menjadi 1×10⁻⁶|Rp 1.000.000.000|
|C|Penambahan dinding pelindung (blast wall)|Mengurangi dampak sebesar 60%|Rp 600.000.000|

### **Batas ALARP Perusahaan**

- **Unacceptable region:** probabilitas > 1×10⁻⁵ per jam
    
- **ALARP region:** 1×10⁻⁶ – 1×10⁻⁵ per jam
    
- **Acceptable region:** < 1×10⁻⁶ per jam
    

---

# **Pertanyaan**

1. Berdasarkan batas ALARP, tentukan posisi risiko awal berada pada kategori apa.
    
2. Evaluasi setiap opsi mitigasi (A, B, dan C):  
    a. Risiko setelah mitigasi apakah masuk kategori acceptable, ALARP, atau unacceptable?  
    b. Apakah biaya mitigasi wajar menurut prinsip **ALARP** (as low as reasonably practicable)?  
    (Gunakan penilaian sederhana berbasis _cost vs risk reduction_).
    
3. Rekomendasikan opsi mitigasi mana yang sebaiknya dipilih menurut pendekatan ALARP. Jelaskan alasannya.
    

---

# **Kunci Jawaban / Pembahasan**

## **1. Posisi risiko awal**

- Frekuensi awal = 1×10⁻⁴
    
- Batas unacceptable = >1×10⁻⁵  
    → Karena 1×10⁻⁴ > 1×10⁻⁵ → **Risiko berada pada kategori UNACCEPTABLE**
    

---

## **2. Evaluasi Setiap Opsi Mitigasi**

### **Opsi A: Gas Detection System**

- Frekuensi baru = 1×10⁻⁵  
    → Termasuk **ALARP region**
    
- Penurunan risiko = dari 1×10⁻⁴ ke 1×10⁻⁵ (90% reduction)
    
- Biaya = Rp 150 juta → relatif rendah  
    **Kesimpulan:**  
    → **Biaya wajar** untuk pengurangan risiko sebesar ini → **Layak diterapkan dalam prinsip ALARP**
    

---

### **Opsi B: Penggantian Material Tangki**

- Frekuensi baru = 1×10⁻⁶ → **Acceptable region**
    
- Penurunan risiko = dari 1×10⁻⁴ ke 1×10⁻⁶ (99% reduction)
    
- Biaya = Rp 1 miliar → tinggi  
    **Penilaian ALARP:**
    
- Meskipun mencapai acceptable region, biaya sangat besar
    
- Dibanding opsi A, marginal improvement (dari 10⁻⁵ ke 10⁻⁶) cukup kecil  
    → **Biaya tidak proporsional** → Tidak wajib dilakukan kecuali memang ada persyaratan regulasi.
    

---

### **Opsi C: Blast Wall**

- Tidak mengubah frekuensi
    
- Dampak berkurang 60% → masih kategori _Major_ atau _High_
    
- Frekuensi tetap 1×10⁻⁵ setelah Opsi A (atau 10⁻⁴ jika berdiri sendiri) → tetap berada pada ALARP atau bahkan unacceptable  
    → Pengurangan risiko tidak signifikan terhadap probabilitas kejadian
    
- Biaya Rp 600 juta → tinggi  
    **Kesimpulan:**  
    → Tidak cost-effective → **Tidak masuk kriteria ALARP**
    

---

## **3. Rekomendasi Opsi Terbaik (Menurut ALARP)**

### **Opsi utama yang direkomendasikan:**

### **➡ Opsi A (Gas Detection System)**

**Alasan:**

- Mengurangi risiko dari unacceptable → ALARP region
    
- Biaya relatif kecil
    
- Perbaikan risiko signifikan
    
- Sejalan dengan prinsip ALARP (“reasonable cost for substantial risk reduction”)
    

### **Opsi B tidak wajib**, namun **boleh dilakukan** jika organisasi menghendaki risiko benar-benar rendah, atau jika regulasi menuntut tingkat acceptable.

### **Opsi C tidak direkomendasikan** karena biaya tinggi dengan manfaat terbatas.
