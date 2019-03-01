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

Jika belum, ikuti petunjuk berikut untuk menginstal semua persyaratan.

## Untuk pengguna Mac
Anda mungkin mengalami beberapa masalah saat kompilasi. Silakan instal Xcode dari App Store terlebih dahulu. Setelah Xcode diinstal, buka Xcode dan buka **Preferences -> Download -> Command Line Tools -> Install** untuk menginstal command line tools.

## Instal Git
- Windows: Unduh & instal git.
- Mac: Instal dengan Homebrew, MacPorts atau installer.
- Linux (Ubuntu, Debian): 
``` bash
$ sudo apt-get install git-core
```
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
Wget:
``` bash
$ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```
Setelah nvm diinstal, restart terminal dan jalankan perintah berikut untuk menginstal Node.js:
``` bash
$ nvm install stable
```

Atau, unduh dan jalankan installer Node.Js.
## Instal Hexo
Setelah semua persyaratan diinstal, Anda dapat menginstal Hexo dengan npm:

``` bash
$ npm install -g hexo-cli 
```
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
```
### 2. Instal plugin [hexo-admin](https://github.com/jaredly/hexo-admin)
``` bash
$ npm install --save hexo-admin
$ hexo server -d
$ open http://localhost:4000/admin/
```
## Menambahkan dan mengganti tema


# Maintenance
## Menambahkan password
Jika Anda menggunakan plugin [hexo-admin](https://github.com/jaredly/hexo-admin) di live server Anda, Anda perlu perlindungan kata sandi. Untuk mengaktifkannya, Anda cukup menambahkan beberapa variabel konfigurasi ke hexo `_config.yml` Anda:
``` bash
admin:
  username: myfavoritename
  password_hash: be121740bf988b2225a313fa1f107ca1
  secret: a secret something
```
Password_hash adalah sebuah bcrypt hash dari kata sandi Anda. Secret digunakan untuk membuat cookie aman, lebih baik jika dibuat panjang dan rumit.

Sebuah utility di Pengaturan admin Hexo dapat melakukan hash pada kata sandi Anda dan membuat `admin` section untuk Anda. Mulai Hexo dan pergi ke `Settings > Setup authentification` dan isi informasi Anda. Salin YAML yang dihasilkan ke `_config.yml` Anda.

Setelah itu, mulai server hexo Anda dan pergi ke `/admin/`, Anda akan diminta untuk memasukkan kata sandi.

## Melakukan kustomisasi post metadata
Untuk menambah dan mengedit post metadata Anda dengan antarmuka admin, tambahkan variabel metadata dan variabel khusus Anda ke hexo `_config.yml` Anda:
``` bash
metadata:
  author_id: defaultAuthorId
  language:
```
Anda dapat memberikan nilai default yang akan digunakan untuk menginisialisasi metadata dari postingan baru. Nilai dapat berupa primitif atau array.

# Cara Pemakaian
Setelah melakukan instalasi hexo, buatlah blog dengan menggunakan Hexo CLI Tool :
``` bash
hexo init <tempat penyimpanan> && $_
```
Lalu tentukan folder tempat meletakkan semua file dari blog tersebut.

Setelah selesai melakukan setup, maka kita telah siap untuk menuliskan artikel pertama. 

Untuk membuat artikel baru, maka ketikkan command: 
``` bash
hexo new post "name of the post"
``` 
Lokasi dari file tersebut akan berada di `source/_posts`

# Pembahasan

# Referensi

# Team
| <a href="https://github.com/DartedMonki" target="_blank">**Afriyadi YR**</a> | <a href="https://github.com/reyhannuurakbar" target="_blank">**Reyhan NA**</a> | <a href="https://github.com/g64160084" target="_blank">**Feterachman BY**</a> | <a href="https://github.com/MarsaMD" target="_blank">**Marsa MD**</a> |
|:---:|:---:|:---:|:---:|
| [![DartedMonki](https://avatars1.githubusercontent.com/u/12370632?s=200&v=4)](https://github.com/DartedMonki)    | [![reyhannuurakbar](https://avatars0.githubusercontent.com/u/29391870?s=200&v=4)](https://github.com/reyhannuurakbar) | [![g64160084](https://0.academia-photos.com/40101472/10977819/12251331/s200_feterachman.berlian_yahya.jpg_oh_14800c1f6d96e6ef3d396437414cb62c_oe_56e1af29)](https://github.com/g64160084)  | [![MarsaMD](https://avatars3.githubusercontent.com/u/29392189?s=200&v=4)](https://github.com/MarsaMD)  |
| <a href="https://github.com/DartedMonki" target="_blank">`github.com/DartedMonki`</a> | <a href="https://github.com/reyhannuurakbar" target="_blank">`github.com/reyhannuurakbar`</a> | <a href="https://github.com/g64160084" target="_blank">`github.com/g64160084`</a> | <a href="https://github.com/MarsaMD" target="_blank">`github.com/MarsaMD`</a> |
| <a href="https://github.com/DartedMonki" target="_blank">`G64160012`</a> | <a href="https://github.com/reyhannuurakbar" target="_blank">`G64160115`</a> | <a href="https://github.com/g64160084" target="_blank">`G64160084`</a> | <a href="https://github.com/MarsaMD" target="_blank">`G64160040`</a> |
