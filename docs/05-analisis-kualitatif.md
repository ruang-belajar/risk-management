# **BAB 5 – METODE ANALISIS RISIKO KUALITATIF**

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

## 5.4 Risk Matrix (Matriks Risiko)

Matriks risiko adalah alat visual untuk mengkombinasikan **probabilitas** dan **dampak**, lalu menentukan tingkat risiko:

| Dampak ↓ / Probabilitas → | 1 (S. Jarang) | 2 (Jarang) | 3 (Mungkin) | 4 (Sering) | 5 (S. Sering) |
| ------------------------- | ------------- | ---------- | ----------- | ---------- | ------------- |
| **5 Katastropik**         | Medium        | Medium     | High        | Extreme    | Extreme       |
| **4 Major**               | Low           | Medium     | High        | High       | Extreme       |
| **3 Moderat**             | Low           | Medium     | Medium      | High       | High          |
| **2 Minor**               | Low           | Low        | Medium      | Medium     | High          |
| **1 Tidak signifikan**    | Low           | Low        | Low         | Medium     | Medium        |

**Kategori Risiko:**
- **Low** → dapat diterima, hanya perlu monitoring.    
- **Medium** → butuh pengendalian tambahan.    
- **High** → perlu tindakan segera.    
- **Extreme** → tidak dapat diterima, harus dieliminasi atau dikendalikan maksimal.    

---

## 5.5 Metode Analisis Kualitatif

### 5.5.1 Risk Ranking / Prioritization

- Mengurutkan risiko berdasarkan level dari rendah ke tinggi.
    
- Digunakan untuk alokasi sumber daya agar fokus pada risiko kritis.
    

### 5.5.2 Risk Scoring

- Memberikan skor dengan formula sederhana:  
    **Risk Score = Probabilitas × Dampak**
    
- Contoh: Risiko A (P=4, D=5) → Skor = 20 → kategori Extreme.
    

### 5.5.3 Heat Map

- Visualisasi risiko dalam bentuk **warna** pada matriks (hijau, kuning, oranye, merah).
    
- Membantu manajemen memahami secara cepat area berisiko tinggi.
    

---

## 5.6 Contoh Kasus Analisis Kualitatif

**Kasus: Laboratorium Kampus**

- Risiko 1: Kebocoran bahan kimia → P=3, D=4 → Skor=12 (High).
    
- Risiko 2: Pemadaman listrik mendadak → P=2, D=3 → Skor=6 (Medium).
    
- Risiko 3: Data eksperimen hilang → P=4, D=2 → Skor=8 (Medium).
    
- Risiko 4: Kebakaran → P=2, D=5 → Skor=10 (High).
    

**Interpretasi:** Risiko dengan skor 12 dan 10 menjadi **prioritas utama** untuk mitigasi.

---

## 5.7 Ringkasan

- Analisis risiko kualitatif menilai **probabilitas dan dampak** tanpa data numerik kompleks.
    
- Metode umum: **risk ranking, risk scoring, risk matrix, heat map**.
    
- Hasil analisis digunakan untuk menentukan **prioritas penanganan risiko**.
    

---

📌 **Tugas untuk Mahasiswa (Bab 5):**

1. Ambil 5 risiko dari **Risk Register (Bab 4)**.    
2. Berikan nilai probabilitas dan dampak (skala 1–5).    
3. Hitung skor risiko (P × D).    
4. Susun ke dalam **Risk Matrix** dan tentukan kategori (Low, Medium, High, Extreme).
    
