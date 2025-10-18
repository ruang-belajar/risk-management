# Membuat **matriks risiko**

Matriks risiko adalah alat visual untuk menilai dan memprioritaskan risiko berdasarkan **kemungkinan (likelihood)** dan **dampak (impact)**. 

## Langkah-langkah

1. **Tentukan tujuan** — untuk proyek, unit, atau organisasi? (mis. proyek IT, operasional pabrik).
    
2. **Pilih ukuran matriks** — umum: **3×3**, **4×4**, atau **5×5**. (5×5 memberi detail paling baik).
    
3. **Definisikan skala untuk Likelihood & Impact**  
    Contoh 5-level:
    
    - 1 = Sangat kecil / sangat tidak mungkin
        
    - 2 = Kecil / jarang
        
    - 3 = Sedang / mungkin
        
    - 4 = Besar / sering
        
    - 5 = Sangat besar / hampir pasti  
        Beri definisi konkret tiap level (frekuensi, contoh).
        
4. **Beri skor**: risiko diberi dua skor: `L` (likelihood) dan `I` (impact).
    
5. **Hitung skor risiko**: biasanya `Skor = L × I` (atau gunakan matriks warna langsung).
    
6. **Buat threshold / zona warna**: tentukan rentang skor untuk Hijau / Kuning / Oranye / Merah.
    
7. **Tentukan tindakan** berdasarkan zona (terima, monitor, mitigasi, hindari).
    
8. **Catat mitigasi, pemilik, dan tenggat** dalam risk register.
    
9. **Tinjau berkala** dan update setelah mitigasi atau perubahan konteks.
    

---

## Contoh matriks 5×5 (skor = L × I)

|Impact \ Likelihood|1 (Sangat kecil)|2 (Kecil)|3 (Sedang)|4 (Besar)|5 (Hampir pasti)|
|---|--:|--:|--:|--:|--:|
|**5 (Sangat tinggi)**|5|10|15|20|25|
|**4 (Tinggi)**|4|8|12|16|20|
|**3 (Sedang)**|3|6|9|12|15|
|**2 (Rendah)**|2|4|6|8|10|
|**1 (Sangat rendah)**|1|2|3|4|5|

Contoh pewarnaan (sesuaikan):

- 1–4 = Hijau (Diterima / Monitor ringan)
    
- 5–9 = Kuning (Perlu pengawasan)
    
- 10–15 = Oranye (Mitigasi diperlukan)
    
- 16–25 = Merah (Aksi prioritas / Hindari)
    

---

## Contoh pengisian (risk register sederhana)

|Risiko|L|I|Skor (L×I)|Zona|Tindakan Mitigasi|Pemilik|Tenggat|
|---|--:|--:|--:|---|---|---|---|
|Gangguan server produksi|4|5|20|Merah|Redundansi server + backup harian|IT Ops|2 minggu|
|Keterlambatan vendor|3|3|9|Kuning|Alternatif vendor, SLA tegas|PM|1 bulan|
|Kesalahan input data|2|2|4|Hijau|Validasi otomatis|QA|ongoing|

---

## Tips praktis & best practices

- **Definisikan kriteria impact** (keuangan, reputasi, keselamatan) secara terukur (mis. kerugian Rp, downtime jam, jumlah pelanggan terdampak).
    
- **Gunakan kombinasi kuantitatif & kualitatif** bila data detail tidak tersedia.
    
- **Tetapkan pemilik risiko** untuk tiap risiko dan langkah mitigasi.
    
- **Sertakan indikator (KRI)** untuk memantau perubahan likelihood.
    
- **Sederhana lebih baik** pada awalnya — mulai 3×3 kalau tim belum familiar, lalu tingkatkan ke 5×5.
    
- **Dokumentasikan asumsi** (mengapa L=4, I=5) supaya penilaian bisa ditinjau ulang.
    

---

## Checklist untuk membuat sekarang

1. Pilih 3×3 / 5×5.
    
2. Tetapkan definisi L dan I.
    
3. Kumpulkan daftar risiko (brainstorm).
    
4. Beri skor L & I untuk tiap risiko.
    
5. Letakkan di matriks & beri warna.
    
6. Buat tindakan, pemilik, tenggat.
    
7. Review setiap periode (mis. bulanan / setelah milestone).
    
