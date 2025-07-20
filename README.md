# 🍚 Rice Variety Classification with CNN

Proyek ini merupakan implementasi klasifikasi varietas beras menggunakan Convolutional Neural Network (CNN) dengan TensorFlow dan Keras. Dataset yang digunakan adalah **Rice Image Dataset** dari Kaggle, yang berisi 75.000 gambar biji beras dari lima varietas berbeda: Arborio, Basmati, Ipsala, Jasmine, dan Karacadag.([Kaggle][1])

## 📁 Dataset

Dataset ini terdiri dari 75.000 gambar, masing-masing varietas memiliki 15.000 gambar. Gambar-gambar ini telah diproses sebelumnya dan memiliki resolusi 250x250 piksel.

Struktur folder dataset setelah dipisah untuk pelatihan, validasi, dan pengujian:

```
dataset/
├── train/
│   ├── Arborio/
│   ├── Basmati/
│   ├── Ipsala/
│   ├── Jasmine/
│   └── Karacadag/
├── val/
│   ├── Arborio/
│   ├── Basmati/
│   ├── Ipsala/
│   ├── Jasmine/
│   └── Karacadag/
└── test/
    ├── Arborio/
    ├── Basmati/
    ├── Ipsala/
    ├── Jasmine/
    └── Karacadag/
```

## 🧠 Model

Model CNN dibangun menggunakan TensorFlow Keras dengan arsitektur sebagai berikut:

* Beberapa lapisan Conv2D dan MaxPooling
* Lapisan Flatten
* Lapisan Dense dengan fungsi aktivasi ReLU
* Lapisan Dropout untuk mengurangi overfitting
* Lapisan Dense akhir dengan fungsi aktivasi softmax untuk klasifikasi multi-kelas([Kaggle][2])

Model dilatih untuk mencapai akurasi minimal 85% pada data validasi.

## 🔍 Evaluasi

* Akurasi dan loss pada data pelatihan dan validasi
* Visualisasi kurva loss dan akurasi
* Confusion Matrix dan classification report
* Prediksi beberapa sampel dari data uji

## 💾 Penyimpanan Model

Model yang telah dilatih disimpan dalam beberapa format untuk berbagai kebutuhan:

* TensorFlow SavedModel (.pb)
* TensorFlow Lite (.tflite) untuk perangkat mobile
* TensorFlow\.js (.json dan .bin) untuk aplikasi web

## ▶️ Menjalankan Notebook

Buka file notebook dan jalankan sel secara berurutan:

```bash
jupyter notebook
```

Atau menggunakan Google Colab.

## 📦 Dependencies

Daftar dependensi ada di file requirements.txt. Beberapa library utama:

* TensorFlow
* Keras
* Numpy
* Pandas
* Matplotlib
* Seaborn
* Splitfolders
* TensorFlow\.js
* OpenCV([Kaggle][4], [arXiv][5])
