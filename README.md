# Prediksi Risiko Penyakit Jantung: Analisis dan Preprocessing Data

Repositori ini berisi eksperimen pemrosesan data (data preprocessing) dan *Exploratory Data Analysis* (EDA) menggunakan **Heart Disease Dataset**. Eksperimen ini merupakan tahapan awal dalam membangun model *Machine Learning* untuk memprediksi apakah seorang pasien memiliki risiko penyakit jantung atau tidak berdasarkan catatan medisnya.

## 📊 Tentang Dataset

Dataset yang digunakan memuat informasi medis pasien yang sangat cocok untuk pemodelan klasifikasi biner. Terdapat 1025 baris data dengan 14 kolom. Beberapa fitur utama di dalam dataset ini meliputi:

* **Usia (Age)**
* **Jenis Kelamin (Sex)**
* **Tekanan Darah (Trestbps)**
* **Kolesterol (Chol)**
* **Detak Jantung Maksimum (Thalach)**
* **Target:** `1` (Berisiko penyakit jantung) dan `0` (Tidak berisiko).

Dataset diunduh secara otomatis melalui Kaggle API (`johnsmith88/heart-disease-dataset`).

## 🛠️ Teknologi dan Pustaka yang Digunakan

Eksperimen ini dibangun menggunakan bahasa pemrograman Python. Berikut adalah pustaka (*library*) utama yang dibutuhkan:

* **Pandas:** Untuk manipulasi dan analisis data tabular.
* **NumPy:** Untuk komputasi numerik dan operasi array.
* **Scikit-Learn:** Khususnya modul `StandardScaler` untuk normalisasi/standarisasi data.
* **Kagglehub:** Untuk mengunduh dataset langsung dari Kaggle ke dalam *notebook*.

## 🚀 Alur Kerja Eksperimen (Workflow)

Eksperimen ini terbagi ke dalam beberapa tahapan utama:

1. **Memuat Dataset:** Mengunduh file `heart.csv` dari Kaggle dan memuatnya ke dalam DataFrame Pandas.
2. **Exploratory Data Analysis (EDA):**
* Memeriksa ringkasan statistik dari masing-masing fitur.
* Mengecek jumlah data yang kosong (*missing values*). Pada dataset ini, ditemukan bahwa data sudah bersih (0 *missing values*).
* Memeriksa distribusi kelas target. Distribusi kelas menunjukkan data yang cukup seimbang (*balanced*), yaitu **526 pasien berisiko** dan **499 pasien tidak berisiko**.


3. **Data Preprocessing:**
* Menghapus data kosong (sebagai tindakan preventif).
* Memisahkan kolom fitur (`X`) dan kolom target (`y`).
* Melakukan standarisasi pada fitur numerik menggunakan `StandardScaler` agar seluruh fitur memiliki skala yang seragam, sehingga mempercepat dan mengoptimalkan performa model *machine learning* nantinya.


4. **Penyimpanan Data:**
* Menggabungkan kembali fitur yang sudah diskalakan dengan label target.
* Menyimpan dataset hasil *preprocessing* ke dalam direktori baru `heart_disease_preprocessing` dengan nama file `heart_preprocessing.csv`.



## 📂 Hasil Output

Setelah menjalankan *notebook* `Eksperimen_MSML.ipynb`, sebuah file baru bernama `heart_preprocessing.csv` akan otomatis terbuat. File ini berisi dataset yang sudah diskalakan dan siap digunakan langsung untuk proses pelatihan model (Model Training) di eksperimen selanjutnya.
