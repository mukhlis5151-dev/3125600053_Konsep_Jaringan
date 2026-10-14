# **KONSEP JARINGAN** 

# **TUGAS 5** 



<!-- Start of picture text -->
ol:ae<br>pens<br><!-- End of picture text -->

Nama : Imam Mukhlis Nur Ismail NRP : 3125600053 Dosen Pengajar : Dr Ferry Astika Saputra ST, M.Sc 

## **PROGRAM STUDI D4 TEKNIK INFORMATIKA** 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA (PENS)** 

**2026** 

## **A. Traceroute** 

Traceroute adalah alat baris perintah yang sederhana namun cerdas untuk melacak jalur yang dilalui paket IP di satu atau banyak jaringan. Awalnya dikembangkan untuk platform berbasis UNIX, tetapi sekarang disertakan dalam sebagian besar sistem operasi, dengan implementasi Windows yang dikenal sebagai "tracert". Output dari perintah ini juga sering disebut sebagai traceroute. Misalnya, jika Anda meminta bantuan terkait kinerja streaming video yang buruk, ISP Anda mungkin akan meminta Anda untuk melakukan traceroute. 

Traceroute terutama digunakan untuk tujuan diagnostik, tetapi juga bisa menjadi alat yang menyenangkan untuk mempelajari tentang jaringan atau sekadar memuaskan rasa ingin tahu yang mendalam. Administrator sistem dan insinyur jaringan dapat menggunakan traceroute untuk melihat bagaimana lalu lintas mengalir di dalam suatu organisasi, dan mengidentifikasi jalur yang tidak teratur atau kurang optimal. Secara eksternal, traceroute dapat menampilkan jalur paket saat melintasi berbagai jaringan, dan dalam beberapa kasus bahkan mengungkapkan berbagai kota atau wilayah geografis yang dilalui lalu lintas. Penyerang berpotensi menggunakan traceroute untuk memetakan jaringan target, itulah sebabnya jenis paket yang digunakan oleh traceroute sering diblokir atau difilter di perimeter jaringan perusahaan. 

Sebagian besar implementasi traceroute juga menampilkan waktu yang dibutuhkan untuk mencapai setiap "hop" antara sumber dan tujuan. Ini sangat berguna ketika mencari akar penyebab hilangnya lalu lintas atau masalah kinerja. Selama satu episode konektivitas sporadis dari kantor rumah saya, saya dapat melihat dari hasil traceroute bahwa ISP saya menghilangkan banyak paket dan secara tidak konsisten mengarahkan paket lain melalui jalur yang aneh dan jauh secara geografis. Beberapa jam kemudian, ISP mengumumkan bahwa kabel fiber optik regional telah diputus oleh kontraktor. 

Traceroute sebenarnya agak seperti trik, karena memanfaatkan sebuah field dalam header paket Internet Protocol (IP) yang sebenarnya tidak pernah dimaksudkan untuk pelacakan jalur atau rute. Standar IP mewajibkan nilai Time-to-Live (TTL) untuk setiap paket IP, yang bertindak sebagai semacam mekanisme penghancuran diri untuk mencegah paket yang tidak dapat dikirim terus beredar di Internet. Setiap router dalam 

suatu jalur diharapkan untuk mengurangi nilai TTL sebesar satu sebelum mengirimkannya lebih jauh. Setelah TTL mencapai nol, proses routing akan berhenti total, dan router terakhir yang memproses paket akan mengirimkan pesan "Time to live exceeded". 

Melebihi nilai TTL bukanlah hal yang diinginkan untuk paket data normal, itulah sebabnya paket tipikal akan memiliki nilai mulai dari 64 hingga 255. Namun, apa yang seharusnya menjadi pesan kesalahan yang menjengkelkan sebenarnya merupakan bagian penting dari cara kerja traceroute. Dengan memanipulasi bidang TTL, traceroute dan program serupa dapat memicu pesan TTL terlampaui dari setiap hop di sepanjang jalur tertentu. Begini cara kerjanya: 

