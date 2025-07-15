# Smoothing dan Noise Reduction pada Dataset CCTV Gender Classifier

## Deskripsi Project

Project ini bertujuan untuk mengimplementasikan teknik smoothing dan noise reduction pada dataset CCTV Gender Classifier. Smoothing adalah teknik pengolahan citra yang digunakan untuk mengurangi noise atau gangguan pada gambar, sehingga menghasilkan citra yang lebih halus dan jelas.

### Apa itu Smoothing?

Smoothing atau penghalusan citra adalah proses filtering yang bertujuan untuk:
- Mengurangi noise pada gambar
- Menghaluskan tekstur yang kasar
- Mengurangi detail yang tidak diinginkan
- Mempersiapkan citra untuk proses lebih lanjut

### Apa itu Noise Reduction?

Noise reduction adalah teknik untuk menghilangkan atau mengurangi gangguan (noise) pada citra yang dapat berupa:
- Salt and pepper noise
- Gaussian noise
- Uniform noise
- Impulse noise

## Dataset

**Dataset yang digunakan:** `/kaggle/input/cctv-gender-classifier-dataset`

Dataset ini berisi gambar-gambar CCTV yang digunakan untuk klasifikasi gender. Gambar-gambar CCTV umumnya memiliki kualitas yang bervariasi dan seringkali mengandung noise karena kondisi pencahayaan, kualitas kamera, dan faktor lingkungan lainnya.

## Metode Filtering yang Diimplementasikan

### 1. Mean Filter (Average Filter)
- Mengganti nilai pixel dengan rata-rata nilai pixel di sekitarnya
- Efektif untuk mengurangi Gaussian noise
- Dapat menyebabkan blur pada tepi gambar

### 2. Median Filter
- Mengganti nilai pixel dengan nilai median dari pixel di sekitarnya
- Sangat efektif untuk mengurangi salt and pepper noise
- Lebih baik dalam mempertahankan tepi gambar

### 3. Gaussian Filter
- Menggunakan kernel Gaussian untuk smoothing
- Memberikan hasil yang lebih natural
- Dapat dikontrol melalui parameter sigma

## Pembagian Tugas

| No | Tugas | Deskripsi | Deliverable |
|----|-------|-----------|-------------|
| 1 | **(Ahmad Nugrahadi)Pencari Data & Setup Kaggle** | - Mencari 1 contoh citra CCTV ber-noise (dari dataset/simulasi)<br>- Menyiapkan notebook Kaggle<br>- Memastikan semua library tersedia (OpenCV, NumPy, Matplotlib, dll) | - Notebook Kaggle yang sudah di-setup<br>- Sample citra ber-noise<br>- Import library yang dibutuhkan |
| 2 | **(Iqbal Maulana)Implementasi Filter (Mean & Median)** | - Implementasi Mean Filter pada citra<br>- Implementasi Median Filter pada citra<br>- Menampilkan perbandingan citra sebelum & sesudah filtering<br>- Visualisasi hasil dengan matplotlib | - Kode implementasi Mean Filter<br>- Kode implementasi Median Filter<br>- Visualisasi before/after comparison |
| 3 | **(Faisyal)Implementasi Filter Gaussian & Eksplorasi** | - Implementasi Gaussian Filter<br>- Eksplorasi parameter sigma yang berbeda<br>- Menampilkan perbandingan citra sebelum & sesudah filtering<br>- Visualisasi hasil dengan berbagai parameter | - Kode implementasi Gaussian Filter<br>- Eksperimen dengan berbagai parameter<br>- Visualisasi hasil filtering |
| 4 | **(Jauhan)Analisis & Dokumentasi Laporan** | - Membandingkan hasil semua filter<br>- Menganalisis kelebihan & kekurangan setiap metode<br>- Membuat dokumentasi lengkap<br>- Kesimpulan dan rekomendasi | - Laporan analisis perbandingan<br>- Tabel kelebihan/kekurangan<br>- Dokumentasi hasil<br>- Kesimpulan |

## Struktur Project

```
smoothing-noise-reduction/
├── notebooks/
│   ├── 01_data_setup.ipynb
│   ├── 02_mean_median_filter.ipynb
│   ├── 03_gaussian_filter.ipynb
│   └── 04_analysis_report.ipynb
├── data/
│   ├── original_images/
│   ├── noisy_images/
│   └── filtered_images/
├── results/
│   ├── comparison_plots/
│   └── analysis_report.md
└── README.md
```

## Library yang Dibutuhkan

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from skimage import filters, util
import pandas as pd
```

## Kriteria Evaluasi

### Metrics yang Digunakan:
1. **PSNR (Peak Signal-to-Noise Ratio)** - Mengukur kualitas citra
2. **MSE (Mean Squared Error)** - Mengukur perbedaan pixel
3. **SSIM (Structural Similarity Index)** - Mengukur kesamaan struktural
4. **Visual Assessment** - Penilaian visual secara subjektif

### Aspek yang Dinilai:
- Kemampuan mengurangi noise
- Preservasi detail penting
- Kualitas tepi gambar
- Computational efficiency

## Timeline

| Minggu | Aktivitas |
|--------|-----------|
| 1 | Setup dataset dan environment |
| 2 | Implementasi Mean & Median Filter |
| 3 | Implementasi Gaussian Filter & Eksplorasi |
| 4 | Analisis hasil dan dokumentasi |

## Expected Outcomes

1. **Implementasi lengkap** dari 3 metode filtering
2. **Perbandingan visual** yang jelas antara citra asli dan hasil filtering
3. **Analisis kuantitatif** menggunakan metrics yang sesuai
4. **Dokumentasi** yang comprehensive tentang kelebihan dan kekurangan setiap metode
5. **Rekomendasi** metode terbaik untuk dataset CCTV

## Kontribusi

Setiap anggota tim bertanggung jawab untuk:
- Menyelesaikan tugas yang telah ditetapkan
- Mendokumentasikan kode dengan baik
- Melakukan testing dan validasi
- Berkontribusi pada laporan akhir
