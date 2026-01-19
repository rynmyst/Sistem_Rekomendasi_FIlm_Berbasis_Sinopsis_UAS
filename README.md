# Sistem_Rekomendasi_Film_Berbasis_Sinopsis_Menggunakan_DeepLearning_dan_Transformer


#  Movie Recommendation System (Transformer + Hybrid)

Sistem rekomendasi film berbasis **Deep Learning** menggunakan **pre-trained Transformer** untuk memahami makna sinopsis film dan **Hybrid Scoring** untuk meningkatkan kualitas rekomendasi.

 **Deployed via Gradio (Notebook-based Interface)**

---

##  Fitur Utama

*  **Transformer-based Embedding** (SentenceTransformer)
*  **Cosine Similarity** untuk pencarian film serupa
*  **Hybrid Recommendation**

  * Similarity embedding
  * Rating film
  * Popularitas (jumlah vote)
*  Visualisasi embedding (Norma & PCA)
*  Antarmuka interaktif menggunakan **Gradio**

---

##  Struktur Project

```
 Tugas Proyek 2
├── 📁 dataset
│   ├── credits.csv
│   ├── keywords.csv
│   ├── links.csv
│   ├── links_small.csv
│   ├── movies_metadata.csv
│   ├── ratings.csv
│   └── ratings_small.csv
│
├── FINAL.ipynb
├── movie_embeddings.pkl
├── movie_nn_model.pkl
├── requirements.txt
└── README.md
```

---

##  Arsitektur Sistem

1. **Input teks film** (sinopsis + genre + keyword)
2. **Transformer Encoder** → embedding numerik
3. **Nearest Neighbors (Cosine Similarity)**
4. **Hybrid Scoring** (Similarity + Rating + Popularitas)
5. **Output rekomendasi film**

 *Tempat diagram arsitektur (opsional)*

> `Gambar 1. Skema Sistem Rekomendasi Film Berbasis Transformer`

---

##  Hasil Evaluasi

*  **Baseline Rating**: 6.14 / 10
*  **Hybrid Rating**: 6.91 / 10
*  **Peningkatan Kinerja**: **+12.5%**
*  Berdasarkan **10 test cases**

✔Hybrid system terbukti lebih stabil dan relevan dibanding similarity murni.



## Cara Menjalankan

<<<<<<< HEAD
###  Install Dependencies
=======
### 1.  Install Dependencies
>>>>>>> 8874945ca688eae1b07bcefcb66004702cb9a495

```bash
pip install -r requirements.txt
```

Atau di notebook:

```python
!pip install -r requirements.txt
```

<<<<<<< HEAD
### 2️Jalankan Notebook
=======
### 2️. Jalankan Notebook
>>>>>>> 8874945ca688eae1b07bcefcb66004702cb9a495

Buka dan jalankan:

```
FINAL.ipynb
```

<<<<<<< HEAD
### 3️Gunakan Aplikasi
=======
### 3️. Gunakan Aplikasi
>>>>>>> 8874945ca688eae1b07bcefcb66004702cb9a495

* Gradio interface akan muncul otomatis
* Masukkan **judul film**
* Sistem menampilkan **rekomendasi film serupa**

---

## Teknologi

* Python
* Sentence Transformers
* HuggingFace Transformers
* Scikit-learn
* Pandas, NumPy
* Matplotlib
* Gradio

---

##  Contoh Input

```
Toy Story
```

##  Contoh Output

* Toy Story 2 (1999)
* Toy Story 3 (2010)
* The 41–Year–Old Virgin Who Knocked Up Sarah Marshall and Felt Superbad About It (2010)
* Child's Play 3 (1991)
* Firestarter (1984)
---

##  Catatan

Proyek ini dikembangkan untuk **tujuan akademik** dan eksplorasi sistem rekomendasi berbasis **Deep Learning**.



