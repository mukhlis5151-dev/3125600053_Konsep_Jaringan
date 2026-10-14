# **KONSEP JARINGAN** 

# **PHYSICAL LAYER** 



<!-- Start of picture text -->
ol:ae<br>pens<br><!-- End of picture text -->

Nama : Imam Mukhlis Nur Ismail NRP : 3125600053 Dosen Pengajar : Dr Ferry Astika Saputra ST, M.Sc 

## **PROGRAM STUDI D4 TEKNIK INFORMATIKA** 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA (PENS)** 

## **2026** 

## **A. SOURCE CODE** 

<mark>import argparse import numpy as np import matplotlib.pyplot as plt</mark> 

def jumlah_harmonisa(theta, nmax): 

<mark>"""Jumlah harmonisa ganjil 1,3,5,...,nmax (amplitudo 1/n), dinormalisasi 4/pi.""" y = np.zeros_like(theta) for n in range(1, nmax + 1, 2): y += np.sin(n * theta) / n return 4 / np.pi * y</mark> def main(): p = argparse.ArgumentParser(description="Visualisasi penjumlahan harmonisa ganjil") p.add_argument("--nmax", type=int, default=9, help="harmonisa tertinggi (ganjil), default 9") p.add_argument("--fasa", type=float, default=60, help="pergeseran fasa I terhadap V (derajat), default 60") p.add_argument("--siklus", type=float, default=2, help="jumlah siklus yang ditampilkan, default 2") <mark>args = p.parse_args() if args.nmax % 2 == 0: args.nmax += 1 # pastikan ganjil phi = np.deg2rad(args.fasa) theta = np.linspace(0, 2 * np.pi * args.siklus, 3000) V = np.sin(theta)</mark> # Pergeseran fasa dasar phi -> harmonisa ke-n bergeser n*phi, supaya bentuk gelombang tetap utuh <mark>I = jumlah_harmonisa(theta - phi, args.nmax) # ---------- Grafk 1: V dan I seperti pada gambar ----------</mark> i <mark>fg1</mark> i <mark>, ax = plt.subplots(fgsize</mark> i <mark>=(10, 4)) ax.plot(theta, V, "k-", lw=1.8, label="V (sinus murni)") ax.plot(theta, I, "k:", lw=1.8, label=f"I (harmonisa 1..{args.nmax})") ax.axhline(0, color="k", lw=1) ax.set_xlabel("ωt (radian)") ax.set_ylabel("Amplitudo")</mark> ax.set_title(f"Tegangan V dan arus I - jumlah harmonisa ganjil sampai ke{args.nmax}") 

<mark>ax.legend(loc="upper right") ax.set_facecolor("#e8e8e8") ax.grid(alpha=0.3) fg1</mark> i <mark>.tight_layout()</mark> 

<mark># ---------- Grafk 2: proses penjumlahan ----------</mark> i <mark>t = np.linspace(0, 2 * np.pi * args.siklus, 3000) ganjil = list(range(1, args.nmax + 1, 2)) fg2</mark> i <mark>, axs = plt.subplots(len(ganjil), 2, fgsize</mark> i <mark>=(11, 1.8 * len(ganjil)), sharex=True) axs = np.atleast_2d(axs) for i, n in enumerate(ganjil): komponen = 4 / np.pi * np.sin(n * t) / n total = jumlah_harmonisa(t, n) axs[i, 0].plot(t, komponen, "b") axs[i, 0].set_ylabel(f"n={n}") axs[i, 1].plot(t, total, "r") axs[i, 1].axhline(0, color="k", lw=0.5) axs[i, 0].grid(alpha=0.3) axs[i, 1].grid(alpha=0.3) axs[0, 0].set_title("Harmonisa ke-n (satu komponen)") axs[0, 1].set_title("Jumlah harmonisa sampai ke-n") axs[-1, 0].set_xlabel("ωt (radian)") axs[-1, 1].set_xlabel("ωt (radian)") fg2</mark> i <mark>.tight_layout() plt.show()</mark> if __name__ == "__main__": <mark>main()</mark> 



<!-- Start of picture text -->
Faw =o x<br>Tegangan V dan arus |-jumlah harmonisa ganjil sampai ke-9<br>2HH<br><i i<br>3 2 a ust radian)6 3 10 2B<br>HEP HFQE<br><!-- End of picture text -->



<!-- Start of picture text -->
[= fot al > 5 x<br>Harmonisa ke-n (satu komponen) Jumlah harmonisa sampai ke-n<br>1 1<br>a a<br>V\ZF\ ID. fr<br>oa z<br>02<br>Z 00 °<br>02<br>-04 a<br>02 1<br>2 00 °<br>-02 a<br>02<br>1<br>on<br>7 00 °<br>-01<br>a<br>-02<br>o1 ’<br>2 00 °<br>-o1 i”<br>of 4 6 8 @ @ $2 4 6 8 1 w<br>ut radian ustiradian)<br>BE Q search — mOgcgaa<br><!-- End of picture text -->

**B. OUTPUT** 

