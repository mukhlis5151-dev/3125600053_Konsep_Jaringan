# **KONSEP JARINGAN** 

# **MODEL OSI TCPIP** 



<!-- Start of picture text -->
ol:ae<br>pens<br><!-- End of picture text -->

Nama : Imam Mukhlis Nur Ismail NRP : 3125600053 Dosen Pengajar : Dr Ferry Astika Saputra ST, M.Sc 

## **PROGRAM STUDI D4 TEKNIK INFORMATIKA** 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA (PENS)** 

**2026** 

## **Level A - Ingatan dan Pemahaman** 

1. Jelaskan alasan komunikasi jaringan disusun berlapis. Komunikasi jaringan disusun berlapis karena proses komunikasi melibatkan pekerjaan yang berbeda, mulai dari mengubah bit menjadi sinyal, mengatur penggunaan media, menentukn alamat tujuan, memilih jlur pengiriman, hingga menyediakan layanan yang dapat digunakan oleh aplikasi. Pembagian menjadi beberapa lapisan memberikan manfaat berikut: 

   - a. Modularitas, yaitu fungsi jaringan yang kompleks dibagi menjadi bagian-bagian yang lebih kecil dan mudah dipahami. 

   - b. Interoperabilitas, yaitu perangkat dan perangkat lunak dari produsen berbeda dapat berkomunikasi selama menggunakan protokol yang sama. 

   - c. Evolusi independen, yaitu teknologi pada satu lapisan dapat dikembangkan atau diganti tanpa harus mendesain ulang seluruh sistem. 

   - d. Mempermudah pengujian dan troubleshooting, karena lokasi gangguan dapat dicari berdasarkan fungsi setiap lapisan. 

   - e. Penggunaan kembali, yaitu satu protokol lapisan bawah dapat digunakan oleh banyak aplikasi dan satu aplikasi dapat berjalan pada beberapa jenis media jaringan. 

2. Bedakan layanan, antarmuka, dan protokol. 

   - a. Layanan atau service Layanan adalah kemampuan yang diberikan oleh suatu lapisan kepada lapisan di atasnya. 

   - b. Antarmuka atau interface 

      - Antarmuka adalah cara lapisan di atas mengakses layanan lapisan di bawah pada sistem atau perangkat yang sama. 

   - c. Protokol atau protocol Protokol adalah aturan komunikasi antara entitas sejawat pada lapisan yang sama, tetapi berada pada sistem yang berbeda. 

3. Sebutkan tujuh lapisan OSI dari bawah ke atas beserta fungsi utamanya. 

   - a. Physical 

      - mengubah bit menjadi sinyal 

      - mengatur karakteristik elektrik, optik, atau radio 

      - menentukan konektor dan media 

      - melakukan modulasi dan pengodean sinyal 

      - mengatur sinkronisasi dan laju transmisi 

   - b. Data link 

      - membentuk frame 

      - menggunakan alamat lokal seperti alamat MAC 

      - mengatur akses terhadap media 

      - mendeteksi kesalahan 

      - meneruskan frame pada jaringan lokal. 

   - c. Network 

      - penggunaan alamat IP 

      - penentuan jalur atau routing 

      - pemilihan next hop 

      - penerusan paket antarjaringan 

   - d. Transport 

      - penggunaan nomor port 

      - multiplexing dan demultiplexing aplikasi 

      - segmentasi data 

      - pengurutan data 

      - retransmisi 

      - kontrol aliran dan kontrol kemacetan, khususnya pada TCP 

   - e. Session 

      - membentuk sesi 

      - mempertahankan sesi 

      - melakukan sinkronisasi 

      - mengakhiri sesi 

      - menyediakan checkpoint untuk pemulihan proses komunikasi 

   - f. Presentation 

      - serialisasi data 

      - konversi format 

      - pengodean karakter 

      - kompresi 

      - transformasi kriptografis atau enkripsi secara konseptual 

   - g. Application 

      - HTTP untuk layanan web; 

      - DNS untuk penamaan; 

      - SMTP untuk pengiriman surel; 

      - SSH untuk akses terminal; 

      - DHCP untuk membantu konfigurasi jaringan 

      - 

4. Sebutkan empat lapisan model TCP/IP. 

   - a. Link 

   - b. Internet 

   - c. Transport 

   - d. Application 

