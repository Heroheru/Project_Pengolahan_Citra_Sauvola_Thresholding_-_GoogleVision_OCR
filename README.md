
# 🚗🔍 Google Cloud Vision untuk Ekstraksi Karakter Plat Nomor Kendaraan  

Repositori ini berisi implementasi **Google Cloud Vision** untuk ekstraksi karakter dari plat nomor kendaraan pada berbagai gambar. Gambar yang digunakan mencakup:  
1. **Gambar asli** (belum difiltering).  
2. **Gambar yang telah difiltering** menggunakan metode **Sauvola** untuk peningkatan akurasi OCR.  

## 📌 Fitur  
✅ Menggunakan **Google Cloud Vision API** untuk Optical Character Recognition (OCR).  
✅ Proses ekstraksi dilakukan pada dua jenis gambar:  
   - **Gambar asli** tanpa preprocessing.  
   - **Gambar yang telah diproses dengan metode Sauvola** untuk meningkatkan kontras dan keterbacaan karakter.  
✅ Analisis perbandingan hasil ekstraksi antara kedua metode.  

## 🛠️ Teknologi yang Digunakan  
- **Python**  
- **Google Cloud Vision API**  
- **OpenCV** (untuk filtering dengan metode Sauvola)  
- **NumPy & Matplotlib** (untuk analisis dan visualisasi)  

## 📂 Struktur Folder  
```
├── input_100/         # Folder berisi dataset gambar plat nomor kendaraan
│   ├── image1.jpg
│   ├── image2.jpg
│   ├── ...
├── output_100/        # Folder hasil ekstraksi OCR dari gambar yang telah difiltering dengan Sauvola
│   ├── filtered_image1.jpg
│   ├── filtered_image2.jpg
│   ├── result_sauvola1.txt
│   ├── result_sauvola2.txt
│   ├── ...
├── [Kode_Program]_Adaptive_Thresholding_Sauvola.py    # Script untuk preprocessing menggunakan metode Sauvola
├── [Kode_Program]_OCR_Google_Vision_API.ipynb         # Notebook untuk ekstraksi karakter dengan Google Cloud Vision
└── README.md          # Dokumentasi proyek
```
> **Note:**  
> - Pastikan semua gambar yang akan diproses disimpan dalam folder **`input_100/`**.  
> - Hasil filtering metode Sauvola akan disimpan di **`output_100/`**.  

## 🚀 Cara Menggunakan  

### 1️⃣ **Persiapan Google Cloud Vision API**  
1. Buat akun dan aktifkan **Google Cloud Vision API** di [Google Cloud Console](https://console.cloud.google.com/).  
2. Unduh file **credentials.json** dan simpan di direktori proyek.  
3. Set environment variable untuk autentikasi:  
   ```bash
   export GOOGLE_APPLICATION_CREDENTIALS="path/to/credentials.json"
   ```

### 2️⃣ **Instalasi Dependensi**  
Pastikan Anda sudah memiliki Python, lalu install library yang dibutuhkan

### 3️⃣ **Eksekusi Program**  

#### 🏁 **Langkah 1: Preprocessing Gambar dengan Metode Sauvola**  
Jalankan skrip **Adaptive Thresholding Sauvola** untuk filtering gambar:  
```bash
python [Kode_Program]_Adaptive_Thresholding_Sauvola.py
```
- Gambar hasil filtering akan disimpan di **`output_100/`**.  

#### 🏁 **Langkah 2: Ekstraksi Karakter dengan Google Cloud Vision**  
Jalankan notebook **OCR Google Vision API** untuk ekstraksi teks dari gambar asli dan gambar hasil filtering Sauvola:  
```bash
jupyter notebook [Kode_Program]_OCR_Google_Vision_API.ipynb
```


## 📊 Analisis Hasil  
- **Perbandingan hasil OCR** antara gambar asli dan gambar yang telah diproses dengan metode Sauvola akan dianalisis.  
- Hasil akan disimpan dalam bentuk teks serta divisualisasikan dengan bounding box pada gambar.  

## 📌 Catatan  
Repositori ini dibuat untuk eksplorasi dan pembelajaran dalam implementasi OCR pada plat nomor kendaraan menggunakan **Google Cloud Vision**.  

