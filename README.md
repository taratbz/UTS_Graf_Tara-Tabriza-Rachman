# UTS Graf Sains Data

## Deskripsi Proyek

Proyek ini dibuat untuk memenuhi tugas Ujian Tengah Semester (UTS) mata kuliah Graf Sains Data. Proyek berfokus pada analisis interaksi pengguna dan item menggunakan dataset Retailrocket serta penerapan konsep graf dan sistem rekomendasi.

Analisis dilakukan menggunakan Python untuk mengolah data interaksi, membentuk representasi User–Item, menghitung kemiripan antar pengguna dan item, serta menghasilkan rekomendasi berdasarkan pola interaksi pengguna.

## Tujuan

- Memahami struktur data interaksi pengguna dan item.
- Membentuk representasi interaksi dalam bentuk User–Item Matrix.
- Menganalisis kemiripan pola interaksi menggunakan cosine similarity.
- Menerapkan metode K-Nearest Neighbors (KNN) untuk rekomendasi item.
- Mengevaluasi hasil rekomendasi menggunakan metrik Hit@5 dan NDCG@5.

## Dataset

Dataset yang digunakan adalah **Retailrocket**, yang berisi catatan interaksi pengguna terhadap item, seperti melihat item (*view*), menambahkan item ke keranjang (*add to cart*), dan melakukan transaksi (*transaction*).

Data dibagi menjadi dua periode:

- **P1 (Training):** digunakan untuk membangun representasi interaksi dan menghasilkan rekomendasi.
- **P2 (Testing):** digunakan untuk mengevaluasi hasil rekomendasi berdasarkan interaksi aktual pengguna.

## Metode

1. **Persiapan Data**  
   Membaca, memfilter, dan mengolah data interaksi pada periode P1 dan P2.

2. **Representasi User–Item**  
   Membentuk matriks interaksi pengguna dan item menggunakan sparse matrix agar pengolahan data lebih efisien.

3. **Analisis Kemiripan**  
   Menggunakan cosine similarity untuk mengukur kemiripan pola interaksi antar pengguna maupun item.

4. **Sistem Rekomendasi KNN**  
   Memilih lima tetangga terdekat berdasarkan nilai similarity, kemudian menghitung skor kandidat item berdasarkan interaksi tetangga tersebut.

5. **Evaluasi Rekomendasi**  
   Mengukur hasil rekomendasi menggunakan Hit@5 dan Normalized Discounted Cumulative Gain at 5 (NDCG@5).

## Teknologi yang Digunakan

- Python
- Pandas
- NumPy
- SciPy
- Scikit-learn
- NetworkX
- Matplotlib
- Neo4j
- Jupyter Notebook

## Struktur Proyek

```text
UTS_Graf_Tara-Tabriza-Rachman/
├── cek_data.ipynb
├── events_P1_training.csv
├── events_P2_testing.csv
├── requirements.txt
└── README.md
```

*Struktur di atas merupakan contoh struktur proyek. Sesuaikan nama file dengan file yang benar-benar tersedia di repository.*

## Cara Menjalankan

1. Clone repository ini atau unduh file proyek.
2. Pastikan Python sudah terinstal.
3. Instal library yang diperlukan menggunakan perintah:

   ```bash
   pip install -r requirements.txt
   ```

4. Pastikan file dataset tersedia pada lokasi yang sesuai dengan path di notebook.
5. Buka `cek_data.ipynb` menggunakan Jupyter Notebook atau Visual Studio Code.
6. Jalankan setiap sel notebook secara berurutan.

Jika notebook menggunakan Neo4j, pastikan server Neo4j aktif dan konfigurasi koneksi sesuai dengan lingkungan yang digunakan.

## Evaluasi

Kinerja rekomendasi dianalisis menggunakan:

- **Hit@5:** mengukur apakah terdapat item rekomendasi yang cocok dengan item yang diinteraksikan pengguna pada periode testing.
- **NDCG@5:** mengukur kualitas urutan rekomendasi berdasarkan relevansi item.

Hasil evaluasi bergantung pada pengguna yang dipilih dan interaksi aktual yang tersedia pada periode testing.

## Penulis

**Tara Tabriza Rachman**  
Proyek UTS Graf Sains Data