5. Mengapa model TCP/IP kadang disajikan sebagai lima lapisan? Karena penyajian menjdi 5 lapisan mempermudah dalam mempelajari perbedaan antara fungsi pengiriman frame pada jaringan lokal yang ditangani Data Link; dan fungsi pengiriman bit atau sinyal melalui media yang ditangani Physical. 

6. Apa perbedaan frame, IP packet, TCP segment, dan UDP datagram? 

   - a. Frame 

Frame adalah unit data pada lapisan Data Link atau Link. Frame digunakan untuk mengirimkan data pada satu tautan atau jaringan lokal. Frame biasanya memiliki header dan trailer yang dapat memuat: 

- alamat MAC sumber; 

- alamat MAC tujuan; 

- tipe protokol lapisan atas; 

- informasi pemeriksaan kesalahan seperti Frame Check Sequence. 

- b. IP packet 

IP packet atau IP datagram adalah unit data pada lapisan Network atau Internet. Paket IP digunakan untuk membawa data dari host sumber menuju host tujuan melintasi satu atau beberapa jaringan. Header-nya memuat informasi seperti: 

   - alamat IP sumber; 

   - alamat IP tujuan; 

   - TTL atau Hop Limit; 

   - identitas protokol lapisan berikutnya. 

- c. TCP segment 

TCP segment adalah unit data milik protokol TCP pada lapisan Transport. TCP segment memiliki informasi pengendalian yang mendukung komunikasi andal, seperti: 

   - nomor port sumber dan tujuan; 

   - sequence number; 

   - acknowledgment number; 

   - flag TCP; 

   - kontrol aliran; 

   - checksum. 

- d. UDP datagram 

UDP datagram adalah unit data milik protokol UDP pada lapisan Transport. UDP datagram memiliki mekanisme yang lebih sederhana dibandingkan TCP. UDP tidak memiliki mekanisme keandalan bawaan seperti: 

      - pembentukan koneksi; 

      - pengurutan data; 

      - retransmisi; 

      - kontrol aliran. 

7. Definisikan header, trailer, dan payload. 

   - a. Header 

Header adalah informasi kendali yang ditempatkan sebelum payload. Header dapat berisi: alamat sumber dan tujuan, nomor port, tipe protocol, nomor urut, informasi panjang data. 

- b. Trailer 

Trailer adalah informasi kendali yang ditempatkan setelah payload. Trailer umumnya digunakan untuk membawa informasi pemeriksaan kesalahan. Contohnya adalah Frame Check Sequence pada frame Ethernet. 

- c. Payload 

Payload adalah data yang dibawa oleh suatu protocol data unit (PDU). Payload pada suatu lapisan biasanya merupakan seluruh PDU dari lapisan di atasnya 

8. Jelaskan enkapsulasi dan dekapsulasi. 

Enkapsulasi adalah proses penambahan informasi kendali ketika data bergerak turun dari lapisan atas menuju lapisan bawah pada perangkat pengirim. Dekapsulasi adalah proses pemeriksaan dan pelepasan informasi kendali ketika data diterima dan bergerak naik dari lapisan bawah menuju lapisan atas pada perangkat penerima. 

9. Apa fungsi multiplexing dan demultiplexing? Multiplexing adalah proses menggabungkan banyak aliran, aplikasi, atau protokol agar dapat menggunakan layanan lapisan bawah yang sama. Multiplexing memungkinkan satu infrastruktur jaringan digunakan bersama oleh berbagai komunikasi. 

Demultiplexing adalah proses memilih pengolah, protokol, atau aplikasi penerima yang sesuai berdasarkan suatu pengenal. 

10. Mengapa OSI tidak boleh dianggap sebagai spesifikasi implementasi? Karena model Open Systems Interconnection (OSI) adalah model konseptual yang membagi komunikasi jaringan dan interoperabilitas ke dalam tujuh lapisan abstrak. Model OSI digunakan untuk: 

   - menyediakan kerangka bersama bagi standardisasi komunikasi; 

   - mengelompokkan fungsi jaringan; 

   - menjelaskan hubungan antarfungsi; 

   - membantu pembelajaran; 

   - membantu klasifikasi protokol dan gangguan; 

   - memberikan bahasa konseptual dalam analisis jaringan. 

