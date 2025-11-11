# Analisis Prediktif Penjualan FMCG Personal Care - Gelar Rasa 2025

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-In--Progress-orange.svg)

Repositori ini berisi analisis data dan pengembangan model prediktif untuk **Data Science Competition Gelar Rasa 2025** yang diselenggarakan oleh HIMASADA UPN "Veteran" Jawa Timur. Proyek ini berfokus pada analisis dataset sintetis transaksi penjualan produk *Personal Care* untuk mengidentifikasi inovasi, memprediksi tren, dan menganalisis kanibalisasi produk.

---

## 🚀 Deskripsi Proyek & Tujuan

Tema kompetisi, *"Revealing Hidden Patterns for Innovation and Strategic Growth in the Digital Era"*, menjadi panduan utama proyek ini. Dengan memanfaatkan dataset transaksional FMCG dari tahun 2020 hingga 2025, proyek ini bertujuan untuk mengubah data mentah menjadi *insight* strategis yang dapat mendorong pertumbuhan bisnis di era digital.

Tujuan utama analisis dalam proyek ini adalah:

1.  **💡 Innovation Radar**: Mengidentifikasi produk-produk dengan potensi pertumbuhan tinggi atau fitur inovatif yang menarik minat konsumen secara signifikan.
2.  **📈 Trend Forecasting**: Membangun model prediktif untuk meramalkan tren penjualan di masa mendatang, serta memahami pergeseran preferensi konsumen.
3.  **🔄 Product Cannibalization Analysis**: Mengevaluasi dampak peluncuran produk baru terhadap penjualan produk-produk lain dalam kategori yang sama.

---

## 📋 Daftar Isi

