<h1 align="center"><b>Tugas 4 Sistem Operasi</b></h1>

Nama | Nim | Mata Kuliah | Dosen Pengampu
---|---|---|---
Adelia Erlyn N.C.P. | 2110131320010 | Sistem Operasi | Dr. Harja Santanapurba, M.Kom / Novan Alkaf B. S. S.Kom., M.T

<hr>

<h1 align="center"><b>Struktur Sistem Operasi</b></h1>
<hr>

<h3 align="center"><b>Pendahuluan</b></h3>

<br>

<p align="justify">Sebuah sistem yang besar dan kompleks seperti sistem operasi modern harus diatur dengan cara membagi task kedalam komponen-komponen kecil agar dapat berfungsi dengan baik dan mudah dimodifikasi. Pada bab ini, kita akan membahas cara komponen-komponen ini dihubungkan satu sama lain. Menurut Silberschatz dan kawan-kawan, ada tiga cara yaitu:</p>

- Struktur Sederhana.
- Pendekatan Berlapis.
- Kernel Mikro.

<p align="justify">Sedangkan menurut Stallings, kita bisa memandang sistem sebagai seperangkat lapisan. Tiap lapisan menampilkan bagian fungsi yang dibutuhkan oleh sistem operasi. Bagian yang terletak pada lapisan yang lebih rendah akan menmpilkan fungsi yang lebih primitif dan menyimpan detail fungsi tersebut.</p>

<br>

<h3 align="center"><b>Struktur Sederhana</b></h3>

<br>

<p align="justify">Banyak sistem yang tidak terstruktur dengan baik, sehingga sistem operasi seperti ini dimulai dengan sistem yang lebih kecil, sederhana, dan terbatas. Kemudian berkembang dengan cakupan yang original. Contoh sistem seperti ini adalah MS-DOS, yang disusun untuk mendukung fungsi yang banyak pada ruang yang sedikit karena keterbatasan perangkat keras untuk menjalankannya. Contoh sistem lainnya adalah UNIX, yang terdiri dari dua bagian yang terpisah, yaitu kernel dan program sistem. Kernel selanjutnya dibagi dua bagian, yaitu antarmuka dan device drivers. Kernel mendukung sistem berkas, penjadwalan CPU, manajemen memori, dan fungsi sistem operasi lainnya melalui system calls.</p>

<br>

<h3 align="center"><b>Pendekatan Berlapis</b></h3>

<br>

<p align="justify">Sistem operasi dibagi menjadi sejumlah lapisan yang masing-masing dibangun di atas lapisan yang lebih rendah. Lapisan yang lebih rendah menyediakan layanan untuk lapisan yang lebih tinggi. Lapisan yang paling bawah adalah perangkat keras, dan yang paling tinggi adalah <i>user-interface</i>.</p>

<p align="justify">Sebuah lapisan adalah implementasi dari obyek abstrak yang merupakan enkapsulasi dari data dan operasi yang bisa memanipulasi data tersebut. Keuntungan utama dengan sistem ini adalah modularitas. Pendekatan ini mempermudah <i>debug</i> dan verifikasi sistem. Lapisan pertama bisa di debug tanpa mengganggu sistem yang lain karena hanya menggunakan perangkat keras dasar untuk implementasi fungsinya. Bila terjadi error saat <i>debugging</i> sejumlah lapisan, error pasti pada lapisan yang baru saja di <i>debug</i>, karena lapisan dibawahnya sudah di <i>debug</i>.</p>

<p align="justify">Sedangkan menurut Tanenbaum dan Woodhull, sistem terlapis terdiri dari enam lapisan, yaitu:</p>

- <p align="justify"><b>Lapisan 0</b>. Mengatur alokasi prosesor, pertukaran antar proses ketika interupsi terjadi atau waktu habis. Lapisan ini mendukung dasar multi-programming pada CPU.</p>
- <p align="justify"><b>Lapisan 1</b>. Mengalokasikan ruang untuk proses di memori utama dan pada 512 kilo word drum yang digunakan untuk menahan bagian proses ketika tidak ada ruang di memori utama.</p>
- <p align="justify"><b>Lapisan 2</b>. Menangani komunikasi antara masing-masing proses dan operator console. Pada lapis ini masing-masing proses secara efektif memiliki opertor console sendiri.</p>
- <p align="justify"><b>Lapisan 3</b>. Mengatur peranti M/K dan menampung informasi yang mengalir dari dan ke proses tersebut.</p>
- <p align="justify"><b>Lapisan 4</b>. Tempat program pengguna. Pengguna tidak perlu memikirkan tentang proses, memori, console, atau manajemen M/K.</p>
- <p align="justify"><b>Lapisan 5</b>. Merupakan operator sistem.</p>