## **Level B - Penerapan dan Analisis** 

11. Petakan HTTP, TLS, TCP, UDP, QUIC, IPv6, ICMP, Ethernet, Wi-Fi, dan DNS ke model TCP/IP. Tandai protokol yang pemetaannya memerlukan penjelasan. 

|Protocol|Lapisan TCP/IP|Penjelasan|
|---|---|---|
|HTTP|Application|HTTP<br>mendukung<br>pertukaran sumber daya<br>web dan menentukan<br>struktur permintaan serta<br>respons antara klien dan<br>server.|
|TLS|Application*|TLS<br>memberikan<br>keamanan<br>saluran<br>komunikasi<br>melalui<br>enkripsi, integritas, dan<br>autentikasi.<br>Pemetaan<br>TLS<br>memerlukan<br>penjelasan karena secara<br>konseptual<br>dapat<br>ditempatkan di antara<br>Application<br>dan<br>Transport.|
|TCP|Transport|TCP<br>menyediakan<br>layanan<br>berorientasi<br>koneksi, aliran byte andal,<br>pengurutan, retransmisi,<br>kontrol aliran, dan kontrol<br>kemacetan.|
|UDP|Transport|UDP<br>menyediakan<br>layanan<br>datagram<br>sederhana<br>tanpa<br>pembentukan koneksi dan<br>tanpa<br>mekanisme<br>keandalan bawaan seperti<br>TCP.|
|QUIC|Transport*|QUIC menjalankan fungsi<br>transport yang aman dan<br>termultipleks,<br>tetapi<br>diimplementasikan di atas<br>UDP.<br>Karena<br>itu,<br>pemetaannya memerlukan<br>penjelasan.|
|IPv6|Internet|IPv6<br>menyediakan<br>pengalamatan logis dan<br>pengantaran<br>paket<br>melintasi<br>beberapa<br>jaringan.|



|ICMP|Internet*|ICMP<br>mendukung|
|---|---|---|
|||pelaporan kesalahan dan<br>diagnostik pada Internet<br>layer. Pemetaan ICMP|
|||memerlukan penjelasan|
|||karena pesan ICMP<br>dibawa di dalam datagram<br>IP, tetapi pemrosesannya<br>dianggap bagian dari<br>Internet layer.|
|Ethernet|Link*|Ethernet<br>menyediakan<br>pengiriman frame pada<br>jaringan lokal. Spesifikasi<br>Ethernet juga memiliki<br>aspek Physical sehingga<br>pemetaannya<br>tidak|
|||sepenuhnya hanya pada<br>satu fungsi.|
|Wi-Fi|Link*|Wi-Fi<br>menyediakan<br>komunikasi jaringan lokal<br>melalui media radio. Wi-<br>Fi mencakup fungsi<br>Physical dan Data Link,<br>sehingga pemetaannya<br>perlu dijelaskan.|
|DNS|Application*|DNS merupakan protokol<br>aplikasi<br>yang<br>menyediakan<br>layanan<br>penamaan. DNS dapat<br>menggunakan beberapa<br>protokol Transport, seperti<br>UDP atau TCP, sehingga<br>tidak selalu berpasangan|
|||dengan satu protokol<br>Transport saja.|



12. Gambarkan enkapsulasi permintaan DNS melalui UDP, IPv4, dan Ethernet. Sebutkan pengenal yang digunakan pada setiap batas. 

||Ethernet frame|||
|---|---|---|---|
|Ethernet heder|Paket I|Pv4||
||IPv4 Header|UDP D|atagram|
|||UDP|DNS Data|
|||Header||
||Ethernet Trailer|||



   - a. Batas antara DNS dan UDP Ketika pesan DNS diserahkan kepada UDP, sistem harus memberi tahu UDP bahwa data tersebut ditujukan untuk layanan DNS. Pengenal yang digunakan adalah nomor port. 

   - b. Batas antara UDP dan IPv4 

      - Setelah UDP membentuk UDP datagram, datagram tersebut dimasukkan ke dalam paket IPv4.  Pv4 harus memiliki penanda agar penerima mengetahui protokol apa yang berada di dalam payload paket IP. Penanda tersebut adalah field Protocol pada header IPv4. 

   - c. Batas antara IPv4 dan Ethernet Setelah paket IPv4 terbentuk, paket tersebut dimasukkan ke dalam payload frame Ethernet. Ethernet perlu memberi tahu perangkat penerima tentang protokol yang terdapat dalam payload frame. Pengenal yang digunakan adalah EtherType. 

