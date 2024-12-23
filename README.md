# ✨ waste-It : Analisis Sentimen Ulasan Aplikasi GO-JEK dengan Menggunakan Model LSTM dan GRU ✨

## Latar Belakang & Tujuan
Aplikasi GO-JEK telah menjadi salah satu super-app terkemuka di Indonesia yang menyediakan berbagai layanan, seperti transportasi, pengiriman makanan, dan pembayaran digital. Ulasan pengguna memegang peran penting dalam menilai kualitas layanan dan kepuasan pelanggan. Analisis sentimen terhadap ulasan ini memberikan wawasan berharga mengenai persepsi pengguna terhadap performa aplikasi, terutama setelah pembaruan fitur atau versi tertentu.Dengan tujuan Mengidentifikasi sentimen positif, negatif, dan netral dalam ulasan aplikasi GO-JEK,Mengevaluasi dampak pembaruan aplikasi terhadap tingkat kepuasan pengguna,Memberikan rekomendasi berbasis data untuk perbaikan dan peningkatan kualitas layanan aplikasi.


Teknologi machine learning, seperti CNN dengan arsitektur InceptionV3 dan MobileNetV2, dapat mengotomatisasi klasifikasi sampah secara cepat dan akurat, mendukung daur ulang yang efisien. Solusi ini membantu mengurangi dampak negatif limbah rumah tangga sekaligus meningkatkan pengelolaan sampah berkelanjutan secara lokal dan global.

**Link Dataset yang digunakan:** [Garbage Dataset](https://www.kaggle.com/datasets/ucupsedaya/gojek-app-reviews-bahasa-indonesia).

**LSTM**

LSTM adalah jenis jaringan saraf tiruan yang termasuk dalam keluarga recurrent neural networks (RNN). LSTM dirancang untuk menangani masalah vanishing gradient yang sering terjadi pada RNN biasa. Model ini sangat efektif untuk mempelajari pola dalam data sekuensial, seperti teks, sinyal waktu (time series), atau data lain yang memiliki dependensi urutan.

**GRU**

GRU adalah jenis jaringan saraf tiruan yang termasuk dalam keluarga recurrent neural networks (RNN). GRU dikembangkan sebagai alternatif dari LSTM dengan struktur yang lebih sederhana, tetapi tetap efektif dalam menangani masalah vanishing gradient dan menangkap pola jangka panjang dalam data sekuensial.

## Dependensi & Langkah Instalasi 📃
dependencies = ["tensorflow>=2.18.0", "joblib>=1.4.2", "scikit-learn>=1.6.0", "streamlit>=1.41.1"]

1. wajib pdm init terlebih dahulu

2. install tensorflow di pdm =
- pdm info -> pastikan sudah berada di .venv
- pdm run python -m pip show tensorflow -> cek tensorflow apakah sudah di .venv
- pdm run python -m ensurepip --upgrade
- pdm run python -m pip install tensorflow
- pdm run python -c "import tensorflow as tf; print(tf._version_)"

## Struktur File 📄
- code/: Berkas kode ipynb dari model klasifikasi.
- src/uap/**app.py**: Berkas aplikasi utama yang berisi rute dan fungsi.
- src/uap/**klasifikasi_Teks.py**: Berkas penerapan dari model untuk klasifikasi dan tampilan antarmuka web.
- src/Model/: Berisi saved model berformat .h5 dari kedua arsitektur.

## Menjalankan App 💻
- Jalankan skrip dengan streamlit run ./src/app.py
- Akses aplikasi di peramban Web dengan alamat http://localhost:8501/


## Hasil Analisis
Berdasarkan perbandingan dari kedua arsitektur di atas, InceptionV3 menjadi model yang unggul apabila dinilai dari segi akurasi, namun grafik loss mengalami overfit. Sedangkan apabila dinilai dari segi grafik validasi MobileNetV2 lebih unggul karena lebih baik namun dari segi akurasi berada di bawah InceptionV3. 
Oleh karena itu, memungkinkan perlunya dilakukan perbaikan dalam pre-processing data seperti ditambahkannya augmentasi. Serta perlu ditambahkannya nilai epoch agar meningkatkan performa model.

## Local Web Deployment

### Tampilan HomePage

![image](assets/hp1.png)
![image](assets/hp2.png)

### Tampilan HomePage Setelah Upload Image

![image](assets/up.png)

### Tampilan Prediction Result

![image](assets/result1.png)
![image](assets/result2.png)
![image](assets/result3.png)

## Author 👨‍💻 
- Andrian Satrio B. | 202110370311518 [@iambethaviaji](https://github.com/iambethaviaji)