- [Struktur Repositori](#-struktur-repositori)
- [Instalasi & Pengaturan](#-instalasi--pengaturan)
- [Dataset](#-dataset)
- [Alur Kerja Proyek](#-alur-kerja-proyek)
- [Ringkasan Hasil & Temuan](#-ringkasan-hasil--temuan)
- [Kontributor](#-kontributor)
- [Lisensi](#-lisensi)

---

### 📂 Struktur Repositori

Proyek ini disusun dengan struktur folder yang sistematis untuk memastikan keterbacaan, skalabilitas, dan reproduktifitas.

```
├── data/              # Folder untuk dataset (tidak di-track oleh Git)
│   ├── raw/           # Data mentah dari kompetisi
│   └── processed/     # Data yang telah dibersihkan dan diproses
├── notebooks/         # Berisi Jupyter Notebooks untuk analisis & eksperimen
├── reports/           # Hasil analisis, visualisasi, dan laporan
│   └── figures/       # Gambar dan plot yang dihasilkan
├── src/               # Kode sumber modular (fungsi & pipeline)
├── submissions/       # Notebook final untuk pengumpulan
├── .gitignore         # Mengabaikan file yang tidak perlu di-track
├── README.md          # Dokumen ini
└── requirements.txt   # Daftar dependensi Python
```

---

### ⚙️ Instalasi & Pengaturan

Untuk menjalankan analisis ini di lingkungan lokal, ikuti langkah-langkah berikut:

1.  **Clone Repository**
    ```bash
    git clone https://github.com/NAMAPENGGUNAANDA/fmcg-gelar-rasa-2025.git
    cd fmcg-gelar-rasa-2025
    ```

2.  **Buat Virtual Environment** (direkomendasikan)
    ```bash
    python -m venv venv
    source venv/bin/activate  # Untuk Windows: venv\Scripts\activate
    ```

3.  **Instal Dependensi**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Pengaturan Dataset**
    -   Unduh dataset kompetisi dari link yang disediakan: `bit.ly/DatasetDSCGelarRasa2025`.
    -   Ekstrak file zip dan letakkan seluruh file `.csv` (`products.csv`, `marketing.csv`, `reviews.csv`, `sales.csv`) ke dalam folder `data/raw/`.
    -   **Penting**: File-file data ini sengaja tidak dilacak oleh Git karena ukurannya yang besar.

---

### 📊 Dataset

Dataset yang digunakan adalah **FMCG Personal Care - Synthetic Dataset**, yang mensimulasikan data transaksi penjualan dari 1 Januari 2020 hingga 31 Desember 2025.

**File Utama:**
-   `products.csv`: Data master produk.
-   `marketing.csv`: Data kampanye pemasaran.
-   `reviews.csv`: Sampel ulasan pelanggan.
-   `sales.csv`: Data transaksi penjualan (~1.000.000 baris).

Detail lebih lanjut mengenai setiap kolom dapat ditemukan di file `README_FMCG_Personal_Care.txt` dan di dalam notebook EDA.

---

### 🔬 Alur Kerja Proyek

Proyek ini mengikuti alur kerja *data science* yang terstruktur:

1.  **Eksplorasi Data & Preprocessing (`notebooks/01_eda_dan_preprocessing.ipynb`)**:
    -   Memuat dataset dan melakukan analisis data eksplorasi (EDA) untuk memahami karakteristik data.
    -   Membersihkan data (menangani nilai yang hilang, duplikat, dan anomali).
    -   Melakukan visualisasi awal untuk mendapatkan *insight*.

2.  **Feature Engineering (`notebooks/02_feature_engineering.ipynb`)**:
    -   Membuat fitur-fitur baru (misalnya, fitur berbasis waktu, agregasi penjualan) untuk memperkaya dataset dan meningkatkan performa model.
    -   Melakukan seleksi fitur untuk memilih variabel yang paling relevan.

3.  **Modeling & Evaluasi (`notebooks/03_modeling_dan_evaluasi.ipynb`)**:
    -   Membangun pipeline model prediktif (misalnya, *Time Series Forecasting* seperti ARIMA, atau model regresi seperti XGBoost).
    -   Melatih model pada data training dan mengevaluasi performanya pada data validasi menggunakan metrik yang relevan (MSE, RMSE, MAPE).
    -   Melakukan analisis kanibalisasi produk berdasarkan hasil prediksi.

4.  **Presentasi Hasil & Pengumpulan (`submissions/submission_GelarRasa2025.ipynb`)**:
    -   Menggabungkan semua analisis, model, dan temuan ke dalam satu notebook yang rapi dan mudah diikuti.
    -   Menyajikan hasil dalam bentuk visualisasi yang jelas dan memberikan rekomendasi strategis berdasarkan *insight* yang didapat.

---

### 📈 Ringkasan Hasil & Temuan

*(Di bagian ini, Anda akan mengisi temuan-temuan kunci dari analisis Anda setelah menyelesaikannya. Berikut contoh placeholder.)*

-   **Innovation Radar**: Ditemukan bahwa produk **[Nama Produk/Tipe Produk]** menunjukkan tren pertumbuhan penjualan tertinggi, terutama di wilayah **[Nama Wilayah]**. Faktor pendorongnya diduga adalah **[Sebutkan Faktor, misal: kampanye influencer, rating positif]**.
-   **Trend Forecasting**: Model **[Nama Model, misal: ARIMA(p,d,q)]** berhasil memprediksi penjualan bulanan dengan tingkat MAPE sebesar **[X.XX]%**. Tren menunjukkan peningkatan permintaan untuk produk dengan ukuran **[Ukuran, misal: >300ml]** dan preferensi konsumen bergeser ke saluran penjualan **[Nama Channel, misal: Official Store]**.
-   **Product Cannibalization**: Peluncuran produk **[Produk Baru]** pada tanggal **[Tanggal]** terbukti **[mengurangi/tidak mengurangi]** penjualan produk **[Produk Lama]** sebesar rata-rata **[Y.YY]%** di channel yang sama, menunjukkan adanya efek kanibalisasi.

---

### 👥 Kontributor

-   **[Nama Anda]** - *[Peran Anda, misal: Data Analyst, Project Lead]*

---

### 📜 Lisensi

Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file `LICENSE` untuk detailnya.

