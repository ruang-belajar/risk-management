# HAZOP (Hazard and Operability Study)
## 🧩 1. Pengertian HAZOP (Hazard and Operability Study)

**HAZOP** (Hazard and Operability Study) adalah **metode analisis risiko sistematis dan terstruktur** yang digunakan untuk **mengidentifikasi potensi bahaya (hazards)** dan **masalah operasional (operability problems)** dalam proses industri, sistem, atau proyek teknik kompleks.

Metode ini dikembangkan pertama kali oleh **Imperial Chemical Industries (ICI)** pada tahun 1960-an untuk meningkatkan **keselamatan dan keandalan proses kimia**, dan kini digunakan luas di berbagai industri — termasuk **minyak dan gas, farmasi, pembangkit listrik, manufaktur, dan teknologi informasi**.

---

## 🎯 2. Tujuan HAZOP

Tujuan utama HAZOP adalah:

1. **Mengidentifikasi potensi bahaya** yang mungkin timbul akibat penyimpangan dari rancangan (design intent).
    
2. **Menilai dampak operasional dan keselamatan** dari penyimpangan tersebut.
    
3. **Menentukan tindakan pencegahan atau mitigasi** untuk mengurangi risiko.
    
4. **Meningkatkan desain dan prosedur operasi** agar sistem menjadi lebih aman dan efisien.
    

---

## ⚙️ 3. Prinsip Dasar HAZOP

HAZOP bekerja berdasarkan **analisis penyimpangan (deviation analysis)** dari **“design intent”** suatu sistem.

- **Design intent** → maksud atau fungsi normal dari suatu bagian sistem.
    
- **Deviation** → kondisi yang menyimpang dari fungsi normal, misalnya “lebih banyak tekanan”, “tidak ada aliran”, “lebih panas”, dll.
    

Metode ini menggunakan **kata kunci (guide words)** untuk membantu tim menemukan potensi penyimpangan dan dampaknya.

---

## 🔑 4. Guide Words (Kata Kunci HAZOP)

Kata kunci HAZOP digunakan untuk menghasilkan ide tentang penyimpangan dari kondisi normal. Berikut contoh yang umum:

|Guide Word|Makna|Contoh Deviation|
|---|---|---|
|**No / Not**|Tidak terjadi|Tidak ada aliran fluida|
|**More**|Terlalu banyak|Tekanan terlalu tinggi|
|**Less**|Terlalu sedikit|Temperatur terlalu rendah|
|**As well as**|Ada tambahan|Aliran ditambah kontaminan|
|**Part of**|Hanya sebagian|Pompa bekerja sebagian waktu|
|**Reverse**|Arah berlawanan|Aliran balik|
|**Other than**|Salah jenis|Zat kimia berbeda masuk sistem|
|**Early / Late**|Waktu tidak sesuai|Katup terbuka terlalu cepat|

---

## 🧠 5. Tim dan Pendekatan HAZOP

HAZOP dilakukan oleh **tim multidisipliner** yang terdiri dari:

- **Ketua (Facilitator):** Memimpin jalannya studi.
    
- **Sekretaris:** Mencatat hasil dan rekomendasi.
    
- **Engineer Proses:** Memahami detail sistem.
    
- **Operator / Maintenance Staff:** Mengetahui operasional lapangan.
    
- **Ahli Keselamatan (Safety Officer):** Menganalisis dampak bahaya.
    

Pendekatan yang digunakan adalah **brainstorming sistematis** berdasarkan **diagram alir proses (P&ID)** atau model sistem yang sedang dikaji.

---

## 🧾 6. Langkah-langkah Pelaksanaan HAZOP

|Tahap|Kegiatan|
|---|---|
|**1. Persiapan**|Menetapkan tujuan, ruang lingkup, tim, dan dokumen (P&ID, prosedur operasi).|
|**2. Pembagian Sistem**|Membagi proses menjadi **node** (bagian atau segmen kecil) untuk dianalisis satu per satu.|
|**3. Identifikasi Deviation**|Menggunakan **guide words** untuk setiap **parameter** (aliran, tekanan, suhu, level, komposisi).|
|**4. Analisis Penyebab dan Konsekuensi**|Menentukan penyebab penyimpangan dan potensi akibatnya terhadap keselamatan, kualitas, atau lingkungan.|
|**5. Evaluasi Proteksi yang Ada**|Mengevaluasi apakah perlindungan yang ada cukup (alarm, interlock, kontrol, SOP).|
|**6. Rekomendasi**|Menyusun tindakan perbaikan untuk mencegah atau memitigasi risiko.|
|**7. Dokumentasi & Review**|Semua hasil dicatat dalam **tabel HAZOP report** dan ditinjau secara berkala.|

