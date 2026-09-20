# K-Medoids Clustering of Indonesian Provinces (IPM 2025)

Proyek ini menerapkan algoritma **K-Medoids** untuk mengelompokkan provinsi-provinsi di Indonesia berdasarkan **Indeks Pembangunan Manusia (IPM) tahun 2025** dan indikator sosial-ekonomi terkait. Tujuannya adalah mengidentifikasi tipologi pembangunan manusia antarprovinsi untuk mendukung analisis kebijakan dan pemerataan pembangunan.

## Latar Belakang
Menurut data BPS, IPM Indonesia meningkat dari 75,02 pada 2024 menjadi 75,90 pada 2025, dengan capaian pada 2025 berkisar antara 54,91 (Papua Pegunungan) hingga 85,05 (DKI Jakarta). Ketimpangan capaian ini menjadi dasar penting untuk mengelompokkan provinsi ke dalam beberapa cluster tipologi pembangunan.

## Tujuan
- Mengelompokkan 38 provinsi Indonesia berdasarkan IPM 2025 dan indikator pendukungnya
- Mengidentifikasi provinsi dengan karakteristik pembangunan manusia yang serupa
- Memberikan insight untuk prioritas kebijakan pembangunan daerah

## Data
Sumber data: [Badan Pusat Statistik (BPS)](https://www.bps.go.id)

Variabel yang digunakan:
- Indeks Pembangunan Manusia (IPM)
- Umur Harapan Hidup (UHH)
- Harapan Lama Sekolah (HLS)
- Rata-rata Lama Sekolah (RLS)
- Pengeluaran per Kapita Disesuaikan

*(variabel kependudukan seperti luas wilayah, jumlah penduduk, dan kepadatan digunakan sebagai konteks tambahan dalam interpretasi hasil cluster)*

## Metodologi
1. Data Cleaning & Exploratory Data Analysis (EDA)
2. Standardisasi data (Z-score)
3. Penentuan jumlah cluster optimal (Elbow Method & Silhouette Score)
4. Clustering menggunakan K-Medoids (PAM)
5. Evaluasi hasil cluster
6. Visualisasi & interpretasi

## Cara Menjalankan
```bash
git clone https://github.com/diraamelia/kmedoids-indonesian-provinces.git
cd kmedoids-indonesian-provinces
pip install -r requirements.txt
jupyter notebook notebooks/kmedoids_analysis.ipynb
```

## Hasil
Analisis K-Medoids menghasilkan **4 cluster optimal** (ditentukan melalui Elbow Method dan Silhouette Score), dengan **Silhouette Score sebesar 0.3745**.

| Cluster | Kategori | Jumlah Provinsi | Rata-rata IPM | Contoh Provinsi |
|---|---|---|---|---|
| 3 | IPM Sangat Tinggi | 6 | 80.68 | DKI Jakarta, DI Yogyakarta, Kepulauan Riau, Bali |
| 2 | IPM Tinggi | 19 | 75.32 | Jawa Barat, Jawa Timur, Riau, Sulawesi Selatan |
| 0 | IPM Sedang | 11 | 71.87 | Papua, Maluku, Nusa Tenggara Timur |
| 1 | IPM Rendah | 2 | 57.78 | Papua Tengah, Papua Pegunungan |

**Temuan utama:**
- Terdapat disparitas signifikan antara provinsi di Indonesia bagian barat/tengah dengan wilayah Papua, khususnya Papua Tengah dan Papua Pegunungan yang membentuk cluster tersendiri dengan capaian pembangunan manusia jauh di bawah provinsi lain.
- Cluster IPM Tinggi (Cluster 2) merupakan cluster terbesar, mencakup mayoritas provinsi di Sumatera, Jawa, Kalimantan, dan Sulawesi — mencerminkan kondisi "rata-rata nasional".
- Sumatera Barat menonjol sebagai satu-satunya provinsi luar Jawa-Bali yang masuk kategori IPM Sangat Tinggi, menarik untuk dikaji lebih lanjut.

Detail lengkap analisis, visualisasi, dan interpretasi tiap cluster dapat dilihat di [`notebooks/kmedoids_analysis.ipynb`](notebooks/kmedoids_analysis.ipynb).

## Lisensi
MIT License

## Author
Dira Amelia Ramma'
