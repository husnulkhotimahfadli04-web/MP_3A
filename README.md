# MINI PROJECT KELOMPOK 3A
## Analisis Data Ekspor dan Impor Berdasarkan Pelabuhan di Indonesia

### 1. Deskripsi Program
Program ini merupakan aplikasi berbasis Python yang digunakan untuk mengolah dan menganalisis data volume ekspor dan impor berdasarkan pelabuhan di Indonesia. Program membaca data dari file CSV, kemudian melakukan perhitungan statistik, pertumbuhan tahunan, serta analisis tren linear untuk mengetahui perkembangan ekspor dan impor.

### 2. Tujuan Program
1. Mengetahui volume ekspor dan impor berdasarkan pelabuhan.
2. Menghitung total ekspor dan impor setiap tahun.
3. Mengetahui rata-rata dan standar deviasi data.
4. Menghitung koefisien variasi ekspor dan impor.
5. Menganalisis pertumbuhan ekspor dan impor setiap tahun.
6. Menentukan persamaan tren linear.
7. Membandingkan perkiraan perkembangan ekspor dan impor hingga tahun 2030.

### 3. Data yang Digunakan
Program menggunakan dataset CSV dengan informasi:
- Tahun: 2015–2024.
- Kategori pelabuhan:
  1. Belawan
  2. Tanjung Priok
  3. Tanjung Perak
  4. Makassar
- Satuan pengukuran: Ton.
- Jenis data: Volume ekspor dan impor.

### 4. Bahasa Pemrograman dan Library
Program dibuat menggunakan:
- Python sebagai bahasa pemrograman.
- `csv` untuk membaca dan mengolah data CSV.
- `statistics` untuk menghitung rata-rata dan standar deviasi populasi.

Seluruh library yang digunakan merupakan library bawaan Python sehingga tidak memerlukan instalasi tambahan.

### 5. Struktur File
```text
Mini Project 3A/
│
├── MP_3A.py
├── prokom_kel3A .csv
└── README.md
```

### 6. Fitur Program

**1. Tabel Ekspor dan Impor**
Menampilkan volume ekspor, impor, dan total berdasarkan masing-masing pelabuhan untuk setiap tahun yang dipilih.

**2. Tabel Historis per Pelabuhan**
Menampilkan perkembangan volume ekspor dan impor masing-masing pelabuhan selama rentang tahun yang dipilih.

**3. Tabel Trend Linear**
Menampilkan perbandingan data aktual dengan hasil perhitungan tren linear ekspor dan impor.

**4. Perbandingan Trend Linear**
Menampilkan perkiraan volume ekspor dan impor serta selisih keduanya sampai tahun 2030.

**5. Ganti Rentang Tahun**
Memungkinkan pengguna mengganti periode analisis tanpa menjalankan ulang program.

### 7. Rumus dan Metode Perhitungan

**A. Rata-rata (Mean)**

Digunakan untuk mengetahui nilai rata-rata volume ekspor dan impor.

Rumus:

X̄ = ΣX / n

Keterangan:
- X̄ = Nilai rata-rata.
- ΣX = Jumlah seluruh data.
- n = Banyaknya data.

**B. Standar Deviasi Populasi**

Digunakan untuk mengetahui tingkat penyebaran data terhadap nilai rata-ratanya.

Rumus:

σ = √(Σ(X − X̄)² / n)

Keterangan:
- σ = Standar deviasi populasi.
- X = Nilai setiap data.
- X̄ = Nilai rata-rata.
- n = Banyaknya data.

**C. Koefisien Variasi (KV)**

Digunakan untuk mengetahui tingkat variasi data dalam bentuk persentase.

Rumus:

KV = (σ / X̄) × 100%

Keterangan:
- KV = Koefisien variasi.
- σ = Standar deviasi.
- X̄ = Nilai rata-rata.

**D. Pertumbuhan Tahunan**

Digunakan untuk mengetahui persentase kenaikan atau penurunan volume ekspor dan impor dari tahun sebelumnya.

Rumus:

Pertumbuhan = ((Xₜ − Xₜ₋₁) / Xₜ₋₁) × 100%

Keterangan:
- Xₜ = Volume pada tahun sekarang.
- Xₜ₋₁ = Volume pada tahun sebelumnya.

**E. Tren Linear**

Digunakan untuk mengetahui kecenderungan perkembangan data berdasarkan periode waktu.

Rumus:

Y = a + bX

Keterangan:
- Y = Nilai tren.
- a = Konstanta.
- b = Koefisien arah atau kemiringan tren.
- X = Periode waktu.

Perhitungan koefisien:

b = Σ((X − X̄)(Y − Ȳ)) / Σ(X − X̄)²

a = Ȳ − bX̄

### 8. Cara Kerja Program
1. Program membaca data dari file CSV.
2. Data dikelompokkan berdasarkan tahun dan kategori pelabuhan.
3. Program mengambil data yang memiliki satuan Ton.
4. Pengguna memasukkan tahun atau rentang tahun yang ingin dianalisis.
5. Program menampilkan menu pilihan.
6. Pengguna memilih jenis analisis.
7. Program melakukan perhitungan sesuai menu yang dipilih.
8. Hasil perhitungan ditampilkan dalam bentuk tabel.
9. Pengguna dapat mengganti rentang tahun atau mengakhiri program.

### 9. Cara Menjalankan Program

Persyaratan:
- Python sudah terinstal.
- File Python dan CSV berada dalam folder yang sama.

Langkah menjalankan:

1. Buka terminal atau Command Prompt.
2. Masuk ke folder proyek.
3. Jalankan perintah berikut:

```bash
python MP_3A.py
```

4. Masukkan tahun atau rentang tahun yang ingin dianalisis.
5. Pilih menu output sesuai kebutuhan.

### 10. Menu Program

| Pilihan | Fungsi |
|---|---|
| 1 | Tabel Ekspor dan Impor |
| 2 | Tabel Historis per Pelabuhan |
| 3 | Tabel Trend Linear |
| 4 | Perbandingan Trend Linear |
| 5 | Ganti Rentang Tahun |
| 0 | Keluar dari Program |

### 11. Penanganan Kesalahan
Program memiliki penanganan beberapa kesalahan, yaitu:
- File CSV tidak ditemukan.
- Nilai data tidak valid.
- Nama kolom CSV tidak sesuai.
- Terjadi pembagian dengan nol.
- Rentang tahun tidak valid.
- Data tahun tidak tersedia.

### 12. Kesimpulan
Program Mini Project Kelompok 3A dapat digunakan untuk mengolah dan menganalisis data ekspor dan impor berdasarkan pelabuhan. Melalui perhitungan statistik dan tren linear, program membantu pengguna memahami perkembangan volume perdagangan dari tahun ke tahun serta memperkirakan kecenderungan perkembangan pada periode berikutnya.

### 13. Identitas Kelompok
**Kelompok:** 3A

**Anggota Kelompok:**
1. (Nama dan NIM anggota 1)
2. (Nama dan NIM anggota 2)
3. (Nama dan NIM anggota 3)
4. (Nama dan NIM anggota 4)

**Mata Kuliah:** Pemrograman Komputer