---

## 📊 7. Contoh Format HAZOP Table

|Node|Parameter|Guide Word|Deviation|Possible Causes|Consequences|Safeguards|Recommendations|
|---|---|---|---|---|---|---|---|
|Pompa P-101|Flow|No|No flow|Pompa rusak, valve tertutup|Overheating, kehilangan suplai|Alarm low flow|Ganti pompa, tambah sensor tekanan|
|Tangki T-201|Level|More|High level|Valve outlet tersumbat|Tumpahan bahan kimia|Level switch|Tambah alarm high-high|

---

## 🏭 8. Contoh Penerapan Nyata

- **Industri Minyak & Gas:**  
    Analisis risiko kebocoran gas dari pipa bertekanan tinggi.
    
- **Industri Kimia:**  
    Menganalisis bahaya reaksi berlebih dalam reaktor kimia.
    
- **PLTU / Pembangkit Listrik:**  
    Menilai risiko overpressure pada boiler.
    
- **IT / Software Safety (adaptasi modern):**  
    Menggunakan prinsip HAZOP untuk mengidentifikasi risiko operasional dalam sistem kontrol industri berbasis software.
    

---

## 📈 9. Kelebihan dan Keterbatasan HAZOP

### ✅ Kelebihan:

- Sistematis dan terdokumentasi dengan baik.
    
- Mengungkap bahaya tersembunyi yang mungkin tidak terlihat pada inspeksi umum.
    
- Mendorong kolaborasi lintas disiplin.
    
- Dapat diterapkan pada berbagai tahap desain dan operasi.
    

### ⚠️ Keterbatasan:

- Memerlukan waktu dan biaya yang besar.
    
- Sangat bergantung pada pengalaman tim.
    
- Kurang efektif untuk sistem non-proses (misalnya sistem administratif).
    
- Tidak selalu memberikan **kuantifikasi risiko**, hanya kualitatif.
    

---

## 📚 10. Referensi

1. IEC 61882:2016 — _Hazard and Operability Studies (HAZOP Studies) – Application Guide._
    
2. Kletz, T. A. (1999). _HAZOP and HAZAN: Identifying and Assessing Process Industry Hazards._
    
3. CCPS (Center for Chemical Process Safety). (2008). _Guidelines for Hazard Evaluation Procedures._
    
4. ISO 31000:2018 — _Risk Management – Guidelines._
    

---

# Contoh Penerapan HAZOP
## 🧩 1. Konteks dan Latar Belakang

Dalam **Software Safety**, HAZOP digunakan untuk **menganalisis potensi bahaya dan kegagalan operasional** pada sistem perangkat lunak yang mengendalikan proses kritis, seperti:

- Sistem kontrol industri (ICS / SCADA),
    
- Sistem avionik dan otomotif,
    
- Sistem medis,
    
- Sistem keamanan siber untuk infrastruktur vital.
    

Tujuannya sama seperti HAZOP proses kimia, yaitu:

> _Mengidentifikasi penyimpangan dari fungsi yang diharapkan (design intent) dan menilai dampaknya terhadap keselamatan dan keandalan sistem._

---

## ⚙️ 2. Pendekatan Adaptif HAZOP untuk Software

Karena perangkat lunak tidak memiliki **parameter fisik** seperti “flow” atau “pressure”, maka parameter HAZOP disesuaikan menjadi parameter **fungsi logika dan data**, misalnya:

|Jenis Parameter Software|Contoh Parameter|
|---|---|
|**Input Data**|Sensor reading, user input|
|**Output Data**|Command ke aktuator, tampilan hasil|
|**Proses / Logika**|Algoritma kontrol, kalkulasi, kondisi logika|
|**Komunikasi**|Pengiriman data antar modul / sistem|
|**Waktu / Timing**|Delay, respon waktu, jadwal eksekusi|

Guide words yang digunakan juga diadaptasi, misalnya:

