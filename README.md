# ci-restserver
Check the recent version at https://github.com/chriskacerguis/codeigniter-restserver

My alternate version https://github.com/ardisaurus/old-rest-ci

## REST
singkatan bahasa Inggris dari Representational State Transfer
adalah suatu gaya arsitektur perangkat lunak untuk untuk pendistibusian sistem hipermedia seperti www. 
Pada arsitektur REST, REST server menyediakan resources (sumber daya/data) dan REST client mengakses dan menampilkan resource tersebut untuk penggunaan selanjutnya.

## CodeIgniter 
merupakan aplikasi sumber terbuka yang berupa framework PHP dengan model MVC (Model, View, Controller) untuk membangun website dinamis dengan menggunakan PHP. 
Dalam penerapan REST pada Codeigniter diperlukan beberapa library tambahan yang tidak disediakan secara default pada Codeigniter, salah satu library yang dapat digunakan adalah library dari Chris Kacerguis.

# Persiapan
Dalam pembuatan Rest API server ini diperlukan :

1. Webserver seperti Xampp, Wampp, atau lainnya.
2. Codeigniter dan library REST server yang diperlukan

# Langkah-langkah:
1. Konfigrasi database (saya menkonfigrasi database kontak yang berisi tabel kontak)
2. Extract CodeIgniter dan Rest Libraries pada folder htdocs
3. Enable autoload libraries: database
4. Masukkan database dan username pada rest_ci/application/config/database.php
5. Setelah itu buat file php baru pada controller di rest_ci/application/controller dengan nama kontak.php
6. Tambahkan code fungsi get pada kontak.php
7. Kemudian uji pada postman, pilih metode get dan masukkan link http://localhost/Tugas-REST-API-Workdhop-Web-Framework/index.php/kontak
   setelah itu klik "Send" Maka akan muncul hasil GET semua pada database 'kontak'
8. Tambahkan code fungsi post pada kontak.php
9. Kemudian uji pada postman, pilih metode post dan masukkan link http://localhost/Tugas-REST-API-Workdhop-WebFramework/index.php/kontak
   setelah itu klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key id dan value id yang akan diubah        misalkan id=1 diikuti value_id_nama=Creyon, 1234567890, lalu klik "Send".
10. Kemudian, lakukan metode get untuk melihat data baru. Maka data dengan id=1 telah berubah nama dari Orayon menjadi Creyon.
11. Tambahkan code fungsi delete pada kontak.php
12. Kemudian uji pada postman, pilih metode post dan masukkan link http://localhost/Tugas-REST-API-WorkdhopWebFramework/index.php/kontak
    setelah itu klik "Body" pada menu dibawah address bar, pilih x-www-form-urlencoded, masukan key id dan value id yang akan dihapus       misalkan id=1, lalu klik "Send".
13. Kemudian, lakukan metode get untuk melihat data baru. Maka data dengan id=1 akan terhapus dalam Rest API Server.
14. SELESAI :)

