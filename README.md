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
    git clone https://github.com/LatiefDataVisionary/fmcg-gelar-rasa-2025.git
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

1.  **Eksplorasi Data & Preprocessing**:
    -   Memuat dataset dan melakukan analisis data eksplorasi (EDA) untuk memahami karakteristik data.
    -   Membersihkan data (menangani nilai yang hilang, duplikat, dan anomali).
    -   Melakukan visualisasi awal untuk mendapatkan *insight*.

2.  **Feature Engineering**:
    -   Membuat fitur-fitur baru (misalnya, fitur berbasis waktu, agregasi penjualan) untuk memperkaya dataset dan meningkatkan performa model.
    -   Melakukan seleksi fitur untuk memilih variabel yang paling relevan.

3.  **Modeling & Evaluasi**:
    -   Membangun pipeline model prediktif (misalnya, *Time Series Forecasting* seperti ARIMA, atau model regresi seperti XGBoost).
    -   Melatih model pada data training dan mengevaluasi performanya pada data validasi menggunakan metrik yang relevan (MSE, RMSE, MAPE).
    -   Melakukan analisis kanibalisasi produk berdasarkan hasil prediksi.

4.  **Presentasi Hasil & Pengumpulan**:
    -   Menggabungkan semua analisis, model, dan temuan ke dalam satu notebook yang rapi dan mudah diikuti.
    -   Menyajikan hasil dalam bentuk visualisasi yang jelas dan memberikan rekomendasi strategis berdasarkan *insight* yang didapat.

---

### 📈 Ringkasan Hasil & Temuan

Based on the analysis conducted in the notebook, here are the key findings:

### **1. Trend Forecasting Excellence**
- **Model Performance**: Tree-based Gradient Boosting models significantly outperformed linear baselines. **LightGBM** emerged as the champion model with an **R² score of approximately 0.60** and a **MAPE of ~13.8%**.
- **Primary Drivers**: Future sales are heavily influenced by temporal patterns (seasonality) and historical momentum (Lag features), as well as specific brand and product type attributes.

### **2. Innovation Radar & Rising Stars**
- **Lifecycle Dynamics**: The engineered feature `is_pre_launch` successfully captured significant market anticipation, identifying products that generated traction even before official release.
- **Top Attributes**: Consumer demand is highest for larger packaging sizes (**340ml and 400ml**), and the **Shampoo** category remains the dominant volume driver.
- **Growth Identification**: Products like Ponds and Sunsilk variants showed the strongest Year-over-Year growth, marking them as the portfolio's "Rising Stars."

### **3. Strategic Cannibalization Insights**
- **Parallel Growth**: The case studies (e.g., PC014 vs PC003) revealed **no significant cannibalization**. In fact, older products saw a slight sales increase (up to +9.16%) following new launches.
- **Market Expansion**: New products appear to reach untapped segments or fulfill different consumer needs, effectively expanding the total category size rather than eroding existing shares.

---

### 👥 Contributors

1. Lathif Ramadhan
2. Rafi Ramadhan
3. Gilbert Mathew

---

### 📜 Lisensi

Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file `LICENSE` untuk detailnya.

