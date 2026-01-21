# Credit Card Customer Segmentation using K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Sklearn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![K-Means](https://img.shields.io/badge/Algorithm-K--Means-green)

## 📌 Project Overview
Proyek ini bertujuan untuk melakukan **segmentasi nasabah kartu kredit** menggunakan algoritma *Unsupervised Learning*, yaitu **K-Means Clustering**. Dengan mengelompokkan nasabah berdasarkan perilaku penggunaan kartu kredit mereka (seperti saldo, total pembelian, dan pembayaran), bank dapat menentukan strategi pemasaran yang lebih personal dan efektif.

Proyek ini dikerjakan sebagai syarat pemenuhan tugas **Ujian Akhir Semester (UAS) Big Data**.

---

## 👨‍💻 Author
* **Nama:** Nazal Syamaidzar Mahendra
* **NIM:** 23.11.5547
* **Universitas:** Universitas Amikom Yogyakarta

---

## 📂 Dataset
Dataset yang digunakan adalah **Credit Card Dataset for Clustering** yang berisi perilaku penggunaan kartu kredit dari sekitar 9.000 nasabah aktif selama 6 bulan terakhir.

* **Sumber Data:** [Kaggle - CC GENERAL.csv](https://www.kaggle.com/arjunbhasin2013/ccdata)
* **Fitur Utama:**
    * `BALANCE`: Saldo yang dimiliki nasabah.
    * `PURCHASES`: Total pembelian yang dilakukan.
    * `CREDIT_LIMIT`: Limit kartu kredit nasabah.
    * `PAYMENTS`: Total pembayaran yang dilakukan.
    * `TENURE`: Jangka waktu layanan kartu kredit.

---

## 🛠️ Metodologi
Langkah-langkah yang dilakukan dalam proyek ini meliputi:

1.  **Data Preprocessing:**
    * Menghapus kolom `CUST_ID` yang tidak relevan.
    * Mengisi nilai kosong (*missing values*) dengan metode *Mean Imputation*.
    * Melakukan standarisasi data menggunakan **Standard Scaler** agar rentang nilai antar fitur setara.
2.  **Feature Selection:**
    * Menggunakan **Principal Component Analysis (PCA)** untuk mereduksi dimensi data dari 17 fitur menjadi 2 komponen utama (`PCA1` & `PCA2`) agar mudah divisualisasikan.
3.  **Modeling:**
    * Menentukan jumlah klaster optimal ($k$) menggunakan **Elbow Method**.
    * Menerapkan algoritma **K-Means Clustering** dengan jumlah klaster $k=4$.
4.  **Evaluasi Model:**
    * Mengukur kualitas klaster menggunakan **Davies-Bouldin Index (DBI)** dan **Silhouette Score**.

---

## 📊 Hasil Clustering
Berdasarkan analisis *Elbow Method*, didapatkan jumlah klaster optimal sebanyak **4 Klaster**. Berikut adalah karakteristik dari setiap segmen:

| Cluster | Tipe Nasabah | Karakteristik Utama |
| :--- | :--- | :--- |
| **0** | **Hemat / Pasif** | Saldo rendah, jarang melakukan pembelian. |
| **1** | **Boros / High Spender** | Total pembelian (`PURCHASES`) sangat tinggi. |
| **2** | **Cicilan Tinggi** | Saldo (`BALANCE`) tinggi, namun pembayaran cicilan lancar. |
| **3** | **Pengguna Tunai** | Sering melakukan tarik tunai (`CASH_ADVANCE`) tinggi. |

*(Catatan: Karakteristik di atas adalah interpretasi umum, detail angka rata-rata terdapat di dalam Notebook).*

---

## 📁 Struktur File
* `CC GENERAL.csv`: Dataset mentah yang digunakan.
* `UAS_BigData_23.11.5547.ipynb`: Jupyter Notebook berisi kode lengkap (Preprocessing, EDA, Modeling, Evaluasi).
* `model_kmeans_uas.pkl`: File model yang sudah dilatih dan disimpan (siap digunakan untuk prediksi).

---

## 🚀 Cara Menjalankan Project
1.  **Clone repositori ini:**
    ```bash
    git clone [https://github.com/username-anda/nama-repo.git](https://github.com/username-anda/nama-repo.git)
    ```
2.  **Install library yang dibutuhkan:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  **Jalankan Notebook:**
    Buka file `.ipynb` menggunakan Jupyter Notebook atau Google Colab.

---

## 📈 Evaluasi Model
Hasil metrik evaluasi untuk model ini adalah:
* **Davies-Bouldin Index:** *[Masukkan Angka DBI Anda]* (Semakin kecil semakin baik)
* **Silhouette Score:** *[Masukkan Angka Silhouette Anda]* (Semakin mendekati 1 semakin baik)

---

**Terima kasih telah berkunjung!**
Jangan ragu untuk memberikan ⭐ bintang jika proyek ini bermanfaat.
