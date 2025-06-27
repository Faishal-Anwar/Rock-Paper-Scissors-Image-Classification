# Klasifikasi Gambar Kertas Gunting Batu dengan CNN

---

Proyek ini mengembangkan model **Convolutional Neural Network (CNN)** untuk mengklasifikasikan gambar gestur tangan "batu", "gunting", dan "kertas".

## Instalasi

1.  **Kloning repositori:**
    ```bash
    git clone https://github.com/Faishal-Anwar/Rock-Paper-Scissors-Image-Classification
    cd Rock-Paper-Scissors-Image-Classification
    ```
2.  **Instal dependensi:**
    ```bash
    pip install -r requirements.txt
    ```
    Daftar dependensi ada di `requirements.txt`.

## Penggunaan

Jalankan **Jupyter Notebook** `ML_KLASIFIKASI_KERTAS_GUNTING_BATU_DENGAN_ALGORITMA_CNN.ipynb`. Notebook ini akan:
* Mengunduh dan menyiapkan dataset.
* Melakukan augmentasi data.
* Melatih model CNN.
* Menampilkan hasil evaluasi (akurasi & _loss_).
* Memungkinkan Anda mencoba prediksi dengan gambar baru.

## Arsitektur Model

Model menggunakan arsitektur CNN Sequential dengan lapisan konvolusi, _max pooling_, _dropout_, dan _dense_. Model dikompilasi dengan _loss_ `categorical_crossentropy` dan _optimizer_ `SGD`.

## Hasil

Model dilatih hingga mencapai akurasi **di atas 96,6%** pada data validasi. Plot akurasi dan _loss_ selama pelatihan juga tersedia di dalam _notebook_.

![Training and Validation Accuracy and Loss](https://raw.githubusercontent.com/dicodingacademy/assets/main/asset_final_project/Plot%20Akurasi%20dan%20Loss.png)
*(Gambar ilustrasi, ganti dengan plot hasil pelatihan Anda.)*

## Kontribusi

Kontribusi dalam bentuk _issue_ atau _pull request_ sangat kami hargai.

## Lisensi

Proyek ini dilisensikan di bawah **Lisensi MIT**.

## Kontak

* **Faishal Anwar Hasyim**
* [LinkedIn](https://www.linkedin.com/in/faishal-anwar-hasyim-1391682a5/)
* [Profil Dicoding](https://www.dicoding.com/users/anwarfaishal86/academies)
