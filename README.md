<h1 align="center"><img src="https://oded.blog/images/2017/07/hexo-logo.png"></h1>

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Maintenance](#maintenance) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi) | [Team](#team)
:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:

# Sekilas Tentang
Sebuah blog framework yang cepat, sederhana, dan kuat yang didukung oleh [Node.js](https://nodejs.org).

## Fitur
- Sangat cepat untuk dibuat
- Mendukung GitHub Flavoured Markdown dan sebagian besar plugin Octopress
- One-command deploy ke GitHub Pages, Heroku, dan lain-lain
- Sistem plugin yang kuat


# Instalasi
Untuk memasang Hexo, Anda perlu menginstal beberapa hal lain terlebih dahulu:
- [Node.js](https://nodejs.org)
- [Git](https://git-scm.com)

Jika komputer Anda sudah memiliki ini, Cukup instal Hexo dengan npm:

``` bash
$ npm install -g hexo-cli 
```
Jika hexo telah terinstall maka pada saat dilakukan pengecekan versi akan muncul output seperti ini

![output hexo](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/output_hexo.PNG)

Jika belum, ikuti petunjuk berikut untuk menginstal semua persyaratan.

## Untuk pengguna Mac
Anda mungkin mengalami beberapa masalah saat kompilasi. Silakan instal Xcode dari App Store terlebih dahulu. Setelah Xcode diinstal, buka Xcode dan buka **Preferences -> Download -> Command Line Tools -> Install** untuk menginstal command line tools.

## Login ke dalam server menggunakan SSH. 
``` bash
$ ssh username@localhost -p 2222
```
![Login](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/Login.PNG)

## Pastikan seluruh paket sistem kita up-to-date

Pada Linux gunakan command berikut

``` bash
$ sudo apt-get update

```

## Instal Git
- Windows: Unduh & instal git.
- Mac: Instal dengan Homebrew, MacPorts atau installer.
- Linux (Ubuntu, Debian): 
``` bash
$ sudo apt-get install git-core
```
![update](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/update.PNG)

- Linux (Fedora, Red Hat, CentOS): 
``` bash
$ sudo yum install git-core
```
## Instal Node.Js
Cara terbaik untuk menginstal Node.js adalah dengan Node Version Manager.

Gunakan skrip sederhana yang secara otomatis menginstal nvm:

cURL:
``` bash
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```
![curl](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/node_curl.PNG)

Wget:
``` bash
$ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```
![wget](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/wget.PNG)

Setelah nvm diinstal, restart terminal dan jalankan perintah berikut untuk menginstal Node.js:
``` bash
$ nvm install stable
```
![nvm](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/nvm.PNG)

Jika sudah terinstal lakukan pengecekan agar memastikan node js sudah terinstal

![version](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/version_nvm&npm.PNG)

Atau, unduh dan jalankan installer Node.Js.
## Instal Hexo
Setelah semua persyaratan diinstal, Anda dapat menginstal Hexo dengan npm:

``` bash
$ npm install -g hexo-cli 
```
Jika hexo telah terinstall maka pada saat dilakukan pengecekan versi akan muncul output seperti ini

![output hexo](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/output_hexo.PNG)

# Konfigurasi

## Sekilas tentang plugin [hexo-admin](https://github.com/jaredly/hexo-admin)
Admin UI untuk blog Hexo. Berdasarkan antarmuka Ghost, dengan inspirasi dari svbtle dan prose.io.
## Instal plugin [hexo-admin](https://github.com/jaredly/hexo-admin)
### 1. Atur hexo dan buat blog
``` bash
$ npm install -g hexo-cli
$ cd ~/
$ hexo init my-blog
$ cd my-blog
$ npm install
$ hexo server -d
```
setelah melakukan perintah diatas kita sudah bisa membuka hexo yang telah terinstal di localhsot kita ,berikut adalah output dari kode diatas apabila sukses membuat hexo dan juga tampilan hompage dari hexo tersebut.
![output init](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/output_init.PNG)

![dashboard](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/dashboard.PNG)

### 2. Instal plugin [hexo-admin](https://github.com/jaredly/hexo-admin)
``` bash
$ npm install --save hexo-admin
$ hexo server -d
$ open http://localhost:4000/admin/
```
setelah melakukan install , akan terbuat page admin secara otomatis , berikut adalah output dari install dan page admin. Walaupun ada error pada saat menginstal tapi program hexo ini tetap berjalan dengan lancar.
![output admin](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/output_admin.PNG)
![admin dashboard](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/admin.PNG)

## Menambahkan dan mengganti tema
### 1. Masuk ke directory projectname anda
``` bash
$ cd my-blog
$ cd themes
```
Seltelah masuk ke folder themes kita clone tema yang di inginkan.
### 2. Clone tema yang diinginkan
Kita gunakan tema clover sebagai contoh
``` bash
$ git clone https://github.com/esappear/hexo-theme-clover.git
```
![clone tema](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/git_clone_tema.PNG)
### 3. Set tema pada *_config.yml* pada root projek
Ubah pada bagian `theme` ganti dengan nama folder tema yang kita clone agar langsung berubah.
``` 
theme : clover
```
![texedit theme](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/textedit_theme.PNG)
### 4. Tambah *hexo-renderer-sass*
``` bash
$ npm install hexo-renderer-sass --save
```
![output sass](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/sass.PNG)
![tema](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/tema_new.PNG)
# Maintenance
## Menambahkan password
Jika Anda menggunakan plugin [hexo-admin](https://github.com/jaredly/hexo-admin) di live server Anda, Anda perlu perlindungan kata sandi. Untuk mengaktifkannya, Anda cukup menambahkan beberapa variabel konfigurasi ke hexo `_config.yml` Anda:
``` bash
admin:
  username: myfavoritename
  password_hash: be121740bf988b2225a313fa1f107ca1
  secret: a secret something
```
![admin](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/admin_kucingku.PNG)
Password_hash adalah sebuah bcrypt hash dari kata sandi Anda. Secret digunakan untuk membuat cookie aman, lebih baik jika dibuat panjang dan rumit.

Sebuah utility di Pengaturan admin Hexo dapat melakukan hash pada kata sandi Anda dan membuat `admin` section untuk Anda. Mulai Hexo dan pergi ke `Settings > Setup authentification` dan isi informasi Anda. Salin YAML yang dihasilkan ke `_config.yml` Anda.

[![Password](http://searlas.top/images/pasted-0.png)](https://github.com/DartedMonki)

Setelah itu, mulai server hexo Anda dan pergi ke `/admin/`, Anda akan diminta untuk memasukkan kata sandi.
![admin dashboard](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/admin_login.PNG)
## Melakukan kustomisasi post metadata
Untuk menambah dan mengedit post metadata Anda dengan antarmuka admin, tambahkan variabel metadata dan variabel khusus Anda ke hexo `_config.yml` Anda:
``` bash
metadata:
  author_id: defaultAuthorId
  language:
```
![meta](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/metadata.PNG)
Anda dapat memberikan nilai default yang akan digunakan untuk menginisialisasi metadata dari postingan baru. Nilai dapat berupa primitif atau array.

# Cara Pemakaian
## Membuat Blog
Setelah melakukan instalasi hexo, buatlah blog dengan menggunakan Hexo CLI Tool :
``` bash
hexo init <tempat penyimpanan> && $_
```
Lalu tentukan folder tempat meletakkan semua file dari blog tersebut.

Setelah selesai melakukan setup, maka kita telah siap untuk menuliskan artikel pertama. 
## Membuat artikel baru
Untuk membuat artikel baru, maka ketikkan command: 
``` bash
hexo new post "name of the post"
``` 
![2nd post](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/2nd_post.PNG)
![2nd postpic](https://github.com/DartedMonki/Hexo/blob/master/Screenshoot/2nd_post_dashboard.PNG)
Lokasi dari file tersebut akan berada di `source/_posts`

## Membuat artikel baru dengan [hexo-admin](https://github.com/jaredly/hexo-admin)
### 1. Pilih tab post
Akan terlihat semua post yang telah dibuat
[![TabPost](https://raw.githubusercontent.com/jaredly/hexo-admin/master/docs/pasted-0.png)](https://github.com/DartedMonki)
## 2. Pilih new post
Ketik isi post baru yang nantinya akan di preview secara real time di editor
[![NewPost](https://raw.githubusercontent.com/jaredly/hexo-admin/master/docs/pasted-1.png)](https://github.com/DartedMonki)

# Pembahasan
Hexo merupakan sebuah blog framework yang cepat, sederhana, dan kuat yang didukung oleh [Node.js](https://nodejs.org). Anda menulis posting dalam Markdown (atau bahasa lain) dan Hexo menghasilkan file statis dengan tema yang indah dalam hitungan detik.

## Kelebihan dan Kekurangan Hexo
### Kelebihan
Berikut merupakan kelebihan dari hexo :
1. Tidak harus bolak-balik upload via FTP jika ingin mengupdate artikel baru
2. Lain halnya dengan Hexo, aplikasi SSG yang dibuat menggunakan nodejs ini memiliki plugin yang bisa deploy website dengan banyak cara salah satunya dengan FTP
3. Dapat dengan cepat create & deploy blog pribadi ke dalam Github Pages
4. Memiliki banyak plugin yang dapat menunjang pembuatan blog
5. Selain hanya membutuhkan resource yang kecil, website statis yang digenerate via tool seperti Hexo menghasilkan output yang kecil, apalagi gambarnya dihosting menggunakan Image Hosting seperti Blogger, Google Photos dan CDN Hosting lainnya
6. Dukungan theme yang banyak

### Kekurangan
Disamping kelebihan, pastinya aplikasi ini memiliki kekurangan antara lain :
1. Kontennya statis, tidak berubah-ubah
2. Terbatas dalam interaksi dengan pengunjung
3. Tidak menggunakan database
4. Tidak menggunakan pemrograman PHP di server
5. Hexo memiliki komunitas yang relatif besar tetapi mayoritas adalah penutur non-Inggris (dari Cina)

## Perbedaan aplikasi Hexo dan aplikasi sejenisnya
Aplikasi sejenis yang juga menggunakan SSG (Static Site Generator) yaitu Jekyll. Sejauh ini Jekyll adalah generator statis yang paling populer karena dibangun dan didukung oleh GitHub dan digunakan untuk layanan populer Halaman GitHub yang digunakan secara gratis untuk meng-host halaman statis untuk situs web pribadi atau proyek. Jekyll memiliki komunitas terbesar di antara generator statis lainnya yang telah menyediakan banyak tutorial, tema open source, dan plugin. Ini dipandang sebagai penantang WordPress di dunia statis dan banyak blogger telah memigrasikan blog mereka dari WordPress ke Jekyll. Di StackOverflow, Jekyll memiliki lebih banyak pertanyaan terkait daripada Hexo.

### Kelebihan dan kekurangan Jekyll
#### Kelebihan
Kelebihan dari Jekyll :
1. Gratis dan open source
2. Anda dapat membangun tema sebagai gems dan mendistribusikannya melalui RubyGems
3. Mudah dan sederhana untuk digunakan
4. Anda dapat dengan mudah melakukan migrasi konten Anda dari platform populer (mis. WordPress) berkat importir Jekyll
5. dukungan Github Pages yang luar biasa
6. Hadir dengan tema minimal default dan layak di luar kotak
#### Kekurangan
Jekyll juga memiliki beberapa kekurangan seperti:
1. Saat konten situs web Anda tumbuh, proses pembuatannya menjadi jauh lebih lambat (ini adalah kelemahan utama Jekyll)
2. Incremental build yang masih dalam percobaan
3. Tidak ada built-in post pagination pada Jekyll 3
4. Tidak mendukung penggunaan variabel dalam judul atau YAML
5. Banyak plugin yang outdated
6. Dependensi gem dapat menyebabkan ketidaksesuaian/incompatible
7. Github Pages mendukung Jekyll tetapi hanya satu set Github-safe-plugin yang dapat digunakan
8. Tidak ada built-in support untuk livereload

Ada lebih sedikit tutorial untuk Hexo dibandingkan dengan Jekyll tetapi dokumentasinya jelas, mudah diikuti dan lebih straightforward serta Hexo berbasis NodeJs yang mudah untuk diinstal. Pada hexo terdapat kumpulan tema yang dapat memanjakan mata serta mudah dalam mendeploynya ke GitHub Pages.

Menggunakan Hexo (atau statis website lainnya) memberikan keuntungan dalam hal SEO karena dengan menggunakan website statis, kita bisa memanfaatkan hosting gratis yang space kecil (antara 5mb-10mb). Website statis yang dihasilkan oleh Hugo dan Hexo juga bisa digunakan pada server yang tidak mendukung PHP server seperti Apache, Nginx, Litespeed, dll. 


# Referensi
https://www.techiediaries.com/jekyll-hugo-hexo/

https://kaqfa.github.io/2016/12/kenapa-saya-memilih-hexo/

# Team
| <a href="https://github.com/DartedMonki" target="_blank">**Afriyadi YR**</a> | <a href="https://github.com/reyhannuurakbar" target="_blank">**Reyhan NA**</a> | <a href="https://github.com/g64160084" target="_blank">**Feterachman BY**</a> | <a href="https://github.com/MarsaMD" target="_blank">**Marsa MD**</a> |
|:---:|:---:|:---:|:---:|
| [![DartedMonki](https://avatars1.githubusercontent.com/u/12370632?s=200&v=4)](https://github.com/DartedMonki)    | [![reyhannuurakbar](https://avatars0.githubusercontent.com/u/29391870?s=200&v=4)](https://github.com/reyhannuurakbar) | [![g64160084](https://0.academia-photos.com/40101472/10977819/12251331/s200_feterachman.berlian_yahya.jpg_oh_14800c1f6d96e6ef3d396437414cb62c_oe_56e1af29)](https://github.com/g64160084)  | [![MarsaMD](https://avatars3.githubusercontent.com/u/29392189?s=200&v=4)](https://github.com/MarsaMD)  |
| <a href="https://github.com/DartedMonki" target="_blank">`github.com/DartedMonki`</a> | <a href="https://github.com/reyhannuurakbar" target="_blank">`github.com/reyhannuurakbar`</a> | <a href="https://github.com/g64160084" target="_blank">`github.com/g64160084`</a> | <a href="https://github.com/MarsaMD" target="_blank">`github.com/MarsaMD`</a> |
| <a href="https://github.com/DartedMonki" target="_blank">`G64160012`</a> | <a href="https://github.com/reyhannuurakbar" target="_blank">`G64160115`</a> | <a href="https://github.com/g64160084" target="_blank">`G64160084`</a> | <a href="https://github.com/MarsaMD" target="_blank">`G64160040`</a> |
