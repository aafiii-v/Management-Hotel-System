<<<<<<< HEAD
# HotelManagement
=======
# Hotel Management System

Proyek ini merupakan sistem manajemen hotel yang dibangun menggunakan teknologi .NET dengan Visual Studio. Aplikasi ini dirancang untuk membantu pengelolaan data hotel, termasuk pemesanan kamar, pengelolaan tamu, dan pengelolaan ketersediaan kamar.

## Fitur Utama
- Memiliki login dan Register
- Manajemen Tamu: Menyimpan data tamu seperti nama, dan informasi kontak.
- Manajemen Pemesanan: Memasukkan data pemesanan kamar secara otomatis menggunakan kode unik yang dihasilkan oleh trigger database.
- Integrasi Database: Menggunakan SQL sebagai backend untuk menyimpan data secara terstruktur.
- Interface Dinamis: Menyediakan antarmuka berbasis Windows Forms untuk kemudahan penggunaan.

## Struktur Proyek
- HotelManagement.sln: File solusi untuk membuka proyek di Visual Studio.
- HotelManagement/: Folder utama yang berisi kode sumber aplikasi.
- packages/: Folder berisi dependensi yang dibutuhkan untuk menjalankan proyek.
- README.md: Dokumentasi proyek (file ini).

## Teknologi yang Digunakan
- Bahasa Pemrograman: 100% C#
- Framework: .NET Framework, Guna2Ui
- Database: MySQL (menggunakan MySqlConnector untuk koneksi)
- IDE: Visual Studio 2022

## Cara Menjalankan Proyek
1. Buka file `HotelManagement.sln` menggunakan Visual Studio 2022.
2. Pastikan database sudah terkonfigurasi sesuai dengan struktur yang ditentukan (lihat bagian **Database**).
3. Jalankan aplikasi dengan menekan tombol **Start** di Visual Studio.

## Diagram
![ERD](https://github.com/aafiii-v/Afi-Naufal-Rizky-Yang/blob/master/HotelManagement/Resources/Screenshot%202024-11-30%20172724.png))

## Database
### Struktur Tabel
Proyek ini menggunakan 3 tabel utama:
1. Tabel Tamu:
   - `kode_tamu` (CHAR, Primary Key) -> MENGGUNAKAN TRIGGER UNTUK MENGISI OTOMATIS KODE TAMU YANG UNIK
   - `nama` (VARCHAR)
   - `kontak` (VARCHAR)

2. Tabel Pemesanan:
   - `kode_pemesanan` (CHAR, Primary Key) -> MENGGUNAKAN TRIGGER UNTUK MENGISI OTOMATIS KODE TAMU YANG UNIK
   - `kode_tamu` (INT, Foreign Key dari tabel tamu)
   - `waktu_masuk` (DATETIME)
   - `waktu_keluar` (DATETIME)
3. Tabel Kamar:
   - `no_kamar` (CHAR, Primary Key) -> MENGGUNAKAN TRIGGER UNTUK MENGISI OTOMATIS KODE TAMU YANG UNIK
   - `tipe_kamar` (VARCHAR)
   - `status_kamar` (ENUM('tersedia', 'dipesan'))

### Trigger
Trigger digunakan untuk menghasilkan `kode_pemesanan` & `kode_tamu` secara otomatis.
begitu juga dengan field `status_kamar`

## Pengembang
- Nama: Afi Naufal Rizky Yang
- Email: [afinaufalrizkyyang24@gmail.com]


>>>>>>> c8f8f5393bd0e1e099554d96cad6f382ab2ced79
