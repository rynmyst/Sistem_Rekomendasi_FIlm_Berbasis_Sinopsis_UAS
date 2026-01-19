Baik. Berikut **README versi terbaru** yang **sesuai dengan kondisi repository saat ini** (dataset lain sudah dihapus, hanya `movies_metadata.csv` yang digunakan).
Bahasanya **formal**, **tanpa emoticon**, dan **siap langsung di-copy ke GitHub**.

---

# Sistem Rekomendasi Film Berbasis Sinopsis Menggunakan Deep Learning dan Transformer

## Deskripsi Proyek

Proyek ini mengimplementasikan **sistem rekomendasi film berbasis konten** dengan memanfaatkan **model Deep Learning Transformer** untuk memahami kemiripan semantik antar film berdasarkan **sinopsis**.
Pendekatan yang digunakan adalah **Hybrid Recommendation System**, yaitu menggabungkan **embedding teks hasil Transformer** dengan **metadata film** seperti rating dan popularitas untuk meningkatkan kualitas rekomendasi.

Aplikasi dikembangkan dalam bentuk **Notebook Python** dan dideploy menggunakan **Gradio** sebagai antarmuka interaktif.

---

## Dataset

Dataset bersumber dari **The Movies Dataset (Kaggle)** oleh Rounak Banik.
Namun, dalam proyek ini **hanya satu file dataset yang digunakan**, yaitu:

* `movies_metadata.csv`

### Alasan Penggunaan Satu Dataset

File `movies_metadata.csv` sudah mencakup informasi utama yang dibutuhkan untuk sistem rekomendasi berbasis konten, antara lain:

* Judul film
* Sinopsis (overview)
* Genre
* Tahun rilis
* Rating dan jumlah voting
* Popularitas

Dataset lain seperti `credits.csv`, `ratings.csv`, dan `keywords.csv` **tidak digunakan** untuk:

* Menghindari ketergantungan pada data user (collaborative filtering)
* Menjaga fokus penelitian pada **content-based recommendation**
* Mengurangi kompleksitas dan ukuran penyimpanan proyek

---

## Struktur Folder

```
.
├── FINAL.ipynb
├── README.md
├── requirements.txt
├── movie_embeddings.pkl
├── movie_nn_model.pkl
└── dataset
    └── movies_metadata.csv
```

---

## Arsitektur Sistem

1. **Preprocessing Teks**

   * Sinopsis dan metadata digabung menjadi satu representasi teks (`combined_text`)
   * Pembersihan teks dan normalisasi

2. **Transformer Embedding**

   * Menggunakan model pre-trained `all-MiniLM-L6-v2`
   * Menghasilkan embedding berdimensi 384 untuk setiap film

3. **Similarity Search**

   * Menggunakan cosine similarity
   * Dipercepat dengan Nearest Neighbors (scikit-learn)

4. **Hybrid Scoring**

   * Skor akhir merupakan kombinasi dari:

     * Similarity score (embedding)
     * Rating film
     * Popularitas (jumlah vote)

---

## Evaluasi Sistem

Evaluasi dilakukan menggunakan beberapa metrik:

* **Semantic Similarity Score**
* **Rating Quality**
* **Diversity**
* **Perbandingan Baseline vs Hybrid**

Hasil evaluasi menunjukkan bahwa pendekatan Hybrid mampu meningkatkan kualitas rekomendasi dengan **peningkatan rata-rata rating sebesar 12.5%** dibandingkan metode baseline.

---

## Teknologi yang Digunakan

* Python
* Sentence Transformers
* Scikit-learn
* Pandas & NumPy
* Matplotlib
* Gradio

---

## Deployment

Aplikasi dijalankan melalui **Gradio Interface** yang terdapat di dalam notebook:

* File utama: `FINAL.ipynb`
* Jalankan seluruh cell hingga bagian Gradio
* Aplikasi akan menampilkan antarmuka web interaktif untuk rekomendasi film

---

## Cara Menjalankan Proyek

1. Clone repository:

```bash
git clone https://github.com/rynmyst/Sistem_Rekomendasi_FIlm_Berbasis_Sinopsis_UAS.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Jalankan notebook:

```bash
jupyter notebook FINAL.ipynb
```

4. Jalankan semua cell hingga Gradio interface muncul.

---

## Catatan

* File `movie_embeddings.pkl` dan `movie_nn_model.pkl` digunakan untuk mempercepat proses tanpa perlu membuat ulang embedding.
* Sistem ini merupakan **content-based recommendation**, tidak menggunakan data interaksi pengguna.

---

Jika mau, saya bisa:

* Menyesuaikan README agar sesuai standar **paper / tugas akhir**
* Membuat versi README **lebih singkat untuk GitHub**
* Menyesuaikan bahasa README agar **selaras dengan laporan teknis dan paper**

Tinggal bilang mau versi yang mana.
