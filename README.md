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

![image](https://user-images.githubusercontent.com/101849655/172671380-c3410122-c552-4e48-a858-3d33dd60515c.png)
