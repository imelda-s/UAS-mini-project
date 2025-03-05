# Mini Project Tabungan

## ⚙️ Cara Mengatur Database
Agar proyek ini dapat berjalan dengan baik, Anda perlu mengatur database terlebih dahulu. Berikut adalah langkah-langkahnya:
1. Membuka phpMyAdmin
- Pastikan XAMPP sudah diinstal di komputer Anda.
- Buka XAMPP Control Panel, lalu Start Apache dan MySQL.
- Buka browser dan ketik `http://localhost/phpmyadmin/` di address bar, lalu tekan Enter.
2. Membuat Database
- Di halaman phpMyAdmin, klik Tab "Database" di bagian atas.
- Pada bagian Create database, masukkan nama database yaitu `tabungan_db`.
- Klik tombol Create untuk membuat database baru.
3. Mengimpor Struktur dan Data Database
- Klik database yang baru dibuat di sidebar kiri.
- Pilih tab Import di menu atas.
- Klik tombol Choose File dan pilih file SQL database yang tersedia dalam proyek (`database.sql`).
- Setelah file dipilih, klik Go untuk mulai mengimpor.
- Jika berhasil, tabel-tabel akan muncul dalam database Anda.

## 🚀 Cara Menjalankan Proyek Secara Lokal
Setelah database siap, Anda bisa menjalankan proyek ini secara lokal dengan langkah-langkah berikut:
1. Menyalakan Server Lokal
- Buka XAMPP Control Panel.
- Klik Start pada Apache dan MySQL untuk menjalankan server.
2. Menempatkan Proyek di Direktori XAMPP
- Buka folder tempat XAMPP diinstal.
- Pindahkan atau ekstrak folder proyek ke dalam folder `htdocs`. Misalnya, jika folder proyek bernama `saving_project`, maka path lengkapnya akan menjadi:
```C:\xampp\htdocs\saving_project\```
3. Konfigurasi Koneksi Database
- Buka file config/database.php dalam proyek.
- Pastikan pengaturan database sesuai dengan database yang telah Anda buat:
```php
define('DB_HOST', 'localhost');
define('DB_NAME', 'my_project_db'); // Nama database yang dibuat di phpMyAdmin
define('DB_USER', 'root'); // Default user phpMyAdmin
define('DB_PASS', ''); // Default password kosong jika belum diubah
```
- Simpan perubahan.
4. Mengakses Proyek di Browser
- Buka browser.
- Ketik URL berikut:
```http://localhost/my_project/```
- Tekan Enter, dan proyek akan berjalan.

## 🔥 Fitur Utama
✅ Autentikasi Pengguna
- Pengguna dapat melakukan registrasi dan login.
- Sistem memastikan hanya pengguna yang telah login yang bisa mengakses fitur tertentu.
✅ Manajemen Tabungan
- Pengguna dapat menyimpan uang dengan jumlah tertentu.
- Admin dapat melihat semua tabungan, sedangkan pengguna hanya bisa melihat tabungannya sendiri.
✅ Manajemen Pengguna
- Admin dapat mengubah peran pengguna (misalnya dari user menjadi admin).
- Admin dapat menghapus pengguna dari sistem.
✅ Sistem Routing Dinamis
- Menggunakan Router untuk menangani navigasi halaman.
- Mendukung URL rewriting menggunakan .htaccess agar URL lebih bersih dan mudah diakses.
✅ Middleware untuk Keamanan
- Menggunakan AuthMiddleware untuk memastikan hanya pengguna yang berhak dapat mengakses halaman tertentu.
- Admin memiliki hak akses khusus untuk fitur manajemen pengguna.