13. Ulangi soal sebelumnya untuk HTTP/3 melalui QUIC. Jelaskan mengapa QUIC tetap dapat dianggap transport meskipun menggunakan UDP. 

   - Pada komunikasi HTTP/3, data HTTP dibawa oleh QUIC. QUIC kemudian menggunakan UDP sebagai pembungkus agar dapat dikirim melalui jaringan IP. Setelah itu, paket IP dimasukkan ke dalam frame Ethernet untuk dikirimkan pada jaringan lokal. 

QUIC tetap dianggap sebagai protokol Transport karena penempatan protokol dalam model lapisan ditentukan terutama berdasarkan fungsi dan layanan yang disediakan, bukan hanya berdasarkan protokol pembungkusnya. 

- a. Pembentukan dan pengelolaan koneksi 

QUIC membangun konteks komunikasi antara klien dan server. 

- b. Pengiriman data yang andal 

   - QUIC mendeteksi kehilangan data dan mengirimkan kembali informasi yang diperlukan. 

- c. Kontrol kemacetan QUIC mengendalikan laju pengiriman agar tidak memperparah kemacetan jaringan. 

- d. Kontrol aliran 

QUIC mengatur jumlah data yang dapat dikirim agar penerima tidak kewalahan. 

- e. Multiplexing beberapa stream 

Satu koneksi QUIC dapat membawa beberapa stream secara bersamaan. 

- f. Pengurutan dalam stream 

Data dalam satu stream dapat diproses sesuai urutan yang diperlukan. 

- g. Keamanan terintegrasi 

QUIC mengintegrasikan TLS untuk membentuk komunikasi yang aman. 

- h. Komunikasi antaraplikasi pada host berbeda Fungsi ini merupakan tanggung jawab utama Transport layer. 

14. Dua host berada pada subnet berbeda. Jelaskan header mana yang berubah dan tetap ketika paket melewati satu router, dengan mengabaikan NAT. Ketika paket melewati satu router tanpa NAT, router melepaskan header dan trailer Layer 2 dari frame yang diterima, memeriksa header IP, kemudian membuat frame Layer 2 baru untuk tautan keluar. Oleh karena itu, alamat MAC sumber dan tujuan serta Frame Check Sequence berubah. Pada header IPv4, alamat IP sumber dan tujuan tetap, tetapi TTL dikurangi satu dan header checksum IPv4 dihitung ulang. Header Transport, termasuk nomor port, pada umumnya tetap, dan data aplikasi juga tidak berubah. Dengan demikian, enkapsulasi Layer 2 berubah pada setiap jaringan yang dirutekan, sedangkan identitas IP sumber dan tujuan dipertahankan secara end-to-end selama tidak terdapat NAT, proxy, atau mekanisme penerjemahan lainnya 

15. Jelaskan perubahan analisis apabila router tersebut juga melakukan NAT/PAT. Jika router melakukan NAT/PAT, router tetap mengganti enkapsulasi Layer 2, mengurangi TTL, dan memperbarui checksum IPv4 seperti router biasa. Namun, router juga melakukan perubahan tambahan berikut: 

   - a. NAT mengubah alamat IP, misalnya alamat IP sumber privat menjadi alamat IP publik. 

   - b. PAT dapat mengubah nomor port, misalnya port sumber internal menjadi port publik yang berbeda. 

   - c. Checksum IPv4 harus diperbarui karena alamat IP dan TTL berubah. 

   - d. Checksum TCP atau UDP harus diperbarui karena alamat IP dan nomor port dapat berubah. 

   - e. Router menyimpan tabel NAT/PAT agar paket respons dapat diterjemahkan kembali ke alamat dan port internal yang sesuai. 

   - f. Alamat MAC dan FCS tetap dibuat ulang karena paket dibungkus dalam frame Layer 2 baru. 

   - g. Data aplikasi biasanya tetap, kecuali terdapat mekanisme perantara yang secara khusus memodifikasi komunikasi. 

