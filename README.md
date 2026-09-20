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


## Cara Menjalankan
```bash
git clone https://github.com/diraamelia/kmedoids-indonesian-provinces.git
cd kmedoids-indonesian-provinces
pip install -r requirements.txt
jupyter notebook notebooks/kmedoids_analysis.ipynb
```

## Hasil
*(akan diisi setelah analisis selesai, ringkasan cluster, jumlah cluster optimal, dan interpretasi tiap cluster)*

## Lisensi
MIT License

## Author
Dira Amelia Ramma
7. Visualisasi & interpretasi

## 📁 Struktur Proyek
