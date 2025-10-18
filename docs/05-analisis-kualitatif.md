# METODE ANALISIS RISIKO KUALITATIF

## 5.1 Pendahuluan

Setelah risiko diidentifikasi, langkah berikutnya adalah **analisis risiko**. Analisis bertujuan untuk menilai **tingkat risiko** berdasarkan dua faktor utama:
1. **Probabilitas (Likelihood)** → seberapa besar kemungkinan risiko terjadi.    
2. **Dampak (Impact/Consequence)** → seberapa besar konsekuensi yang ditimbulkan jika risiko terjadi.
    
Analisis risiko bisa dilakukan dengan dua pendekatan:
- **Kualitatif** → menggunakan penilaian deskriptif (low, medium, high).    
- **Kuantitatif** → menggunakan data numerik, probabilitas statistik, simulasi.
    
Pada bab ini dibahas pendekatan **kualitatif** karena paling sering digunakan di banyak organisasi.

---
## 5.2 Tujuan Analisis Kualitatif

1. Menentukan **tingkat prioritas** risiko.    
2. Memberikan gambaran cepat tanpa membutuhkan data numerik yang rumit.    
3. Membantu manajemen dalam pengambilan keputusan awal.    
4. Menjadi dasar untuk analisis kuantitatif (jika diperlukan).
    
---
## 5.3 Skala Penilaian Risiko
### 5.3.1 Probabilitas (Likelihood)

| Skor | Deskripsi     | Contoh                             |
| ---- | ------------- | ---------------------------------- |
| 1    | Sangat Jarang | Terjadi sekali dalam 10 tahun      |
| 2    | Jarang        | Terjadi sekali dalam 5 tahun       |
| 3    | Mungkin       | Terjadi sekali per tahun           |
| 4    | Sering        | Terjadi beberapa kali per tahun    |
| 5    | Sangat Sering | Terjadi hampir setiap bulan/minggu |

### 5.3.2 Dampak (Consequence/Impact)

| Skor | Deskripsi        | Contoh                                 |
| ---- | ---------------- | -------------------------------------- |
| 1    | Tidak Signifikan | Gangguan kecil, tidak berdampak serius |
| 2    | Minor            | Kerugian kecil, perbaikan cepat        |
| 3    | Moderat          | Kerugian sedang, gangguan operasional  |
| 4    | Major            | Kerugian besar, downtime panjang       |
| 5    | Katastropik      | Cedera fatal, kerugian sangat besar    |

---

## 4. Risk Matrix (Matriks Risiko)

Matriks risiko adalah alat visual untuk mengkombinasikan **probabilitas** dan **dampak**, lalu menentukan tingkat risiko:
### 4.1. Langkah-langkah Membuat Matrik Risiko

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

### 4.2. Contoh matriks 5×5 (skor = L × I)

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

### 4.3. Contoh pengisian (risk register sederhana)

|Risiko|L|I|Skor (L×I)|Zona|Tindakan Mitigasi|Pemilik|Tenggat|
|---|--:|--:|--:|---|---|---|---|
|Gangguan server produksi|4|5|20|Merah|Redundansi server + backup harian|IT Ops|2 minggu|
|Keterlambatan vendor|3|3|9|Kuning|Alternatif vendor, SLA tegas|PM|1 bulan|
|Kesalahan input data|2|2|4|Hijau|Validasi otomatis|QA|ongoing|

---

### 4.4. Tips praktis & best practices

- **Definisikan kriteria impact** (keuangan, reputasi, keselamatan) secara terukur (mis. kerugian Rp, downtime jam, jumlah pelanggan terdampak).
    
- **Gunakan kombinasi kuantitatif & kualitatif** bila data detail tidak tersedia.
    
- **Tetapkan pemilik risiko** untuk tiap risiko dan langkah mitigasi.
    
- **Sertakan indikator (KRI)** untuk memantau perubahan likelihood.
    
- **Sederhana lebih baik** pada awalnya — mulai 3×3 kalau tim belum familiar, lalu tingkatkan ke 5×5.
    
- **Dokumentasikan asumsi** (mengapa L=4, I=5) supaya penilaian bisa ditinjau ulang.
    

---

## 5. Metode Analisis Kualitatif

### 5.1 Risk Ranking / Prioritization

- Mengurutkan risiko berdasarkan level dari rendah ke tinggi.
    
- Digunakan untuk alokasi sumber daya agar fokus pada risiko kritis.
    

### 5.2. Risk Scoring

- Memberikan skor dengan formula sederhana:  
    **Risk Score = Probabilitas × Dampak**
    
- Contoh: Risiko A (P=4, D=5) → Skor = 20 → kategori Extreme.
    

### 5.3. Heat Map

- Visualisasi risiko dalam bentuk **warna** pada matriks (hijau, kuning, oranye, merah).
    
- Membantu manajemen memahami secara cepat area berisiko tinggi.
    

---

## 6. Contoh Kasus Analisis Kualitatif

**Kasus: Laboratorium Kampus**

- Risiko 1: Kebocoran bahan kimia → P=3, D=4 → Skor=12 (High).
    
- Risiko 2: Pemadaman listrik mendadak → P=2, D=3 → Skor=6 (Medium).
    
- Risiko 3: Data eksperimen hilang → P=4, D=2 → Skor=8 (Medium).
    
- Risiko 4: Kebakaran → P=2, D=5 → Skor=10 (High).
    

**Interpretasi:** Risiko dengan skor 12 dan 10 menjadi **prioritas utama** untuk mitigasi.

---

## 5.7. Ringkasan

- Analisis risiko kualitatif menilai **probabilitas dan dampak** tanpa data numerik kompleks.
    
- Metode umum: **risk ranking, risk scoring, risk matrix, heat map**.
    
- Hasil analisis digunakan untuk menentukan **prioritas penanganan risiko**.
    

---

📌 **Tugas untuk Mahasiswa (Bab 5):**

1. Ambil 5 risiko dari **Risk Register (Bab 4)**.    
2. Berikan nilai probabilitas dan dampak (skala 1–5).    
3. Hitung skor risiko (P × D).    
4. Susun ke dalam **Risk Matrix** dan tentukan kategori (Low, Medium, High, Extreme).
    
