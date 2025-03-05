# Mini Project Tabungan

Mini project tabungan ini adalah aplikasi web yang memungkinkan mahasiswa untuk melakukan tabungan dan melihat riwayat tabungan yang sudah mereka lakukan. Admin memiliki hak istimewa untuk mengelola pengguna dan melihat semua tabungan yang ada.

1. Cara Mengatur Database
- Jalankan XAMPP (MySQL Database dan Apache Web Server)
- Buka phpMyAdmin melalui browser di http://localhost/phpmyadmin 



2. Cara Menjalankan Proyek Secara Lokal

Download atau Clone Repository

Jika menggunakan Git, jalankan perintah berikut di terminal:

git clone https://github.com/username/mini-donasi.git
cd mini-donasi

Jika tidak menggunakan Git, cukup download project dalam bentuk ZIP dan ekstrak.

Konfigurasi Koneksi Database

Buka file config/database.php dan ubah pengaturan database sesuai dengan lingkungan Anda:

private $host = 'localhost';
private $db_name = 'donasi_db';
private $username = 'root';
private $password = '';

Jika menggunakan XAMPP/MAMP, pastikan MySQL berjalan sebelum melanjutkan.

Menjalankan Server Lokal

Jika menggunakan PHP built-in server, jalankan perintah berikut:

php -S localhost:8000

Jika menggunakan XAMPP/MAMP, pindahkan folder project ke dalam htdocs dan akses melalui browser dengan membuka http://localhost/mini-donasi.

3. Fitur Utama yang Telah Diimplementasikan
✅ Autentikasi Pengguna:
- Pengguna bisa mendaftar dan login menggunakan email dan password yang aman.
- Password dienkripsi menggunakan hashing sebelum disimpan.
- Pengguna bisa logout untuk mengakhiri sesi mereka.

✅ Manajemen Donasi:
- Pengguna bisa memberikan donasi dengan jumlah tertentu dan menambahkan pesan.
- User biasa hanya bisa melihat donasi yang mereka buat sendiri.
- Admin bisa melihat semua donasi dari semua pengguna.

✅ Manajemen Pengguna (Hanya Admin Pertama):
- Admin pertama bisa menjadikan user lain sebagai admin atau kembali sebagai user.
- Admin pertama bisa menghapus user, tetapi tidak bisa menghapus dirinya sendiri.

✅ Keamanan & Middleware:
- isAuthenticated() memastikan hanya pengguna yang sudah login bisa mengakses fitur donasi.
- isAdmin() memastikan hanya admin yang bisa masuk ke halaman admin.
- isFirstAdmin() memastikan hanya admin pertama yang bisa mengelola user lain.