# Linear-Regression-dengan-Python
Tugas Linear Regression dengan Python

# 🎮 Video Games Sales Analysis & Linear Regression

Tugas ini dibangun di atas Jupyter Notebook (Google Colab) untuk menganalisis hubungan antara Tahun Rilis game dengan Total Penjualan Global.

## 📁 Dataset
Dataset yang digunakan berasal dari Kaggle: [Video Games Sales](https://www.kaggle.com/datasets/ulrikthygepedersen/video-games-sales). Dataset ini diunduh secara otomatis menggunakan library `kagglehub` di dalam *notebook*.

Kolom utama yang dianalisis dalam proyek ini:
* `year`: Tahun rilis game (Variabel Independen / X)
* `global_sales`: Total penjualan game secara global dalam jutaan kopi (Variabel Dependen / Y)

## 🛠️ Library yang Digunakan
* `pandas` (Manipulasi Data)
* `matplotlib` & `seaborn` (Visualisasi Data)
* `scikit-learn` (Machine Learning & Evaluasi Model)
* `kagglehub` (Pengambilan Dataset)

## 🚀 Alur Tugas (Langkah-langkah di Notebook)

1. **Eksplorasi Data (EDA):** Memuat dataset dan membuat visualisasi *Line Chart* untuk melihat tren total penjualan game dari tahun ke tahun.
2. **Pra-pemrosesan Data:** Membersihkan data dengan menghapus baris yang memiliki nilai *null* (kosong) pada kolom tahun rilis.
3. **Pembangunan Model:** * Memisahkan data menjadi *Training Set* (80%) dan *Testing Set* (20%).
   * Melatih algoritma **Simple Linear Regression** menggunakan *Training Set*.
4. **Evaluasi Model:** Menguji model dengan *Testing Set* untuk mendapatkan persamaan garis regresi (Slope & Intercept), serta menghitung matriks evaluasi **Mean Squared Error (MSE)** dan **R-squared (R2) Score**.
5. **Visualisasi Hasil:** Membuat *Scatter Plot* untuk membandingkan sebaran data aktual dengan garis lurus (garis regresi) hasil tebakan model.

## 📊 Kesimpulan & Analisis Hasil
Berdasarkan pengujian model, diperoleh skor evaluasi yang sangat rendah (**R2 Score mendekati 0.0001**). Hal ini **bukanlah sebuah error**, melainkan temuan analitis yang penting:

1. **Korelasi Non-Linear:** Variabel Tahun Rilis (`year`) tidak memiliki hubungan linier yang kuat dengan Penjualan Global (`global_sales`). Tren penjualan game secara historis membentuk kurva fluktuatif (meningkat tajam di era 2000-an dan kemudian menurun), bukan garis lurus.
2. **Indikasi Underfitting:** Algoritma Regresi Linier terlalu sederhana dan kaku untuk memetakan sebaran data penjualan game yang sangat bervariasi di setiap tahunnya. Akibatnya, model gagal menangkap pola sebenarnya dari data dan mengalami *Underfitting*.
