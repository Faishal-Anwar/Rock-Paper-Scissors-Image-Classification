# Klasifikasi Gambar Batu-Gunting-Kertas dengan CNN

<p align="center">
  <img src="https://raw.githubusercontent.com/dicodingacademy/assets/main/asset_final_project/Plot%20Akurasi%20dan%20Loss.png" width="600">
  <br>
  <i>(Gambar ini adalah ilustrasi plot akurasi dan loss dari proses pelatihan.)</i>
</p>

## 📖 Gambaran Umum Proyek
Proyek ini mendemonstrasikan implementasi **Convolutional Neural Network (CNN)** untuk menyelesaikan masalah klasifikasi gambar multi-kelas. Studi kasus yang digunakan adalah permainan klasik "Batu, Gunting, Kertas". Model dilatih untuk mengenali dan mengklasifikasikan gambar gestur tangan ke dalam tiga kategori tersebut dengan tingkat akurasi yang tinggi.

Proyek ini mencakup seluruh alur kerja machine learning, mulai dari pengumpulan dan persiapan data, augmentasi gambar untuk memperkaya dataset, perancangan arsitektur model CNN, proses pelatihan, hingga evaluasi performa model.

### ✨ Fitur Utama
* **Klasifikasi Tiga Kelas**: Mampu membedakan antara gestur tangan batu, gunting, dan kertas.
* **Augmentasi Data**: Menggunakan `ImageDataGenerator` dari TensorFlow untuk meningkatkan variasi data latih dan mencegah *overfitting*.
* **Arsitektur CNN**: Membangun model sekuensial yang terdiri dari lapisan konvolusi dan *pooling* untuk ekstraksi fitur yang efektif.
* **Evaluasi Model**: Menampilkan visualisasi plot akurasi dan *loss* untuk data latih dan validasi.
* **Prediksi Interaktif**: Notebook memungkinkan pengguna untuk mengunggah gambar baru dan melihat hasil prediksi dari model yang telah dilatih.

## ⚙️ Arsitektur Model
Model yang digunakan adalah arsitektur CNN sekuensial yang dibangun dengan TensorFlow/Keras. Struktur utamanya adalah sebagai berikut:
1.  **Lapisan Konvolusi (`Conv2D`)**: Beberapa lapisan konvolusi dengan fungsi aktivasi `ReLU` untuk mengekstraksi fitur visual dari gambar seperti tepi, bentuk, dan tekstur.
2.  **Lapisan Max-Pooling (`MaxPooling2D`)**: Mengurangi dimensi spasial (lebar dan tinggi) dari *feature map* untuk membuat representasi fitur lebih efisien dan tahan terhadap variasi posisi.
3.  **Lapisan Flatten**: Mengubah data dari format 2D (matriks) menjadi format 1D (vektor) agar dapat diproses oleh lapisan *fully connected*.
4.  **Lapisan Dropout**: Menonaktifkan sebagian neuron secara acak selama pelatihan untuk mengurangi *overfitting*.
5.  **Lapisan Dense (Fully Connected)**: Lapisan akhir yang berfungsi sebagai klasifikator. Menggunakan fungsi aktivasi `softmax` untuk menghasilkan probabilitas untuk setiap kelas (batu, gunting, kertas).

Model dikompilasi menggunakan:
* **Loss Function**: `categorical_crossentropy`, cocok untuk masalah klasifikasi multi-kelas.
* **Optimizer**: `SGD` (Stochastic Gradient Descent) atau `Adam` untuk mengoptimalkan bobot model selama pelatihan.

## 📊 Hasil
Model berhasil dilatih dan mencapai tingkat akurasi **di atas 96.6%** pada set data validasi. Analisis lebih lanjut mengenai kurva pembelajaran (akurasi dan *loss*) tersedia secara lengkap di dalam Jupyter Notebook.

## 🛠️ Setup Environment (Penerapan Lokal)
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
Perintah ini akan membuka tab baru di browser web Anda. Dari sana, navigasikan dan buka file ML_KLASIFIKASI_KERTAS_GUNTING_BATU_DENGAN_ALGORITMA_CNN.ipynb untuk menjalankan kode.
