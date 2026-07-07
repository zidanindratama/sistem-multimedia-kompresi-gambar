# Sistem Multimedia - Kompresi Gambar

Repository ini berisi project Ujian Akhir Semester mata kuliah **Sistem Multimedia** dengan topik analisis kompresi gambar menggunakan algoritma **JPEG lossy compression** dan library **Python Pillow**.

## Identitas

- Nama: Muhamad Zidan Indratama
- NPM: 50422968
- Kelas: 4IA08
- Mata Kuliah: Sistem Multimedia
- Dosen Pengampu: Dr. Aviarini Indrati., SKom., MM.

## Deskripsi Project

Project ini digunakan untuk menguji pengaruh kompresi JPEG terhadap ukuran file dan kualitas gambar. Pengujian dilakukan pada tiga gambar dengan karakteristik berbeda, kemudian hasilnya dibandingkan berdasarkan ukuran file sebelum kompresi, ukuran file sesudah kompresi, rasio kompresi, MSE, PSNR, dan pengamatan visual.

Implementasi utama berada dalam Jupyter Notebook menggunakan Python. Program membaca gambar dari folder input, mengompresi gambar ke format JPEG dengan parameter `quality=60`, menyimpan hasil kompresi, lalu membuat tabel hasil pengujian dalam format CSV dan Markdown.

## Struktur Repository

```text
.
├── project-kompresi-gambar/
│   ├── notebook/
│   │   └── kompresi_gambar_pillow.ipynb
│   ├── data/
│   │   ├── input/original/
│   │   ├── output/compressed/
│   │   └── results/
│   ├── README.md
│   └── requirements.txt
├── laporan-kompresi-gambar/
│   ├── gambar/
│   ├── jurnal-dan-buku/
│   ├── Laporan Kompresi Gambar - Muhamad Zidan Indratama - 50422968.docx
│   └── Laporan Kompresi Gambar - Muhamad Zidan Indratama - 50422968.pdf
├── ATA2025-2026 SoalUAS Sistem Multimedia TI.pdf
└── README.md
```

## Algoritma yang Digunakan

Algoritma yang dianalisis adalah **JPEG lossy compression**. Secara umum, tahapan kompresi JPEG meliputi:

1. Konversi ruang warna RGB ke YCbCr
2. Pembagian gambar ke blok 8x8 piksel
3. Discrete Cosine Transform (DCT)
4. Quantization
5. Entropy coding

JPEG termasuk kompresi lossy karena sebagian informasi visual dikurangi untuk menghasilkan ukuran file yang lebih kecil.

## Metrik Evaluasi

Pengujian menggunakan beberapa metrik berikut:

| Metrik | Fungsi | Interpretasi |
|---|---|---|
| Rasio kompresi | Membandingkan ukuran file asli dan hasil kompresi | Semakin besar pengurangan ukuran file, semakin efisien kompresi |
| MSE | Mengukur rata-rata kuadrat perbedaan pixel | Semakin kecil MSE, semakin mirip hasil kompresi dengan gambar asli |
| PSNR | Mengukur kualitas gambar berdasarkan galat kompresi | Semakin tinggi PSNR, semakin baik kualitas gambar secara kuantitatif |
| Evaluasi visual | Membandingkan tampilan asli dan hasil kompresi | Digunakan untuk melihat perubahan detail, warna, dan ketajaman |

## Cara Menjalankan Project

Masuk ke folder project:

```bash
cd project-kompresi-gambar
```

Install dependency:

```bash
pip install -r requirements.txt
```

Jalankan JupyterLab:

```bash
python -m jupyterlab notebook/kompresi_gambar_pillow.ipynb
```

Jalankan semua cell pada notebook dari atas sampai bawah.

## Input dan Output

Gambar asli diletakkan di:

```text
project-kompresi-gambar/data/input/original/
```

Gambar hasil kompresi akan tersimpan di:

```text
project-kompresi-gambar/data/output/compressed/
```

Tabel hasil pengujian akan tersimpan di:

```text
project-kompresi-gambar/data/results/hasil_pengujian.csv
project-kompresi-gambar/data/results/hasil_pengujian.md
```

## Hasil Pengujian

Project ini sudah diuji menggunakan tiga gambar:

- `01-manusia.jpg`
- `02-pemandangan.jpg`
- `03-teks.jpg`

Hasil pengujian dapat dilihat pada file:

```text
project-kompresi-gambar/data/results/hasil_pengujian.md
```

## Catatan

Repository ini juga menyertakan dokumen laporan dalam format `.docx` dan `.pdf`, gambar pendukung laporan, serta referensi pustaka yang digunakan dalam penyusunan laporan.
