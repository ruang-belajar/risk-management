## 3. VaR untuk Risiko Operasional (Contoh Sederhana Pendekatan Parametrik)

VaR juga dapat diterapkan untuk mengukur risiko non-pasar seperti **risiko operasional** (misalnya, kerugian akibat kegagalan sistem, penipuan, atau _human error_).

- **Kasus:** Perusahaan logistik menghitung potensi kerugian maksimum akibat "Kecelakaan Kerja/Kerusakan Aset" dalam sebulan.
    
- **Periode:** 1 Bulan.
    
- **Tingkat Kepercayaan:** 90%.
    
- **Data Historis:**
    
    - Rata-rata kerugian bulanan akibat kasus tersebut $(\mu) = \text{Rp10.000.000}$.
        
    - Deviasi standar kerugian bulanan $(\sigma) = \text{Rp3.000.000}$.
        
    - Nilai $Z$ untuk tingkat kepercayaan 90% (atau signifikansi 10%) adalah $\approx 1,28$.
        
- Perhitungan VaR (dalam nilai Rupiah):
    $$VaR = \text{Rata-rata Kerugian} + (Z \times \text{Deviasi Standar})$$
    $$VaR = \text{Rp10.000.000} + (1,28 \times \text{Rp3.000.000})$$
        $$VaR = \text{Rp10.000.000} + \text{Rp3.840.000}$$
   $$VaR = \text{Rp13.840.000}$$
    
- **Interpretasi:** Dengan tingkat kepercayaan 90%, kerugian maksimum yang mungkin diderita Perusahaan logistik akibat kecelakaan kerja/kerusakan aset dalam satu bulan diperkirakan **tidak akan melebihi Rp13.840.000**. Terdapat 10% kemungkinan kerugian akan lebih besar.
    