16. Sebuah capture menunjukkan checksum TCP salah pada paket keluar, tetapi tidak ada gangguan komunikasi. Ajukan hipotesis yang berkaitan dengan NIC offload. Checksum TCP yang terlihat salah pada paket keluar, sementara komunikasi tetap berjalan normal, kemungkinan besar disebabkan oleh fitur TCP checksum offload pada NIC. Dalam mekanisme ini, sistem operasi menyerahkan perhitungan checksum akhir kepada kartu jaringan. Wireshark menangkap paket sebelum paket diproses oleh NIC, sehingga nilai checksum yang terlihat pada capture masih belum final dan dapat ditandai sebagai salah. Sesaat sebelum paket benar-benar dikirim ke media, NIC menghitung atau melengkapi checksum menjadi nilai yang benar. Hipotesis ini dapat diuji dengan melakukan capture pada titik setelah NIC, membandingkan paket keluar dan masuk, memeriksa pengaturan offload, atau menonaktifkan checksum offload sementara untuk pengujian. Namun, checksum salah tidak boleh langsung diabaikan jika kesalahan juga terlihat pada titik jaringan lain, terjadi retransmisi, atau komunikasi mengalami gangguan 

17. Pengguna dapat membuka portal dengan alamat IP, tetapi tidak dengan nama. Gunakan model lapisan untuk menyusun diagnosis. Jika portal dapat dibuka menggunakan alamat IP tetapi tidak menggunakan nama, konektivitas pada Physical, Link, Internet, dan kemungkinan Transport layer telah berfungsi. Masalah paling mungkin berada pada Application layer, khususnya proses resolusi DNS. Diagnosis dilakukan dengan memeriksa konfigurasi server DNS melalui ipconfig /all, menguji resolusi nama menggunakan nslookup, membandingkan alamat hasil DNS dengan alamat portal yang benar, membersihkan cache DNS, memeriksa file hosts, serta memastikan kueri DNS tidak diblokir oleh firewall atau kebijakan jaringan. Jika nama portal hanya tersedia pada DNS internal, koneksi jaringan atau VPN yang sesuai juga harus diperiksa. Apabila nslookup berhasil tetapi portal tetap tidak dapat dibuka, pemeriksaan dilanjutkan ke TLS, sertifikat, konfigurasi virtual host, proxy, dan aplikasi. Dengan demikian, keberhasilan akses melalui alamat IP mempersempit diagnosis ke layanan penamaan atau fungsi lapisan atas, bukan langsung dianggap sebagai kegagalan jaringan secara keseluruha 

18. Ping ke server berhasil, tetapi HTTPS gagal. Susun sedikitnya enam hipotesis pada lapisan Transport hingga Application. 

|a.|Hipotesis 1: Port TCP|443 tertutup|
|---|---|---|
||ICMP|: diizinkan|
||TCP port 443|: tertutup|
||Hasil ping|: berhasil|
||Hasil HTTPS|: gagal|



Hal ini dapat terjadi karena: 

- layanan HTTPS belum dikonfigurasi 

- server web tidak mendengarkan pada port 443 

- konfigurasi port salah 

- layanan hanya berjalan pada port lain 

- layanan HTTPS berhenti 

Jika port tertutup, server dapat menolak koneksi dengan mengirimkan TCP Reset atau koneksi langsung gagal. 

b. Firewall atau ACL memblokir TCP port 443 Aturan firewall: ICMP Echo Request  → Allow ICMP Echo Reply    → Allow TCP Destination 443 → Deny 

Pemblokiran dapat terjadi pada: 

- firewall di komputer pengguna; 

- firewall jaringan; 

- router; 

- firewall server; 

- stateful firewall; 

   - kebijakan jaringan kampus; 

   - perangkat keamanan di antara pengguna dan server. 

- c. Sertifikat TLS tidak valid 

Server dapat dijangkau dan TLS handshake dapat dimulai, tetapi peramban menolak sertifikat server. Masalah sertifikat dapat berupa: 

- sertifikat kedaluwarsa 

- sertifikat belum berlaku 

- nama domain tidak cocok dengan nama pada sertifikat 

- sertifikat ditandatangani otoritas yang tidak dipercaya 

- rantai sertifikat tidak lengkap 

- sertifikat telah dicabut 

- sertifikat diterbitkan untuk nama server yang berbeda 

