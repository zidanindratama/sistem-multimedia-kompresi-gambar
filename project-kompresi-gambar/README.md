# Analisis Kompresi Gambar Menggunakan Algoritma JPEG dengan Python Pillow

Project ini digunakan untuk menguji kompresi gambar menggunakan Python dan library Pillow.
Hasil pengujian mencakup ukuran file, rasio kompresi, MSE, PSNR, dan preview visual.

## Identitas

- Nama: Muhamad Zidan Indratama
- NPM: 50422968
- Kelas: 4IA08
- Mata Kuliah: Sistem Multimedia

## Struktur Folder

```text
project-kompresi-gambar/
  notebook/
    kompresi_gambar_pillow.ipynb
  data/
    input/
      original/
    output/
      compressed/
    results/
  requirements.txt
  README.md
```

## Cara Pakai

1. Install dependency:

```bash
pip install -r requirements.txt
```

2. Masukkan minimal tiga gambar ke folder:

```text
data/input/original/
```

3. Jalankan Jupyter Notebook:

```bash
jupyter notebook notebook/kompresi_gambar_pillow.ipynb
```

Jika command `jupyter` belum tersedia di PATH, gunakan:

```bash
python -m jupyterlab notebook/kompresi_gambar_pillow.ipynb
```

4. Jalankan semua cell dari atas sampai bawah.

5. Hasil kompresi akan tersimpan di:

```text
data/output/compressed/
```

6. Tabel hasil pengujian akan tersimpan di:

```text
data/results/hasil_pengujian.csv
data/results/hasil_pengujian.md
```

## Catatan

Notebook menggunakan algoritma JPEG lossy compression melalui Pillow dengan parameter default `quality=60` dan `optimize=True`.
MSE dan PSNR dihitung otomatis dari perbandingan pixel gambar asli dan gambar hasil kompresi.
