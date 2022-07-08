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

