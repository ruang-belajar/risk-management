
## Menghitung Volatilitas Portofolio (lebih dari 1 aset)

Jika terdapat dua aset A dan B:

$$\sigma_p = \sqrt{w_A^2\sigma_A^2 + w_B^2\sigma_B^2 + 2w_Aw_B\rho_{AB}\sigma_A\sigma_B}$$

Keterangan:

- $w_A, w_B$ = proporsi nilai aset
    
- $\sigma_A, \sigma_B$ = volatilitas masing-masing
    
- $\rho_{AB}$ = korelasi antar aset

**Contoh perhitungan — Dua Aset**

**Asumsi:**

- Nilai portofolio $V = Rp\ 2.000.000.000$.
    
- Dua aset A dan B dengan bobot nilai (proporsi) $w = [0{,}6,\ 0{,}4]$. (60% di A, 40% di B)
    
- Standar deviasi harian: 
	- $\sigma_A = 2{,}0\% = 0{,}02;$
	- $\sigma_B = 1{,}2\% = 0{,}012$.
    
- Korelasi $\rho_{AB} = 0{,}5$.
    
- Confidence 95% → $Z = 1{,}645$.
    

**Langkah:**

1. Buat matriks kovarians (\Sigma):
    
    - $\Sigma_{AA} = \sigma_A^2 = 0{,}02^2 = 0{,}0004$
        
    - $\Sigma_{BB} = \sigma_B^2 = 0{,}012^2 = 0{,}000144$
        
    - $\Sigma_{AB} = \rho_{AB}\sigma_A\sigma_B = 0{,}5 \times 0{,}02 \times 0{,}012$
        
        - $0{,}02 \times 0{,}012 = 0{,}00024$
            
        - Dikalikan 0.5 → $0{,}00024 \times 0{,}5 = 0{,}00012$
             
    
    Jadi:  
    $$\Sigma = \begin{pmatrix}  
    0{,}0004 & 0{,}00012 \\  
    0{,}00012 & 0{,}000144  
    \end{pmatrix}  
    $$
    
2. Hitung $\sigma_p = \sqrt{w^\top \Sigma w}$ dengan $w = \begin{pmatrix}0{,}6\\0{,}4\end{pmatrix}$.
    
    - Hitung vektor menengah $u = \Sigma w$:
        
        - Baris 1: 
	        - $0{,}0004 \times 0{,}6 + 0{,}00012 \times 0{,}4$            
            - $0{,}0004 \times 0{,}6 = 0{,}00024$                
            - $0{,}00012 \times 0{,}4 = 0{,}000048$                
            - Jumlah = $0{,}00024 + 0{,}000048 = 0{,}000288$
                
        - Baris 2: 
	        - $0{,}00012 \times 0{,}6 + 0{,}000144 \times 0{,}4$            
            - $0{,}00012 \times 0{,}6 = 0{,}000072$                
            - $0{,}000144 \times 0{,}4 = 0{,}0000576$                
            - Jumlah = $0{,}000072 + 0{,}0000576 = 0{,}0001296$
        
        Jadi $u = \begin{pmatrix}0{,}000288\\0{,}0001296\end{pmatrix}$.
        
    - Sekarang $w^\top u = 0{,}6 \times 0{,}000288 + 0{,}4 \times 0{,}0001296$
        
        - $0{,}6 \times 0{,}000288 = 0{,}0001728$
            
        - $0{,}4 \times 0{,}0001296 = 0{,}00005184$
            
        - Jumlah = $0{,}0001728 + 0{,}00005184 = 0{,}00022464$
            
    - Jadi $\sigma_p = \sqrt{0{,}00022464}$
        
        - $\sqrt{0{,}00022464} \approx 0{,}015$ (karena $0{,}015^2 = 0{,}000225$ sangat dekat)
            
    
    → $\sigma_p \approx 0{,}015 = 1{,}5\%$ per hari.
    
3. VaR:  
    $$\text{VaR} = Z \times \sigma_p \times V = 1{,}645 \times 0{,}015 \times 2.000.000.000$$
    
    - $1{,}645 \times 0{,}015 = 1{,}645 \times 15/1000 = (1{,}645 \times 15)/1000$
        
        - $1{,}645 \times 15 = 24{,}675$
            
        - Dibagi 1000 → $24{,}675/1000 = 0{,}024675$
            
    - $0{,}024675 \times 2.000.000.000$
        
        - 1% dari V = 20.000.000 (karena 0,01×2.000.000.000 = 20.000.000)
            
        - 2% = 40.000.000
            
        - $0{,}004675 × V = 2.000.000.000 × 4{,}675/1000 = (2.000.000.000 × 4{,}675)/1000$
            
            - $2.000.000.000 × 4{,}675 = 9.350.000.000$
                
            - Dibagi 1000 → $9.350.000.000/1000 = 9.350.000$
                
        - Jadi $0{,}024675 = 0{,}02 + 0{,}004675) → (40.000.000 + 9.350.000 = 49.350.000$
    $$\boxed{\text{VaR}_{\text{harian, 95\%}} \approx Rp\ 49.350.000}$$

---
