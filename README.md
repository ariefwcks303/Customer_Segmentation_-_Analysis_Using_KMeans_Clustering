Customer Segmentation using K-Means Clustering

Proyek ini bertujuan untuk mengelompokkan pelanggan pusat perbelanjaan ke dalam beberapa segmen strategis menggunakan algoritma **K-Means Clustering**. Analisis ini memberikan wawasan mendalam tentang perilaku konsumen untuk mendukung pengambilan keputusan bisnis yang berbasis data.

## 📊 Ikhtisar Data

Dataset terdiri dari 200 baris data pelanggan yang telah diproses dengan teliti (menjaga integritas data tetap 200 baris tanpa data yang hilang).
Variabel utama yang dianalisis:

- **Age** (Usia)
- **Annual Income (k$)** (Pendapatan Tahunan)
- **Spending Score (1-100)** (Skor Pengeluaran)

## 🛠️ Metodologi & Alur Kerja

1. **Data Preparation**: Memastikan tipe data konsisten (Pandas DataFrame).
2. **Optimal K-Search**: Menggunakan _Elbow Method_ untuk mencari titik "siku" terbaik.
3. **Clustering Execution**: Menggunakan `KMeans(init='k-means++', algorithm='elkan')` untuk akurasi dan kecepatan proses.
4. **Visualisasi**: Pemetaan wilayah (_Decision Boundary_) untuk interpretasi segmen yang lebih jelas.

## 🚀 Hasil Analisis & Visualisasi

### 1. Segmentasi Pendapatan vs. Skor Pengeluaran (K=5)

Ini adalah model yang paling krusial untuk strategi pemasaran. Data terbagi menjadi 5 zona wilayah yang jelas:

| Cluster       | Profil Pelanggan                  | Interpretasi Bisnis                       |
| :------------ | :-------------------------------- | :---------------------------------------- |
| **Cluster 1** | Pendapatan Rendah, Belanja Tinggi | Pelanggan Loyal/Impulsif (Target Promosi) |
| **Cluster 2** | Pendapatan Tinggi, Belanja Tinggi | **Target Utama (Sultan)**                 |
| **Cluster 3** | Pendapatan & Belanja Menengah     | Target Stabilitas (Massa Terbesar)        |
| **Cluster 4** | Pendapatan Rendah, Belanja Rendah | Segmen Berisiko                           |
| **Cluster 5** | Pendapatan Tinggi, Belanja Rendah | Target Potensial (Perlu Stimulus Promo)   |

> **Visualisasi**: Model ini menghasilkan peta 5 warna dengan _Decision Boundaries_ yang menunjukkan batas tegas antar segmen pelanggan.

### 2. Segmentasi Usia vs. Skor Pengeluaran (K=4)

- **Temuan**: Pelanggan usia muda mendominasi skor belanja tinggi. Semakin bertambah usia, skor belanja cenderung menurun dan lebih stabil di angka menengah.

### 3. Segmentasi Multidimensi (3D)

- **Hasil**: Dengan menggabungkan tiga variabel, ditemukan 6 kelompok pelanggan yang lebih spesifik, memisahkan perilaku belanja bukan hanya berdasarkan uang, tapi juga faktor generasi (usia).

## 📈 Kesimpulan Strategis

- **Akurasi Data**: Penggunaan 200 baris data utuh memberikan hasil clustering yang sangat padat dan tidak bias.
- **Rekomendasi**: Perusahaan harus memprioritaskan loyalitas pada **Cluster Pendapatan Tinggi-Belanja Tinggi** dan merancang kampanye edukasi untuk **Cluster Pendapatan Tinggi-Belanja Rendah** agar skor pengeluaran mereka meningkat.

## 💻 Teknologi

- **Python** (Pandas, NumPy)
- **Scikit-Learn** (KMeans)
- **Matplotlib & Seaborn** (Static Plots)
- **Plotly** (3D Interactive Visualization)

---

_Dibuat sebagai laporan analisis segmentasi konsumen - Desember 2025._
