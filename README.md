# Rock-Paper-Scissors Image Classification with CNN

## Ringkasan Proyek
Proyek ini merupakan implementasi dari algoritma **Convolutional Neural Network (CNN)** menggunakan TensorFlow/Keras untuk menyelesaikan masalah klasifikasi gambar multi-kelas, yaitu mendeteksi gestur tangan dalam permainan **Batu, Gunting, dan Kertas**.

Model dilatih menggunakan dataset dari Dicoding: [`rockpaperscissors`](https://github.com/dicodingacademy/assets/releases/download/release/rockpaperscissors.zip), yang mencakup lebih dari 2.000 gambar gestur dengan latar belakang beragam.

---

## Fitur Utama

- **Klasifikasi 3 Kelas**: Mendeteksi gestur tangan: batu, gunting, dan kertas.
- **Augmentasi Citra**: Menggunakan `ImageDataGenerator` untuk memperluas variasi data dan mencegah overfitting.
- **Arsitektur CNN Modular**: Terdiri dari beberapa lapisan konvolusi, pooling, dropout, dan fully connected.
- **Akurasi Tinggi**: Model mampu mencapai akurasi validasi **>96.6%**.
- **Prediksi Interaktif**: Notebook memungkinkan prediksi terhadap gambar baru yang diunggah.

---

## Arsitektur Model

Model dibangun secara sekuensial dengan TensorFlow:

1. **Conv2D + MaxPooling2D**: Untuk mengekstraksi fitur spasial.
2. **Flatten**: Mengubah representasi matriks menjadi vektor.
3. **Dropout**: Mengurangi overfitting.
4. **Dense (Fully Connected)**: Layer klasifikasi akhir.

**Konfigurasi:**
- **Optimizer**: `RMSprop`
- **Loss Function**: `categorical_crossentropy`
- **Activation**: `ReLU` di layer konvolusi, `Softmax` di output.

---

## Hasil Pelatihan

![image](https://github.com/user-attachments/assets/63c7a5b1-41d9-4d50-84a3-834ca3ff4368)


Model menunjukkan performa yang sangat baik dengan:

- Akurasi pelatihan dan validasi tinggi (>96%)
- Overfitting minimal
- Visualisasi plot akurasi dan loss tersedia di dalam notebook

---
## Setup Environment (Penerapan Lokal)
Ikuti langkah-langkah berikut untuk menyiapkan dan menjalankan proyek ini di lingkungan lokal Anda.

#### 1. Kloning Repository
Buka terminal atau command prompt Anda dan jalankan perintah berikut:
```bash
git clone [https://github.com/Faishal-Anwar/Rock-Paper-Scissors-Image-Classification.git](https://github.com/Faishal-Anwar/Rock-Paper-Scissors-Image-Classification.git)
cd Rock-Paper-Scissors-Image-Classification
```

#### 2. Buat Virtual Environment
Sangat disarankan untuk menggunakan virtual environment agar dependensi proyek tidak bercampur dengan instalasi Python global Anda.
```bash
virtualenv venv
```

#### 3. Aktifkan Virtual Environment
```bash
venv\Scripts\activate
```
macOS/Linux:
```bash
source venv/bin/activate
```
Setelah aktif, nama environment (venv) akan muncul di awal baris terminal Anda.

#### 4. Instal Dependensi
Instal semua pustaka Python yang dibutuhkan yang tercantum dalam file requirements.txt.
```bash
pip install -r requirements.txt
```

#### 5. Jalankan Jupyter Notebook
Setelah semua dependensi terinstal, jalankan server Jupyter Notebook.
```bash
jupyter notebook
```
Perintah ini akan membuka tab baru di browser web Anda. Dari sana, navigasikan dan buka file notebook.ipynb untuk menjalankan kode.
