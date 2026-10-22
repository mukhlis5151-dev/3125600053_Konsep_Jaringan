**KONSEP JARINGAN**

**TUGAS 6**

<img
src="G:\My Drive\Tugas Semester 3\Konsep Jaringan\Tugas 6 Konsep Jaringan_files/media/image1.png"
style="width:4.74097in;height:3.3625in" />

> Nama : Imam Mukhlis Nur Ismail
>
> NRP : 3125600053
>
> Dosen Pengajar : Dr Ferry Astika Saputra ST, M.Sc

**PROGRAM STUDI D4 TEKNIK INFORMATIKA**

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA (PENS)**

**2026**

Sebuah kampus memiliki alokasi jaringan 10.252.108.0/24 yag kemudian
dibagi menjadi empat segmen dengan kebutuhan host sebagai berikut.

- Laboratorium A: 90 host

- Laboratorium B: 60 host

- Administrasi: 14 host

- End-point: 2 endpoint

> Tentukan untuk setiap segmen

- IP Network

- Host pertama

- Host terakhir

- Broadcast

- Subnet Mask (prefix baru)

- Jumlah host yang tersedia

1.  Laboratorium A: 90 host

2^6 – 2 = 90 🡺 geser 1 bit

128 64 32 16 8 4 2 1

0 1 1 1 1 1 1 1

| IP Network | Host pertama | Host terakhir | Broadcast | Subnet Mask | Jumlah host |
|:---|----|----|----|----|----|
| 10.252.108.0 | 10.252.108.1 | 10.252.108.126 | 10.252.108.127 | /25 | 126 |

2.  Laboratorium B: 60 host

2^5 – 2 = 60 🡺 geser 2 bit

128 64 32 16 8 4 2 1

0 0 1 1 1 1 1 1

| IP Network | Host pertama | Host terakhir | Broadcast | Subnet Mask | Jumlah host |
|:---|----|----|----|----|----|
| 10.252.108.128 | 10.252.108.129 | 10.252.108.190 | 10.252.108.191 | /26 | 62 |

3.  Administrasi: 14 host

2^4 – 2 = 14 🡺 geser 4 bit

128 64 32 16 8 4 2 1

0 0 0 0 1 1 1 1

| IP Network | Host pertama | Host terakhir | Broadcast | Subnet Mask | Jumlah host |
|:---|----|----|----|----|----|
| 10.252.108.192 | 10.252.108.193 | 10.252.108.206 | 10.252.108.207 | /28 | 14 |

4.  End-point (2 endpoint)

2^2 – 2 = 2 endpoint 🡺 geser 6 bit

128 64 32 16 8 4 2 1

0 0 0 0 0 0 1 1

| IP Network | Host pertama | Host terakhir | Broadcast | Subnet Mask | Jumlah host |
|:---|----|----|----|----|----|
| 10.252.108.208 | 10.252.108.209 | 10.252.108.210 | 10.252.108.211 | /30 | 2 |
