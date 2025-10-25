# Event Tree Analysis

**Event Tree Analysis (ETA)** adalah **metode analisis risiko yang bersifat induktif (forward-looking)** yang digunakan untuk **menilai berbagai kemungkinan konsekuensi dari suatu kejadian awal (initiating event)** dalam sistem. Dengan kata lain, ETA menjelaskan **bagaimana suatu kejadian dapat berkembang melalui berbagai jalur kejadian selanjutnya**, tergantung dari **apakah sistem pengaman atau pengendali berfungsi atau gagal**.

---

## 🧩 Konsep Dasar ETA

ETA dimulai dari **satu kejadian awal (initial event)** — misalnya kegagalan komponen, kesalahan manusia, atau gangguan eksternal — kemudian diuraikan menjadi **rangkaian kejadian lanjutan (sub-events)** yang menunjukkan **apakah sistem pengaman bekerja atau tidak**.  
Hasil akhirnya berupa **pohon kejadian (event tree)** yang memperlihatkan semua **kemungkinan jalur dan akibatnya (outcomes)** beserta **probabilitas masing-masing**.

---

## ⚙️ Langkah-langkah dalam Event Tree Analysis

1. **Identifikasi Kejadian Awal (Initiating Event)**  
    Tentukan peristiwa pemicu yang menjadi titik awal analisis, misalnya “kebocoran gas”, “server crash”, atau “gagal login”.
    
2. **Identifikasi Fungsi Pengaman atau Sistem Tanggap Darurat (Safety Functions)**  
    Daftar semua sistem atau mekanisme yang dirancang untuk mencegah, mengendalikan, atau mengurangi dampak kejadian awal — misalnya alarm, sistem backup, atau firewall.
    
3. **Bentuk Struktur Pohon Kejadian (Event Tree Structure)**  
    Gambarkan kejadian awal di sisi kiri, lalu buat percabangan dua arah:
    
    - “Berhasil” (fungsi pengaman bekerja)
        
    - “Gagal” (fungsi pengaman tidak bekerja)
        
4. **Kombinasikan Semua Kemungkinan Jalur (Paths)**  
    Setiap jalur mencerminkan kombinasi dari keberhasilan dan kegagalan berbagai fungsi pengaman.
    
5. **Hitung Probabilitas Setiap Jalur**  
    Dengan mengalikan probabilitas dari setiap kejadian di jalur tersebut.
    
6. **Tentukan Konsekuensi (Outcome)**  
    Setiap jalur berakhir pada suatu konsekuensi yang dapat dinilai dari segi **keparahan, biaya, atau dampak keselamatan**.
    
7. **Evaluasi Hasil dan Tentukan Risiko**  
    Menggunakan kombinasi **probabilitas dan konsekuensi** untuk menentukan tingkat risiko total.
    

---

## 📊 Contoh Sederhana ETA (Kasus Sistem Informasi)

**Kejadian awal:** Server utama mengalami crash.  
**Sistem pengaman:**

![](img/Pasted%20image%2020251024225758.png)

---

## 📘 Kelebihan ETA

- Menganalisis **berbagai skenario hasil dari satu kejadian awal**.
    
- Cocok untuk **analisis sistem kompleks** seperti sistem informasi, nuklir, kimia, atau penerbangan.
    
- Mudah dipahami secara visual.
    

## ⚠️ Kekurangan ETA

- Hanya menganalisis **dampak dari satu kejadian awal** (tidak cocok untuk multi-failure).
    
- Dapat menjadi sangat kompleks jika banyak fungsi pengaman.
    
- Membutuhkan **data probabilitas yang akurat**.
    

---

## 💡 Kesimpulan

Event Tree Analysis adalah **alat penting dalam manajemen risiko dan keselamatan sistem** yang membantu organisasi memahami bagaimana suatu kejadian bisa berkembang dan mempengaruhi sistem secara keseluruhan, serta bagaimana **efektivitas sistem pengendali** dapat mengurangi konsekuensinya.

---

## Referensi

- https://www.softwareideas.net/eta-event-tree-analysis