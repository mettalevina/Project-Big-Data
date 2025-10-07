# Project-Big-Data
Proyek ini adalah project UAS untuk mata kuliah Big Data yang berfokus pada penerapan teknik Unsupervised Learning untuk analisis data iklim. Disini digunakan algoritma K-Means Clustering untuk mengidentifikasi dan membandingkan pola angin harian yang dominan di tiga wilayah geografis Indonesia yang berbeda: Aceh, Lampung, dan Jakarta.

Data dan Prapemrosesan
- Sumber Data: Data cuaca harian historis (1 Januari 2011 – 31 Desember 2021) dari arsip publik Badan Meteorologi, Klimatologi, dan Geofisika (BMKG) .
- Total Sampel: 10.907 sampel harian.
- Variabel Utama:
    a. ff_avg: Kecepatan angin rata-rata harian.
    b. ddd_car: Arah angin dominan harian (dalam satuan derajat).
- Rekayasa Fitur Krusial (Feature Engineering): Untuk mengatasi sifat sirkular data arah, variabel kecepatan dan arah angin diubah menjadi Vektor Kartesius U (Barat-Timur) dan V (Selatan-Utara).
- Standarisasi Data: Fitur U dan V distandarisasi menggunakan StandardScaler untuk memastikan kontribusi yang seimbang dalam proses clustering .

Metodologi (K-Means Clustering)
- Penentuan K Optimal: Jumlah klaster yang optimal (k) ditentukan menggunakan Metode Elbow dengan memvisualisasikan Within-Cluster Sum of Squares (WCSS). Analisis ini menunjukkan bahwa k=4 adalah jumlah klaster yang paling optimal.
- Penerapan K-Means: Model diterapkan pada komponen Vektor U-V yang telah distandarisasi.
- Interpretasi Hasil: Empat pola angin diinterpretasikan menggunakan visualisasi Wind Rose dan dinamika monsun:
    a. Cluster 0: Pola Monsun Barat (angin konsisten dari Barat/Barat Daya).
    b. Cluster 1: Pola Monsun Timur (angin stabil dari Timur/Tenggara).
    c. Cluster 2: Pola Angin Tenang & Bervariasi (kecepatan rendah, arah bervariasi, khas periode peralihan musim) .
    d. Cluster 3: Pola Angin Utara Kencang (angin bertiup kencang dari arah Utara).

Kesimpulan:
Jakarta secara signifikan didominasi oleh Cluster 2 (Pola Angin Tenang & Bervariasi), mengindikasikan sirkulasi udara yang lebih lambat. Sedangkan Aceh dan Lampung menunjukkan distribusi pola yang lebih beragam dan dipengaruhi kuat oleh siklus monsun, dengan proporsi tinggi untuk Cluster 0 (Monsun Barat) dan Cluster 1 (Monsun Timur) .
