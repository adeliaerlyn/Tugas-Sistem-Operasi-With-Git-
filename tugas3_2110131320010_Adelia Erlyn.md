<h1 align="center"><b>Tugas 3 Sistem Operasi</b></h1>

Nama | Nim | Mata Kuliah | Dosen Pengampu
---|---|---|---
Adelia Erlyn N.C.P. | 2110131320010 | Sistem Operasi | Dr. Harja Santanapurba, M.Kom / Novan Alkaf B. S. S.Kom., M.T

<hr>

_**Deskripsi Tugas**_ <br>

<hr><br>

```
1. Pelajari topik Komponen Sistem Operasi, Layanan Sistem Operasi  dan Sistem Call
2. Berikan minimal 3 contoh untuk  setiap (1) komponen sistem operasi, (2) layanan sistem operasi serta (3) system call yang ada pada komputer kalian.
3. Contoh berupa screenshot yang ada di Sistem Operasi Kalian. Kemudian berikan penjelasan.
4. Contohnya ada manajemen file berkas, maka contohnya adalah cara membuat folder. Buatlah tutorial membuat folder disertai screenshot di laptop kalian. 
5. Screenshot contoh ini bisa menggunakan OS Windows atau OS Linux.
```

<br><hr>

<u>_**Penyelesaian Tugas**_ </u><br>
<hr><br>

## **1. Komponen Sistem Operasi**

<br>

### _Manajemen Memori Utama (Windows Task Manager)_ 

<br>

<p align="center"><img src="img/TUGAS3_F1.png" width="500px"></p>
<br>

<p align="justify">Pada task manager berguna untuk memantau proses aplikasi yang berjalan serta penggunaan memory pada setiap proses. Task manager dapat diakses dengan :</p>

<b>ctrl + alt + del</b> 

atau klik kanan pada task bar lalu pilih task manager.

<br>

### _Manajemen berkas (File Explorer Windows)_

<br>

<p align="justify">File manager berguna untuk mengelola, menghapus, membuat, atau menggandakan file yang ada di dalam sistem operasi.</p>

<br>

<p align="center"><img src="img/TUGAS3_F2.png" width="500px"></p><br>

<p align="center"><img src="img/TUGAS3_F3.png" width="700px"></p>
<br>

<p align="justify">Manajemen berkas pada windows dapat dengan mudah diakses dengan :

<b>klik kanan, pilih new, kemudian klik icon folder</b>.</p> 

<br>

### _Command Interpreter system (Command Promt /CMD windows)_

<br>

<p align="center"><img src="img/TUGAS3_F5.png" width="500px"></p><br>

<p align="center"><img src="img/TUGAS3_F4.png" width="500px"></p>
<br>

<p align="justify">Command Prompt atau lebih dikenal dengan CMD adalah salah satu aplikasi command line interpreter (CLI) yang ada di sistem operasi Windows. Perintah CMD berfungsi untuk memberikan berbagai perintah kepada komputer tanpa perlu menavigasi program berbasis GUI seperti File Explorer, Control Panel, dan sebagainya. 

Command Prompt dapat diakses dengan :

<b>Buka pencarian, ketikan cmd, kemudian klik Command Prompt Open.</b></p>

<br>

## **2. Layanan Sistem Operasi**

<br>

### _Layanan Manipulasi Berkas (File Explorer Windows)_

<br>

<p align="center"><img src="img/TUGAS3_F8.png" width="700px"></p>
<br>

<p align="justify">Layanan ini berguna untuk memberikan akses kepada user untuk memanipulasi berkas yang ada di dalam computer mereka. User dapat membuat folder atau berkas baru di dalam media penyimpanan. Peran file manager dalam sIstem operasi sangat vital, terutama untuk pengelolaan dan penyimpanan file system operasi itu sendiri maupun hasil Input/output proses.</p> 

Membuat folder dapat diakses dengan :

<b>klik kanan, pilih new, kemudian klik icon folder, ketikan nama folder yang ingin dibuat.</b>

<br>

<p align="center"><img src="img/TUGAS3_F14.png" width="700px"></p>
<br>

User dapat memasukan file di dalam folder yang sudah dibuat

<br>

<p align="center"><img src="img/TUGAS3_F13.png" width="700px"></p>
<br>

Menghapus folder dapat diakses dengan :

<b>klik kanan, klik emoji sampah</b> atau <b>klik Show more options, dan klik delete</b>

<br>

### _Layanan Deteksi Error (Task Manager & CMD windows)_

<br>

<p align="center"><img src="img/TUGAS3_F6.jpeg" width="500px"></p><br>

<p align="center"><img src="img/TUGAS3_F7.png" width="500px"></p>
<br>

<p align="justify">Layanan ini berfungsi untuk mendeteksi terjadinya error dan tindakan apa yang perlu dilakukan oleh system operasi maupun user. Deteksi ini akan aktif apabila ada salah satu bagian dari file system operasi atau layanan system operasi mengalami kerusakan, failure, atau berhenti beroperasi. Ketika deteksi aktif maka akan muncul notifikasi untuk pengguna dan tindakan apa yang harus dilakukan.</p>

Cara mengakses taks manager :

<b>ctrl + alt + del</b> kemudian <b>pilih Services</b>
<br>

<p align="center"><img src="img/TUGAS3_F12.png" width="500px"></p>
<br>

<br>

### _Layanan Proteksi (Account Manager windows dan Windows Security)_

<br>

<p align="center"><img src="img/TUGAS3_F9.png" width="650px"></p><br>

<p align="center"><img src="img/TUGAS3_F10.png" width="650px"></p>
<br>

<p align="justify">Layanan ini berfungsi untuk meberikan proteksi kepada pengguna dari serangan luar yang berasal dari luar kuasa pengguna. Seperti akses illegal, ransomware, virus, dan lai-lain. Account Manager pada windows berfungsi untuk mengatur siapa saja yang dapat masuk dan menggunakan computer dan membatasi apa saja yang dapat dilakukan oleh pengguna tersebut. Sedangkan windows security berfungsi untuk melindungi system operasi dari serangan ransomware, virus, serta thread-thread berbahaya lainnya.</p>

<p align="justify">Cara mengaksesnya</p>

<b>Buka Settings, kemudian cari dan klik Privacy & Security</b>

<br>

## **Sistem Call**

<br>

<p align="justify">Menurut artikel yang diunggah oleh : guptayp, Sytem Call digunakan untuk melakukan suatu proses yang dikehendaki user. Oleh karena itu harus ada suatu bentuk komunikasi antara user dan hardware. Komunikasi itu terjadi dalam bentuk system calls. SO melalui shell-nya akan menangkap perintah dari user yang kemudian akan dikomunikasikan melalui system calls. Disinilah peran SO sebagai jembatan komunikasi antara user dan hardware itu terjadi. System calls itu sendiri umumnya ditulis dalam bahasa C dan C++. Type system call :</p>

- Manajemen Proses
- Manajemen Berkas
- Manajemen Kiranti
- System Call Informasi/Pemeliharaan
- Komunikasi

<br>

### _Manajemen Berkas (Pembuatan File pada Command Prompt)_

<br>

<p align="center"><img src="img/TUGAS3_F11.png" width="700px"></p>

<br> 

<p align="justify">Cara mengakses dan membuat folder baru menggunakan command prompt yaitu :</p>
<b>User membuka Command Prompt, ketik mkdir (Nama Folder yang akan Dibuat)</b><i> Contohnya : mkdir FOLDER_SO</i>. <b>Enter, kemudian ketik 'dir'.</b>


Maka folder sudah selesai dibuat.
