#latihan1: Penggunaan GIT
langkah pertama adalah instalasi

Nama : Febriyani Nurhida

Nim : 312210222

Kelas : TI 22.A2

### PENGGUNAAN GIT 


### APA ITU GIT ?
* Git adalah salah satu sistem pengontrol versi (Version ControlSystem) pada proyek perangkat lunak yang diciptakan oleh Linux Torvalds.
* Pengontrol versi bertugas mencatat setiap perubahan pada fileproyek yang dikerjakan oleh banyak orang maupun sendiri.
* Git dikenal juga dengan distributed revision control (VCS terdistribusi),artinya penyimpanan database Git tidak hanya berada dalam satutempat saja.


### INSTALASI GIT
* Download **Git**, buka website resminya Git `(git-scm.com)`.
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
![gambar1](ss/ss1.png)
* setelah selesai mengunduh file git, install Git
![gambar2](ss/ss2.png)

* lalu klik next terus seperti gambar di bawah
![gambar3](ss/ss3.png)
![gambar4](ss/ss4.png)
![gambar5](ss/ss5.png)
![gambar6](ss/ss6.png)
![gambar7](ss/ss7.png)
![gambar8](ss/ss8.png)
![gambar9](ss/ss9.png)
![gambar10](ss/ss10.png)
![gambar11](ss/ss11.png)
![gambar12](ss/ss12.png)
![gambar13](ss/ss13.png)
![gambar14](ss/ss14.png)
![gambar15](ss/ss15.png)
![gambar16](ss/ss16.png)
* tunggu proses instalasi hingga selesai
![gambar17](ss/ss17.png)

* Selamat, Git sudah terinstal di Windows
![gambar18](ss/ss18.png)

### Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi ``user.name dan user.email``
* konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository.

* apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah `git commit`

* Config Global Repository

`$ git config --global user.name “nama_user"`

`$ git config --global user.email “nama_user”`
![gambar23](ss/ss23.png)

### Perintah Dasar Git

* `git init`, perintah untuk membuat repository local
* `git add`, perintah untuk menambahkan file baru, atau perubahan pada file pada staging sebelum proses commit.
* `git commit`, perintah untuk menyimpan perubahan kedalam database git.
* `git push -u origin master`, perintah untuk mengirim perubahan pada repository local menuju server repository.
* `git clone [url]`, perintah untuk membuat working directory yang diambil dari repositry sever.
* `git remote add origin [url]`, perintah untuk menambahkan remote server/reopsitory server pada local repositry ``(working directory)``
* `git pull`, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository


### Membuat Reposiory Local

* Buka direktory aktif, misal: **d:\labs_pemrograman1** (buka menggunakan Windows Explorer)
* klik kanan pada direktory aktif tersebut, dan pilih menu **Git Bash**, sehingga muncul git bash commad
* Buat direktory project praktikum pertama dengan nama **latihan1**
``$ mkdir latihan1
$ cd latihan1``
* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah **cd** ``(change directory)``
* direktory aktif menjadi: **d:\labs_pemrograman1\latihan1

![gambar24](ss/ss24.png)

### Membuat Reposiory Local

* Jalankan perintah **git init**, untuk membuat repository local.
`$ git init`
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .**git**
* Pada direktori tersebut, semua perubahan pada `working directory` akan disimpan.
![gambar25](ss/ss25.png)

### Menambahkan File baru pada repository

* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
* disini kita akan coba buat satu file bernama README.md (text file)
`$ echo “# Latihan 1” >> README.md`
* File **README.md** berhasil dibuat.
![gambar25](ss/ss25.png)


### Menambahkan File baru pada repository

* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
`$ git add README.md`
* File **README.md** berhasil ditambahkan.
![gambar26](ss/ss26.png)

### `Commit` (Menyimpan perubahan ke database)

* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah git commit -m “komentar commit”
`$ git commit -m “File pertama saya”`
* Perubahan berhasil disimpan.

![gambar27](ss/ss27.png)
* Server reopsitory yang akan kita gunakan adalah (http://github.com)
![gambar19](ss/ss19.png)
* Anda harus membuat akun terlebih dahulu.
* Pada laman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository
![gambar21](ss/ss21.png)


### Membuat repository server

* Isi nama repositorynya, misal: labpy1.
* lalu klik tombol Create repository
![gambar22](ss/ss22.png)

### Menambahkan Remote Repository

* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
* Untuk menambahkan remote repository server, gunakan perintah **git remote add origin [url]**
`$ git remote add origin https://github.com/rizkyy/Latihan-git.git`


### Push (Mengirim perubahan ke server)

* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
`$ git push -u origin master`
* Perintah ini akan meminta memasukkan username dan password pada akun github.com

![gambar28](ss/ss28.png)
* Buka laman github.com, arahkan pada repositorinya.
* Maka perubahan akan terlihat pada laman tersebut.

![gambar31](ss/ss31.png)



### Clone Repository

* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
* Untuk melakukan cloning, gunakan perintah `git clone [url]`

![8](https://user-images.githubusercontent.com/73010098/96368959-31452300-1181-11eb-983c-f38ec11f48d5.png)
### Kegunaan file README.md

* Apabila kita menggunakan github, untuk memberikan penjelasan awal pada project yang kita buat, maka dapat menggunakan sebuah file yang bernama README.md
* Pada file tersebut kita dapat membuat dokumentasi awal dari setiap project yang kita buat untuk memberikan penjelasan atau sekedar cara penggunaan dari aplikasi yang kita kembangkan.
* Penulisan file README.md berbasis teks, dan untuk pemformatannya menggunakan Markdown format.
* untuk lebih jelasnya, dapat anda pelajari cara penggunaan markdown pada url berikut: https://guides.github.com/features/mastering-markdown/



### Author : Febriyani Nurhida