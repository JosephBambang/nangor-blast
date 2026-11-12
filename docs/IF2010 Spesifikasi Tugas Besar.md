**Spesifikasi Tugas Besar
IF2010 Pemrograman Berorientasi Objek 2026**

Tim Asisten Lab Pemrograman 2023

| Versi | : **1.0** |
| --- | --- |
| Tgl. Revisi Terakhir | : - |
| Deadline | : 17 November 2026, 20.10 WIB (Milestone 1)  4 Desember 2026, 20.10 WIB (Milestone 2) |

#

#

# Daftar Revisi

1. -

# Daftar Isi

[**Daftar Revisi 2**](#_kgr7w4gbduqd)

[**Daftar Isi 3**](#_hx8m79idyn5e)

[**Overview 6**](#_b3ft2cjq8zlm)

[**Pedoman 7**](#_1hpht14jyggr)

[**Latar Belakang 9**](#_capwkk5qyjuy)

[**Spesifikasi Sistem 11**](#_c0r80oksdmj)

[Ketentuan Umum 11](#_4mb44mvt91yk)

[Ketentuan Teknis 11](#_72uaxpb7lwzh)

[**Spesifikasi Permainan 13**](#_6v9h6bmjung)

[F00 - Inisialisasi Permainan 13](#_vmmy32c8eq39)

[F00.1. Atribut 13](#_t0d3957fzyio)

[F00.2. Proses Inisialisasi 14](#_gq9anjqyhc4d)

[F00.3. Validasi Map 14](#_mvwn7rday43n)

[F00.4. Restart 14](#_2661j6ki7f8t)

[F01 - Player 15](#_iyvbzpmtxlg4)

[F01.1. Atribut 15](#_7z1vafo3xcs7)

[F01.2. Perilaku dan Aturan 16](#_22a3jjl0gso6)

[F01.2.1. Pergerakan 16](#_ife7lw9dmqho)

[F01.2.2. Nyawa 16](#_dbf1lcuxrx70)

[F01.2.3. Aksi Player 16](#_v155ggq5qkg3)

[F01.2.4. Respawn 17](#_py38r3afqh2v)

[F01.2.5. Interaksi dengan Bomb 17](#_cp0w5bz4d00g)

[F02 - Bomb 19](#_nx0w7i2eg2iu)

[F02.1. Atribut 19](#_jdd4arwtod81)

[F02.2. Jenis Bomb 19](#_r5en3v6uqycz)

[F02.2.1. Normal Bomb 19](#_8f9bczl6qndo)

[F02.2.2. Pumped Bomb 20](#_qfeacgmq546p)

[F02.2.3. Remote Bomb 20](#_mf92gbzcgkik)

[F02.3. Aturan Bomb 21](#_n5uypb2mj6ua)

[F02.3.1. Aksi Player 21](#_if7ru7lrtlec)

[F02.3.2. Aksi Pemilihan Pumped Bomb 22](#_c7d5mc6ppgfe)

[F02.3.3. Aksi Remote Detonate 22](#_bxu7rljfc82s)

[F03 - Explosion 24](#_1ncoxvdixu3l)

[F03.1. Atribut 24](#_1t25qnd3qbp6)

[F03.2. Perilaku dan Aturan 24](#_suqhj74hzvt)

[F04 - Block 26](#_q79phoe41xq5)

[F04.1. Atribut 26](#_eql3wbeikj6)

[F04.2. Jenis Block 26](#_ipw3cdm1l0dg)

[F04.2.1. Indestructible Block 26](#_l7r5vy2j57jd)

[F04.2.2. Destructible Block 26](#_h9c66k9k06lw)

[F04.2.3. Reinforced Block 27](#_ecqnk770tjcv)

[F05 - Enemy 28](#_ib0t0k4w2guc)

[F05.1. Atribut 28](#_1gp53m8b5aj4)

[F05.2. Normal Enemy 28](#_f0oaabkmbarh)

[F05.3. Boss Enemy 29](#_wf5ldv5kqald)

[F05.3.1 Aturan Umum Boss Enemy 29](#_qy1pms53ugwx)

[F05.3.2. Boss Green Garden - Draco 31](#_r2oh2cswuiuw)

[F05.3.3. Boss Blue Resort - Leviathan 32](#_grq4r53swcn8)

[F05.3.4. Boss Red Mountain - Hades 33](#_6gel89o7tl7q)

[F05.3.5. Boss White Glacier - Mantis 34](#_1fsg0wj1jkhq)

[F05.3.6. Boss Black Fortress - Cerberus dan Altair 35](#_czoebbvjbwgf)

[F06 - Power-Up 36](#_88jna9a6qzgw)

[F06.1. Atribut 36](#_3rzvicpukpi4)

[F06.2. Jenis Power-Up 37](#_5g2my5o1w03f)

[F06.3. Aturan Power-Up 37](#_6xdjl77p0m5s)

[F07 - Map 38](#_tc965mlt8lt0)

[F07.1. Ketentuan Umum Map 38](#_t8z4rcpexbyp)

[F07.2. Legenda 38](#_qmfxgtyaw0dn)

[F07.3. Map dan Mekanisme Lingkungan 39](#_z8y0rxrre24x)

[Aturan Umum Gate (Khusus Blue Resort dan Black Fortress) 39](#_2b25lwkcl0gu)

[F07.3.1. MAP TYPE A: Green Garden 40](#_nd522l30ffbh)

[F07.3.2. MAP TYPE B: Blue Resort 41](#_63kvxcz5ur2x)

[F07.3.3. MAP TYPE C: Red Mountain 42](#_y1wgbccy8n4d)

[F07.3.4. MAP TYPE D: White Glacier 43](#_bn1zsq6s0l2w)

[F07.3.5. MAP TYPE E: Black Fortress 44](#_qegh5mv2nubp)

[F08 - Score 46](#_gl5idsd36qam)

[F08.1. Aturan Score 46](#_v5ee50dsvot7)

[F09 - Game Flow 47](#_xwhl0ak4mngf)

[F09.1. Menu Utama 47](#_t8oi4ptvcwx)

[F09.1.1. Tampilan Menu 47](#_1vz2izcw21xs)

[F09.1.2 Aturan Menu 47](#_hz6iyri0894d)

[F09.2. Game State 48](#_bipzyeeexre9)

[F09.3. Game Process 49](#_w4qanh2xwqfz)

[F09.4. Game Over 50](#_1mxribr1n86u)

[F09.5. Pause 51](#_sdcx9st2mty0)

[**Bonus 52**](#_3w87ayrq2soq)

[B01 - GUI 52](#_9x94hodyjhoz)

[B02 - Bomb Kick 52](#_f3acy1nif0nl)

[B03 - Map Maker 53](#_92sjiomyedbk)

[B04 - Local Multiplayer 53](#_v47972oics8n)

[B05 - Design Pattern 54](#_6zyjbtcy99np)

[BXX - Kreativitas 54](#_1jbv3zqv5qal)

[**Ketentuan Umum 55**](#_mea1kc9ojcwe)

[A. Timeline Pengerjaan 56](#_qo1xquqcyka5)

[B. Asistensi 56](#_e7qcz0nrzomb)

[**Pengumpulan dan Deliverables 58**](#_rxm5c6p3rhj)

[A. Milestone 1 58](#_ffaa3qwyuvbp)

[B. Milestone 2 58](#_88312j4fj5jq)

[Source Code 59](#_hr0fii97xdxv)

[Buklet 59](#_1qfx7pxbx22w)

[Log Activity 60](#_yw6nnxw224po)

[**Referensi 61**](#_s1ydygfksv2q)

[**Extras 62**](#_pis51b3yhq3h)

#

# Overview

Tugas Besar ini dirancang untuk mengintegrasikan konsep Pemrograman Berorientasi Objek (OOP) ke dalam sebuah permainan berbasis CLI. Kalian akan membangun permainan **Bomberman** menggunakan bahasa pemrograman Java.

Melalui tugas besar ini, kalian diharapkan mampu menerapkan konsep OOP dalam membangun aplikasi yang modular, terstruktur, dan mudah dikembangkan. Kalian juga akan mempelajari bagaimana mengelola interaksi antarobjek, mengatur alur permainan, serta menerapkan concurrency pada aktivitas yang berjalan secara bersamaan.

# Pedoman

Berikut merupakan pedoman yang dapat Anda ikuti selama proses pengerjaan tugas besar

1. Lakukan **validasi** untuk setiap input yang akan dimasukkan.
2. Gunakan ***build automation tools*** seperti **Gradle** atau **Maven** untuk melakukan manajemen *build* dan *package*.
3. Gunakan library tambahan seperti **JLine** atau **Lanterna** untuk mendukung pembacaan input keyboard dan pengelolaan tampilan terminal secara *real-time*.
4. Apabila Anda ingin mengimplementasikan **Graphical User Interface (GUI)**, maka **rencanakan sejak awal**, tidak bisa dikerjakan mendadak di akhir. Pastikan program kalian cukup modular dari awal pengerjaan. Sebagai referensi, Anda bisa menerapkan [<u>MVC</u>](https://www.dicoding.com/blog/apa-itu-mvc-pahami-konsepnya/).
5. Dalam mengerjakan program, **lakukan asesmen untuk meninjau** bagian mana saja yang **perlu konkurensi** dan **tidak perlu konkurensi**. Tidak semua bagian perlu dikonkurensikan. Kalian cukup menerapkan konkurensi pada **aksi yang relevan**.
6. Penggunaan ***lock*** harus **dilakukan secara hati-hati**, jangan sampai menyebabkan [*<u>deadlock</u>*](https://en.wikipedia.org/wiki/Deadlock_%28computer_science%29). Apabila tidak menggunakan *synchronized* maupun *lock*, hati-hati pula terhadap [*<u>race condition</u>*](https://en.wikipedia.org/wiki/Race_condition).
7. Buat program Anda **mudah diobservasi** sejak awal. Lakukan *logging* secara terstruktur untuk bagian-bagian kode yang dianggap penting. Alih-alih hanya menggunakan println(), coba eksplorasi pustaka *logger* seperti **SLF4J**. Anda **dapat** **memberi nama *thread*** untuk memudahkan proses *debug* melalui *log* yang dihasilkan.
8. Detail terkait atribut maupun *method* yang didefinisikan dalam spesifikasi ini bersifat **rekomendasi dan tidak saklek**(**dapat Anda modifikasi**) asalkan sesuai dengan tujuan permainan.
9. **KERJAKAN SECARA TERSTRUKTUR DAN KOORDINASIKAN PEKERJAAN ANDA**. Terapkan ***Git workflow*** (misalnya gunakan skema *branching*) untuk memastikan *commit* bermasalah dapat di-*revert* dengan mudah.
10. **Uji program kalian dengan saksama dan menyeluruh sebelum demo**. Hanya karena program kalian bisa di-*compile*, bukan berarti program kalian *foolproof*. Seluruh fitur juga harus diuji bersamaan (*integration test*), sebab fitur dapat saling mempengaruhi fitur lainnya. **GUNAKAN EMPATI DAN BERSIKAP INISIATIF, jangan hanya memedulikan pekerjaan Anda saja.**

#

# Latar Belakang

**DISCLAIMER:** Cerita berikut **TIDAK BERHUBUNGAN** dengan spesifikasi Tugas Besar. Anda dapat menyelesaikan tugas besar tanpa melihat latar belakang sama sekali.

![](data:image/png;base64...)

Di Nangor Falls, kejadian aneh bukanlah sesuatu yang benar-benar baru. Namun, beberapa hari terakhir, aktivitas anomali mulai meningkat secara tidak wajar. Suara ledakan terdengar dari dalam hutan, bebatuan berpindah tempat dengan sendirinya, dan makhluk-makhluk misterius mulai bermunculan dari bawah tanah.

Paman Frod yang sedang meneliti fenomena tersebut menemukan sebuah jaringan lorong bawah tanah yang diduga menjadi sumber kemunculan para makhluk anomali. Sayangnya, jalan menuju lokasi tersebut dipenuhi penghalang dan berbagai makhluk yang tidak ramah terhadap pengunjung.

Deeper akhirnya ditugaskan untuk menyelidiki lokasi tersebut. Berbekal sebuah perangkat peledak eksperimen buatan Paman Frod, Deeper harus membuka jalan, menghancurkan penghalang, dan menetralkan setiap makhluk anomali yang ditemuinya.

**Mebel:** "Kamu yakin alat itu aman? Terakhir kali Paman Frod membuat sesuatu, kulkas kita malah bisa berbicara."

**Paman Frod:** "Secara teori, alat ini sangat aman. Hanya saja, jangan berdiri terlalu dekat ketika alatnya aktif."

**Deeper:** "Tunggu, jadi aku harus masuk ke sana sendirian?"

**Mebel:** "Tenang saja! Aku akan mengawasimu dari luar. Semoga saja."

Kini, Deeper harus menyelesaikan penyelidikan sebelum seluruh wilayah Nangor Falls dikuasai oleh makhluk anomali. Bantu Deeper menggunakan perangkatnya dengan tepat, mengalahkan seluruh musuh, dan menemukan jalan keluar dari setiap wilayah!

# Spesifikasi Sistem

## Ketentuan Umum

Anda diminta untuk membuat permainan berbasis **Command Line Interface (CLI)** bernama **Nangor Blast** menggunakan bahasa pemrograman **Java**. Tuliskan tahapan untuk melakukan kompilasi dan menjalankan program pada file README.md yang dikumpulkan bersama dengan source code. **Nangor Blast** dimainkan oleh 1 pemain yang mengendalikan Deeper untuk melakukan investigasi di berbagai lokasi di Nangor Falls. Tujuan permainan adalah mengalahkan seluruh Normal Enemy dan Boss Enemy pada map serta mencapai pintu keluar. Untuk mewujudkan tujuan tersebut, terdapat beberapa aksi yang perlu dilakukan oleh pemain yang dijelaskan pada bagian [<u>ini</u>](#_iyvbzpmtxlg4). Penjelasan mengenai aksi dapat dibaca pada bagian Actions, sedangkan gambaran besar flow permainan dapat dibaca pada bagian [<u>ini</u>](#_xwhl0ak4mngf). Setiap kelompok mendapatkan **satu tipe dasar map** yang harus dikembangkan dan dimodifikasi sesuai pembagian kelompok. Pembagian tipe map dapat dilihat pada bagian [<u>ini</u>](#_tc965mlt8lt0), sedangkan penjelasan mengenai karakteristik dan ketentuan masing-masing tipe map juga dapat dibaca pada bagian tersebut.

## Ketentuan Teknis

Berikut merupakan hal-hal yang wajib diimplementasikan pada aplikasi yang Anda buat. Perhatikan konsep-konsep OOP serta desain aplikasi kalian!

1. *Inheritance*
2. *Abstract Class / Interface*
3. *Polymorphism*
4. *Generics*
5. *Exceptions*
6. *Collections*
7. *Concurrency*

Penerapan konsep-konsep tersebut dibebaskan kepada Anda. Namun, seluruh konsep wajib diterapkan pada aplikasi yang dibuat dan dapat dijelaskan ketika asistensi maupun demo.

Anda juga harus mengimplementasikan **minimal 2 buah Design Pattern dan minimal 3 SOLID Principles** selama proses pembuatan aplikasi. Anda dapat melihat berbagai jenis Design Pattern, definisi, dan contoh implementasinya melalui [*<u>Design Patterns</u>* <u>(refactoring.guru)</u>](https://refactoring.guru/design-patterns), sedangkan SOLID Principles dapat dipelajari melalui [<u>SOLID</u> *<u>Principles</u>* <u>(geeksforgeeks)</u>](https://www.geeksforgeeks.org/system-design/solid-principle-in-programming-understand-with-real-life-examples/).

WARNING: CICIL PENGERJAAN DARI JAUH-JAUH HARI DAN KERJAKAN DENGAN KONSISTEN. JIKA MENGERJAKAN DEKAT DENGAN DEADLINE, SANGAT BERESIKO TUGAS BESAR INI TIDAK SELESAI DENGAN BAIK!

#

# Spesifikasi Permainan

## F00 - Inisialisasi Permainan

Inisialisasi permainan merupakan proses menyiapkan seluruh komponen yang diperlukan sebelum permainan dimulai. Proses ini mencakup pemuatan map, pembuatan entitas permainan, serta pengaturan kondisi awal pemain dan permainan.

### F00.1. Atribut

Sistem permainan **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| currentMap | Map | Map yang sedang dimainkan |
| player | Player | Pemain yang dikendalikan |
| enemies | Collection of Enemy | Daftar musuh pada map |
| bombs | Collection of Bomb | Daftar bomb aktif |
| explosions | Collection of Explosion | Daftar ledakan yang sedang berlangsung. |
| blocks | Collection of Block | Daftar blok pada map |
| powerUps | Collection of PowerUp | Daftar Power-Up yang tersedia |
| score | Integer | Skor awal permainan |
| timer | Integer | Waktu permainan yang tersisa |
| gameState | GameState | Kondisi permainan saat ini |

### F00.2. Proses Inisialisasi

1. Sistem memuat map yang ditentukan untuk kelompok pada [<u>F07 - Map</u>](#_tc965mlt8lt0).
2. Sistem membuat entitas berdasarkan informasi pada map.
3. Player dan Normal Enemy ditempatkan pada titik spawn masing-masing.
4. Boss Enemy ditempatkan pada area boss yang ditentukan.
5. Bomb dan Explosion dimulai dalam keadaan kosong.
6. Skor dimulai dari 0 dan timer dimulai dari 300 detik.
7. Mekanisme lingkungan map dimulai sesuai kondisi awal map.
8. Permainan memasuki state PLAYING setelah inisialisasi selesai.

### F00.3. Validasi Map

1. Map memiliki ukuran 14 × 10 tile.
2. Map memiliki tepat satu titik spawn Player, lima titik spawn Normal Enemy, satu titik spawn Boss, dan tepat satu pintu keluar.
3. Setiap titik spawn Normal Enemy menghasilkan tepat satu Normal Enemy.
4. Seluruh titik spawn harus berada pada tile yang dapat dilalui dan tidak boleh saling menempati.
5. Player memiliki jalur untuk mencapai area boss dan pintu keluar.
6. Map harus memiliki jalur yang memungkinkan pemain menyelesaikan permainan, termasuk dengan mempertimbangkan block dan mekanisme lingkungan.
7. Jika map tidak valid, sistem menampilkan pesan kesalahan dan permainan tidak dimulai.

### F00.4. Restart

1. Restart mengembalikan posisi dan kondisi seluruh entitas serta mekanisme map ke kondisi awal.
2. Nyawa, kapasitas bomb, jangkauan ledakan, skor, dan timer dikembalikan ke nilai awal.

## F01 - Player

*Player* adalah entitas yang dikendalikan oleh pemain dalam **Nangor Blast**. Pemain mengendalikan Deeper untuk menjelajahi lokasi di Nangor Falls, mengalahkan makhluk anomali, dan menemukan pintu keluar pada setiap *map*. *Player* dapat bergerak ke empat arah, memasang bom, dan mengambil *Power-Up* yang ditemukan selama permainan.

### F01.1. Atribut

*Player* **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| position | Position | Posisi *player* pada grid map |
| direction | Direction | Arah terakhir player bergerak. |
| lives | Integer | Jumlah nyawa yang tersisa |
| bombCapacity | Integer | Jumlah maksimum bom aktif yang dapat dimiliki |
| activeBombs | Integer | Jumlah bom milik player yang sedang aktif |
| blastRange | Integer | Jangkauan ledakan bom |
| speed | Double | Kecepatan pergerakan player |
| invulnerable | Boolean | Menandakan player sedang kebal terhadap kerusakan |
| remoteUnlocked | Boolean | Menandakan player telah memperoleh Remote Detonator. |

Player memulai permainan dengan 3 nyawa, kapasitas bomb 1, dan jangkauan ledakan 1 tile. Kapasitas bomb maksimum adalah 3, jangkauan ledakan maksimum adalah 5 tile, dan nyawa maksimum adalah 5.

### F01.2. Perilaku dan Aturan

### F01.2.1. Pergerakan

1. Player dapat bergerak ke atas, bawah, kiri, dan kanan menggunakan *keyboard* secara real-time.
2. Player tidak dapat melewati block, enemy, bomb aktif, Gate tertutup, atau batas map.
3. Pergerakan dilakukan sesuai kecepatan player dan tidak dapat menembus penghalang.
4. Player dapat bergerak pada tile yang dapat dilalui.
5. Pergerakan pada Ice Tile mengikuti aturan [<u>F07.3.4 White Glacier</u>](#_bn1zsq6s0l2w) .

### F01.2.2. Nyawa

1. Player kehilangan satu nyawa ketika terkena Explosion, serangan boss, kontak dengan Normal Enemy, atau hazard map.
2. Player tidak menerima damage berulang dari aktivasi yang sama meskipun tetap berada dalam area berbahaya selama serangan berlangsung.
3. Player yang sedang dalam kondisi invulnerable tidak menerima damage dari serangan atau hazard.
4. Player yang kehilangan nyawa akan respawn pada titik spawn dengan invulnerability selama 1,5 detik.
5. Player yang kehabisan nyawa menyebabkan permainan berakhir dengan kondisi LOSE.

### F01.2.3. Aksi Player

*Player* **mempunyai aspek sebagai berikut.**

| **Aktivitas** | **Keterangan** |
| --- | --- |
| Trigger | *Keyboard*, contoh W (atas), A (kiri), S (bawah), D (kanan). |
| Input | Pemain menekan tombol gerak sesuai arah yang diinginkan. |
| Proses | Player bergerak menuju tile yang dituju jika tile tersebut dapat dilalui. |
| Output | Posisi player berubah atau tetap jika gerakan terhalang. |
| Kondisi Kegagalan | Tile tujuan terhalang atau berada di luar map. |
| Durasi | Sesuai kecepatan player. |

### F01.2.4. Respawn

1. Player muncul kembali pada titik spawn setelah kehilangan nyawa selama masih memiliki nyawa tersisa.
2. Player memperoleh invulnerability selama 1,5 detik setelah respawn.
3. Jika titik spawn tidak dapat digunakan karena sedang ditempati entitas atau objek lain, sistem mencari tile kosong terdekat yang dapat dilalui untuk menempatkan kembali player.

### F01.2.5. Interaksi dengan Bomb

1. Player dapat memasang bomb pada tile tempat ia berdiri jika kapasitas bomb masih tersedia.
2. Player dapat meninggalkan tile bomb, tetapi tidak dapat memasuki kembali tile yang masih ditempati bomb aktif.
3. Bomb yang telah selesai meledak mengembalikan kapasitasnya kepada player.
4. Player dapat memilih Normal Bomb atau Pumped Bomb sesuai aturan [<u>F02 - Bomb</u>](#_79c85gow70ak).
5. Player hanya dapat menggunakan Remote Bomb setelah memperoleh Remote Detonator.

###

## F02 - Bomb

Bomb merupakan senjata utama *player* untuk menghancurkan block dan mengalahkan enemy.

### F02.1. Atribut

*Bomb* **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| position | Position | Posisi bom pada grid map |
| type | BombType | Jenis bom |
| owner | Player | Pemilik bom |
| fuseTime | Double | Waktu tersisa sebelum bom meledak |
| blastRange | Integer | Jangkauan ledakan bom |
| active | Boolean | Menandakan bom masih aktif |

### F02.2. Jenis Bomb

### F02.2.1. Normal Bomb

Normal Bomb merupakan jenis bom dasar yang dapat digunakan player sejak awal permainan.

1. Normal Bomb merupakan jenis bomb yang digunakan player ketika permainan pertama kali dimulai.
2. Normal Bomb dapat dipilih kembali kapan saja.
3. Normal Bomb meledak 3 detik setelah dipasang.
4. Jangkauan ledakannya mengikuti blastRange milik player.

### F02.2.2. Pumped Bomb

Pumped Bomb merupakan jenis bom dengan daya ledak yang lebih besar dibandingkan Normal Bomb.

1. Pumped Bomb tersedia sejak awal permainan.
2. Player dapat memilih Pumped Bomb sebelum memasangnya.
3. Pumped Bomb meledak 4,5 detik setelah dipasang.
4. Jangkauan ledakan Pumped Bomb adalah 2 tile lebih jauh daripada Normal Bomb milik player.
5. Jangkauan maksimum Pumped Bomb adalah 7 tile.
6. Pumped Bomb dapat menghancurkan Reinforced Block.
7. Pumped Bomb memberikan 2 damage kepada boss yang sedang rentan.
8. Pumped Bomb menggunakan satu kapasitas bomb selama aktif.

### F02.2.3. Remote Bomb

Remote Bomb merupakan jenis bom yang dapat diledakkan secara manual oleh player.

1. Remote Bomb hanya dapat digunakan setelah player memperoleh Remote Detonator.
2. Remote Bomb tidak meledak berdasarkan fuse time.
3. Player dapat memicu seluruh Remote Bomb aktif miliknya melalui perintah DETONATE.
4. Jangkauan ledakan Remote Bomb mengikuti blastRange milik player.
5. Remote Bomb memberikan 1 damage kepada boss yang sedang rentan.
6. Remote Bomb menggunakan satu kapasitas bomb selama aktif.

### F02.3. Aturan Bomb

1. Normal Bomb menjadi jenis bomb yang dipilih secara default ketika permainan dimulai.
2. Pemilihan jenis bomb berlaku untuk pemasangan berikutnya sampai player memilih jenis bomb lain atau permainan di-restart.
3. Sistem menampilkan jenis bomb yang sedang dipilih.
4. Pemilihan jenis bomb tidak mengubah jenis bomb yang telah dipasang sebelumnya.
5. Bomb hanya dapat ditempatkan pada tile yang dapat dilalui dan tidak ditempati bomb aktif lain.
6. Bomb yang telah dipasang tidak dapat dipindahkan, kecuali melalui bonus [<u>Bomb Kick</u>](#_f3acy1nif0nl).
7. Bomb yang terkena Explosion dari bomb lain langsung terpicu.
8. Bomb hanya menghasilkan satu Explosion dalam satu aktivasi.
9. Fuse bomb berjalan secara real-time.

### F02.3.1. Aksi Player

*Bomb* **mempunyai aspek sebagai berikut.**

| **Aktivitas** | **Keterangan** |
| --- | --- |
| Trigger | Pemain menekan suatu *key* pada *keyboard* untuk memasang bomb. |
| Input | Tombol memasang bomb, misal tombol B. |
| Proses | Player memasang jenis bomb yang sedang dipilih pada tile tempat player berdiri. |
| Output | Bomb muncul pada tile player dan kapasitas bomb berkurang satu. |
| Kondisi Kegagalan | Kapasitas bomb penuh atau tile tidak dapat ditempati bomb. |
| Durasi | Fuse Normal Bomb 3 detik dan Pumped Bomb adalah 4,5 detik; Remote Bomb menunggu perintah detonasi. |

### F02.3.2. Aksi Pemilihan Pumped Bomb

Pemilihan *Bomb* **mempunyai aspek sebagai berikut.**

| **Aktivitas** | **Keterangan** |
| --- | --- |
| Trigger | Pemain menekan suatu *key* untuk memilih Pumped Bomb. |
| Input | Tombol memilih bomb, misal tombol E. |
| Proses | Jenis bomb untuk pemasangan berikutnya berubah menjadi Pumped Bomb. |
| Output | Sistem menampilkan jenis bomb yang dipilih. |
| Durasi | Berlaku sampai jenis bomb diubah atau permainan di-restart. |

### F02.3.3. Aksi Remote Detonate

Pemilihan *Bomb* **mempunyai aspek sebagai berikut.**

| **Aktivitas** | **Keterangan** |
| --- | --- |
| Trigger | Pemain menekan suatu *key* untuk detonasi Remote Bomb. |
| Input | Tombol detonasi bomb, misal tombol Q. |
| Proses | Seluruh Remote Bomb aktif milik player dipicu untuk meledak. |
| Output | Remote Bomb menghasilkan Explosion. |
| Kondisi Kegagalan | Tidak ada Remote Bomb aktif milik player. |
| Durasi | Explosion berlangsung 0,5 detik. |

## F03 - Explosion

Explosion merupakan efek yang dihasilkan ketika bomb meledak. Explosion digunakan untuk menghancurkan blok, memberikan kerusakan kepada musuh, serta memengaruhi entitas lain yang berada dalam jangkauannya.

### F03.1. Atribut

Explosion **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| position | Position | Posisi pusat ledakan |
| blastRange | Integer | Jangkauan ledakan |
| duration | Double | Durasi ledakan berlangsung |
| owner | Player | Pemilik bomb yang menghasilkan ledakan |
| active | Boolean | Menandakan ledakan masih berlangsung |

### F03.2. Perilaku dan Aturan

1. Explosion berlangsung selama 0,5 detik dan menyebar ke atas, bawah, kiri, kanan, dan tengah.
2. Explosion berhenti ketika mengenai Indestructible Block sesuai aturan [<u>F04 - Block</u>](#_q79phoe41xq5).
3. Explosion dapat mengenai player, Normal Enemy, Boss Enemy, dan bomb aktif, kecuali Power-Up, yang berada dalam jangkauannya.
4. Player tidak kebal terhadap ledakan bomb miliknya sendiri, kecuali sedang berada dalam kondisi invulnerable.
5. Normal Enemy selalu menerima damage dari Explosion yang mengenainya, sedangkan Boss Enemy hanya menerima damage ketika rentan.
6. Rantai ledakan dapat memicu bomb lain berada dalam jangkauannya dan harus dibatasi agar permainan tidak macet.
7. Indestructible Block menghentikan penyebaran Explosion. Tile Indestructible Block tidak menjadi bagian dari area Explosion.
8. Destructible Block dapat dihancurkan ketika berada dalam jangkauan ledakan. Explosion berhenti pada Destructible Block tersebut dan tidak menyebar ke tile setelahnya.
9. Tile yang sebelumnya ditempati Destructible Block tidak menjadi bagian dari area Explosion. Setelah block hancur, tile tersebut dapat dilalui.
10. Reinforced Block menghentikan penyebaran Explosion dari seluruh jenis bomb. Namun, Reinforced Block hanya dapat dihancurkan oleh Pumped Bomb.
11. Jika Reinforced Block terkena Pumped Bomb, block akan hancur. Explosion tetap berhenti pada block tersebut dan tidak menyebar ke tile setelahnya.
12. Gate dalam kondisi CLOSED menghentikan penyebaran Explosion, sedangkan Gate dalam kondisi OPEN dapat dilewati Explosion.
13. Water Tile dan Ice Tile tidak menghalangi penyebaran Explosion.
14. Tile khusus lingkungan lainnya tidak mengubah jangkauan penyebaran Explosion kecuali ditentukan secara khusus dalam mekanisme map.

## F04 - Block

Block merupakan objek map yang menghalangi pergerakan dan penyebaran Explosion.

### F04.1. Atribut

Block **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| position | Position | Posisi block pada grid map |
| active | Boolean | Menandakan block masih berada pada map |

### F04.2. Jenis Block

### F04.2.1. Indestructible Block

Indestructible Block merupakan block yang tidak dapat dihancurkan.

1. Indestructible Block menghalangi pergerakan player dan enemy.
2. Indestructible Block menghentikan penyebaran Explosion.
3. Indestructible Block tidak dapat ditempati bomb.

### F04.2.2. Destructible Block

Destructible Block merupakan block yang dapat dihancurkan menggunakan Explosion.

1. Destructible Block menghalangi pergerakan player dan enemy selama masih berada pada map.
2. Destructible Block menghentikan penyebaran Explosion pada tilenya.
3. Destructible Block dapat menyimpan Power-Up yang muncul setelah block dihancurkan.
4. Tile Destructible Block dapat dilalui setelah block hancur.

### F04.2.3. Reinforced Block

Reinforced Block merupakan block yang hanya dapat dihancurkan menggunakan Pumped Bomb.

1. Reinforced Block hanya dapat dihancurkan menggunakan Pumped Bomb.
2. Explosion dari Normal Bomb atau Remote Bomb tidak dapat menghancurkan Reinforced Block.
3. Reinforced Block menghalangi pergerakan player dan enemy selama masih berada pada map.
4. Tile Reinforced Block dapat dilalui setelah block hancur.
5. Reinforced Block digunakan pada Green Garden.

## F05 - Enemy

Enemy merupakan makhluk anomali yang menghalangi player dalam menyelesaikan map. Enemy dapat bergerak pada map dan memberikan damage kepada player ketika terjadi kontak. Setiap map memiliki jenis Boss Enemy yang menjadi tantangan utama sebelum player dapat menyelesaikan map.

### F05.1. Atribut

Enemy **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| position | Position | Posisi enemy pada map |
| health | Integer | Jumlah health enemy |
| speed | Double | Kecepatan pergerakan enemy |
| scoreValue | Integer | Skor yang diperoleh ketika enemy dikalahkan |
| active | Boolean | Menandakan enemy masih aktif |

### F05.2. Normal Enemy

Setiap map memiliki tepat 5 Normal Enemy. Normal Enemy hanya memiliki 1 nyawa. Setiap Normal Enemy memiliki salah satu dari dua perilaku, yaitu patrol atau chase. Kalian bebas menentukan jumlah Normal Enemy untuk masing-masing perilaku, selama totalnya tetap 5.

1. Patrol Enemy selalu bergerak mengikuti jalur patrol yang telah ditentukan.
2. Chase Enemy memiliki dua kondisi, yaitu PATROL dan CHASE.
3. Chase Enemy berada dalam kondisi PATROL ketika Player berada di luar jarak deteksi.
4. Chase Enemy berpindah ke kondisi CHASE ketika Player memasuki jarak deteksi, yaitu 3 tile dari Enemy, dan bergerak mendekati Player.
5. Chase Enemy kembali ke kondisi PATROL ketika Player keluar dari jarak deteksi. Enemy bergerak kembali menuju jalur patrol yang telah ditentukan.

### F05.3. Boss Enemy

Boss Enemy merupakan musuh utama pada map yang memiliki health lebih besar dan pola serangan khusus. Boss Enemy menjadi tantangan utama yang harus dikalahkan player sebelum pintu keluar dapat digunakan.

### F05.3.1 Aturan Umum Boss Enemy

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| maxHealth | Integer | Health maksimum boss. |
| currentPhase | Integer | Fase boss saat ini. |
| direction | Direction | Arah hadap boss yang digunakan untuk menentukan arah serangan. |
| attackPattern | AttackPattern | Pola serangan boss. |
| attackCooldown | Double | Waktu tunggu sebelum serangan berikutnya. |
| vulnerable | Boolean | Menandakan boss sedang rentan terhadap damage. |

**Mekanisme Serangan Boss**

Setiap Boss Enemy menjalankan serangan melalui tahapan berikut.

1. Boss memilih satu pola serangan dari pola serangan yang tersedia pada fase saat ini.
2. Pemilihan serangan dilakukan secara acak dari pola yang dapat digunakan sesuai kondisi dan jangkauannya.
3. Serangan yang sama tidak dipilih dua kali berturut-turut apabila masih terdapat pola serangan lain yang dapat digunakan.
4. Sistem menampilkan peringatan pada tile yang akan terkena serangan selama 1 detik sebelum serangan aktif (Peringatan dapat ditampilkan menggunakan simbol, misal simbol !).
5. Arah dan target serangan ditentukan ketika Warning dimulai. Keduanya tidak berubah hingga serangan selesai.
6. Setelah waktu peringatan berakhir, serangan diaktifkan sesuai durasi yang ditentukan. Player yang berada pada area serangan ketika serangan aktif akan kehilangan 1 nyawa.
7. Setelah serangan selesai, Boss memasuki kondisi cooldown selama 5 detik.

**Aturan Umum Boss**

1. Setiap Boss menempati satu tile pada map.
2. Setiap Boss memiliki 8 health, kecuali Cerberus dan Altair yang masing-masing memiliki 4 health.
3. Boss memiliki dua fase dan memasuki fase kedua ketika health mencapai setengah dari health maksimum.
4. Boss hanya memasuki kondisi rentan selama 4 detik pertama dari cooldown setelah menyelesaikan serangan tertentu yang telah ditentukan pada deskripsi masing-masing Boss.
5. Normal Bomb dan Remote Bomb memberikan 1 damage kepada boss yang rentan, sedangkan Pumped Bomb memberikan 2 damage.
6. Boss tidak dapat melewati Indestructible Block atau batas area pertarungan.
7. Boss dapat memberikan damage sebanyak 1 nyawa kepada player melalui serangan atau kontak.
8. Serangan boss tidak merusak block jenis apapun sehingga serangan berbentuk garis lurus dan projectile akan berhenti ketika mengenai Block.
9. Boss yang dikalahkan memberikan skor sesuai [<u>F08 - Score</u>](#_gl5idsd36qam).
10. Pola serangan boss berlangsung secara real-time.

### F05.3.2. Boss Green Garden - Draco

Draco merupakan boss berbentuk naga bersayap yang menjaga kawasan reruntuhan Green Garden. Draco rentan setelah menyelesaikan Fire Breath dan Swoop.

| **Tipe** | **Area** | **Deskripsi** | **Durasi** | **Perubahan di Fase 2** |
| --- | --- | --- | --- | --- |
| Fire Breath | Garis lurus | Draco menyemburkan api ke arah player dalam satu baris atau kolom. | 1 detik | Durasi serangan menjadi 0,5 detik. |
| Bite | Tile di depan Draco | Draco menggigit tile yang berada tepat di depannya. Serangan dilakukan ketika player berada dalam jangkauan gigitan. | 0,75 detik | Jangkauan gigitan meningkat menjadi 2 tile di depan Draco. |
| Swoop | Garis lurus | Draco bergerak menuju posisi *player* ketika serangan dimulai. Serangan hanya dapat digunakan ketika Draco dan player berada pada baris atau kolom yang sama. Pergerakan berhenti ketika mencapai target atau terhalang. | 1 detik | Durasi terjangan menjadi 0,5 detik. |
| Wing Gust | Area sekitar Draco | Draco mengepakkan sayap dan menghasilkan hembusan angin yang menyerang 8 tile di sekelilingnya, termasuk tile diagonal. | 1 detik | Area serangan meningkat menjadi 24 tile di sekeliling Draco dalam radius 2 tile. |

### F05.3.3. Boss Blue Resort - Leviathan

Leviathan merupakan makhluk air berukuran besar yang menjaga kawasan perairan Blue Resort. Leviathan rentan setelah menyelesaikan Tail Splash dan Tsunami.

| **Tipe** | **Area** | **Deskripsi** | **Durasi** | **Perubahan di Fase 2** |
| --- | --- | --- | --- | --- |
| Tail Splash | Area sekitar Leviathan | Leviathan mengibaskan ekornya dan menghasilkan percikan air yang menyerang 8 tile di sekelilingnya, termasuk tile diagonal. | 1 detik | Durasi serangan menjadi 0,5 detik. |
| Angler Smash | Garis lurus | Leviathan menyerang jalur lurus sepanjang 3 tile di depan arah hadap Leviathan. | 1 detik | Jangkauan serangan meningkat menjadi 4 tile. |
| Bubble Attack | Projectile | Leviathan menembakkan gelembung air menuju posisi player yang ditentukan ketika Warning dimulai. Gelembung bergerak secara horizontal atau vertikal dan berhenti ketika mengenai Block atau mencapai target. | 0,75 detik | Leviathan menembakkan 2 gelembung menuju posisi target yang berbeda. |
| Tsunami | Garis melintang pada salah satu baris atau kolom | Leviathan menyerang seluruh tile pada satu baris atau kolom yang melewati posisi player ketika Warning dimulai. | 1,5 detik | Dua baris atau kolom arena terkena serangan. |

### F05.3.4. Boss Red Mountain - Hades

Hades merupakan mesin pertambangan yang dimodifikasi menjadi mesin tempur dan menjaga kawasan vulkanik Red Mountain. Hades rentan setelah menyelesaikan Heavy Punch dan Spin Attack.

| **Tipe** | **Area** | **Deskripsi** | **Durasi** | **Perubahan di Fase 2** |
| --- | --- | --- | --- | --- |
| Heavy Punch | Garis lurus | Hades menghantam tanah menggunakan lengan mekanisnya sepanjang 3 tile lurus di depan arah hadap Hades. | 1 detik | Area hantaman meluas hingga dua tile tambahan di samping tile paling ujung sehingga membentuk pola seperti huruf T. |
| Spin Attack | Area sekitar Hades | Hades memutar tubuh atau senjata mekanisnya sehingga menyerang 8 tile di sekelilingnya. | 1 detik | Area serangan meningkat hingga radius 2 tile dari Hades. |
| Beam Attack | Garis lurus | Hades menembakkan sinar energi sepanjang satu baris atau kolom arena yang melewati posisi player ketika Warning dimulai. | 1 detik | Hades menembakkan 2 sinar energi pada dua baris atau kolom yang berdekatan. |
| Ground Slam | Area di depan Hades | Hades menghantam tanah dan menghasilkan gelombang kejut pada area berukuran 3 × 3 tile di depannya. | 1,5 detik | Area gelombang kejut meningkat menjadi 3 × 4 tile. |

### F05.3.5. Boss White Glacier - Mantis

Mantis merupakan makhluk anomali berbentuk belalang sembah berukuran besar yang menjaga kawasan es White Glacier. Mantis rentan setelah menyelesaikan serangan Scythe Swipe atau Jump Slam.

| **Tipe** | **Area** | **Deskripsi** | **Durasi** | **Perubahan di Fase 2** |
| --- | --- | --- | --- | --- |
| Scythe Swipe | Area di depan Mantis | Mantis mengayunkan bagian tubuhnya yang menyerupai sabit untuk menyerang 3 tile di depannya secara melebar. | 1 detik | Jangkauan serangan menjadi hingga 3 × 2 di depan Mantis. |
| Jump Slam | Area target | Mantis melompat menuju tile target dan menghantam area berukuran 3 × 3 tile yang berpusat pada lokasi pendaratannya. Tile target ditentukan berdasarkan posisi player ketika serangan dimulai. | 1 detik | Area hantaman meningkat menjadi 5 × 5 tile. |
| Spiderling | Pemanggilan enemy | Mantis memanggil 3 Hatchling (*Normal Enemy*) pada tile kosong di dekatnya. Hatchling merupakan musuh tambahan yang bergerak mendekati player dan memberikan 1 damage ketika bersentuhan dengannya. | 1 detik | Jumlah Hatchling yang dipanggil meningkat menjadi 4. |
| Wall Crawl | Pergerakan boss | Mantis bergerak cepat menyusuri jalur di dekat dinding arena untuk berpindah posisi. Mantis tidak memberikan damage selama perpindahan, tetapi dapat menyerang player melalui kontak setelah mencapai tujuannya. | 1 detik | Setelah berpindah posisi, Mantis langsung melakukan Scythe Swipe ke arah player. |

### F05.3.6. Boss Black Fortress - Cerberus dan Altair

Black Fortress memiliki dua pertarungan boss yang harus dihadapi secara berurutan.

**Cerberus**

Cerberus merupakan mesin tempur yang menjaga fasilitas utama Black Fortress. Cerberus menjadi rentan setelah menyelesaikan Missile Barrage atau Laser Sweep. Setelah Cerberus dikalahkan, Altair muncul pada area pertarungan yang sama.

| **Tipe** | **Area** | **Deskripsi** | **Durasi** | **Perubahan di Fase 2** |
| --- | --- | --- | --- | --- |
| Missile Barrage | Beberapa tile target | Cerberus menargetkan 3 tile kosong yang berbeda. Salah satu tile merupakan posisi player ketika Warning dimulai, sedangkan tile lainnya dipilih secara acak. Semua misil menghantam target setelah peringatan selesai. | 1 detik | Jumlah misil meningkat menjadi 5. |
| Laser Sweep | Garis lurus | Cerberus menyerang seluruh tile pada satu baris atau kolom yang melewati posisi player ketika Warning dimulai. | 1 detik | Dua baris atau kolom yang berdekatan terkena serangan. |

**Altair**

Altair merupakan pengendali utama Black Fortress yang bertarung menggunakan mesin tempur Vega. Altair memiliki dua fase. Altair memasuki fase kedua ketika health mencapai 2. Altair menjadi rentan setelah menyelesaikan Vega Beam atau X-Beam.

| **Tipe** | **Area** | **Deskripsi** | **Durasi** | **Perubahan di Fase 2** |
| --- | --- | --- | --- | --- |
| Vega Beam | Satu baris atau kolom | Altair menembakkan sinar energi yang menyerang seluruh tile pada satu baris atau kolom yang melewati posisi player ketika Warning dimulai. | 1 detik | Serangan Vega Beam digantikan oleh X-Beam. |
| X-Beam | Satu baris dan satu kolom | Altair menembakkan dua sinar energi yang saling berpotongan membentuk tanda tambah (+). Titik perpotongan ditentukan berdasarkan posisi player ketika Warning dimulai. Setiap arah serangan berhenti ketika bertemu Block. | 1,5 detik | X-Beam menjadi serangan utama Altair pada fase kedua. |

## F06 - Power-Up

Power-Up merupakan item yang dapat ditemukan player pada map dan memberikan peningkatan kemampuan. Power-Up dapat muncul setelah Destructible Block dihancurkan atau ditempatkan pada lokasi tertentu.

### F06.1. Atribut

Power-Up **setidaknya memiliki atribut sebagai berikut.**

| **Nama Atribut** | **Tipe** | **Keterangan** |
| --- | --- | --- |
| position | Position | Posisi Power-Up pada map |
| type | PowerUpType | Jenis Power-Up |
| active | Boolean | Menandakan Power-Up masih tersedia |

### F06.2. Jenis Power-Up

| **Jenis** | **Keterangan** |
| --- | --- |
| Bomb Up | Meningkatkan bombCapacity sebanyak 1 hingga maksimum 3. |
| Fire Up | Meningkatkan blastRange sebanyak 1 hingga maksimum 5 tile. |
| Speed Up | Meningkatkan kecepatan pergerakan player sebesar 50% dari kecepatan awal dengan maksimum sebesar 100%. |
| Remote Detonator | Membuka kemampuan menggunakan Remote Bomb. |
| Heart | Menambah nyawa player sebanyak 1 hingga maksimum 5. |

### F06.3. Aturan Power-Up

1. Player memperoleh Power-Up ketika memasuki tile tempat Power-Up berada.
2. Power-Up yang telah diambil dihapus dari map.
3. Power-Up tidak dapat diambil oleh enemy.
4. Power-Up yang muncul dari Destructible Block berada pada tile yang dapat dilalui.
5. Efek Power-Up tidak hilang ketika player kehilangan nyawa.
6. Efek Power-Up berlaku hingga permainan berakhir atau di-restart.
7. Setiap Destructible Block memiliki probabilitas sebesar 30% untuk menghasilkan Power-Up ketika dihancurkan.
8. Jika Power-Up berhasil dihasilkan, sistem memilih tepat satu jenis Power-Up secara acak dari seluruh jenis Power-Up yang tersedia.
9. Setiap map menyediakan minimal satu Remote Detonator yang dijamin dapat diperoleh Player.

## F07 - Map

Map merupakan area permainan berbentuk grid yang menjadi tempat player, enemy, bomb, block, Power-Up, dan pintu keluar berada. Setiap kelompok hanya mengimplementasikan satu map yang telah ditentukan.

### F07.1. Ketentuan Umum Map

1. Setiap map memiliki ukuran 14 × 10 tile.
2. Setiap map memiliki tepat satu titik spawn player, lima titik spawn Normal Enemy, satu titik spawn boss, dan tepat satu pintu keluar.
3. Setiap map memiliki Indestructible Block dan Destructible Block.
4. Setiap map memiliki mekanisme lingkungan khusus sesuai tema kawasan.
5. Layout map mengikuti susunan yang diberikan pada spesifikasi ini.
6. Setiap kelompok hanya mengimplementasikan map yang ditentukan.
7. Map harus dapat diselesaikan dalam batas waktu permainan.

### F07.2. Legenda

| **Simbol** | **Keterangan** |
| --- | --- |
| # | Indestructible Block |
| D | Destructible Block |
| R | Reinforced Block |
| . | Walkable Space |
| P | Player |
| E | Normal Enemy |
| B | Boss |
| X | Exit |
| W | Water Tile |
| S | Switch |
| G | Gate CLOSED |
| g | Gate OPEN |
| H | Lava Tile |
| I | Ice Tile |
| L | Laser Trap |
| \* | Explosion |
| ! | Warning |
| + | Power-Up Bomb Up |
| f | Power-Up Fire Up |
| s | Power-Up Speed Up |
| r | Power-Up Remote Detonator |
| h | Power-Up Heart |

### F07.3. Map dan Mekanisme Lingkungan

### Aturan Umum Gate (Khusus Blue Resort dan Black Fortress)

1. Gate merupakan penghalang yang memiliki dua kondisi, yaitu OPEN dan CLOSED.
2. Seluruh Gate dimulai dalam kondisi CLOSED.
3. Gate dalam kondisi OPEN dapat dilewati player dan enemy serta tidak menghalangi penyebaran Explosion.
4. Gate dalam kondisi CLOSED menghalangi pergerakan player dan enemy serta menghentikan penyebaran Explosion.
5. Gate yang berubah menjadi CLOSED akan menunggu hingga tile-nya kosong sebelum benar-benar menutup.

### F07.3.1. MAP TYPE A: Green Garden

Green Garden merupakan kawasan taman dan reruntuhan kuno. Kawasan ini memiliki struktur batu yang menghalangi perjalanan Deeper.

**Layout**

| **1 2 3 4 5 6 7 8 9 10 11 12 13 14**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **1 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **2 | #| P| .| .| D| .| .| .| D| .| .| .| X| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **3 | #| .| #| .| #| #| #| .| #| .| D| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **4 | #| .| #| .| .| .| #| .| .| E| #| #| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **5 | #| D| .| .| R| .| .| .| R| .| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **6 | #| #| #| .| #| #| #| .| #| #| #| E| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **7 | #| .| E| .| D| .| .| .| #| .| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **8 | #| .| #| #| #| .| #| .| .| .| B| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **9 | #| E| .| .| .| .| D| .| .| .| .| .| E| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **10 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+** |
| --- |

**Mekanisme Lingkungan**

1. Green Garden memiliki Reinforced Block yang merepresentasikan struktur batu kuno.
2. Reinforced Block hanya dapat dihancurkan menggunakan Pumped Bomb.
3. Normal Bomb dan Remote Bomb tidak dapat menghancurkan Reinforced Block.
4. Reinforced Block menghentikan penyebaran Explosion sampai berhasil dihancurkan.

### F07.3.2. MAP TYPE B: Blue Resort

Blue Resort merupakan kawasan resort yang memiliki saluran air dan jembatan. Perubahan kondisi saluran air dapat membuka atau menutup jalur tertentu.

**Layout**

| **1 2 3 4 5 6 7 8 9 10 11 12 13 14**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **1 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **2 | #| P| .| .| .| W| .| .| .| D| .| .| X| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **3 | #| .| #| #| W| #| #| .| #| #| .| E| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **4 | #| .| .| S| W| G| .| .| .| D| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **5 | #| #| #| W| W| W| #| #| .| #| #| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **6 | #| .| E| .| W| .| .| .| #| .| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **7 | #| D| .| .| G| .| .| .| W| .| .| B| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **8 | #| .| .| .| S| .| E| .| W| .| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **9 | #| E| .| .| .| .| .| .| D| .| .| .| E| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **10 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+** |
| --- |

**Mekanisme Lingkungan**

1. Blue Resort memiliki Water Tile, Switch, dan Gate.
2. Water Tile memperlambat kecepatan pergerakan player sebesar 50% selama player berada pada tile tersebut.
3. Player tetap dapat memasuki Water Tile.
4. Switch mengubah kondisi seluruh Gate pada map secara bersamaan.
5. Ketika player memasuki tile Switch, seluruh Gate berubah dari OPEN menjadi CLOSED atau sebaliknya.
6. Kondisi Gate yang telah berubah akan tetap berlaku sampai player memasuki tile Switch kembali.
7. Setiap Switch pada map memiliki fungsi yang sama terhadap seluruh Gate.
8. Ketentuan perubahan kondisi Gate mengikuti [<u>Aturan Umum Gate</u>](#_2b25lwkcl0gu).

### F07.3.3. MAP TYPE C: Red Mountain

Red Mountain merupakan kawasan pegunungan vulkanik dan pertambangan. Kawasan ini memiliki jalur sempit dan area lava yang dapat membahayakan player.

**Layout**

| **1 2 3 4 5 6 7 8 9 10 11 12 13 14**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **1 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **2 | #| P| .| .| D| .| .| .| H| .| .| .| X| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **3 | #| .| #| #| .| #| #| .| H| #| #| E| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **4 | #| .| .| .| H| .| .| .| H| .| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **5 | #| #| #| .| #| #| #| .| #| #| #| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **6 | #| D| E| .| H| .| .| .| D| .| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **7 | #| .| #| #| .| #| #| #| .| #| #| H| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **8 | #| .| .| .| H| E| .| .| .| B| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **9 | #| E| .| .| D| .| .| .| .| H| .| .| E| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **10 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+** |
| --- |

**Mekanisme Lingkungan**

1. Red Mountain memiliki Lava Tile yang dapat dilalui dan mengalami erupsi secara berkala.
2. Lava Tile menjalankan siklus DORMANT, WARNING, dan ERUPTING secara berulang.
3. Durasi kondisi DORMANT adalah 3 detik.
4. Lava Tile memasuki kondisi WARNING selama 1 detik sebelum erupsi.
5. Player yang berada pada Lava Tile ketika kondisi ERUPTING berlangsung kehilangan maksimal satu nyawa.
6. Lava Tile kembali ke kondisi DORMANT setelah erupsi selesai.

### F07.3.4. MAP TYPE D: White Glacier

White Glacier merupakan kawasan pegunungan es yang memiliki permukaan licin.

**Layout**

| **1 2 3 4 5 6 7 8 9 10 11 12 13 14**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **1 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **2 | #| P| .| .| I| .| .| .| D| .| .| .| X| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **3 | #| .| #| #| I| #| #| .| #| #| .| E| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **4 | #| .| E| .| I| .| .| .| .| I| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **5 | #| #| #| .| #| #| #| .| #| #| #| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **6 | #| D| .| .| I| .| .| .| D| .| E| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **7 | #| .| #| #| .| #| #| #| .| #| #| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **8 | #| .| .| .| I| .| .| .| .| B| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **9 | #| E| .| .| D| .| .| .| .| I| .| .| E| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **10 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+** |
| --- |

**Mekanisme Lingkungan**

1. White Glacier memiliki Ice Tile yang memengaruhi pergerakan player.
2. Player yang memasuki Ice Tile terus bergerak mengikuti arah gerak terakhirnya dan tidak dapat mengubah arah menghadap.
3. Player berhenti pada tile biasa yang dapat dilalui atau tile sebelum penghalang.
4. Pergerakan pada Ice Tile tidak memperbolehkan player menembus block, bomb, atau enemy.
5. Bomb tidak terpengaruh oleh mekanisme pergerakan player pada Ice Tile.

### F07.3.5. MAP TYPE E: Black Fortress

Black Fortress merupakan kawasan benteng mekanis yang menjadi pusat fasilitas utama Nangor Falls. Kawasan ini memiliki sistem keamanan berupa Gate dan Laser Trap.

**Layout**

| **1 2 3 4 5 6 7 8 9 10 11 12 13 14**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **1 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **2 | #| P| .| .| D| .| .| .| L| .| .| .| X| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **3 | #| .| #| #| .| #| #| .| #| #| .| E| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **4 | #| .| E| .| S| .| .| G| .| .| L| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **5 | #| #| #| .| #| #| #| .| #| #| #| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **6 | #| D| .| .| L| .| .| .| D| .| E| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **7 | #| .| #| #| .| #| #| #| .| #| #| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **8 | #| .| .| .| S| .| .| G| .| B| .| .| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **9 | #| E| .| .| .| .| D| .| .| .| .| E| .| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+**  **10 | #| #| #| #| #| #| #| #| #| #| #| #| #| #|**  **+--+--+--+--+--+--+--+--+--+--+--+--+--+--+** |
| --- |

**Mekanisme Lingkungan**

1. Black Fortress memiliki Switch, Gate, dan Laser Trap.
2. Gate merupakan penghalang mekanis yang menutup jalur tertentu.
3. Gate tidak menutup selama tilenya masih ditempati player, enemy, atau bomb, penutupan ditunda sampai kosong.
4. Seluruh Laser Trap dimulai dalam kondisi aktif.
5. Ketika player memasuki tile Switch, seluruh Gate terbuka dan seluruh Laser Trap menjadi nonaktif selama 6 detik.
6. Setelah 5 detik, sistem menampilkan peringatan selama 1 detik sebelum Laser Trap kembali aktif.
7. Setelah 6 detik, Laser Trap kembali aktif dan Gate mulai melakukan proses penutupan.
8. Jika player memasuki Switch kembali ketika mekanisme masih berlangsung, durasi 6 detik dihitung ulang sejak aktivasi terakhir.
9. Player hanya menerima satu damage dari setiap Laser Trap dalam satu periode aktif.

## F08 - Score

Score merupakan nilai yang diperoleh player selama permainan. Score digunakan untuk menunjukkan pencapaian player dalam mengalahkan enemy dan menyelesaikan map.

### F08.1. Aturan Score

1. Score dimulai dari 0.
2. Player memperoleh skor ketika mengalahkan Normal Enemy atau Boss Enemy.
3. Nilai skor ditentukan sebagai berikut.

| **Sumber** | **Score** |
| --- | --- |
| Normal Enemy dikalahkan | 100 |
| Boss Enemy, kecuali Cerberus dan Altair, dikalahkan | 500 |
| Cerberus dan Altair dikalahkan | 250 per boss |
| *Player* masih memiliki nyawa tersisa | 100 per nyawa |
| Timer tersisa | 10 per detik |

1. Score ditampilkan selama permainan berlangsung.
2. Score bonus dari timer dan nyawa tersisa diberikan hanya ketika player mencapai WIN
3. Score akhir ditampilkan ketika permainan berakhir, baik WIN maupun LOSE.
4. Score kembali menjadi 0 ketika permainan di-restart.

## F09 - Game Flow

*Game Flow* merupakan pengaturan alur permainan selama permainan berlangsung, mulai dari pemrosesan input pemain hingga pemeriksaan kondisi akhir permainan.

### F09.1. Menu Utama

Menu utama merupakan tampilan awal permainan yang digunakan pemain untuk memilih aktivitas sebelum memulai atau keluar dari permainan.

### F09.1.1. Tampilan Menu

Ketika program dijalankan, sistem menampilkan menu utama Nangor Blast yang setidaknya memiliki pilihan berikut.

| **Pilihan** | **Keterangan** |
| --- | --- |
| Start Game | Memulai permainan dan menjalankan proses inisialisasi sesuai [<u>F00 – Inisialisasi Permainan</u>](#_vmmy32c8eq39). |
| How to Play | Menampilkan petunjuk permainan, tujuan permainan, serta daftar kontrol yang dapat digunakan pemain. |
| Exit | Mengakhiri program permainan. |

### F09.1.2 Aturan Menu

1. Menu utama ditampilkan ketika program pertama kali dijalankan.
2. Pemain memilih menu menggunakan input keyboard sesuai pilihan yang tersedia.
3. Ketika pemain memilih Start Game, sistem melakukan proses inisialisasi permainan dan memasuki kondisi PLAYING.
4. Ketika pemain memilih How to Play, sistem menampilkan petunjuk permainan. Setelah selesai, pemain dapat kembali ke menu utama.
5. Ketika pemain memilih Exit, program permainan dihentikan.
6. Jika pemain memberikan input yang tidak sesuai dengan pilihan menu, sistem menampilkan pesan kesalahan dan meminta pemain memasukkan pilihan kembali.

### F09.2. Game State

Permainan memiliki kondisi sebagai berikut.

| **Game State** | **Keterangan** |
| --- | --- |
| MENU | Permainan berada pada menu utama. |
| PLAYING | Permainan sedang berlangsung. |
| PAUSED | Permainan sedang dijeda. |
| WIN | Player berhasil menyelesaikan map. |
| LOSE | Player kehabisan nyawa atau waktu. |

### F09.3. Game Process

![](data:image/png;base64...)

Game Process merupakan proses utama yang berjalan selama permainan berada dalam kondisi **PLAYING**. Proses ini terdiri atas beberapa bagian yang berjalan secara paralel untuk memperbarui kondisi permainan.

1. **User Input**

Sistem menerima input dari pemain melalui keyboard, seperti perintah untuk bergerak, memasang bomb, memilih jenis bomb, dan melakukan detonasi Remote Bomb.

1. **Player Action**

Sistem memproses input pemain dan menjalankan aksi sesuai ketentuan pada [<u>F01 - Player</u>](#_iyvbzpmtxlg4) dan [<u>F02 - Bomb</u>](#_f3acy1nif0nl).

1. **Enemy Loop**

Sistem memperbarui pergerakan dan perilaku Normal Enemy serta Boss Enemy. Normal Enemy menjalankan perilaku patrol dan chase, sedangkan Boss Enemy menjalankan pola serangan sesuai mekanisme yang telah ditentukan.

1. **Bomb & Map Loop**

Sistem memperbarui mekanisme bomb dan lingkungan map. Proses ini meliputi perhitungan waktu ledakan bomb, pemrosesan Explosion, penghancuran block, serta pembaruan mekanisme lingkungan seperti Water Tile, Lava Tile, Ice Tile, Gate, Switch, dan Laser Trap.

1. **Print Map**

Sistem menampilkan kondisi map terbaru setelah seluruh proses diperbarui. Tampilan mencakup posisi player, enemy, bomb, dan Explosion, serta informasi permainan seperti nyawa, score, dan timer.

Seluruh proses tersebut berjalan secara berulang selama permainan berlangsung. Timer juga terus berkurang selama permainan berada dalam kondisi PLAYING.

### F09.4. Game Over

Setelah setiap siklus Game Process selesai, sistem memeriksa apakah permainan telah berakhir.

1. **WIN:** Player berhasil mengalahkan seluruh Enemy dan Boss Enemy, serta mencapai pintu keluar.
2. **LOSE:** Player kehabisan nyawa atau timer mencapai 0.

Apabila kondisi akhir permainan belum terpenuhi, Game Process kembali dijalankan. Jika permainan telah berakhir, sistem menghentikan proses permainan dan menampilkan score akhir.

### F09.5. Pause

Player dapat menjeda permainan melalui perintah yang tersedia. Ketika permainan berada dalam kondisi PAUSED, seluruh proses permainan dihentikan sementara, termasuk pergerakan enemy, waktu ledakan bomb, mekanisme lingkungan, dan pengurangan timer. Player dapat memilih untuk melanjutkan permainan, melakukan restart, atau kembali ke menu utama. Ketika permainan dilanjutkan, proses permainan kembali berjalan dengan kondisi terakhir sebelum dijeda.

#

# Bonus

## B01 - GUI

Kalian dapat mengimplementasi GUI pada tugas besar ini. GUI membuat game kalian memiliki UI dan visual yang membuat game menjadi lebih hidup dan mudah berinteraksinya. Dalam melakukan implementasi GUI, kalian dibebaskan untuk menggunakan *package* apapun, contoh *package* GUI yang dapat digunakan yaitu Java Swing (sudah bawaan dari Java sehingga kalian tidak perlu meng-*install* sendiri), atau JavaFX (*package third-party* sehingga kalian perlu meng-*install*-nya). Contoh implementasi program menggunakan GUI dapat dilihat referensi kodenya pada tautan [<u>ini</u>](https://github.com/jjenkov/javafx-examples). Perlu diingat bahwa kalian diberi kebebasan dalam implementasi dan tidak harus mengikuti alternatif pada referensi. Untuk mempermudah proses pengembangan dan kolaborasi, **sangat disarankan** menggunakan **MVC (*Model*, *View*, *Controller*)**.

## B02 - Bomb Kick

Kalian dapat mengimplementasikan kemampuan Bomb Kick yang memungkinkan player untuk menendang bomb ke arah tertentu. Bomb yang ditendang akan bergerak hingga menabrak penghalang, mencapai batas map, atau bertemu dengan objek lain yang menghalangi pergerakannya. Bomb yang sedang bergerak tetap mengikuti aturan waktu ledak dan mekanisme Explosion yang berlaku. Kemampuan ini dapat dimanfaatkan untuk menyerang enemy dari jarak tertentu atau memindahkan bomb ke posisi yang lebih strategis. Implementasi harus memperhatikan interaksi bomb dengan player, block, bomb lain, dan entitas pada map.

## B03 - Map Maker

Kalian dapat mengimplementasikan fitur *Map Maker* yang memungkinkan pemain membuat atau mengubah map permainan. Pemain dapat menentukan susunan block, posisi spawn, lokasi enemy, Power-Up, dan pintu keluar sesuai aturan map yang berlaku. Map yang dibuat harus melalui proses validasi agar dapat dimainkan dan diselesaikan. Fitur ini dapat **dilengkapi dengan kemampuan menyimpan dan memuat map** sehingga map hasil kreasi pemain dapat digunakan kembali.

## B04 - Local Multiplayer

Local Multiplayer merupakan fitur tambahan yang memungkinkan dua pemain bermain bersama pada satu perangkat dalam mode cooperative multiplayer (co-op). Kedua pemain bekerja sama untuk mengalahkan Normal Enemy dan Boss Enemy serta menyelesaikan map.

**Ketentuan:**

1. Setiap pemain memiliki kontrol dan status masing-masing, termasuk posisi dan jumlah nyawa.
2. Kedua pemain berada pada map yang sama dan menghadapi Normal Enemy serta Boss Enemy yang sama.
3. Kedua pemain dapat memasang bomb dan menggunakan Power-Up sesuai aturan permainan.
4. Power-Up yang diambil hanya memberikan efek kepada pemain yang mengambilnya.
5. Score dan timer digunakan bersama oleh kedua pemain.
6. Explosion dari bomb dapat memberikan damage kepada kedua pemain yang berada dalam jangkauannya, termasuk pemilik bomb, sesuai aturan F03 – Explosion.
7. Permainan berakhir dengan kondisi LOSE apabila timer mencapai 0 atau seluruh pemain kehabisan nyawa.
8. Permainan berakhir dengan kondisi WIN apabila seluruh Boss Enemy telah dikalahkan dan setidaknya satu pemain yang masih aktif mencapai pintu keluar.

Untuk kontrol keyboard, **masing-masing pemain harus memiliki pemetaan tombol yang berbeda** agar kedua pemain dapat memberikan input secara bersamaan.

## B05 - Design Pattern

Kalian disarankan menerapkan hingga 5 *design pattern* atau sebagai pengembangan dari pola yang digunakan pada fitur wajib. Setiap *design pattern* yang diterapkan harus memiliki tujuan yang jelas dan sesuai dengan kebutuhan permainan. Kelompok wajib menjelaskan pola yang digunakan, alasan pemilihannya, serta bagian kode yang menerapkannya.

## BXX - Kreativitas

Kalian bebas mengembangkan fitur tambahan lain yang meningkatkan kualitas, tantangan, atau pengalaman bermain Nangor Blast. Fitur yang dikembangkan harus **memiliki manfaat yang jelas** dan tidak sekadar menambahkan objek atau tampilan tanpa interaksi yang berarti. Implementasi bonus Creativity akan dinilai berdasarkan kreativitas, tingkat kesulitan, kualitas implementasi, serta kesesuaiannya dengan permainan.

#

# Ketentuan Umum

Folder terpusat: [<u>Tugas Besar IF2010 26/27</u>](https://drive.google.com/drive/folders/1JSl0zf-KkxLEGBA_cp2Tp8f7LutgdaOT?usp=sharing)

1. Tugas dikerjakan berkelompok dengan anggota kelompok sebanyak 4–5 orang per kelompok dengan anggota kelompok yang telah ditentukan oleh asisten. Link **pembagian kelompok, tipe map** serta **pemilihan asisten** dapat dilihat pada tautan berikut:

[<u>IF2010 Pembagian Kelompok & Asisten</u>](https://docs.google.com/spreadsheets/d/1n0fHYYrKpNgz794MzcGnSPl4G39j7kGIoeNkSK1CPlY/edit?usp=sharing)

1. **Form Asistensi** dapat dilihat pada tautan berikut: [<u>Form Asistensi</u>](https://docs.google.com/forms/d/e/1FAIpQLSfH9rZDDNYQ8hs5QALlRKu44X3lXXA4GclbEePfIeYxwwKbXA/viewform?usp=header)
2. Pertanyaan terkait Tugas Besar, dapat diajukan dalam **Spreadsheets QNA** yang ada pada tautan berikut:

[<u>QnA IF2010 2026/2027 - Tugas Besar 1</u>](https://docs.google.com/spreadsheets/d/1iO31PrJfTks09Yx7SjoOk0abn1PxKf4abTsmV15_Ohw/edit?usp=sharing)

Mekanisme pengerjaan silakan perhatikan bagian [<u>Pengumpulan dan Deliverables</u>](#_rxm5c6p3rhj)

## Timeline Pengerjaan

| **Kegiatan** | **Deadline** | |
| --- | --- | --- |
| **Tanggal** | **Jam (WIB)** |
| **Release Tugas Besar** | 9 November 2026 | **12.00** |
| Pengisian Asisten Kelompok | 11 November 2026 | 20.10 |
| **Pengerjaan Tugas Besar** | | |
| - Deadline Asistensi 1 | 16 November 2026 | 20.10 |
| - Deadline *Milestone* 1 | 17 November 2026 | 20.10 |
| - Deadline Asistensi 2 | 3 Desember 2026 | 20.10 |
| * Deadline *Milestone* 2 | 4 Desember 2026 | 20.10 |

## Asistensi

1. Setiap kelompok akan dibantu oleh seorang asisten pembimbing. Asistensi wajib dilakukan kepada asisten pembimbing.
2. Anggota kelompok menghubungi asisten pembimbing untuk mengajukan asistensi atau bertanya.
3. Asisten pembimbing bertugas untuk membimbing pengerjaan Tugas Besar dan melakukan klarifikasi terhadap spesifikasi Tugas Besar.
4. Asistensi wajib dilakukan sebanyak **minimal dua kali**, satu kali sebelum *milestone* 1 dan yang kedua sebelum *milestone* 2. Berikut adalah ketentuan asistensi wajib.
   1. Asistensi 1 (untuk klarifikasi spesifikasi tugas): paling lambat **16 November 2026**. Wajib.
   2. Asistensi 2: paling lambat hari **3 Desember 2026**. Wajib.
   3. Asistensi 3: Opsional, silakan hubungi asisten pembimbing untuk mengajukan asistensi tambahan jika diperlukan.
5. Untuk semua asistensi, paling lambat menghubungi asisten pembimbing **J-24** sebelum waktu asistensi yang diajukan.
6. Asistensi **bukan sesi untuk membahas ulang spesifikasi**, tetapi untuk klarifikasi atau bertanya bagian yang tidak dimengerti. **Asisten tidak akan membahas kembali spesifikasi saat asistensi**.
7. Paling lambat **1 jam** setelah asistensi selesai, masing-masing anggota kelompok yang hadir pada asistensi wajib mengisi form asistensi secara daring melalui Google Form.
   1. Form catatan asistensi: [<u>di sini</u>](https://docs.google.com/forms/d/e/1FAIpQLSfH9rZDDNYQ8hs5QALlRKu44X3lXXA4GclbEePfIeYxwwKbXA/viewform?usp=publish-editor)
   2. Sertakan juga bukti kehadiran asistensi berupa screenshot atau foto dengan asisten.
   3. Tidak diperkenankan untuk meng-copy paste catatan kemajuan milik orang lain.

# Pengumpulan dan Deliverables

## Milestone 1

1. Pada Milestone 1, Anda perlu mengumpulkan link repository GitHub dan 2 dokumen, yaitu pembagian tugas setiap anggota kelompok dan struktur dari objek-objek yang terdapat pada game (disarankan menggunakan class diagram). **Harap mengundang asisten pembimbing** yang bersangkutan **pada repository GitHub**. Akun GitHub asisten akan dituliskan pada sheets pembagian kelompok.
2. Tidak ada aturan penamaan khusus *repository* GitHub.
3. Repository **minimal berisi**:
   1. Folder **src**: Berisi kode program Java, termasuk kelas, fungsi, dan komponen yang digunakan.
   2. Folder **config**: Berisi contoh data atau file konfigurasi yang dapat dimuat oleh program..
   3. Folder **doc**: Berisi dokumen dan dokumentasi terkait tugas besar dalam format PDF, seperti buklet dan dokumentasi pendukung lainnya..
   4. **Makefile**: File konfigurasi yang berisi sekumpulan aturan untuk mengotomatisasi proses kompilasi, build, menjalankan, dan membersihkan program.
   5. **README.md**: Berisi setidaknya penjelasan ringkas program, kebutuhan dan tahapan kompilasi program, cara menjalankan program, pembagian tugas, serta daftar fitur beserta status pengerjaannya.
4. Format dari kedua dokumen adalah PDF dan wajib dikumpulkan pada form ini.

## Milestone 2

1. Pada Milestone 2, anda perlu mengumpulkan Source Code, Buklet, dan Log Activity. Pengumpulan akan dilakukan dengan membuat **release** pada Repository Github kelompok masing-masing. Release harus sudah mencakup Source Code, Buklet dan Log Activity. Waktu Release tidak boleh melewati deadline pengumpulan. Di saat pengumpulan, pastikan repository Github tugas besar sudah di set menjadi **publik**. Pengumpulan dilakukan pada link form ini.
2. Berikut adalah spesifikasi source code, buklet, dan log activity.

## Source Code

1. Teknik yang digunakan dalam pembuatan aplikasi permainan Nangor Blast dibebaskan, namun terdapat beberapa konsep OOP yang **WAJIB** diimplementasikan di aplikasi yang Anda buat, yaitu:
2. Inheritance
3. Abstract Class / Interface
4. Polymorphism
5. Generics
6. Exceptions
7. Collections
8. Concurrency
9. Program harus diimplementasikan menggunakan bahasa Java.
10. Tuliskan tahapan untuk melakukan kompilasi dan menjalankan program pada file README.md.

## Buklet

1. Pada Tugas Besar kali ini, format laporan diubah menjadi bentuk buklet. Buklet yang dibuat memiliki ketentuan sebagai berikut.
2. Berukuran A5
3. Tidak lebih dari 15 halaman
4. Format PDF
5. Berisi setidaknya:
6. Halaman cover, yang berisi nama dan nomor kelompok, serta nama dan NIM anggota kelompok.
7. User manual dan deskripsi jalannya permainan (gameplay).
8. Nama, peran, dan pembagian tugas anggota kelompok.
9. Struktur final dari objek-objek yang terdapat pada game (disarankan menggunakan class diagram)
10. Design pattern yang digunakan
11. Cerita tentang proses pengembangan
    1. Pada bagian ini kalian menceritakan proses pengembangan Tugas Besar ini dari awal sampai akhir. Kalian boleh mencantumkan screenshot rapat, hasil ideasi, corat-coret Miro/Jamboard, atau dokumentasi apapun yang mendukung jalan cerita kalian.
    2. Cantumkan juga rancangan awal dan apa saja perubahan yang dilakukan (apabila implementasi beda dari rancangan) dan kenapa perlu dilakukan perubahan tersebut.
12. Dibuat sekreatif dan semenarik mungkin. Desain, tipografi, pewarnaan, dan tata letak dibebaskan kepada kalian.
13. Bahasa yang digunakan tidak harus baku, tetapi tetap serius dan terkesan friendly.

## Log Activity

1. Log Activity harus memuat progress masing - masing anggota dan disatukan menjadi satu dokumen.
2. Tabel di dalam dokumen minimal harus memiliki format sebagai berikut.

Kebin / 18225000

| **Waktu** | **Kegiatan** | **Hasil** |
| --- | --- | --- |
| 30 November 2026 | Kegiatan 1 | Fitur A lancar tanpa bug |
| 3 Desember 2026 | Kegiatan 2 | Class B masih ada bug X |

# Referensi

* [<u>Dev.java - Getting to Know the Language</u>](https://dev.java/learn/language/)
* [<u>Dev.java - The Collections Framework</u>](https://dev.java/learn/api/collections-and-streams/collections-framework/)
* [<u>Oracle - Java SE 25: java.util.concurrent Package</u>](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/util/concurrent/package-summary.html)
* [<u>Game Programming Patterns - Game Loop</u>](https://gameprogrammingpatterns.com/game-loop.html)
* [<u>Refactoring.Guru - Design Patterns</u>](https://refactoring.guru/design-patterns)
* [<u>GeeksforGeeks - OOD Principles | SOLID</u>](https://www.geeksforgeeks.org/software-engineering/ood-principles-solid/)
* [<u>Oracle - Java SE 25: javax.swing Package</u>](https://docs.oracle.com/en/java/javase/25/docs/api/java.desktop/javax/swing/package-summary.html)
* [<u>OpenJFX - Getting Started with JavaFX</u>](https://openjfx.io/openjfx-docs/)
* [<u>GitHub Docs - About Git</u>](https://docs.github.com/en/get-started/using-git/about-git?utm_source=chatgpt.com)
* [<u>Gradle - User Manual</u>](https://docs.gradle.org/current/userguide/?utm_source=chatgpt.com)
* [<u>Apache Maven - Getting Started Guide</u>](https://maven.apache.org/guides/getting-started/?utm_source=chatgpt.com)
* [<u>SLF4J - User Manual</u>](https://www.slf4j.org/manual.html?utm_source=chatgpt.com)

# Extras

“[<u>https://codeforces.com/gym/101246/problem/C</u>](https://codeforces.com/gym/101246/problem/C)”

~ Null Cipher

![](data:image/png;base64...)

“Yuk bisa yuk”

~ Bitter Candy

“Kata gw mah Nangor Falls dibom aja satu kota”

~ Clear-Sight Ivan

“Seru deh speknya, jadi semangat ngerjainnya - STI’25, probably”

~ Flannel-Wendy