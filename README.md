# UAS-Semester-1

NAMA  : MUHAMMAD ILHAM MUBAROK

KELAS : TI.20.A2

NIM   : 312010278

Soal UAS diantaranya;

![screen 1](/gambar/screen1.png)

hasil package

 ![screen 2](/gambar/screen2.png)


SOAL 1 (Daftar_Nilai)

Pada soal pertama, dibawah ini saya telah menyantumkan beberapa syntax yang nantinya akan menghasilkan semua
modul dari package Daftar_Nilai yang diantaranya adalah (Tambah Data, Ubah Data, Hapus Data, Dan Cari Data)


P = print
while True:
    P("")
    P("")
    c = input("L)ihat, T)ambah, U)bah, H)apus, C)ari, K)eluar: ")
    if c.lower() == 'q':
        break
    elif c.lower() == 'l':
        i = open('database.txt','r').read().splitlines()
        P(" ╔═════════════════════════════════════════════════════════════════════╗")
        P(" ╠════════════════════════════ DAFTAR KONTAK ══════════════════════════╣")
        P(" ╠══════════════════╦══════════════════╦═══════╦═══════╦═══════╦═══════╣")
        P(" ║      NAMA        ║       NIM        ║ TUGAS ║  UTS  ║  UAS  ║ AKHIR ║")
        P(" ╠══════════════════╬══════════════════╬═══════╬═══════╬═══════╬═══════╣")
        for l in i:
            if l == '':
                pass
            else:
                l1 = l.replace('Nama : ','').replace('Nim : ','').replace('Tugas : ','').replace('UTS : ','').replace('UAS : ','').replace('Akhir : ','')
                na,ni,tu,uts,uas,akhir = l1.strip().split('|')
                P((' ║ ')+(na[:15]).ljust(17,'.')+('║ ')+(ni).ljust(17)+('║ ')+(tu).ljust(6)+('║ ')+(uts).ljust(6)+('║ ')+(uas).ljust(6)+('║ ')+(akhir).ljust(6)+('║'))
        P(" ╚══════════════════╩══════════════════╩═══════╩═══════╩═══════╩═══════╝")
		
		
		