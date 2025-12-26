# Laporan Proyek Sistem Rekomendasi (Dicoding - Machine Learning Terapan)

## 1. Project Overview
Sistem rekomendasi membantu pengguna menemukan item yang relevan dari banyak pilihan. Pada kasus katalog film, pengguna sering kesulitan memilih film yang sesuai preferensinya (misalnya genre atau tema tertentu). Proyek ini membangun sistem rekomendasi film sederhana yang mampu menghasilkan rekomendasi Top-N dengan dua pendekatan yang berbeda: **Content-Based Filtering** dan **Collaborative Filtering**.

**Mengapa penting:** rekomendasi yang baik meningkatkan pengalaman pengguna, mempercepat discovery, dan berpotensi meningkatkan engagement/retensi.

**Referensi singkat:**
- Ricci, Rokach, Shapira (2015). *Recommender Systems Handbook* (konsep umum sistem rekomendasi).
- Konsep TF-IDF & Cosine Similarity (content-based) dan Matrix Factorization (collaborative).

## 2. Business Understanding

### 2.1 Problem Statements
1. Bagaimana memberikan rekomendasi film yang mirip berdasarkan konten (genre + ringkasan) dari film yang disukai pengguna?
2. Bagaimana memberikan rekomendasi film berdasarkan pola rating pengguna lain (kolaboratif)?

### 2.2 Goals
1. Menghasilkan rekomendasi **Top-N** film dengan pendekatan content-based.
2. Menghasilkan rekomendasi **Top-N** film dengan pendekatan collaborative filtering.
3. Mengevaluasi performa rekomendasi menggunakan metrik yang sesuai untuk Top-N recommendation.

### 2.3 Solution Approach (Tambahan)
- **Approach 1: Content-Based Filtering**
  - Membuat representasi fitur teks film (genre + ringkasan) menggunakan TF-IDF.
  - Mengukur kemiripan antar film dengan cosine similarity.
  - Rekomendasi dihasilkan dari film yang mirip dengan film favorit/seed.
- **Approach 2: Collaborative Filtering**
  - Membuat matriks user-item rating.
  - Menerapkan matrix factorization (TruncatedSVD) untuk mempelajari latent factors.
  - Memperkirakan rating item yang belum ditonton, lalu rekomendasikan Top-N tertinggi.

## 3. Data Understanding
Dataset yang digunakan berupa dataset mini (contoh) berisi:
- Tabel **movies**: id, title, genres, overview
- Tabel **ratings**: user_id, movie_id, rating

Ringkasan:
- Jumlah user: dibangun dari data contoh (puluhan interaksi).
- Jumlah item: puluhan film contoh.
- Jumlah interaksi: puluhan rating.
- Karakteristik: sparse (tidak semua user memberi rating semua film).

**Deskripsi fitur:**
- `movie_id`: id film.
- `title`: judul film.
- `genres`: genre (teks).
- `overview`: ringkasan singkat (teks).
- `user_id`: id pengguna.
- `rating`: rating 1–5.

**EDA & insight:**
- Distribusi jumlah rating per user dan per film membantu melihat potensi cold-start.
- Distribusi rating (misal dominan 4–5) mempengaruhi definisi “relevant item”.

## 4. Data Preparation
Tahapan yang dilakukan:
1. Pembersihan data sederhana (cek duplikasi, missing).
2. Menentukan item relevan: rating >= 4 dianggap relevant.
3. Train-test split per user (holdout): sebagian interaksi per user disimpan sebagai test.
4. Untuk content-based: menggabungkan `genres` + `overview` menjadi fitur teks dan membangun TF-IDF matrix.
5. Untuk collaborative: encoding user & item dan membangun matriks user-item.

Alasan:
- Split per user diperlukan agar evaluasi Top-N mengukur kemampuan model merekomendasikan item yang benar-benar belum terlihat di data train.
- TF-IDF membantu mengubah teks menjadi vektor numerik.
- Matrix factorization membantu menangkap pola preferensi bersama antar user.

## 5. Modeling and Result

### 5.1 Model 1: Content-Based Filtering
**Algoritma:** TF-IDF + cosine similarity.  
**Output:** Top-N film paling mirip dengan seed film.  
**Kelebihan:** bekerja baik saat data rating sedikit, mudah dijelaskan.  
**Kekurangan:** tidak menangkap “wisdom of the crowd”, sulit mengatasi variasi preferensi yang tidak tercermin di konten.

### 5.2 Model 2: Collaborative Filtering
**Algoritma:** Matrix factorization (TruncatedSVD pada matriks user-item).  
**Output:** Top-N film dengan prediksi skor tertinggi untuk user (yang belum dirating).  
**Kelebihan:** bisa menangkap pola preferensi antar user.  
**Kekurangan:** cold-start untuk user/item baru, perlu interaksi yang cukup.

## 6. Evaluation
Metrik Top-N yang digunakan:

- **Precision@K**
  - Mengukur proporsi item rekomendasi (Top-K) yang relevan.
  - Formula: Precision@K = (jumlah item relevan dalam Top-K) / K
- **Recall@K**
  - Mengukur seberapa banyak item relevan berhasil ditemukan dalam Top-K.
  - Formula: Recall@K = (jumlah item relevan dalam Top-K) / (jumlah item relevan di test)

Evaluasi dilakukan per user, lalu dirata-ratakan (macro average).  
Hasil evaluasi ditampilkan pada notebook dalam bentuk tabel untuk kedua pendekatan.

## 7. Kesimpulan
Dua pendekatan menghasilkan rekomendasi Top-N dan dapat dievaluasi menggunakan Precision@K dan Recall@K. Content-based unggul untuk penjelasan & cold-start item (selama ada metadata), sedangkan collaborative menangkap preferensi kolektif namun membutuhkan interaksi yang memadai. Pengembangan selanjutnya dapat menambah dataset lebih besar, implicit feedback, dan tuning hyperparameter.
