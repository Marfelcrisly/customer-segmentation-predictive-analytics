# End-to-End Data Analytics: Customer Segmentation and Predictive Modeling

Proyek ini mengombinasikan teknik **Unsupervised Learning (Clustering)** untuk mengelompokkan data pelanggan, yang kemudian dilanjutkan dengan **Supervised Learning (Klasifikasi)** menggunakan Decision Tree dan Random Forest untuk memprediksi target cluster secara otomatis.

## 📂 Struktur Repositori
* **data/**: Berisi dataset hasil clustering (`data_clustering.csv`).
* **models/**: Berisi file model format `.h5` (Clustering, Decision Tree, Random Forest, dan Tuned Model).
* **notebooks/**: File Jupyter Notebook `.ipynb` proses eksekusi project dari awal hingga akhir.

## 🛠️ Alur Kerja Proyek
1. **Tahap 1: Clustering (Unsupervised)**
   * Melakukan Exploratory Data Analysis (EDA) dan visualisasi histogram fitur numerik.
   * Menggunakan metode Case-Based Reasoning (CBR) / K-Means untuk ekstraksi cluster.
   * Menghasilkan dataset baru yang dilengkapi label `Target`.

2. **Tahap 2: Klasifikasi (Supervised)**
   * Memuat dataset hasil clustering sebagai ground truth.
   * Menerapkan One-Hot Encoding pada fitur kategorikal dan membagi data dengan `train_test_split` (stratify=y).
   * Membangun model dengan **Decision Tree** serta eksperimen menggunakan **Random Forest**.
   * Melakukan Hyperparameter Tuning menggunakan **GridSearchCV** untuk optimasi performa.

## 📊 Hasil Evaluasi Model
* **Decision Tree (Baseline)**: Menunjukkan performa awal yang stabil untuk klasifikasi target.
* **Random Forest (Explore)**: Mengalami peningkatan akurasi dan generalisasi yang lebih baik.
* **Random Forest (Tuned)**: Menghasilkan performa paling optimal setelah melewati proses tuning parameter.
