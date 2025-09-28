# Eksplorasi-Autoencoder
Proyek ini merupakan implementasi dan eksplorasi Autoencoder berbasis Convolutional Neural Network (CNN) menggunakan dataset Fashion-MNIST. Tujuan utama bukan hanya menghasilkan citra rekonstruksi yang baik, tetapi juga memahami bagaimana struktur encoder–decoder memengaruhi representasi laten dan kualitas rekonstruksi.

Tujuan
Mengeksplorasi arsitektur autoencoder dengan 3 lapisan encoder dan 3 lapisan decoder.
Menganalisis performa rekonstruksi menggunakan metrik kuantitatif (MSE dan SSIM).
Mengeksplorasi representasi laten menggunakan PCA/t-SNE untuk melihat distribusi antar kelas.

Dataset
Fashion-MNIST
60.000 data latih, 10.000 data uji
Gambar grayscale ukuran 28x28 piksel, terdiri dari 10 kelas kategori pakaian

Arsitektur Model
Encoder: Conv2D + ReLU (32, 64, 128 filter)
Bottleneck: representasi laten berdimensi 128
Decoder: Conv2DTranspose untuk mengembalikan dimensi asli (28×28×1)

Hasil & Analisis
Metrik kuantitatif:
MSE rendah pada kategori sederhana (misal: Bag, Trouser).
SSIM tinggi menunjukkan struktur global citra berhasil dipertahankan.
Rekonstruksi visual: Autoencoder mampu menangkap pola global, tetapi detail halus (lipatan kain, tekstur) cenderung hilang.
Representasi laten: hasil PCA menunjukkan distribusi data cenderung membentuk cluster per kelas, meski masih ada tumpang tindih pada kategori mirip.

Contoh Output
Rekonstruksi citra: baris atas citra asli, baris bawah hasil rekonstruksi.
Visualisasi latent space (PCA): clustering antar kelas Fashion-MNIST.

Cara Menjalankan
Clone repository
git clone https://github.com/username/autoencoder-fashionmnist.git
cd autoencoder-fashionmnist

Install dependencies
pip install -r requirements.txt

Jalankan notebook untuk training & evaluasi
jupyter notebook autoencoder_fashionmnist.ipynb
