## 2. VaR Aset Tunggal (Metode Simulasi Historis)

Metode ini menggunakan data historis kerugian atau _return_ aktual untuk memperkirakan kerugian masa depan, tanpa mengasumsikan distribusi normal.

- **Kasus:** Bank ingin mengukur risiko posisi obligasi jangka panjang senilai **Rp5.000.000.000**.
    
- **Periode:** 10 Hari.
    
- **Tingkat Kepercayaan:** 99%.
    
- **Data Historis:** Bank mengumpulkan 100 data perubahan nilai (kerugian/keuntungan) obligasi selama periode 10 hari terakhir dan mengurutkannya dari yang terendah (kerugian terbesar) ke tertinggi.
    
- **Langkah Perhitungan:**
    
    1. Tentukan jumlah observasi terburuk (persentil) yang akan digunakan: $1 - 99\% = 1\%$.
        
    2. Cari data kerugian yang berada pada persentil ke-1 dari 100 data: $100 \times 1\% = \text{observasi ke-1}$ (kerugian terbesar).
        
    3. Misalkan data kerugian terbesar (observasi ke-1) selama 10 hari tersebut adalah **-0,8%** dari nilai obligasi.
        
- Perhitungan VaR (dalam nilai Rupiah):
    
    $$VaR_{\text{Rp}} = |\text{Kerugian pada persentil ke-}1| \times \text{Nilai Obligasi}$$
    
    $$VaR_{\text{Rp}} = 0,8\% \times \text{Rp5.000.000.000}$$
    
    $$VaR_{\text{Rp}} = \text{Rp40.000.000}$$
    
- **Interpretasi:** Dengan tingkat kepercayaan 99%, kerugian maksimum yang mungkin terjadi pada posisi obligasi Bank selama 10 hari ke depan diperkirakan **tidak akan melebihi Rp40.000.000**. Ada 1% kemungkinan kerugian akan lebih besar dari jumlah ini.
    
