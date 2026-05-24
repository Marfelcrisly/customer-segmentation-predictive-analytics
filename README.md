# End-to-End Data Analytics: Customer Segmentation and Predictive Modeling

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

Proyek ini mengombinasikan teknik **Unsupervised Learning (Clustering)** untuk mengelompokkan data pelanggan, yang kemudian dilanjutkan dengan **Supervised Learning (Klasifikasi)** menggunakan algoritma *Decision Tree* dan *Random Forest* untuk memprediksi target cluster secara otomatis.

## 📊 Highlight Visualisasi (Insight)

*(Kamu bisa mengganti tulisan ini nanti dengan gambar asli dari Colab-mu dengan cara upload ke folder assets)*

> **Analisis Cluster Pelanggan**
> 
> `![Visualisasi Cluster](assets/nama_file_gambar_kamu.png)`
>
> *Insight Singkat: Berdasarkan hasil clustering, kita dapat melihat pemisahan yang jelas antara kelompok pelanggan yang loyal dan pelanggan baru... (ubah sesuai temuanmu)*

---

## 📂 Struktur Repositori
* **`data/`**: Berisi dataset hasil clustering (`data_clustering.csv`).
* **`models/`**: Berisi file model format `.h5` (Clustering, Decision Tree, Random Forest, dan Tuned Model).
* **`notebooks/`**: File Jupyter Notebook `.ipynb` proses eksekusi *project* dari awal hingga akhir.

## 🛠️ Alur Kerja Proyek
1. **Tahap 1: Clustering (Unsupervised)**
   * Melakukan Exploratory Data Analysis (EDA) dan visualisasi fitur numerik.
   * Menggunakan K-Means / metode pengelompokkan untuk ekstraksi cluster pelanggan.
   * Menghasilkan dataset baru yang dilengkapi label `Target`.

2. **Tahap 2: Klasifikasi (Supervised)**
   * Memuat dataset hasil clustering sebagai *ground truth*.
   * Menerapkan *One-Hot Encoding* dan membagi data dengan `train_test_split` (`stratify=y`).
   * Membangun model dengan **Decision Tree** serta eksperimen dengan **Random Forest**.
   * Melakukan *Hyperparameter Tuning* menggunakan **GridSearchCV** untuk optimasi performa.

## 📈 Hasil Evaluasi Model Terbaik
Setelah melakukan serangkaian *tuning*, model **Random Forest** menunjukkan performa yang sangat luar biasa dalam memprediksi segmentasi pelanggan:

| Model | Status | Keterangan |
| :--- | :---: | :--- |
| **Decision Tree** | Baseline | Menunjukkan performa awal yang stabil. |
| **Random Forest** | Explore | Mengalami peningkatan generalisasi yang baik. |
| **Random Forest (Tuned)** | **Best Model** | Menghasilkan performa paling optimal setelah *GridSearchCV*. |
