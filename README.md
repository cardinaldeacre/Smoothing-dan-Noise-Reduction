# Smoothing dan Noise Reduction pada Citra CCTV

Repositori ini merupakan hasil proyek tugas kelompok dalam mata kuliah pengolahan citra digital, dengan fokus pada penerapan teknik **smoothing** dan **noise reduction** terhadap citra CCTV yang terkena gangguan noise.

## 📌 Tujuan Proyek

Mengeksplorasi dan membandingkan berbagai metode filter smoothing (Mean, Median, Gaussian) untuk mengurangi noise pada citra. Setiap metode diuji menggunakan citra CCTV yang mengandung noise, lalu dianalisis efektivitasnya.

---

## 📂 Struktur Folder

```
Smoothing-dan-Noise-Reduction/
│
├── data/                # Dataset citra CCTV (ber-noise)
├── mean_median.ipynb    # Implementasi filter Mean & Median
├── gaussian_filter.ipynb# Implementasi filter Gaussian & eksplorasi tambahan
├── laporan.md           # Dokumentasi hasil analisis
├── README.md            # Dokumentasi proyek ini
```

---

## 🛠️ Teknologi & Library

- Python (3.x)
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Jupyter Notebook (via Kaggle)

---

## 🔍 Metode Filtering

| Metode Filter | Deskripsi Singkat |
|---------------|-------------------|
| **Mean Filter** | Meratakan nilai pixel dengan tetangganya untuk mengurangi noise |
| **Median Filter** | Mengganti pixel dengan median nilai tetangga, efektif untuk salt-and-pepper noise |
| **Gaussian Filter** | Menggunakan distribusi Gaussian, mempertahankan detail lebih baik |

---

## 🧪 Hasil & Perbandingan

Perbandingan visual dilakukan pada setiap metode:
- Citra asli vs hasil filter Mean
- Citra asli vs hasil filter Median
- Citra asli vs hasil filter Gaussian

Analisis lengkap dapat dilihat pada file: [`laporan.md`](./laporan.md)

---

## 📊 Pembagian Tugas Kelompok

| Nama                     | Tugas                                                                 |
|--------------------------|-----------------------------------------------------------------------|
| **Ahmad Nugrahadi**      | - Pencari data <br> - Setup Notebook Kaggle & library                |
| **Iqbal Maulana**        | - Implementasi filter Mean & Median <br> - Visualisasi hasil         |
| **Fayshal Karan Athilla**| - Implementasi filter Gaussian <br> - Eksplorasi lanjutan            |
| **Jauhan Ahmad**         | - Dokumentasi & analisis hasil <br> - Evaluasi kelebihan/kekurangan |

---

## 📌 Catatan Tambahan

- Dataset diambil dari sumber publik/open-source dan disimulasikan jika perlu.
- Semua eksperimen dilakukan di Kaggle Notebook untuk kemudahan replikasi.

---

## 📄 Lisensi

Proyek ini didistribusikan untuk tujuan edukasi. Silakan gunakan dan modifikasi dengan menyertakan atribusi kepada kontributor.

---

## 🤝 Kontribusi

Silakan buat *pull request* jika ingin menyempurnakan kode, dokumentasi, atau menambahkan eksperimen baru!