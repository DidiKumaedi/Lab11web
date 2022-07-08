# Lab11web

Nama    : Didi Kumaedi

NIM     : 312010002

Kelas   : TI.20.D.1

Matkul  : Pemrograman Web

Laporan Praktikum

Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi
pada webserver. Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan
pengembangan Codeigniter 4.
Berikut beberapa ekstensi yang perlu diaktifkan:
- php-json ekstension untuk bekerja dengan JSON;

- php-mysqlnd native driver untuk MySQL;

- php-xml ekstension untuk bekerja dengan XML;

- php-intl ekstensi untuk membuat aplikasi multibahasa;

- libcurl (opsional), jika ingin pakai Curl.

Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian
Apache klik Config -> PHP.ini

![image](https://user-images.githubusercontent.com/101849655/172670428-d8ed52bf-5498-4dff-8800-adc8bcbe629e.png)

Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan
diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.

![image](https://user-images.githubusercontent.com/101849655/172670573-dca658b7-e2f7-4ff6-89d1-1a2c4d7ca84d.png)

Instalasi Codeigniter 4
Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara
manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara
manual.

- Unduh Codeigniter dari website https://codeigniter.com/download

- Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.

- Ubah nama direktory framework-4.x.xx menjadi ci4.

- Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

![image](https://user-images.githubusercontent.com/101849655/172670906-7e207e5d-9104-420f-8a11-90a70dd5f7e0.png)

Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk
mengakses CLI buka terminal/command prompt.

Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat
(xampp/htdocs/lab11_ci/ci4/)
Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah: php spark

![image](https://user-images.githubusercontent.com/101849655/172671137-82a6ee2f-bda0-428f-b041-04faa81a8a6e.png)

Mengaktifkan Mode Debugging
Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk
mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.
Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan
pesan kesalahan seperti berikut.

![image](https://user-images.githubusercontent.com/101849655/172672638-cda874fe-e06c-4ad8-9ae9-3143074642d9.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis
errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi
pada environment variable CI_ENVIRINMENT menjadi development.

Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable
CI_ENVIRINMENT menjadi development.

![image](https://user-images.githubusercontent.com/101849655/172691606-73c61bcc-2e14-45b0-a39e-7f2bc36615fc.png)

![image](https://user-images.githubusercontent.com/101849655/172691796-9747a1d6-c247-41cf-9a4a-438d6a0fd878.png)

![image](https://user-images.githubusercontent.com/101849655/172691910-c2b4aa55-943d-43ed-b002-4e8ea82be399.png)

##Routing dan Controller

Router terletak pada file app/config/Routes.php. Pada file tersebut kita dapat mendefinisikan route untuk aplikasi yang kita buat.

Contoh: ```$routes->get('/', 'Home::index'); Kode tersebut akan mengarahkan rute untuk halaman home.

## Membuat Route Baru.

Tambahkan kode berikut di dalam Routes.php

![image](https://user-images.githubusercontent.com/101849655/172693557-2cb57665-7455-4741-a6a3-e4d0c8f08fd8.png)

Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah berikut. php spark routes

![image](https://user-images.githubusercontent.com/101849655/172693634-ead3475a-d774-4b8b-8e4d-1af64b143329.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about

![image](https://user-images.githubusercontent.com/101849655/172694207-e690eec1-e04c-4d43-ae73-9fecfe516ed1.png)

Ketika diakses akan mucul tampilan error 404 file not found, itu artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

## Membuat Controller

Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.

![image](https://user-images.githubusercontent.com/101849655/172714976-77de3f23-be5f-4871-8a4e-e20f5d8b0b00.png)

hasil 
![image](https://user-images.githubusercontent.com/101849655/177944013-b4edb8f9-3e5d-471c-a075-8fd5954ca16f.png)

Tambahkan method baru pada controllers page berikkut

![image](https://user-images.githubusercontent.com/101849655/177940506-e5d3cc0a-4045-4f9c-bcc2-3073321b086c.png)

hasil

![image](https://user-images.githubusercontent.com/101849655/177943903-1120a088-aef3-43b0-87ff-b05d1f8cfe92.png)

Membuat View Selanjutnya dalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.

![image](https://user-images.githubusercontent.com/101849655/177943437-b0d2382b-8478-4a11-944e-da757413af83.png)

Ubah method about pada class Controller Page menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/101849655/177943607-81b9be82-db4e-4377-a3e8-d55cac01cc53.png)

![image](https://user-images.githubusercontent.com/101849655/177943779-5524df28-2955-4f7f-a92a-8faa19912d2f.png)

hasil

![image](https://user-images.githubusercontent.com/101849655/177944529-df14b680-9b08-452d-9c6f-55fcb312b6f7.png)

Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

![image](https://user-images.githubusercontent.com/101849655/177946696-4b719ded-e9fb-404e-b83f-a8a668f41f30.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php File app/view/template/header.php

![image](https://user-images.githubusercontent.com/101849655/177946833-1b78d82b-5eda-4d44-85ed-8af8d75a5c9a.png)

![image](https://user-images.githubusercontent.com/101849655/177946930-d4114e69-20af-4f51-89a0-497a6b7cf418.png)

![image](https://user-images.githubusercontent.com/101849655/177947097-e5b6dbc8-2fb9-44b0-9e46-ebb69f4d0466.png)


# Praktikum 12

Membuat Database: Studi Kasus Data Artikel

Membuat Database

CREATE DATABASE lab_ci4

Membuat Tabel

![image](https://user-images.githubusercontent.com/101849655/177954304-062fb1db-e054-4a9f-b004-77a034060fe6.png)

Konfigurasi koneksi database Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Konfigurasi dapat dilakukan dengan du acara, yaitu pada file app/config/database.php atau menggunakan file .env. Pada praktikum ini kita gunakan konfigurasi pada file .env.

![image](https://user-images.githubusercontent.com/101849655/177955063-ce54589d-b9c1-4e4b-98ea-d4ea0037b1d7.png)

Membuat Model
Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada
direktori app/Models dengan nama ArtikelModel.php

![image](https://user-images.githubusercontent.com/101849655/177955776-e2535516-7dc6-4eef-bca1-40954cdb0acc.png)

Membuat Controller
Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers.

![image](https://user-images.githubusercontent.com/101849655/177955939-3ee0f78b-a397-488a-83e8-4e837dd560d3.png)

Membuat View
Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file
baru dengan nama index.php.

![image](https://user-images.githubusercontent.com/101849655/177956871-3f4273ce-3ffb-4e47-a315-cb6785489277.png)

hasil

![image](https://user-images.githubusercontent.com/101849655/177956996-ddcbd201-3023-4897-9416-4110fd5a944a.png)

Belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada database agar dapat ditampilkan datanya

![image](https://user-images.githubusercontent.com/101849655/177957640-308e8e9d-6299-431b-b957-a02f50f5d2ca.png)

hasil

![image](https://user-images.githubusercontent.com/101849655/177957824-6917fd83-3c24-48b4-8353-30c5b871725a.png)

Membuat View Detail
Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php.

![image](https://user-images.githubusercontent.com/101849655/178027030-73b36020-820c-4691-9cad-704c2fbfce99.png)

![image](https://user-images.githubusercontent.com/101849655/178027407-37186923-99e3-4d0e-aa93-5f785d674cf3.png)

![image](https://user-images.githubusercontent.com/101849655/178027638-11080b2f-2fce-4132-96d2-56aa0d5fd25c.png)

Membuat Menu Admin
Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada
Controller Artikel dengan nama admin_index().

![image](https://user-images.githubusercontent.com/101849655/178028673-c92db06b-2985-4b1b-aa16-7739d63aecce.png)

Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php

![image](https://user-images.githubusercontent.com/101849655/178029460-8df42772-ff3f-452e-b468-04a15263a541.png)

![image](https://user-images.githubusercontent.com/101849655/178029505-a2940c31-e460-4cc6-8cbc-e772894eeb28.png)

Tambahkan routing untuk menu admin seperti berikut:

![image](https://user-images.githubusercontent.com/101849655/178030664-e6227e5e-41a8-49f1-b8cd-f8e09bc9a131.png)

Akses menu admin dengan url http://localhost:8080/admin/artikel

![image](https://user-images.githubusercontent.com/101849655/178031327-4a308acd-cebf-4e29-8961-9954b738f448.png)

Menambah Data Artikel, tambahkan fungsi/method baru pada Controller Artikel dengan nama add().

![image](https://user-images.githubusercontent.com/101849655/178031805-48edfe90-3d59-41b3-be36-e1ff0cf46a7b.png)

Kemudian buat view untuk form tambah dengan nama form_add.php

![image](https://user-images.githubusercontent.com/101849655/178032477-ef4f81ba-78d7-4250-9afa-05f123741b3a.png)

![image](https://user-images.githubusercontent.com/101849655/178032677-09011a63-7efe-4ca5-aa23-dfdddd8252a0.png)

Mengubah Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().

![image](https://user-images.githubusercontent.com/101849655/178033154-f4a23f9e-d1b7-4237-8345-72b30fca05fa.png)

Kemudian buat view untuk form tambah dengan nama form_edit.php

![image](https://user-images.githubusercontent.com/101849655/178033423-60f94951-18e2-4007-91df-b65ecf6f265b.png)

![image](https://user-images.githubusercontent.com/101849655/178033606-510aac15-bfa9-49ae-a70b-ff8693476521.png)

Menghapus Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().

![image](https://user-images.githubusercontent.com/101849655/178034421-d2d08033-9537-45db-9ed6-faab87de67f7.png)


# Praktikum 13

Langkah-langkah Praktikum Persiapan. Untuk memulai membuat modul Login, yang perlu disiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui XAMPP.

Membuat Tabel: User Login

![image](https://user-images.githubusercontent.com/101849655/178036536-de6f285f-8652-4f6f-9d2c-b7a5a79892da.png)

Membuat Model User
Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada
direktori app/Models dengan nama UserModel.php

![image](https://user-images.githubusercontent.com/101849655/178036897-7f298f7e-c74e-43d5-988a-4cf84529e2ef.png)

Membuat Controller User
Buat Controller baru dengan nama User.php pada direktori app/Controllers.
Kemudian tambahkan method index() untuk menampilkan daftar user, dan method
login() untuk proses login.

![image](https://user-images.githubusercontent.com/101849655/178039010-795e6336-d907-4436-8a5b-b37c2c1580cb.png)

![image](https://user-images.githubusercontent.com/101849655/178040272-84d0caad-a3c1-40d7-85c6-ea3ab2ad0f91.png)

Membuat View Login Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php.

![image](https://user-images.githubusercontent.com/101849655/178041357-55cc3d21-bd3c-4e81-8896-87e33060c77a.png)

Membuat Database Seeder
Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul
login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat
database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:

![image](https://user-images.githubusercontent.com/101849655/178042043-8ceb1517-0502-4e09-b72b-9c52cf607ae1.png)

Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori /app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut

![image](https://user-images.githubusercontent.com/101849655/178042493-dceb550b-e808-46be-85c3-a04ecff8babe.png)

Selanjutnya buka kembali CLI dan ketik perintah berikut:

![image](https://user-images.githubusercontent.com/101849655/178043219-d3677c50-cc97-4321-ae96-f175eee9b971.png)

Uji Coba Login Selanjutnya buka url http://localhost:8080/user/login seperti berikut:

![image](https://user-images.githubusercontent.com/101849655/178043434-5ade7ab3-96d9-4b2d-81f9-e0e9ca32654d.png)

Menambahkan Auth Filter Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters.

![image](https://user-images.githubusercontent.com/101849655/178045737-973ce4e5-cc6b-4168-887d-f483455eecef.png)

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut: 'auth' => App\Filters\Auth::class

![image](https://user-images.githubusercontent.com/101849655/178046619-d99afaa1-d856-4b2e-96df-107bce946925.png)

Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.

![image](https://user-images.githubusercontent.com/101849655/178047250-b96b2daa-3475-4feb-8eff-313046b34bff.png)

Percobaan Akses Menu Admin Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut diakses maka, akan dimuculkan halaman login.

![image](https://user-images.githubusercontent.com/101849655/178047578-e012313e-a95f-4108-bc62-9da6423879f7.png)

Fungsi Logout Tambahkan method logout pada Controller User seperti berikut:

![image](https://user-images.githubusercontent.com/101849655/178048050-bdff59ff-11df-471d-952f-53914a30e77b.png)


# Praktikum 14

Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi kode pada method admin_index seperti berikut.

![image](https://user-images.githubusercontent.com/101849655/178058209-f8e96d1a-4fdd-446f-b994-19098f84151d.png)

Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut dibawah deklarasi tabel data.

![image](https://user-images.githubusercontent.com/101849655/178058542-80d75fa0-f5ce-49c8-829d-2d8bdf20b385.png)

Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat hasilnya.

![image](https://user-images.githubusercontent.com/101849655/178058675-55ff59c0-f0d5-4de8-b792-cfd80e56c183.png)

Membuat Pencarian Pencarian data digunakan untuk memfilter data.

Untuk membuat pencarian data, buka kembali Controller Artikel, pada method admin_index ubah kodenya seperti berikut

