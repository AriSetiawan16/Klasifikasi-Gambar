
#  Proyek Deep Learning: Klasifikasi Daun Tomat

Proyek ini dikembangkan untuk membuat model deep learning yang mampu mengidentifikasi kondisi kesehatan daun tomat melalui citra gambar.  
Tujuan utama proyek ini adalah untuk membantu deteksi dini penyakit tanaman menggunakan teknologi klasifikasi berbasis AI.

---

## 📊 Performa Model

| Evaluasi                     | Skor       |
|-------------------------------|------------|
| Akurasi Data Uji (Testing)     | `98.70%`   |
| Akurasi Akhir Pelatihan (Train) | `98.37%`  |
| Akurasi Data Validasi          | `98.17%`   |

Model menunjukkan hasil yang sangat stabil dan akurat di seluruh tahap evaluasi.

---

## 🖼️ Tentang Proyek

Model CNN dikembangkan untuk mengklasifikasikan daun tomat ke dalam **empat kategori utama**:

- `Late_blight`
- `Septoria_leaf_spot`
- `Tomato_Yellow_Leaf_Curl_Virus`
- `Healthy`

Dataset diambil dari subset **PlantVillage** yang fokus hanya pada daun tomat.

---

## 📁 Rincian Dataset

- **Asal Dataset**: [PlantVillage di Kaggle](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset)
- **Jumlah Total Gambar**: `54,305`
- **Jumlah Gambar Daun Tomat**: `18,160`

Dataset ini mengandung berbagai penyakit tanaman, tetapi hanya gambar daun tomat yang dipilih untuk pelatihan model.

---

## 🛠️ Arsitektur Model

Model dibangun dengan framework **TensorFlow** dan **Keras**, menggunakan struktur dasar berikut:

- Layer konvolusi `Conv2D`
- Layer pooling `MaxPooling2D`
- Layer dense fully connected `Dense`
- Regularisasi dengan `Dropout`
- Aktivasi fungsi `ReLU` dan `Softmax`

Optimasi menggunakan **Adam Optimizer**, dengan fungsi loss **categorical_crossentropy**.

---

## 🚀 Keunggulan Proyek

- Data preprocessing otomatis (resize, normalisasi)
- Data augmentasi untuk meningkatkan generalisasi
- Konversi model ke format **TF Lite** dan **TFJS**
- Interface prediksi gambar interaktif di Google Colab
- Struktur model modular dan siap deployment

---

## 📦 Output Proyek

- `SavedModel` format TensorFlow
- `model.h5` file untuk Keras
- `model_converted.tflite` untuk mobile apps
- `tfjs_model/` folder untuk penggunaan di web

---

## 🖼️ Kelas Keluaran

| Nama Kelas                        | Penjelasan |
|------------------------------------|------------|
| `Late_blight`                      | Penyakit busuk daun oleh *Phytophthora infestans* |
| `Septoria_leaf_spot`               | Penyakit bintik daun oleh *Septoria lycopersici* |
| `Tomato_Yellow_Leaf_Curl_Virus`    | Infeksi virus yang menyebabkan daun melengkung dan menguning |
| `Healthy`                          | Daun dalam kondisi sehat tanpa penyakit |

---

## 🔍 Contoh Hasil Prediksi

<div align="center">

  <img src="images/Inference.png" alt="Inference Example" width="300"/>
  <p><em>Contoh prediksi: Healthy (Confidence 100%)</em></p>

</div>

---
