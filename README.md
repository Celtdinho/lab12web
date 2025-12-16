# Praktikum 12 – Framework Modular PHP

## Nama : Naufal Rafi Haryanto
## Nim : 312410118
## Kelas : TI.24.A1

## Deskripsi

Praktikum ini bertujuan untuk menerapkan konsep **Framework Modular menggunakan PHP OOP** dengan fitur autentikasi pengguna. Aplikasi dibangun menggunakan PHP native, MySQL, dan konsep MVC sederhana (routing, module, template).

Fitur utama yang dibuat pada Praktikum 12 adalah **Login**, **Profil User**, dan **Ganti Password**, dengan pengelolaan session serta penggunaan `password_hash()` dan `password_verify()` untuk keamanan.

---

## Fitur Aplikasi

* Routing modular menggunakan `.htaccess`
* Template terpusat (header, sidebar, footer)
* Login user menggunakan session
* Proteksi halaman (hanya bisa diakses setelah login)
* Halaman profil user
* Fitur ganti password
* Password terenkripsi menggunakan hashing
* Tampilan UI sederhana dan konsisten dengan CSS

---

## Struktur Folder

```
lab11_php_oop/
├── index.php
├── .htaccess
├── assets/
│   └── css/
│       └── style.css
├── class/
│   └── database.php
├── template/
│   ├── header.php
│   ├── sidebar.php
│   └── footer.php
├── module/
│   ├── user/
│   │   ├── login.php
│   │   ├── profile.php
│   │   └── logout.php
│   └── home/
│       └── index.php
└── database.sql
```

---

## Konfigurasi Database

1. Buat database MySQL dengan nama bebas (contoh: `latihan_oop`)
2. Import file `database.sql`
3. Atur koneksi database pada file:

   ```
   class/database.php
   ```

Contoh akun default:

```
Username: admin
Password: admin123
```

---

## Cara Menjalankan Aplikasi

1. Pindahkan folder `lab11_php_oop` ke dalam direktori `htdocs`
2. Aktifkan Apache dan MySQL melalui XAMPP
3. Pastikan `AllowOverride All` aktif di Apache
4. Akses aplikasi melalui browser:

   ```
   http://localhost/lab11_php_oop/user/login
   ```

---

## Alur Login

1. User membuka halaman login
2. User memasukkan username dan password
3. Sistem memverifikasi data menggunakan `password_verify()`
4. Jika berhasil, session dibuat dan user diarahkan ke halaman utama
5. Menu profil dan logout akan muncul setelah login

---

## Catatan Penting

* File module tidak boleh diakses langsung melalui path file
* Akses halaman harus melalui routing (contoh: `/user/login`)
* Password tidak disimpan dalam bentuk teks asli
* Session digunakan untuk menjaga status login

---

## Kesimpulan

Dengan praktikum ini, mahasiswa memahami konsep dasar framework modular sederhana menggunakan PHP, penerapan OOP, pengelolaan session, keamanan password, serta pemisahan logika aplikasi dan tampilan.

Praktikum ini menjadi dasar untuk pengembangan aplikasi web yang lebih kompleks di masa depan.

---

**Nama Praktikan:** …………………
**NIM:** …………………
**Mata Kuliah:** Pemrograman Web / OOP PHP