<br>

<p align="justify">Menurut Stallings, model tingkatan sistem operasi yang mengaplikasikan prinsip ini dapat dilihat pada tabel berikut, yang terdiri dari level-level dibawah ini:</p>

- <p align="justify"><b>Lapisan 1</b>. Terdiri dari sirkuit elektronik dimana obyek yang ditangani adalah register memory cell, dan gerbang logika. Operasi pada obyek ini seperti membersihkan register atau membaca lokasi memori.</p>
- <p align="justify"><b>Lapisan 2</b>. Pada level ini adalah set instruksi pada prosesor. Operasinya adalah instruksi bahasa-mesin, seperti menambah, mengurangi, load dan store.</p>
- <p align="justify"><b>Lapisan 3</b>. Tambahan konsep prosedur atau subrutin ditambah operasi call atau return.</p>
- <p align="justify"><b>Lapisan 4</b>. Mengenalkan interupsi yang menyebabkan prosesor harus menyimpan perintah yang baru dijalankan dan memanggil rutin penanganan interupsi.</p>

<br>

<p align="justify">Empat level pertama bukan bagian sistem operasi tetapi bagian perangkat keras. Meski pun demikian beberapa elemen sistem operasi mulai tampil pada level-level ini, seperti rutin penanganan interupsi. Pada level 5, kita mulai masuk kebagian sistem operasi dan konsepnya berhubungan dengan <i>multi-programming</i>.</p>

- <p align="justify"><b>Lapisan 5</b>. Level ini mengenalkan ide proses dalam mengeksekusi program. Kebutuhan-kebutuhan dasar pada sistem operasi untuk mendukung proses ganda termasuk kemampuan men-suspend dan me-resume proses. Hal ini membutuhkan register perangkat keras untuk menyimpan agar eksekusi bisa ditukar antara satu proses ke proses lainnya.</p>
- <p align="justify"><b>Lapisan 6</b>. Mengatasi penyimpanan sekunder dari komputer. Level ini untuk menjadwalkan operasi dan menanggapi permintaan proses dalam melengkapi suatu proses.</p>
- <p align="justify"><b>Lapisan 7</b>. Membuat alamat logik untuk proses. Level ini mengatur alamat virtual ke dalam blok yang bisa dipindahkan antara memori utama dan memori tambahan. Cara-cara yang sering dipakai adalah menggunakan ukuran halaman yang tetap, menggunakan segmen sepanjang variabelnya, dan menggunakan cara keduanya. Ketika blok yang dibutuhkan tidak ada dimemori utama, alamat logis pada level ini meminta transfer dari level 6.</p>

<br>

<p align="justify">Sampai point ini, sistem operasi mengatasi sumber daya dari prosesor tunggal. Mulai level 8, sistem operasi mengatasi obyek eksternal seperti peranti bagian luar, jaringan, dan sisipan komputer kepada jaringan.</p>

- <p align="justify"><b>Lapisan 8</b>. Mengatasi komunikasi informasi dan pesan-pesan antar proses. Dimana pada level 5 disediakan mekanisme penanda yang kuno yang memungkinkan untuk sinkronisasi proses, pada level ini mengatasi pembagian informasi yang lebih banyak. Salah satu peranti yang paling sesuai adalah <i>pipe (pipa)</i> yang menerima output suatu proses dan memberi input ke proses lain.</p>
- <p align="justify"><b>Lapisan 9</b>. Mendukung penyimpanan jangka panjang yang disebut dengan berkas. Pada level ini, data dari penyimpanan sekunder ditampilkan pada tingkat abstrak, panjang variabel yang terpisah. Hal ini bertentangan tampilan yang berorientasikan perangkat keras dari penyimpanan sekunder.</p>
- <p align="justify"><b>Lapisan 10</b>. Menyediakan akses ke peranti eksternal menggunakan antarmuka standar.</p>
- <p align="justify"><b>Lapisan 11</b>. Bertanggung-jawab mempertahankan hubungan antara internal dan eksternal <i>identifier</i> dari sumber daya dan obyek sistem. Eksternal <i>identifier</i> adalah nama yang bisa dimanfaatkan oleh aplikasi atau pengguna. Internal <i>identifier</i> adalah alamat atau indikasi lain yang bisa digunakan oleh level yang lebih rendah untuk meletakkan dan mengontrol obyek.</p>
- <p align="justify"><b>Lapisan 12</b>. Menyediakan suatu fasilitator yang penuh tampilan untuk mendukung proses. Hal ini merupakan lanjutan dari yang telah disediakan pada level 5. Pada level 12, semua info yang dibutuhkan untuk manajemen proses dengan berurutan disediakan, termasuk alamat virtual di proses, daftar obyek dan proses yang berinteraksi dengan proses tersebut serta batasan interaksi tersebut, parameter yang harus dipenuhi proses saat pembentukan, dan karakteristik lain yang mungkin digunakan sistem operasi untuk mengontrol proses.</p>
- <p align="justify"><b>Lapisan 13</b>. Menyediakan antarmuka dari sistem operasi dengan pengguna yang dianggap sebagai <i>shell</i> atau dinding karena memisahkan pengguna dengan sistem operasi dan menampilkan sistem operasi dengan sederhana sebagai kumpulan servis atau pelayanan.</p>

