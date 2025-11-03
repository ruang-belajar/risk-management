## 3️⃣ Kasus Perbandingan Opsi Investasi (Pohon Keputusan)

Sebuah perusahaan memiliki kelebihan dana dan harus memilih antara dua opsi investasi: **Proyek X** (yang lebih berisiko) atau **Proyek Y** (yang lebih stabil).

### Data Kasus

|**Opsi Investasi**|**Skenario Hasil**|**Probabilitas (P)**|**Dampak Moneter (I) (Keuntungan)**|
|---|---|---|---|
|**Proyek X** (Berisiko Tinggi)|Sukses Besar|30% (0.3)|Rp1.500.000.000|
||Sukses Moderat|40% (0.4)|Rp500.000.000|
||Gagal (Rugi)|30% (0.3)|-Rp300.000.000|
|**Proyek Y** (Stabil)|Sukses Tinggi|60% (0.6)|Rp600.000.000|
||Sukses Rendah|40% (0.4)|Rp200.000.000|

### Tugas: Hitung dan Bandingkan EMV

1. Hitung EMV untuk Proyek X.
    
2. Hitung EMV untuk Proyek Y.
    
3. Tentukan opsi mana yang sebaiknya dipilih berdasarkan nilai EMV tertinggi.
    
4. Gambarkan struktur Pohon Keputusan (secara konseptual).
    

---

### 1. Perhitungan EMV Proyek X

|**Skenario**|**Probabilitas (P)**|**Dampak Moneter (I)**|**EMV (P×I)**|
|---|---|---|---|
|Sukses Besar|0.3|Rp1.500.000.000|Rp450.000.000|
|Sukses Moderat|0.4|Rp500.000.000|Rp200.000.000|
|Gagal (Rugi)|0.3|-Rp300.000.000|-Rp90.000.000|
|**Total EMV (Proyek X)**|**1.0**||**Rp560.000.000**|

$$\text{EMV Proyek X} = \text{Rp}450.000.000 + \text{Rp}200.000.000 + (-\text{Rp}90.000.000) = \mathbf{\text{Rp}560.000.000}$$

---

### 2. Perhitungan EMV Proyek Y

|**Skenario**|**Probabilitas (P)**|**Dampak Moneter (I)**|**EMV (P×I)**|
|---|---|---|---|
|Sukses Tinggi|0.6|Rp600.000.000|Rp360.000.000|
|Sukses Rendah|0.4|Rp200.000.000|Rp80.000.000|
|**Total EMV (Proyek Y)**|**1.0**||**Rp440.000.000**|

$$\text{EMV Proyek Y} = \text{Rp}360.000.000 + \text{Rp}80.000.000 = \mathbf{\text{Rp}440.000.000}$$

---

### 3. Kesimpulan Keputusan

Dengan membandingkan kedua nilai EMV:

- **EMV Proyek X:** **Rp560.000.000**
    
- **EMV Proyek Y:** **Rp440.000.000**
    

Secara finansial, **Proyek X** memiliki **nilai harapan moneter yang lebih tinggi** (Rp560 Juta) dibandingkan Proyek Y (Rp440 Juta). Oleh karena itu, berdasarkan kriteria EMV, perusahaan **sebaiknya memilih Proyek X**.

### 4. Representasi Pohon Keputusan

Pohon Keputusan (_Decision Tree_) secara visual menunjukkan proses ini, dimulai dari simpul keputusan (persegi) diikuti oleh simpul probabilitas (lingkaran).

1. **Simpul Keputusan (Persegi):** Pilihan awal, yaitu "Pilih Investasi."
    
2. **Cabang Keputusan:** Cabang-cabang yang mewakili pilihan: "Proyek X" dan "Proyek Y."
    
3. **Simpul Probabilitas (Lingkaran):** Di akhir setiap cabang, muncul simpul yang mewakili hasil yang mungkin.
    
4. **Cabang Hasil:** Dari simpul probabilitas, cabang-cabang mengarah ke hasil akhir dan probabilitasnya.
    

#### Struktur Pohon (Konseptual)

```
[Mulai]
   |
   +---[PILIHAN INVESTASI (Kotak Keputusan)]
        |
        +--- Proyek X (EMV = Rp560 Juta)
        |     |
        |     +--- (Lingkaran Probabilitas)
        |           |
        |           +--- Sukses Besar (0.3) -> Keuntungan Rp1.5 M
        |           +--- Sukses Moderat (0.4) -> Keuntungan Rp500 Juta
        |           +--- Gagal (0.3) -> Rugi -Rp300 Juta
        |
        +--- Proyek Y (EMV = Rp440 Juta)
              |
              +--- (Lingkaran Probabilitas)
                    |
                    +--- Sukses Tinggi (0.6) -> Keuntungan Rp600 Juta
                    +--- Sukses Rendah (0.4) -> Keuntungan Rp200 Juta
```

