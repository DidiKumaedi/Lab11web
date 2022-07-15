Nama  : Didi Kumaedi

NIM  : 312010002

Kelas : TI.20.D.1

Matkul  : 

# Praktikum 11

Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian 
Apache klik Config -> PHP.ini

![image](https://user-images.githubusercontent.com/101645216/172682171-f83123b3-09b6-46e9-9776-219c3414f77d.png)

![image](https://user-images.githubusercontent.com/101645216/172682353-478d2d3b-7935-4dda-a865-0288546f3db0.png)

Unduh Codeigniter dari website https://codeigniter.com/download
Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.
Ubah nama direktory framework-4.x.xx menjadi ci4.
Buka browser dengan alamat http://localhost/lab11_ci/ci4/public

![image](https://user-images.githubusercontent.com/101645216/172682588-d7f6581f-ad42-49eb-956b-669ad51420c0.png)

Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk 
mengakses CLI buka terminal/command prompt. 

![image](https://user-images.githubusercontent.com/101645216/172682730-2055ea75-523e-4d6c-9117-aa3efadaca24.png)

Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat 
(xampp/htdocs/lab11_ci/ci4/) 
Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:
php spark

![image](https://user-images.githubusercontent.com/101645216/172682842-7ee98867-0d2f-4bba-af8d-2940239d1898.png)





Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis 
errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi 
pada environment variable CI_ENVIRINMENT menjadi development.

![image](https://user-images.githubusercontent.com/101645216/172683073-3fe275f5-a71b-4fa4-bce7-04089b79d8fc.png)

![image](https://user-images.githubusercontent.com/101645216/172683553-17f8551c-aeff-43ab-8374-9bb52501bbd8.png)

Contoh error yang terjadi. Untuk mencoba error tersebut, ubah kode pada file 
app/Controller/Home.php hilangkan titik koma pada akhir kode.

![image](https://user-images.githubusercontent.com/101645216/172683711-cc5e5188-e8de-4e82-bc40-0a2066d2c54e.png)


Struktur Direktori
Untuk lebih memahami Framework Codeigniter 4 perlu mengetahui struktur direktori 
dan file yang ada. Buka pada Windows Explorer atau dari Visual Studio Code -> 
Open Folder.


![image](https://user-images.githubusercontent.com/101645216/172683940-79f4cb1f-a9e4-4467-9559-9cd465e8cd89.png)


Router terletak pada file app/config/Routes.php


![image](https://user-images.githubusercontent.com/101645216/172684112-60d0c4c1-9615-4735-af18-0db2134f1caf.png)


Membuat Route Baru.
Tambahkan kode berikut di dalam Routes.php
$routes->get('/about', 'Page::about');
$routes->get('/contact', 'Page::contact');
$routes->get('/faqs', 'Page::faqs');


![image](https://user-images.githubusercontent.com/101645216/172684281-cb7fce81-48f1-4a32-a8d5-ffcd7749504f.png)

php spark routes

![image](https://user-images.githubusercontent.com/101645216/172684347-78559ec1-3cb8-4920-948c-350617732b30.png)


![image](https://user-images.githubusercontent.com/101645216/172684668-e8d506c4-8c84-4cbd-a8a9-593d2a03e684.png)


Membuat Controller


![image](https://user-images.githubusercontent.com/101645216/172684870-ad6dd10d-36bb-47c0-8bdc-473a0cbe6127.png)


Hasil browser 

![image](https://user-images.githubusercontent.com/101645216/173799474-df457441-0dd9-4d82-a3f6-ee9a6da9b14d.png)


Tambahkan method baru pada Controller Page seperti berikut.

![image](https://user-images.githubusercontent.com/101645216/172686664-698be1a4-575c-4b50-8a62-70bd850d5a46.png)

Hasil Browsee


![image](https://user-images.githubusercontent.com/101645216/173799676-5796ef35-e703-41eb-b417-454927317fbe.png)

Membuat View
Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file 
baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi 
kodenya seperti berikut.

![image](https://user-images.githubusercontent.com/101645216/172686147-c4dc606d-954f-43b9-9650-112cbab9a0c4.png)

Ubah method about pada class Controller Page menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/101645216/172686336-96045a86-6b5f-4962-94f8-d9d5a63a9bf3.png)

Hasil browser 

![image](https://user-images.githubusercontent.com/101645216/173800155-548604c1-91dc-4eba-8c10-4ea1a42a92c7.png)


Buat file css pada direktori public dengan nama style.css (copy file dari praktikum 
lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

![image](https://user-images.githubusercontent.com/101645216/172687341-c58a5d55-661a-4871-809c-17af2f369ffb.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan 
footer.php
File app/view/template/header.php

![image](https://user-images.githubusercontent.com/101645216/172687422-39eb2b90-4143-4334-ae0d-bacfd3378fd9.png)

File app/view/template/footer.php

![image](https://user-images.githubusercontent.com/101645216/172687498-4acfc86d-0fe5-43b5-a1d7-7e470c847ce9.png)

Hasil browser

![image](https://user-images.githubusercontent.com/101645216/173800501-5d804763-e17e-4756-819d-d94309277adb.png)


Pertanyaan dan Tugas
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

- About

![image](https://user-images.githubusercontent.com/101645216/172710266-19959c82-232a-480f-9c72-d228b70971ea.png)

Hasil browser
![image](https://user-images.githubusercontent.com/101645216/172711935-35087aa3-bd33-4342-bc53-2e4262de0c4c.png)

# Praktikum 12

Membuat Database: Studi Kasus Data Artikel

Membuat Database

CREATE DATABASE lab_ci4

Membuat Tabel

![image](https://user-images.githubusercontent.com/101645216/173198146-9dd93805-7da0-47a4-948e-80983fc7b3fb.png)

Konfigurasi koneksi database
Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. 
Konfigurasi dapat dilakukan dengan du acara, yaitu pada file app/config/database.php
atau menggunakan file .env. Pada praktikum ini kita gunakan konfigurasi pada file .env.


![image](https://user-images.githubusercontent.com/101645216/173198278-16d260a6-0fae-4398-b02c-58d6bd544cd8.png)

Membuat Model
Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada 
direktori app/Models dengan nama ArtikelModel.php

![image](https://user-images.githubusercontent.com/101645216/173198511-3a19e209-cd57-417f-835e-edbc892271ce.png)

Membuat Controller
Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers.

![image](https://user-images.githubusercontent.com/101645216/173198580-ae62900a-ee2c-4179-976a-125bc9c2e884.png)

Membuat View
Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file 
baru dengan nama index.php.

![image](https://user-images.githubusercontent.com/101645216/173299306-a5232f75-2f17-465e-9703-300bd923aa42.png)


Hasil browser

![image](https://user-images.githubusercontent.com/101645216/173299191-4bc09d79-be8b-4223-9a89-b22e9911ba7e.png)

Belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada 
database agar dapat ditampilkan datanya

![image](https://user-images.githubusercontent.com/101645216/173299468-99fc2de4-9af8-4f99-bd05-3ef35fbe4a46.png)
  
Hasil browser

![image](https://user-images.githubusercontent.com/101645216/173814999-08f81a93-d550-4be4-ad9f-0fb0df96f580.png)

Membuat Tampilan Detail Artikel yaitu Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. dengan cara tambahkan fungsi baru pada Controller Artikel dengan nama view().

![image](https://user-images.githubusercontent.com/101645216/173815816-bcf3ecb8-2c54-456e-93e6-af071682580d.png)

Membuat View Detail. Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php.

![image](https://user-images.githubusercontent.com/101645216/173816028-f50ddfc0-b80c-4537-8ea9-7554f673e23b.png)

Membuat Routing untuk artikel detail, Buka Kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail.

![image](https://user-images.githubusercontent.com/101645216/173816282-0c99a899-c66b-43db-b21f-594a61325696.png)


Kemudian klik pada artikel 1 atau dua untuk melihat hasilnya.

![image](https://user-images.githubusercontent.com/101645216/173816436-7a0c294b-3296-4289-b251-aedaf00468e6.png)

Membuat Menu Admin, menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index().

![image](https://user-images.githubusercontent.com/101645216/173816642-ed75d690-5e55-482d-9e60-c1b5e0ffd9fe.png)

selanjutnya buat view untuk tampilan admin dengan nama admin_index.php

![image](https://user-images.githubusercontent.com/101645216/173816903-7c94b4cc-a666-4cb2-9000-377f4bb826d2.png)

![image](https://user-images.githubusercontent.com/101645216/173816991-479bb096-4aa3-4fba-81cc-ed55f923cc6a.png)


Tambahkan routing untuk menu admin seperti berikut

![image](https://user-images.githubusercontent.com/101645216/173817202-381f3d46-4122-456f-87f3-a97cf421bd0d.png)

Akses menu admin dengan url http://localhost:8080/admin/artikel


![image](https://user-images.githubusercontent.com/101645216/173818346-3f92ff92-6776-4bf2-884c-ea8283f3ce0f.png)


Menambah Data Artikel, tambahkan fungsi/method baru pada Controller Artikel dengan nama add().

![image](https://user-images.githubusercontent.com/101645216/173817717-f6b28e3b-f9a4-4812-9b1e-3c753bf57ff8.png)


Kemudian buat view untuk form tambah dengan nama form_add.php

![image](https://user-images.githubusercontent.com/101645216/173817854-bf7fc367-98e6-4205-b7b4-73cca70ec337.png)


Hasil Browser

![image](https://user-images.githubusercontent.com/101645216/173818469-434eee83-2c8a-4b17-ab0f-a135175eace2.png)

Mengubah Data, tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().

![image](https://user-images.githubusercontent.com/101645216/173818645-413d29a7-8aad-4747-843a-592e3863c27d.png)

Kemudian buat view untuk form tambah dengan nama form_edit.php

![image](https://user-images.githubusercontent.com/101645216/173818782-d7e31a4f-aae6-4c2b-a8f1-ecae1c93a9c2.png)

Hasil browser

![image](https://user-images.githubusercontent.com/101645216/173818896-3430a4e1-610a-4738-b847-a3ca5c5e84ba.png)


Menghapus Data, tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().


![image](https://user-images.githubusercontent.com/101645216/173819017-4b24d2e8-01ce-4693-835d-562bd5476976.png)

# PRAKTIKUM 13
Langkah-langkah Praktikum
Persiapan.
Untuk memulai membuat modul Login, yang perlu disiapkan adalah database server
menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui
XAMPP.

Membuat Tabel: User Login

![image](https://user-images.githubusercontent.com/101645216/174441767-1abab8f0-0fa5-4ff4-9cc7-c150ffb3b39d.png)


![image](https://user-images.githubusercontent.com/101645216/174441809-94d997da-2996-4283-b822-464e9800a712.png)

Membuat Model User
Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada 
direktori app/Models dengan nama UserModel.php

![image](https://user-images.githubusercontent.com/101645216/174940056-6fc19694-6b9e-496d-8691-2c159c85a4b1.png)

Membuat Controller User
Buat Controller baru dengan nama User.php pada direktori app/Controllers.
Kemudian tambahkan method index() untuk menampilkan daftar user, dan method 
login() untuk proses login.

![image](https://user-images.githubusercontent.com/101645216/174940110-713bb859-2fea-4be0-9481-18ab7b7ff95b.png)

![image](https://user-images.githubusercontent.com/101645216/174940150-8551b872-1a4a-4284-8fb8-e053d5868ede.png)

Membuat View Login
Buat direktori baru dengan nama user pada direktori app/views, kemudian buat file 
baru dengan nama login.php. 

![image](https://user-images.githubusercontent.com/101645216/174940298-62244678-957e-45ed-aac7-965b49c95db4.png)

![image](https://user-images.githubusercontent.com/101645216/174940334-e2c7de25-6f75-48d8-b4e8-52f7180f97f4.png)

Membuat Database Seeder

![image](https://user-images.githubusercontent.com/101645216/174940393-c1607569-3a1d-47ec-bbda-4509cb63a2c9.png)

Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori 
/app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut

![image](https://user-images.githubusercontent.com/101645216/174940443-204f02b7-9855-4f91-a63e-f252f53eaa1c.png)


![image](https://user-images.githubusercontent.com/101645216/174940471-8d149d9f-bb66-4977-b2fd-190a7fc6a593.png)


Uji Coba Login
Selanjutnya buka url http://localhost:8080/user/login seperti berikut:


![image](https://user-images.githubusercontent.com/101645216/174940575-1764086a-d0b3-4e58-bcfe-ba3e5da4584a.png)

Menambahkan Auth Filter
Selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php
pada direktori app/Filters. 

![image](https://user-images.githubusercontent.com/101645216/174944381-07f54172-4043-44c8-8f32-4820e7938329.png)


Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:
'auth' => App\Filters\Auth::class


![image](https://user-images.githubusercontent.com/101645216/174944428-eed2bc21-d237-4999-a3d0-5c93dbd431e8.png)

 
Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya


![image](https://user-images.githubusercontent.com/101645216/174944573-388f94b9-ab0b-4023-bf1e-fe7c9603e66c.png)

Percobaan Akses Menu Admin
Buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut 
diakses maka, akan dimuculkan halaman login. 


![image](https://user-images.githubusercontent.com/101645216/174944638-fb47716c-b334-4599-9eb1-063ecb312c67.png)


Fungsi Logout
Tambahkan method logout pada Controller User seperti berikut:


![image](https://user-images.githubusercontent.com/101645216/174945034-3701e03c-a0d9-4ccf-8c43-29be76c75f95.png)

# Praktikum 14

Langkah-langkah Praktikum
Membuat Pagination

Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi
kode pada method admin_index seperti berikut.

![image](https://user-images.githubusercontent.com/101645216/175769855-fdfab778-2801-4aff-a3b1-859771a1c290.png)

Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut
dibawah deklarasi tabel data.


![image](https://user-images.githubusercontent.com/101645216/175770002-a4b30671-7c1e-40af-a4c5-370d6042b4ab.png)


Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat
hasilnya.


![image](https://user-images.githubusercontent.com/101645216/175770528-1dfd7a66-751d-406b-bcc5-f47562e3d3ff.png)

Membuat Pencarian
Pencarian data digunakan untuk memfilter data.

Untuk membuat pencarian data, buka kembali Controller Artikel, pada method
admin_index ubah kodenya seperti berikut

![image](https://user-images.githubusercontent.com/101645216/175770586-224a5e9d-c9c6-465f-bb02-044bf4250553.png)

Kemudian buka kembali file views/artikel/admin_index.php dan tambahkan form
pencarian sebelum deklarasi tabel seperti berikut:

![image](https://user-images.githubusercontent.com/101645216/175770964-49d4d197-4180-40bf-a5ef-c25a7c8e0f8b.png)


Dan pada link pager ubah seperti berikut


![image](https://user-images.githubusercontent.com/101645216/175770983-183050af-517b-4aaf-b1e2-48ff9bb90799.png)


Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata
kunci tertentu pada form pencarian.


![image](https://user-images.githubusercontent.com/101645216/175770993-d6ab0499-7c3d-4668-ba93-9366beba8489.png)


Upload Gambar
Menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller
Artikel, sesuaikan kode pada method add seperti berikut:


![image](https://user-images.githubusercontent.com/101645216/175771137-1952553e-9a04-4e9f-ad81-e651c409be22.png)

Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti
berikut.

![image](https://user-images.githubusercontent.com/101645216/175771223-9c8756d5-1944-4ea3-9af9-7cc5325b7682.png)


Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut.


![image](https://user-images.githubusercontent.com/101645216/175771263-5bbae990-5c0b-4836-8b42-139e4fe93227.png)


Ujicoba file upload dengan mengakses menu tambah artikel.


![image](https://user-images.githubusercontent.com/101645216/175772082-f7f524f1-cbd2-4d37-bee7-bf1ee63e6e2b.png)
