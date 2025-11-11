## 1. VaR Portofolio Saham (Metode Variansi-Kovariansi / Parametrik)

Metode ini mengasumsikan bahwa _return_ aset terdistribusi secara normal.

- **Kasus:** Seorang investor memiliki portofolio saham senilai **Rp100.000.000**.
    
- **Periode:** 1 Hari.
    
- **Tingkat Kepercayaan:** 95%.
    
- **Data Historis:**
    
    - Rata-rata _return_ harian portofolio $(\mu) = 0,1\%$.
        
    - Deviasi standar _return_ harian portofolio $(\sigma) = 1,5\%$.
        
    - Nilai $Z$ untuk tingkat kepercayaan 95% (atau signifikansi 5%) adalah $\approx 1,645$.
        
- Perhitungan VaR (dalam persentase):
    
    $$VaR_{\%} = \mu - (Z \times \sigma)$$
    $$VaR_{\%} = 0,1\% - (1,645 \times 1,5\%)$$    $$VaR_{\%} = -2,3675\%$$
    
- Perhitungan VaR (dalam nilai Rupiah):
    
    $$VaR_{\text{Rp}} = |VaR_{\%}| \times \text{Nilai Portofolio}$$
    $$VaR_{\text{Rp}} = 2,3675\% \times \text{Rp100.000.000}$$
    $$VaR_{\text{Rp}} = \text{Rp2.367.500}$$
    
- **Interpretasi:** Dengan tingkat kepercayaan 95%, kerugian maksimum yang mungkin diderita investor atas portofolio ini dalam satu hari ke depan diperkirakan **tidak akan melebihi Rp2.367.500**. Ada 5% kemungkinan kerugian akan lebih besar dari jumlah tersebut.
    
