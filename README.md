# Analisis Variabilitas Volume Ekspor dan Impor pada Empat Pelabuhan Utama Indonesia

Program Python untuk menganalisis perkembangan volume ekspor dan impor pada Pelabuhan Belawan, Tanjung Priok, Tanjung Perak, dan Makassar selama periode pengamatan 2015–2025. Analisis dilakukan menggunakan statistik deskriptif dan metode tren linear (*linear trend*) untuk melihat pola perubahan serta memperkirakan volume perdagangan hingga tahun 2030.

## Daftar Isi
1. [Latar Belakang](#latar-belakang)
2. [Tujuan](#tujuan)
3. [Fitur Utama](#fitur-utama)
4. [Metodologi](#metodologi)
5. [Struktur Repositori](#struktur-repositori)
6. [Persyaratan Sistem](#persyaratan-sistem)
7. [Cara Menjalankan Program](#cara-menjalankan-program)
8. [Panduan Penggunaan](#panduan-penggunaan)
9. [Format Data](#format-data)
10. [Keterbatasan](#keterbatasan)
11. [Tim](#tim)

## 1. Latar Belakang

Pelabuhan memiliki peran penting dalam mendukung perdagangan internasional melalui kegiatan bongkar dan muat barang. Perubahan volume ekspor dan impor dapat menunjukkan perkembangan arus perdagangan pada suatu pelabuhan.

Program ini menggunakan data dari _Hub Network_ (HUBNET) Kementerian Perhubungan yang mencakup empat pelabuhan utama Indonesia, yaitu Belawan, Tanjung Priok, Tanjung Perak, dan Makassar. Data diolah untuk mengetahui perkembangan volume perdagangan, tingkat variasinya, serta kecenderungan perubahannya berdasarkan data historis.

## 2. Tujuan

- Mengetahui perkembangan volume ekspor dan impor pada empat pelabuhan utama.
- Membandingkan volume perdagangan antarpelabuhan.
- Mengukur variasi volume ekspor dan impor menggunakan statistik deskriptif.
- Mengidentifikasi kecenderungan perubahan volume melalui tren linear.
- Menghasilkan estimasi volume ekspor dan impor hingga tahun 2030.

## 3. Fitur Utama

| Fitur | Keterangan |
|---|---|
| Tabel Ekspor dan Impor | Menampilkan volume ekspor, impor, dan total perdagangan setiap pelabuhan berdasarkan tahun. |
| Tabel Historis per Pelabuhan | Menampilkan perkembangan volume ekspor dan impor setiap pelabuhan dalam rentang tahun yang dipilih. |
| Ringkasan Statistik | Menghitung rata-rata, standar deviasi, koefisien variasi, dan pertumbuhan tahunan. |
| Tabel Tren Linear | Menampilkan perbandingan nilai aktual dengan hasil perhitungan tren linear. |
| Perbandingan Tren Linear | Menampilkan estimasi volume ekspor dan impor hingga tahun 2030. |
| Input Rentang Tahun | Memungkinkan pengguna menentukan atau mengganti periode pengamatan. |

## 4. Metodologi

Pengolahan data dilakukan secara terpisah untuk volume ekspor dan impor. Perhitungan statistik digunakan untuk menggambarkan karakteristik data, sedangkan tren linear digunakan untuk melihat kecenderungan perubahan volume berdasarkan urutan waktu.

### Penentuan Nilai dan Perhitungan

### 1. Rata-rata (*Mean*)

\[
\bar{X}=\frac{\sum_{t=1}^{n}X_t}{n}
\]

Keterangan:
- \(\bar{X}\) = rata-rata volume ekspor atau impor.
- \(X_t\) = volume pada periode ke-\(t\).
- \(n\) = jumlah periode pengamatan.
- \(\sum\) = penjumlahan seluruh nilai data.

### 2. Pertumbuhan (*Growth*)

\[
G_t=\frac{X_t-X_{t-1}}{X_{t-1}}\times100\%
\]

Keterangan:
- \(G_t\) = persentase pertumbuhan volume.
- \(X_t\) = volume pada tahun berjalan.
- \(X_{t-1}\) = volume pada tahun sebelumnya.

### 3. Standar Deviasi (*Standard Deviation*)

\[
SD=\sqrt{\frac{\sum_{t=1}^{n}(X_t-\bar{X})^2}{n}}
\]

Keterangan:
- \(SD\) = standar deviasi atau tingkat penyebaran data.
- \(X_t\) = volume pada periode ke-\(t\).
- \(\bar{X}\) = rata-rata volume.
- \(n\) = jumlah periode pengamatan.

### 4. Koefisien Variasi (KV)

\[
KV=\frac{SD}{\bar{X}}\times100\%
\]

Keterangan:
- \(KV\) = koefisien variasi dalam persentase.
- \(SD\) = standar deviasi.
- \(\bar{X}\) = rata-rata volume.

### 5. Tren Linear (*Linear Trend*)

\[
\hat{Y}=a+bX
\]

Perhitungan koefisien:

\[
b=\frac{\sum(X_i-\bar{X})(Y_i-\bar{Y})}{\sum(X_i-\bar{X})^2}
\]

\[
a=\bar{Y}-b\bar{X}
\]

Keterangan:
- \(\hat{Y}\) = nilai volume berdasarkan tren.
- \(a\) = konstanta atau titik potong garis tren.
- \(b\) = koefisien kemiringan garis tren.
- \(X_i\) = indeks urutan periode pengamatan.
- \(Y_i\) = volume aktual pada periode ke-\(i\).
- \(\bar{X}\) dan \(\bar{Y}\) = rata-rata indeks periode dan volume aktual.
  
Hasil persamaan tren digunakan untuk menghitung nilai kecenderungan pada periode pengamatan dan memperkirakan volume hingga tahun 2030. Nilai estimasi negatif dibatasi menjadi nol dalam program.

## 5. Struktur Repositori

```text
repository-MP-3A/
│
├── MP_3A.py
├── prokom_kel3A.csv
│
├── Dokumentasi/
│   └── LAPORAN MP 3A REVISI.docx
│
└── README.md
```

| File/Folder | Keterangan |
|---|---|
| `MP_3A.py` | Program utama untuk membaca, mengolah, dan menganalisis data. |
| `prokom_kel3A.csv` | Dataset volume ekspor dan impor. |
| `Dokumentasi/` | Berisi laporan mini project. |
| `README.md` | Dokumentasi penggunaan program. |

## 6. Persyaratan Sistem

| Komponen | Persyaratan |
|---|---|
| Bahasa Pemrograman | Python 3 |
| Library | `csv`, `statistics` |
| Format Dataset | CSV |
| Pemisah Kolom | Titik koma (`;`) |
| Encoding | UTF-8 / UTF-8-SIG |
| Sistem Operasi | Windows, Linux, atau macOS yang mendukung Python 3 |
| Koneksi Internet | Tidak diperlukan saat program dijalankan |

## 7. Cara Menjalankan Program

1. Pastikan Python 3 telah terpasang.
2. Unduh atau salin seluruh file repositori ke komputer.
3. Letakkan file `MP_3A.py` dan dataset CSV pada lokasi yang sesuai.
4. Sesuaikan variabel `nama_file` pada kode dengan lokasi file CSV di komputer.

Contoh:

```python
nama_file = r"C:\Users\Nama\Documents\prokom_kel3A.csv"
```

5. Buka terminal atau Command Prompt pada direktori program.
6. Jalankan perintah berikut:

```bash
python MP_3A.py
```

7. Masukkan rentang tahun ketika diminta oleh program.

## 8. Panduan Penggunaan

Setelah program dijalankan, pengguna diminta memasukkan tahun atau rentang tahun pengamatan. Program kemudian menampilkan menu berikut:

| Pilihan | Menu | Fungsi |
|---|---|---|
| 1 | Tabel Ekspor dan Impor | Menampilkan volume ekspor, impor, dan total setiap tahun. |
| 2 | Tabel Historis per Pelabuhan | Menampilkan data historis masing-masing pelabuhan. |
| 3 | Tabel Tren Linear | Menampilkan nilai aktual dan nilai tren linear. |
| 4 | Perbandingan Tren Linear | Menampilkan estimasi volume hingga tahun 2030. |
| 5 | Ganti Rentang Tahun | Mengubah periode pengamatan. |
| 0 | Keluar | Menghentikan program. |

Pengguna dapat memilih menu sesuai kebutuhan. Menu akan terus ditampilkan hingga pengguna memilih angka `0`.

## 9. Format Data

Dataset disimpan dalam format CSV dengan pemisah titik koma (`;`). Kolom yang digunakan oleh program adalah:

| Nama Kolom | Keterangan |
|---|---|
| `id_tabel` | Identitas tabel sumber data. |
| `kategori` | Nama pelabuhan. |
| `satuan` | Satuan pengukuran volume. |
| `tahun` | Tahun pengamatan. |
| `nilai` | Nilai volume barang. |

Program mengambil data dengan satuan `Ton`. Setiap tahun dan pelabuhan menyimpan dua nilai volume yang digunakan sebagai ekspor dan impor berdasarkan urutan kemunculannya dalam CSV.

Cakupan analisis dalam laporan meliputi:
- Pelabuhan Belawan.
- Pelabuhan Tanjung Priok.
- Pelabuhan Tanjung Perak.
- Pelabuhan Makassar.
- Periode pengamatan 2015–2025.
- Satuan volume: ton.

Sumber data: Kementerian Perhubungan Republik Indonesia melalui HUBNET.

## 10. Keterbatasan

- Hasil analisis bergantung pada kelengkapan dan ketepatan dataset yang digunakan.
- Penentuan nilai ekspor dan impor pada kode saat ini bergantung pada urutan data dalam CSV, bukan identifikasi berdasarkan kolom jenis arus barang secara eksplisit.
- Data yang digunakan merupakan data agregat tahunan sehingga tidak memberikan rincian berdasarkan komoditas, perusahaan, terminal, biaya, maupun waktu tunggu.
- Tren linear hanya menggambarkan kecenderungan berdasarkan data historis dan tidak menjamin kondisi perdagangan pada periode berikutnya.
- Estimasi hingga tahun 2030 merupakan hasil ekstrapolasi model, bukan kepastian volume perdagangan aktual.
- Perhitungan tren linear memerlukan minimal dua tahun pengamatan.

## 11. Tim 

**Kelompok 3A – Teknik Industri, Universitas Andalas**

| No. | Nama | NIM |
|---|---|---|
| 1 | Zhafira Wafda | 2610931021 |
| 2 | Marsya Tri Ananda | 2610937004 |
| 3 | Iffah Astilah Rahmah Manik | 2610933010 |
| 4 | Husnul Khotimah Fadli | 2610931037 |
