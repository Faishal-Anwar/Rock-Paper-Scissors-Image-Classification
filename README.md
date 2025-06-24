# Klasifikasi Gambar Kertas Gunting Batu dengan Algoritma CNN

---

Proyek ini bertujuan untuk membuat model klasifikasi gambar yang mampu mengklasifikasikan gestur tangan "batu", "gunting", dan "kertas".

### Daftar Isi

1.  [**Objektif Proyek**](#1-objektif-proyek)
2.  [**Instalasi**](#2-instalasi)
    * [Pengaturan Lingkungan](#pengaturan-lingkungan)
    * [Dataset](#dataset)
3.  [**Penggunaan**](#3-penggunaan)
4.  [**Arsitektur Model**](#4-arsitektur-model)
5.  [**Hasil**](#5-hasil)
6.  [**Kontribusi**](#6-kontribusi)
7.  [**Lisensi**](#7-lisensi)
8.  [**Kontak**](#8-kontak)

---

### 1. Objektif Proyek

Tujuan utama dari proyek ini adalah untuk mengembangkan model **Convolutional Neural Network (CNN)** yang secara akurat dapat mengklasifikasikan gambar gestur tangan batu, kertas, dan gunting. Aplikasi potensial dari model ini meliputi game interaktif atau sistem pengenalan gestur.

---

### 2. Instalasi

#### Pengaturan Lingkungan

Untuk menjalankan proyek ini, Anda memerlukan **Python** dan beberapa pustaka. Sangat disarankan untuk menggunakan _virtual environment_ untuk mengelola dependensi.

1.  **Kloning repositori:**

    ```bash
    git clone <URL_repositori_Anda> # Ganti dengan URL repositori GitHub Anda
    cd <nama_repositori_Anda> # Ganti dengan nama folder repositori Anda
    ```

2.  **Buat _virtual environment_ (opsional, tapi disarankan):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # Untuk Windows: `venv\Scripts\activate`
    ```

3.  **Instal pustaka yang dibutuhkan:**

    Pustaka-pustaka berikut digunakan dalam proyek ini. Anda bisa menginstalnya menggunakan `pip`:

    ```bash
    pip install -r requirements.txt
    ```

    Berikut adalah daftar dependensi utama beserta versinya (berdasarkan `requirements.txt` yang dihasilkan):

    ```
    absl-py==1.4.0
    astunparse==1.6.3
    certifi==2024.6.2
    charset-normalizer==3.3.2
    flatbuffers==24.3.25
    gast==0.5.4
    google-pasta==0.1.1
    grpcio==1.64.1
    h5py==3.11.0
    idna==3.7
    keras==3.3.3
    libclang==18.1.1
    Markdown==3.6
    MarkupSafe==2.1.5
    matplotlib==3.8.4
    ml-dtypes==0.3.2
    numpy==1.26.4
    opt-einsum==3.3.0
    packaging==24.0
    Pillow==10.3.0
    protobuf==4.25.3
    requests==2.32.3
    scipy==1.13.1
    setuptools==69.5.1
    six==1.16.0
    tensorboard==2.16.2
    tensorboard-data-server==0.7.2
    tensorflow==2.16.1
    tensorflow-io-gcs-filesystem==0.37.0
    termcolor==2.4.0
    typing_extensions==4.12.2
    urllib3==2.2.1
    Werkzeug==3.0.3
    wrapt==1.16.0
    zipfile36==0.1.3
    ```

    **Catatan:** Versi spesifik mungkin sedikit berbeda tergantung kapan Anda membuat file `requirements.txt`.

#### Dataset

Dataset yang digunakan untuk proyek ini adalah dataset **"Rock-Paper-Scissors"** yang tersedia secara publik di GitHub.

* Dataset diunduh dan diekstrak secara otomatis oleh Jupyter Notebook yang disediakan (`ML_KLASIFIKASI_KERTAS_GUNTING_BATU_DENGAN_ALGORITMA_CNN.ipynb`).
* Dataset ini terdiri dari gambar-gambar yang dikategorikan ke dalam tiga kelas: `rock` (batu), `paper` (kertas), dan `scissors` (gunting).

---

### 3. Penggunaan

Untuk melatih dan mengevaluasi model, cukup jalankan **Jupyter Notebook** `ML_KLASIFIKASI_KERTAS_GUNTING_BATU_DENGAN_ALGORITMA_CNN.ipynb`. Notebook ini akan melakukan langkah-langkah berikut:

1.  **Mengunduh dan mengekstrak** dataset.
2.  **Melakukan pra-pemrosesan** gambar menggunakan `ImageDataGenerator` untuk augmentasi dan pembagian menjadi _training set_ dan _validation set_.
3.  **Membangun dan mengkompilasi** model CNN.
4.  **Melatih** model dengan _callback_ kustom untuk penghentian awal (early stopping) dan pelacakan waktu pelatihan.
5.  **Mengevaluasi** performa model menggunakan plot untuk akurasi dan _loss_.
6.  **Menyimpan** model yang telah dilatih.
7.  **Memungkinkan prediksi manual** menggunakan gambar yang diunggah.

Anda dapat memodifikasi _notebook_ untuk bereksperimen dengan berbagai pengaturan _hyperparameter_ atau arsitektur model.

---

### 4. Arsitektur Model

Model yang digunakan adalah **CNN Sequential** dengan lapisan-lapisan berikut:

* **Lapisan Konvolusi (`Conv2D`):** Mengekstrak fitur dari gambar.
* **Lapisan _Max Pooling_ (`MaxPooling2D`):** Mengurangi dimensi dan biaya komputasi.
* **Lapisan _Dropout_ (`Dropout`):** Mencegah _overfitting_.
* **Lapisan _Flatten_ (`Flatten`):** Mengubah _feature map_ 2D menjadi vektor 1D.
* **Lapisan _Dense_ (`Dense`):** Lapisan terhubung penuh untuk klasifikasi. Lapisan terakhir menggunakan aktivasi `softmax` untuk klasifikasi multi-kelas.

**Ringkasan arsitektur model:**
