# Klasifikasi Penyakit Daun Padi

Tugas UTS mata kuliah Pengantar Algoritma Deep Learning. Pada proyek ini kami membandingkan dua model, yaitu MLP dan CNN, untuk mengenali empat jenis penyakit daun padi dari gambar.

## Dataset

Dataset: [Rice Leaf Disease Classification India](https://huggingface.co/datasets/Project-AgML/rice_leaf_disease_classification_india) (Hugging Face, Project-AgML; lisensi CC BY 4.0 sebagaimana tercantum pada halaman sumber).

Terdapat empat kelas: **Bacterialblight, Blast, Brownspot, dan Tungro**. Dari 5.932 gambar awal, 1.180 gambar duplikat identik dihapus sehingga digunakan 4.752 gambar. Data dibagi menjadi 3.326 untuk training, 713 untuk validation, dan 713 untuk testing.

## Cara menjalankan

1. Buka [Google Colab](https://colab.research.google.com/).
2. Unggah `notebooks/klasifikasi_penyakit_daun_padi.ipynb`.
3. Jalankan sel kode dari atas ke bawah. Gunakan GPU jika tersedia.
4. Notebook akan mengambil dataset langsung dari Hugging Face, lalu melatih dan menguji MLP serta CNN.

Diperlukan koneksi internet untuk mengunduh dataset dan memasang library yang belum tersedia. Daftar library juga ada di `requirements.txt`.

## Hasil pengujian

| Model | Akurasi testing | Loss | F1-score macro |
|---|---:|---:|---:|
| MLP | 52,45% | 1,0808 | 43,53% |
| CNN | 95,23% | 0,1212 | 95,01% |

Angka tersebut berasal dari hasil eksekusi notebook yang disimpan pada proyek ini. Grafik dan confusion matrix dapat dilihat di folder `reports/`.

## Isi folder

- `data/`: catatan sumber dataset.
- `notebooks/`: kode Colab beserta output eksperimen.
- `src/`: disediakan sesuai panduan tugas; seluruh kode saat ini masih ada di notebook.
- `models/`: model CNN yang sudah dilatih. Model MLP disimpan dalam arsip hasil Colab terpisah karena ukuran filenya besar.
- `reports/`: grafik, confusion matrix, tabel evaluasi, dan hasil prediksi.

Proyek ini baru mencakup tahap UTS. Pengembangan aplikasi dan transfer learning belum dilakukan.
