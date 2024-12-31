- Manajemen Produk dan Transaksi

- Deskripsi Aplikasi
Aplikasi ini dirancang untuk membantu staf perusahaan retail skala kecil dalam mengelola produk dan mencatat transaksi penjualan. Aplikasi berbasis desktop ini dibangun menggunakan Python dengan paradigma Pemrograman Berorientasi Objek (OOP) dan antarmuka grafis menggunakan Tkinter. Data disimpan dalam database MySQL untuk kemudahan pengelolaan lebih lanjut.

- Fitur Utama
1. Manajemen Produk
   - Fitur CRUD (Create, Read, Update, Delete) untuk produk.
   - Atribut produk:
     - ID Produk (Primary Key, Auto Increment)
     - Nama Produk
     - Harga Produk

2. Proses Transaksi
   - Pilih produk melalui dropdown berdasarkan Nama Produk.
   - Input jumlah produk yang akan dibeli.
   - Hitung otomatis total harga (Jumlah x Harga Produk).
   - Simpan transaksi ke database dengan atribut:
     - ID Transaksi (Primary Key, Auto Increment)
     - ID Produk (Foreign Key ke tabel produk)
     - Jumlah Produk
     - Total Harga
     - Tanggal Transaksi
   - Tampilkan daftar transaksi (Nama Produk, Jumlah, Total Harga, Tanggal Transaksi).

3. Antarmuka Pengguna (GUI)
   - Desain sederhana dan fungsional menggunakan Tkinter.
   - Tampilan data produk dan transaksi menggunakan tabel.

- Teknologi yang Digunakan
a. Bahasa Pemrograman: Python
b. GUI Library: Tkinter
c. Database: MySQL (dikelola melalui phpMyAdmin)

- Persyaratan Sistem
1. Python 3.x
2. MySQL Server
3. Paket Python tambahan:
   `mysql-connector-python`

- Cara Menjalankan Aplikasi
1. Persiapan Database
   - Buat database dengan nama `retail_db` di MySQL.
   - Jalankan file dump database (`retail_db.sql`) yang telah disediakan untuk membuat tabel `produk` dan `transaksi`.

2. Persiapan Python
   - Instal dependensi dengan perintah berikut:
     pip install mysql-connector-python

3. Menjalankan Aplikasi
   - Jalankan file Python aplikasi:
     python main.py

4. Interaksi dengan Aplikasi
   - Tambah, perbarui, dan hapus data produk melalui tab "Manajemen Produk".
   - Tambah transaksi baru melalui tab "Transaksi".
   - Lihat daftar produk dan transaksi dalam tabel pada masing-masing tab.

- Struktur Tabel Database

- Tabel `produk`
| Kolom        | Tipe Data        | Keterangan          |
|--------------|------------------|---------------------|
| id_produk    | INT (Auto Increment) | Primary Key       |
| nama_produk  | VARCHAR(255)     | Nama produk         |
| harga_produk | DECIMAL(10, 2)   | Harga produk        |

- Tabel `transaksi`
| Kolom             | Tipe Data        | Keterangan                  |
|-------------------|------------------|-----------------------------|
| id_transaksi      | INT (Auto Increment) | Primary Key           |
| id_produk         | INT              | Foreign Key ke tabel produk |
| jumlah_produk     | INT              | Jumlah produk               |
| total_harga       | DECIMAL(10, 2)   | Total harga transaksi       |
| tanggal_transaksi | DATE             | Tanggal transaksi           |

 Dokumentasi Tambahan
- Manajemen Error
  - Validasi input dilakukan untuk memastikan data valid, seperti memastikan harga dan jumlah adalah angka positif.
  - Pesan error akan ditampilkan dalam dialog jika terjadi kesalahan.

- Desain Antarmuka
  - Menggunakan gaya "clam" dari Tkinter untuk tampilan modern.
  - Tabel dengan font yang mudah dibaca dan tata letak intuitif.

- File yang Disertakan
1. `main.py`: File Python utama aplikasi.
2. `retail_db.sql`: File dump database untuk tabel `produk` dan `transaksi`.
3. `README.md`: Dokumentasi aplikasi ini.

- Kontributor
1. Nama: [Nama Anda]
2. Email: [Email Anda]
3. Universitas: [Nama Universitas Anda]

- Lisensi
Aplikasi ini dikembangkan untuk keperluan pembelajaran dan tidak ditujukan untuk penggunaan komersial tanpa izin.