1. Pengguna menjalankan perintah traceroute (atau tracert) dan menentukan host target. Jika host ditentukan dalam bentuk nama domain, traceroute akan mencoba untuk menyelesaikannya. 

2. Traceroute mengirimkan paket data menuju target dengan nilai TTL yang diatur ke "1". Router pertama di jalur tersebut akan mengurangi nilai tersebut sebesar 1, yang seharusnya memicu pesan "TTL terlampaui" yang dikirim kembali ke host tempat program traceroute dijalankan. 

3. Dengan detail hop pertama yang sudah ada, traceroute akan meningkatkan nilai TTL menjadi “2”. Router pertama di jalur tersebut masih akan mengurangi nilainya sebesar 1, tetapi karena TTL tidak lagi langsung turun ke nol, paket dapat melanjutkan satu hop lagi. Setelah nilai TTL mencapai nol (dalam hal ini, pada router kedua di jalur tersebut), pesan "TTL terlampaui" lainnya harus dihasilkan dan dikirim kembali ke traceroute. 

4. Proses ini berulang, dengan traceroute meningkatkan TTL sebesar 1 setiap kali, hingga tujuan tercapai atau batas atas jumlah hop terpenuhi. Secara default, batas atasnya adalah 30 hop, tetapi nilai yang berbeda dapat ditentukan saat perintah dijalankan. 

5. Setelah selesai, traceroute akan mencetak semua hop dalam jalur tersebut, beserta jumlah waktu yang dibutuhkan untuk setiap hop dan kembali (ini dikenal sebagai Waktu Perjalanan Pulang Pergi). 

Secara default, traceroute akan mengirimkan tiga paket ke setiap hop dalam jalur tersebut. Jenis paket yang tepat bervariasi antara implementasi, dan juga dapat diubah dengan flag yang berbeda, tetapi metodologi dasar yang sama digunakan dalam semua kasus. 

## **B. TTL** 

Time to Live (TTL) adalah mekanisme yang membatasi periode waktu sebuah paket data dalam komputer atau jaringan. TTL dapat diimplementasikan sebagai counter atau timestamp yang terdapat dalam data. 

Setelah perhitungan atau jangka waktu telah berlalu, data akan dibuang. Dalam jaringan komputer, TTL mencegah paket data yang masuk secara terus menerus (tanpa batas). Dalam penerapannya, TTL digunakan untuk meningkatkan kinerja caching atau meningkatkan privasi. 

TTL dapat kamu temukan ketika melakukan ping pada suatu website menggunakan command line seperti CMD. Fungsinya, untuk membatasi waktu dalam ping dalam jangka waktu tertentu. 

Jika dalam satu program ping TTL bernilai 50, maka dalam batawan waktu tertentu hingga waktu TTL semakin berkurang dan juga paket data telah melewati banyak router, maka makin lama TTL akan habis atau expired. TTL sengaja dibatasi agar tidak terjadi perputaran jaringan atau circular routing. 

Semakin besar nilai latency atau ping, maka komunikasi internet semakin buruk atau melambat. 

Dalam DNS, TTL merupakan jenis tanggal kadaluarsa yang dimasukkan pada DNS. TTL berfungsi untuk memberi tahu resolveer server berapa lama ia harus menyimpan catatan tersebut dalam cache-nya. 

Semakin lama TTL, semakin lama resolver menyimpan informasi itu dalam cache. Sebaliknya, semakin pendek TTL semakin pendek pula waktu resolver emnyimpan data informasi tersebut dalam cache. 

Singkatnya, TTL berupa pengaturan untuk setiap catatan DNS yang menentukan berapa lama resolver seharusnya melakuakan cache query DNS sebelum query berakhir dan yang baru perlu dilakukan. 

Peranan penting TTL dalam DNS antara lain: 

1. Untuk mencapai keseimbangan terbaik antara memiliki TTL rendah (memungkinkan perubahan rendah jika diperlukan) dan TTL tinggi (memanfaatkan caching DNS) untuk DNS Record yang jarang diganti. 

2. Untuk penghematan, karena sebagian besar penyedia DNS juga membebankan biaya berdasarkan berapa banyak permintaan DNS yang kamu lakukan. 



