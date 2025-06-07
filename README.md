# ♻️ Ekstraksi Fitur Warna, Bentuk, dan Tekstur untuk Klasifikasi Sampah RGB

## 👥 Anggota Kelompok
- **Angelina Geronsiana Yudrikewati** — 152023077  
- **Farisy Ilman Syarif** — 152023135  
- **Mesa Melinda** — 152023178  

## Deskripsi Proyek

Proyek ini mengimplementasikan sistem klasifikasi citra untuk mengidentifikasi berbagai jenis sampah (misalnya, plastik, kertas, organik) berdasarkan fitur-fitur visual yang diekstraksi dari gambar. Sistem ini menggunakan kombinasi fitur warna, bentuk, dan tekstur, kemudian melatih model pembelajaran mesin seperti Support Vector Machine (SVM) dan K-Nearest Neighbors (KNN) untuk melakukan klasifikasi.

Fitur-fitur utama yang diekstrak meliputi:
* **Warna**: Histogram RGB dan HSV, statistik mean dan standar deviasi channel warna.
* **Bentuk**: Luas, keliling, rasio aspek, ekstensi, soliditas, dan Hu Moments.
* **Tekstur**: Properti Gray Level Co-occurrence Matrix (GLCM) seperti kontras, dissimilarity, homogenitas, energi, korelasi, serta Local Binary Pattern (LBP) dan Shannon Entropy.

## Fitur Utama

* **Ekstraksi Fitur Komprehensif**: Menggabungkan fitur warna, bentuk, dan tekstur untuk representasi citra yang kaya.
* **Visualisasi Tahapan Ekstraksi**: Opsi untuk menampilkan langkah-langkah ekstraksi fitur secara visual untuk setiap gambar, membantu pemahaman dan debugging.
* **Preprocessing Otomatis**: Penyesuaian ukuran gambar dan konversi ruang warna.
* **Normalisasi Fitur**: Menggunakan `StandardScaler` untuk memastikan fitur memiliki skala yang seragam, meningkatkan kinerja model.
* **Pelatihan Model Fleksibel**: Mendukung model klasifikasi SVM dan KNN, dengan mudah dapat diperluas untuk model lain.
* **Evaluasi Model**: Melaporkan akurasi, _confusion matrix_, dan _classification report_ untuk setiap model yang dilatih.
* **Penyimpanan Fitur**: Fitur yang diekstraksi dapat disimpan ke file CSV untuk analisis lebih lanjut.
  
## Hasil
Skrip akan mencetak akurasi, classification report (presisi, recall, f1-score), dan confusion matrix untuk setiap model (SVM dan KNN) yang dilatih.
