# STRIDE

**STRIDE** adalah **metode analisis ancaman (threat modeling)** yang digunakan untuk mengidentifikasi berbagai jenis ancaman keamanan dalam sistem informasi atau aplikasi.  
Metode ini dikembangkan oleh **Microsoft** sebagai bagian dari pendekatan _Secure Development Lifecycle (SDL)_ untuk membantu pengembang memikirkan ancaman sejak tahap desain sistem.

---

## 🔹 Arti STRIDE

Kata **STRIDE** merupakan akronim dari enam kategori ancaman utama:

|Huruf|Jenis Ancaman|Penjelasan|Contoh|
|:--|:--|:--|:--|
|**S**|**Spoofing Identity**|Pemalsuan identitas untuk mengakses sistem secara tidak sah.|Penyerang berpura-pura menjadi pengguna sah dengan mencuri kredensial (username/password).|
|**T**|**Tampering with Data**|Mengubah atau memanipulasi data tanpa izin.|Mengubah data transaksi di database atau paket data di jaringan.|
|**R**|**Repudiation**|Pengguna menyangkal telah melakukan suatu tindakan (dan sistem tidak dapat membuktikan sebaliknya).|Pengguna menghapus log aktivitas agar tidak terlacak.|
|**I**|**Information Disclosure**|Kebocoran informasi sensitif kepada pihak yang tidak berhak.|Data pengguna terekspos akibat kesalahan konfigurasi API.|
|**D**|**Denial of Service (DoS)**|Mengganggu layanan agar tidak bisa digunakan oleh pengguna sah.|Serangan yang membanjiri server dengan permintaan palsu.|
|**E**|**Elevation of Privilege**|Meningkatkan hak akses tanpa izin.|Pengguna biasa mengeksploitasi celah untuk menjadi admin.|

---

## 🔹 Tujuan STRIDE

Tujuan utama metode STRIDE adalah:

- Mengidentifikasi **potensi ancaman keamanan** sejak tahap desain sistem.
    
- Menentukan **tindakan mitigasi** yang sesuai sebelum sistem dikembangkan atau diimplementasikan.
    
- Meningkatkan **kesadaran keamanan** di antara tim pengembang dan arsitek sistem.
    

---

## 🔹 Cara Penerapan STRIDE

1. **Modelkan sistem** menggunakan _data flow diagram (DFD)_ atau arsitektur sistem.
    
2. **Identifikasi komponen**: proses, data store, data flow, dan external entities.
    
3. **Evaluasi setiap komponen** terhadap enam kategori ancaman STRIDE.
    
4. **Catat ancaman dan mitigasinya** dalam _threat list_ atau _risk register_.
    
5. **Rencanakan kontrol keamanan** untuk setiap ancaman (misalnya autentikasi, enkripsi, logging, dll).
    

---

## 🔹 Contoh Singkat

Misalnya dalam sistem **aplikasi login pengguna**:

- **Spoofing:** Penyerang mencoba meniru pengguna sah → solusi: _multi-factor authentication (MFA)_.
    
- **Tampering:** Modifikasi data login di jaringan → solusi: gunakan _HTTPS/SSL encryption_.
    
- **Repudiation:** Pengguna menyangkal telah login → solusi: aktifkan _audit log_.
    
- **Information Disclosure:** Password muncul dalam log → solusi: hindari penyimpanan teks polos.
    
- **Denial of Service:** Serangan brute-force → solusi: _rate limiting_ dan _CAPTCHA_.
    
- **Elevation of Privilege:** Eksploitasi bug untuk jadi admin → solusi: _role-based access control (RBAC)_.
    