|Guide Word|Makna Software|Contoh|
|---|---|---|
|**No / Not**|Tidak terjadi / tidak dikirim|Data sensor tidak diterima|
|**More**|Nilai terlalu tinggi|Output lebih besar dari batas aman|
|**Less**|Nilai terlalu kecil|Perintah throttle terlalu rendah|
|**As well as**|Ada tambahan data|Sistem mengirim sinyal ganda|
|**Other than**|Salah tipe / format|Data korup / salah tipe data|
|**Early / Late**|Waktu tidak sesuai|Respons sistem terlalu lambat|

---

## 🧠 3. Studi Kasus: Sistem Kontrol Suhu Otomatis di Ruang Server

### **Deskripsi Sistem:**

Perangkat lunak **mengontrol suhu ruang server** dengan:

- Membaca data sensor suhu,
    
- Membandingkan dengan setpoint (misal 24°C),
    
- Mengaktifkan pendingin (AC) bila suhu > setpoint,
    
- Mengirim alarm bila suhu melebihi ambang kritis (30°C).
    

---

## 🧾 4. Contoh Analisis HAZOP Software Safety

|Node / Modul|Parameter|Guide Word|Deviation|Possible Causes|Consequences|Safeguards|Recommendations|
|---|---|---|---|---|---|---|---|
|**Sensor Input Module**|Sensor data|No|Tidak ada data dari sensor|Sensor gagal, koneksi terputus, buffer overflow|Sistem tidak menyadari suhu naik → Overheating|Watchdog timer, default fail-safe value|Tambahkan redundansi sensor dan alarm "sensor failure"|
|**Control Logic Module**|Setpoint comparison|More|Output lebih tinggi dari batas aman|Bug dalam logika perbandingan, overflow variabel|Pendingin bekerja berlebihan, energi boros, kondensasi|Range checking|Validasi algoritma dan uji batas ekstrem|
|**Actuator Command Module**|Command signal|Other than|Sinyal salah dikirim (misal “OFF” saat harus “ON”)|Data korup, error komunikasi antar modul|Pendingin mati saat suhu tinggi → overheating server|Log error + retry mekanisme|Tambahkan checksum dan verifikasi perintah|
|**Alarm Handler Module**|Alarm message|Late|Alarm dikirim terlambat|Thread delay, CPU overload|Operator terlambat merespon → risiko kerusakan server|Prioritas interrupt untuk alarm|Optimalkan thread scheduling|
|**Communication Module**|Data transmission|As well as|Data dikirim ganda|Loop logic error, retry mechanism salah|Sistem menerima perintah dua kali → output tidak stabil|Error handling untuk duplikasi|Terapkan ID unik untuk setiap pesan|

---

## 🧩 5. Penjelasan Hasil

Dari tabel di atas:

- Setiap **modul perangkat lunak** dianggap sebagai _node_.
    
- **Guide words** membantu menemukan kemungkinan penyimpangan fungsi.
    
- **Dampak keselamatan (safety impact)** diidentifikasi berdasarkan konsekuensi kegagalan logika.
    
- Hasilnya menghasilkan rekomendasi yang bersifat:
    
    - _Desain teknis_ (misalnya redundansi sensor),
        
    - _Prosedural_ (misalnya alarm failure test),
        
    - _Organisasional_ (misalnya pelatihan operator).
        

---

## 🧠 6. Keunggulan HAZOP dalam Software Safety

✅ Mendorong **pemikiran sistematis** terhadap interaksi antar modul.  
✅ Dapat diintegrasikan dengan **FMEA (Failure Mode and Effect Analysis)** untuk perhitungan risiko kuantitatif.  
✅ Mendeteksi **anomali logika dan komunikasi** yang sering menjadi penyebab utama insiden software safety.  
✅ Cocok untuk **software safety-critical** di sistem industri, otomotif, atau kesehatan.

---

## ⚠️ 7. Keterbatasan

- Tidak mudah diterapkan untuk sistem software yang sangat kompleks tanpa dokumentasi arsitektur yang baik.
    
- Membutuhkan **kolaborasi antara ahli software dan safety engineer**.
    
- Hasilnya bersifat **kualitatif**, bukan numerik.
    

---

## 📚 8. Referensi

1. IEC 61882:2016 — _Hazard and Operability Studies (HAZOP Studies) – Application Guide._
    
2. IEC 61508:2010 — _Functional Safety of Electrical/Electronic/Programmable Electronic Safety-related Systems._
    
3. NASA (2019). _Software Safety Guidebook (NASA-GB-8719.13)._
    
4. McDermid, J. (1999). _Software Hazard and Operability Studies._ University of York.
    
