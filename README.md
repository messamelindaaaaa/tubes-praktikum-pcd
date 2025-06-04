# ♻️ Identifikasi Sampah Plastic, Paper, dan Glass Menggunakan Fitur Warna, Bentuk, dan Tekstur

## 👥 Anggota Kelompok
- **Angelina Geronsiana Yudrikewati** — 152023077  
- **Farisy Ilman Syarif** — 152023135  
- **Mesa Melinda** — 152023178  

---

## 📌 Deskripsi Proyek
Proyek ini merupakan implementasi sistem identifikasi sampah otomatis menggunakan teknik **Pengolahan Citra Digital (PCD)** dan algoritma **Machine Learning tradisional**. Fokus utama adalah mengidentifikasi kategori sampah (`plastic`, `paper`, `glass`) berdasarkan **fitur visual** dari citra RGB, seperti **warna**, **bentuk**, dan **tekstur**.

---

## 🎯 Tujuan Utama Proyek
1. Mengembangkan program untuk ekstraksi fitur **warna**, **bentuk**, dan **tekstur** dari citra RGB.
2. Mengembangkan program untuk melakukan **klasifikasi citra** menggunakan fitur yang telah diekstrak dan model Machine Learning.

---

## 🗑️ Kategori Sampah yang Diklasifikasi
Proyek ini berfokus pada klasifikasi 3 kategori utama:
1. **Plastic** – fokus pada ekstraksi fitur **Tekstur**
2. **Paper** – fokus pada ekstraksi fitur **Warna**
3. **Glass** – fokus pada ekstraksi fitur **Bentuk**

---

## 🧪 Tahapan Implementasi

### 1️⃣ Preprocessing Citra
- **Pembacaan Citra**: Menggunakan `Pillow` untuk membuka citra dan mengonversinya ke RGB.
- **Resize**: Semua citra diubah ukurannya menjadi `128x128` piksel dengan `cv2.resize`.
- **Konversi Grayscale**: Digunakan untuk ekstraksi **tekstur** dan **bentuk** menggunakan `cv2.cvtColor`.

### 2️⃣ Ekstraksi Fitur
Menangkap karakteristik visual dari setiap kategori:

#### 🔹 Plastic – Fitur Tekstur
- **Metode**: Local Binary Pattern (LBP) dari `scikit-image`
- **Deskripsi**: Menangkap pola lokal dengan histogram nilai-nilai LBP.

#### 🔸 Paper – Fitur Warna
- **Metode**: Histogram warna dalam ruang warna HSV.
- **Deskripsi**: RGB dikonversi ke HSV, lalu dihitung histogram dari setiap channel.

#### 🔷 Glass – Fitur Bentuk
- **Metode**: Hu Moments + Properti Geometri
- **Deskripsi**:
  - Blur dan thresholding adaptif untuk membedakan objek dari latar belakang.
  - Deteksi kontur menggunakan `cv2.findContours`.
  - Hitung Hu Moments dan fitur geometri seperti area, perimeter, dan rasio aspek.

---

### 3️⃣ Klasifikasi Citra
Menggunakan fitur yang diekstrak untuk membangun model klasifikasi.

- **Pembagian Data**: 70% data training, 30% data testing dengan `train_test_split` dan `stratify`.
- **Model**:
  - **K-Nearest Neighbors (KNN)**: Klasifikasi berdasarkan mayoritas dari K tetangga terdekat.
  - **Support Vector Machine (SVM)**: Mencari hyperplane terbaik yang memisahkan kelas.
- **Evaluasi**: Menggunakan **accuracy_score** untuk mengukur performa.

---

## 📁 Hasil Output
Setelah menjalankan `main.py`, file output yang akan dihasilkan:

- `output_fitur_ekstraksi.csv` – Semua fitur yang diekstrak dari citra.
- `predictions_knn.csv` – Hasil prediksi dari model KNN.
- `predictions_svm.csv` – Hasil prediksi dari model SVM.
- `training_data_info.csv` – Informasi citra training.
- `testing_data_info.csv` – Informasi citra testing.

---