d. Sesi pengguna atau token tidak valid Koneksi TCP dan TLS dapat berhasil, tetapi pengguna tetap tidak bisa menggunakan portal karena sesi aplikasi gagal. Masalahnya dapat berupa: 

   - token sesi kedaluwarsa 

   - cookie tidak valid 

   - cookie diblokir 

   - sesi pada server sudah dihapus 

   - pengguna belum terautentikasi 

   - waktu token tidak sesuai 

   - state sesi antara server dan klien tidak cocok 

- e. Layanan web HTTPS berhenti atau salah konfigurasi Kemungkinan penyebabnya: 

   - web server berhenti 

   - proses aplikasi mengalami crash 

   - layanan belum dijalankan 

   - server web mendengarkan pada alamat atau port yang salah 

   - konfigurasi virtual host salah 

   - konfigurasi HTTPS belum diaktifkan 

   - aplikasi gagal dimuat 

Ping hanya membuktikan bahwa perangkat dapat memberikan respons ICMP. Ping tidak menguji kesehatan proses aplikasi. Repositori menegaskan bahwa ketika koneksi Transport terbentuk tetapi transaksi HTTP gagal, diagnosis harus bergerak ke lapisan Application dan memeriksa status HTTP serta log server 

f. Kesalahan konfigurasi nama domain atau virtual host Server web dapat menjalankan beberapa situs dengan satu alamat IP. Nama domain digunakan untuk menentukan situs atau virtual host yang harus melayani permintaan. Kemungkinan masalah: 

   - nama domain mengarah ke server yang salah 

   - virtual host untuk nama portal tidak tersedia 

   - konfigurasi nama host tidak cocok 

   - SNI mengarah ke konfigurasi TLS yang salah 

   - record DNS menunjuk ke alamat lama 

   - portal hanya bisa diakses menggunakan nama tertentu 

19. Bandingkan sesi aplikasi dengan koneksi TCP. Berikan contoh ketika sesi bertahan setelah koneksi berubah. 

Koneksi TCP adalah hubungan komunikasi pada Transport layer yang menyediakan aliran byte andal, pengurutan, retransmisi, kontrol aliran, dan kontrol kemacetan. Koneksi tersebut dikenali berdasarkan alamat IP dan nomor port kedua endpoint. Sementara itu, sesi aplikasi merupakan konteks hubungan pengguna dengan suatu layanan yang dapat menyimpan status login, identitas, hak akses, atau aktivitas pengguna. Sesi biasanya dikenali menggunakan cookie, Session ID, atau token. Satu sesi aplikasi dapat menggunakan beberapa koneksi TCP, sehingga berakhirnya koneksi TCP tidak selalu mengakhiri sesi. Sebagai contoh, setelah pengguna login ke portal, server memberikan token sesi. Ketika koneksi TCP terputus dan peramban membuat koneksi TCP baru dengan port sumber berbeda, token yang sama dapat dikirimkan kembali. Jika masih valid, server tetap mengenali pengguna sebagai pengguna yang sudah login. Dengan demikian, koneksi TCP mempertahankan keadaan komunikasi Transport, sedangkan sesi aplikasi mempertahankan konteks aktivitas pengguna pada lapisan aplikasi 

20. Jelaskan mengapa enkripsi tidak dapat selalu ditempatkan secara mutlak pada Presentation layer. 

Enkripsi tidak dapat selalu ditempatkan secara mutlak pada Presentation layer karena teknologi enkripsi dapat bekerja pada beberapa lapisan sesuai fungsi dan cakupan perlindungannya. Enkripsi memang sering dipetakan ke Presentation layer karena lapisan tersebut menangani transformasi representasi data. Namun, MACsec dan keamanan Wi-Fi melindungi komunikasi pada Link layer, IPsec bekerja pada Internet layer, TLS secara tradisional berada di antara Application dan Transport, sedangkan aplikasi dapat mengenkripsi langsung data sebelum diserahkan ke jaringan. Oleh karena itu, posisi enkripsi harus ditentukan berdasarkan aset yang dilindungi, titik dimulainya enkripsi, titik terminasi atau dekripsi, cakupan jalur yang diamankan, ancaman yang dihadapi, dan metadata yang masih terlihat. Model lapisan digunakan sebagai alat analisis, bukan aturan mutlak yang mengharuskan semua mekanisme enkripsi berada pada satu lapisan 

