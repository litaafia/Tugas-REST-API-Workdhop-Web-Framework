# ci-restserver
Check the recent version at https://github.com/chriskacerguis/codeigniter-restserver

My alternate version https://github.com/ardisaurus/old-rest-ci

## REST, singkatan bahasa Inggris dari Representational State Transfer 
adalah suatu gaya arsitektur perangkat lunak untuk untuk pendistibusian sistem hipermedia seperti www.

Pada arsitektur REST, REST server menyediakan resources (sumber daya/data) dan REST client mengakses dan menampilkan resource tersebut untuk penggunaan selanjutnya.

Untuk memungkinkan komunikasi data antara client dan server, codeigniter membutuhkan library tambahan berupa library curl. Curl adalah sebuah program yang memungkinan kita memindai data dari atau ke sebuah server. Salah satu library curl yang dapat digunakan adalah library curl dari Phil Sturgeon yang terdapat pada folder application/libraries/REST_Controller.php.

## Dalam pembuatan Rest API Server ini dibutuhkan:

Webserver seperti XAMPP, WAMPP, dll.
CodeIgniter dan library Rest Server seperti Library Curl yang dibuat oleh Phil Sturgeon seperti yang telah disebutkan diatas.
Setelah semuanya siap, kita akan masuk langkah-langkah nya, let's go!

JANGAN LUPA ENABLE AUTOLOAD LIBRARIES = 'database'!

Extract CodeIgniter dan Library Rest Server dan pindah ke folder htdocs supaya terdetect oleh webserver XAMPP kita. Silakan rename folder jika diperlukan
Masukkan http://localhost/Praktek4_E41181766/index.php/rest_server pada adress bar browser kita
Kemudian, konfigurasi database kita, sebagai contoh, kita buat database dengan nama 'kontak'
Selanjutnya, kita buat tabel baru bernama 'telepon'
Isi tabel 'telepon' dengan kolom 'id', 'nama', 'nomor'
Setelah itu, buka database.php pada folder /application/config dan isikan field: 'username' = 'root' 'database' = 'kontak'
Ok, sekarang kita masuk pada inti Rest API yaitu fungsi GET, POST, dan PUT Proses ini dilakukan menggunakan aplikasi pihak ketiga yaitu Postman for Windows

Buat file php baru di folder application/controllers dengan nama kontak.php Tambahkan sebuah kode fungsi get pada kontak.php, silakan cek application/controllers/kontak.php untuk keterangan lebih lanjut.
Sekarang kita masuk pada aplikasi Postman

Untuk menguji kode yang telah dibuat buka Postman, Pilih metode GET, masukan http://localhost/Praktek4_E41181766/index.php/kontak pada address bar lalu klik "Send". Maka akan muncul hasil GET semua data pada database 'kontak'
Kita juga bisa GET (menampilkan) salah satu data dengan menggunakan 'id', masukkan http://localhost/Praktek4_E41181766/index.php/kontak?id=1. Maka akan muncul data dengan 'id'= 1 saja.
Tambahkan sebuah kode fungsi post pada kontak.php, silakan cek application/controllers/kontak.php untuk keterangan lebih lanjut.
Untuk mengujinya buka Postman, pilih metode POST, masukan http://localhost/Praktek4_E41181766/index.php/kontak pada address bar, klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key dan value yang diperlukan (id, nama, nomor), lalu klik "Send".
Kemudian, lakukan metode get untuk melihat data baru.
Tambahkan sebuah kode fungsi put pada kontak.php, silakan cek application/controllers/kontak.php untuk keterangan lebih lanjut.
Untuk mengujinya buka Postman, pilih metode PUT, masukan http://localhost/Praktek4_E41181766/index.php/kontak pada address bar, klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key id dan value id yang akan diubah misalkan id=1 diikuti value_id_nama=Creyon, 1234567890, lalu klik "Send".
Kemudian, lakukan metode get untuk melihat data baru. Maka data dengan id=1 telah berubah nama dari Orayon menjadi Creyon.
Tambahkan sebuah kode fungsi delete pada kontak.php, silakan cek application/controllers/kontak.php untuk keterangan lebih lanjut.
Untuk mengujinya buka Postman, pilih metode PUT, masukan http://localhost/Praktek4_E41181766/index.php/kontak pada address bar, klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key id dan value id yang akan dihapus misalkan id=1, lalu klik "Send".
Kemudian, lakukan metode get untuk melihat data baru. Maka data dengan id=1 akan terhapus dalam Rest API Server.
SELESAI!
