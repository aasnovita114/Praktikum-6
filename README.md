# praktikum-6
Nama : Aas novitasari
NIM : 312210167
Kelas : TI.22.A1
Latihan
Buat Dictionary daftar kontak

Nama sebagai key, dan nomor sebagai value
Tampilkan kontaknya Ari
Tambah kontak baru dengan nama Riko, nomor 087654544
Ubah kontak Dina dengan nomor baru 088999776
Tampilkan semua Nama
Tampilkan semua Nomor
Tampilkan daftar Nama dan nomornya
Hapus kontak Dina
Langkah-langkah :
Buat program terlebih dahulu seperti gambar di bawah ini
![latihan1](https://user-images.githubusercontent.com/116045324/204202403-10e235a6-f573-4ec2-b682-fe48973e38c5.PNG)


daftarKontak = {"Nama":"Nomer Telpon"}
kontak       = {'Ari':'081267888', 'Dina' : '087677776'}

#print
print(30*"═")
print("    Nama    |  Nomor Telepon  ") #prinr daftarkontak
print(30*"-")
print("   # Ari    | ", kontak['Ari']) #print kontak Ari
print("   # Dina   | ", kontak['Dina']) #print kontak Dina
print(30*"═")

#Tampilkan kontaknya Ari
print("Tampilkan kontaknya Ari")
print("    Ari     | ", kontak['Ari']) #print kontak Ari
print(30*"═")
#Tambah kontak baru dengan nama Riko, nomor 087654544
print("Tambah kontak baru dengan nama Riko, nomor 087654544")
kontak['Riko'] = '087654544'
print("    Riko    | ", kontak['Riko'])
print(30*"═")

#Ubah kontak Dina dengan nomor baru 088999776
print("Ubah kontak Dina dengan nomor baru 088999776")
kontak['Dina'] = '088999776'
print("    Dina    | ", kontak['Dina'])
print(30*"═")

#Tampilkan semua Nama
print("Tampilkan semua Nama")
print(kontak.keys())
print(30*"═")

#Tampilkan semua Nomor
print("Tampilkan semua Nomor")
print(kontak.values())
print(30*"═")

#Tampilkan daftar Nama dan nomornya
print("Tampilkan daftar Nama dan nomornya")
print(kontak.items())
print(30*"═")

#MengHapus kontak Dina
print("Hapus kontak Dina")
kontak.pop('Dina')
print(kontak.items())
print(30*"═")
Hasil Run
![hasilrunlatihan1](https://user-images.githubusercontent.com/116045324/204202600-82d2f648-d835-410f-91f2-dff725e145f2.PNG)

![hasilrunlatihan-1](https://user-images.githubusercontent.com/116045324/204202631-ab54f9ad-4fb8-46be-a978-d4a94dd059ee.PNG)

Praktikum 5
Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan :

Program dibuat dengan menggunakan Dictionary
Tampilkan menu pilihan : (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas : 30%, UTS : 35%, UAS : 35%)
Buat flowchart dan penjelasan programnya pada README.md.
Commit dan push repository ke github.
Langkah-langkah :
Buat programnya terlebih dahulu seperti gambar di bawah ini
![latihan2](https://user-images.githubusercontent.com/116045324/204202758-708dd889-fbb0-44e5-a691-fa9a5a79e43e.PNG)

print("====================================")
print("======>  Program Input Nilai  <======")
print("====================================")
data = {}
while True:
    print("")
    m = input("===>> (L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : <=== ")
    print("================================================================")
    print("| NO |  Nama     |   Nim    |  Tugas  |  UTS  |  UAS  |   Akir |")
    print("================================================================")
    print(">>>>>>>>>>>>>>>>>>>>>>>> TIDAK ADA DATA <<<<<<<<<<<<<<<<<<<<<<<<")
    if m.lower() == 'k':
        break

    elif m.lower() == 'l':
        print("----- DAFTAR NILAI -----")
        print("==================================================================================")
        print("| NO |   NAMA     |   NIM        |  TUGAS   |   UTS     |   UAS      |  AKHIR    |")
        print("==================================================================================")
        i = 0
        for x in data.items():
            i += 1
            print("|  1 |{0:9}   |{1:9}     |{2:9} |{3:9}  |{4:9}   |{5:9}  |" .format(x[0], x[1][0],
                                                                                       x[1][1], x[1][2], x[1][3],
                                                                                       x[1][4], i))

        else:
            print("====================>>>>>>>>>>>>> Tidak Ada Data <<<<<<<<<<<<<====================")

    elif m.lower() == 't':
        print("--------------- Tambah Data ---------------")
        nama = input("Nama                  : ")
        nim = input("Nim                   : ")
        tugas = float(input("Masukan Nilai Tugas   : "))
        uts = float(input("Masukan Nilai UTS     : "))
        uas = float(input("Masukan Nilai UAS     : "))
        akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
        data[nama] = nim, tugas, uts, uas, akhir

    elif m.lower() == 'u':
        print("----- Ubah Data Mahasiswa -----")
        nama = input("Nama  : ")
        if nama in data.keys():
            nim = input("Nim : ")
            tugas = float(input("masukan nilai tugas : "))
            uts = float(input("masukan nilai Uts : "))
            uas = float(input("masukan nilai uas : "))
            akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
            data[nama] = nim, tugas, uts, uas, akhir

        else:
            print("Tidak Ada data")

    elif m.lower() == 'h':
        print("Hapus Data Mahasiswa")
        nama = input("nama : ")
        if nama in data.keys():
            print("Datanya", nama, "adalah {0}".format(data[nama]))
        else:
            print("Tidaak Ada Data")

    else:
        print("Pilih menu yang tersedia")
Hasil Run
![hasilrunlatihan2](https://user-images.githubusercontent.com/116045324/204202814-4d982a60-c501-4c0e-9f6d-043379eb9cd0.PNG)
![hasilrunlatihan-2](https://user-images.githubusercontent.com/116045324/204202875-0de6189a-7f74-454e-8b40-f2329f69fa12.PNG)


Penjelasan Program :
Buatlah Dictionary berupa Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS.
Lalu
#flowchart
![image](https://user-images.githubusercontent.com/116045324/204203436-7800e2b2-71bd-4cba-b6de-e6c66397620b.png)
