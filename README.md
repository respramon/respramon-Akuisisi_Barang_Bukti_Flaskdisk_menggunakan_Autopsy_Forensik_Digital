# 📁 Digital Forensics: Imaging Flashdisk dengan USB Write Blocker & FTK Imager

Dokumentasi ini menjelaskan langkah-langkah untuk membuat image dari flashdisk menggunakan **USB Write Blocker** dan **FTK Imager**, dengan memastikan integritas data menggunakan verifikasi hash.

---

## 🛠️ Alat yang Digunakan

* **USB Write Blocker** (Software)
* **FTK Imager**
* **Flashdisk (barang bukti)**
* **Laptop/PC Forensik**

---

## 📌 Langkah-langkah

### 1. Instalasi

* Install USB Write Blocker dan FTK Imager pada perangkat forensik Anda.

### 2. Menjalankan USB Write Blocker

* Jalankan aplikasi USB Write Blocker.

* Akan muncul tampilan seperti berikut:

  ![USB Write Blocker Interface](https://github.com/user-attachments/assets/216a2a47-cbea-45d4-8ced-5e03b120cd87)

* Ketik `1` lalu tekan **Enter** untuk mengaktifkan proteksi tulis (write protection) pada USB.

### 3. Hubungkan Flashdisk

* Hubungkan flashdisk yang akan di-image ke laptop/perangkat forensik.
* USB Write Blocker akan memastikan bahwa tidak ada data yang tertulis ke flashdisk selama proses berlangsung.

### 4. Menjalankan FTK Imager

* Buka **FTK Imager**.
* Pilih menu: `File > Create Disk Image...`.
* Pilih **Physical Drive**, lalu klik **Next**.
* Pilih **nama flashdisk** yang sesuai dari daftar drive, lalu klik **Finish**.

### 5. Pengaturan Imaging

* Centang opsi **"Verify images after they are created"**

  > Ini berfungsi untuk menghitung dan mencocokkan hash barang bukti dengan hasil imaging.

* Klik **Add...**, kemudian pilih format **Raw (dd)**.

### 6. Mengisi Identitas Barang Bukti

* Isikan informasi identitas barang bukti seperti:

  * Case Number
  * Evidence Number
  * Examiner Name
  * Notes (opsional)

### 7. Menentukan Lokasi dan Nama File

* Pada menu **"Select Image Destination"**:

  * Pilih lokasi penyimpanan hasil image.
  * Tentukan nama file yang sesuai.

### 8. Mengatur Fragmentasi Image

* Pada bagian **"Image Fragment Size (MB)"**, isikan ukuran flashdisk.
  Misalnya: jika flashdisk berukuran **16 GB**, maka isi dengan `16384`.

### 9. Mulai Proses Imaging

* Klik **Finish**, lalu tunggu proses imaging hingga selesai.
* Setelah selesai, FTK Imager akan melakukan verifikasi hash secara otomatis.

---

## ✅ Selesai

Image flashdisk berhasil dibuat dan diverifikasi. Hasil dapat digunakan untuk analisis forensik tanpa mengubah barang bukti asli.

---

> Dokumentasi ini dapat dijadikan referensi dasar dalam praktik digital forensik menggunakan metode *live acquisition* berbasis perangkat lunak.