<br>

<p align="justify">Dapat disimpulkan bahwa lapisan sistem operasi secara umum terdiri atas empat bagian, yaitu:</p>

1. <p align="justify"><b>Perangkat Keras</b>. Lebih berhubungan kepada perancang sistem. Lapisan ini mencakup lapisan 0 dan 1 menurut Tanenbaum, dan level 1 sampai dengan level 4 menurut Stallings.</p>
2. <p align="justify"><b>Sistem operasi</b>. Lebih berhubungan kepada programer. Lapisan ini mencakup lapisan 2 menurut Tanenbaum, dan level 5 sampai dengan level 7 menurut Stallings.</p>
3. <p align="justify"><b>Kelengkapan</b>. Lebih berhubungan kepada programer. Lapisan ini mencakup lapisan 3 menurut Tanenbaum, dan level 8 sampai dengan level 11 menurut Stallings.</p>
4. <p align="justify"><b>Program aplikasi</b>. Lebih berhubungan kepada pengguna aplikasi komputer. Lapisan ini mencakup lapisan 4 dan lapisan 5 menurut Tanebaum, dan level 12 dan level 13 menurut Stallings.

<br>

<p align="justify">Salah satu kesulitan besar dalam sistem terlapis disebabkan karena sebuah lapisan hanya bisa menggunakan lapisan-lapisan dibawahnya, misalnya: <i>backing-store driver</i>, normalnya di atas penjadwal CPU sedangkan pada sistem yang besar, penjadwal CPU punya informasi tentang proses yang aktif yang ada di memori. Oleh karena itu, info ini harus dimasukkan dan dikeluarkan dari memori, sehingga membutuhkan <i>backing-store</i> driver dibawah penjadwal CPU. Kesulitan lainnya adalah paling tidak efisien dibandingkan tipe lain. Ketika pengguna mengeksekusi M/K, akan mengeksekusi lapisan M/K, lapisan manajemen memori, yang memanggil lapisan penjadwal CPU.</p>

<br>

<h3 align="center"><b>Kernel-mikro</b></h3>

<br>

<p align="justify">Metode ini menyusun sistem operasi dengan mengeluarkan semua komponen yang tidak esensial dari <i>kernel</i>, dan mengimplementasikannya sebagai program sistem dan level pengguna. Hasilnya <i>kernel</i> yang lebih kecil. Pada umumnya mikrokernel mendukung proses dan menajemen memori yang minimal, sebagai tambahan utnuk fasilitas komunikasi.</p>

<p align="justify">Fungsi utama mikrokernel adalah mendukung fasilitas komunikasi antara program klien dan bermacam-macam layanan yang juga berjalan di <i>user space</i>. Komunikasi yang dilakukan secara tidak langsung, didukung oleh sistem <i>message passing</i>, dengan bertukar pesan melalui mikrokernel.</p>

<p align="justify">Salah satu keuntungan mikrokernel adalah ketika layanan baru akan ditambahkan ke <i>user space</i>, <i>kernel</i> tidak perlu dimodifikasi. Kalau pun harus, perubahan akan lebih sedikit. Hasil sistem operasinya lebih mudah untuk ditempatkan pada suatu desain perangkat keras ke desain lainnya. kernel-mikro juga mendukung keamanan reliabilitas lebih, karena kebanyakan layanan berjalan sebagai pengguna proses. Jika layanan gagal, sistem operasi lainnya tetap terjaga. Beberapa sistem operasi yang menggunakan metode ini adalah TRU64 UNIX, MacOSX, dan QNX.</p>


