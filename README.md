# Labs5
<body>
    <table border="1">
        <tr>
            <th> Nama</th>
            <th>NIM</th>
            <th>Kelas</th>
        </tr>
        <tr>
            <td>Muhamad Suryanegara</td>
            <td>312110447</td>
            <td>TI.21.A.1</td>
        </tr>
    </table>
</body>

# Dictonary Python

## Tugas Latihan
- <b>Soal</b><p>
![soal](https://user-images.githubusercontent.com/92678339/145685857-e3d0b30e-d9fe-460f-9c49-cbfed08cf175.png)
<p>

- <b>Codiingan</b><p>
```bash
# Latihan 1

a = {'Ari':'081267888', 'Dina':'087654588'}  # Nama sebagai key, dan nomor sebagai value
print ("Buat Dictionary daftar kontak")
print ("Nama | Nomor Telpon")

print ("Menampilkan dictonary kontak")
print (a)
print (50*"-")

print ("Tampilkan kontak Ari")
print (a['Ari']) #Tampilkan kontak Ari
print (50*"-")

print ("Menambah kontak baru dengan nama Riko, nomor 087654544")
a.update({'Riko':'087654544'}) #Menambah kontak baru dengan nama Riko, nomor 087654544
print (a)
print (50*"-")

print ("mengubah kontak Dina dengan nomor baru 088999776")
a['Dina'] = '088999776' # mengubah kontak Dina dengan nomor baru 088999776
print (a)
print (50*"-")

print ("Tampilkan semua nama")
print(a.keys()) #Tampilkan semua nama
print (50*"-")

print ("Tampilkan semua nomor")
print(a.values()) #Tampilkan semua nomor
print (50*"-")

print ("Tampilkan daftar Nama dan nomornya")
print (a.items()) #Tampilkan daftar Nama dan nomornya
print (50*"-")

print ("Menghapus kontak Dina")
del a['Dina'] #Menghapus kontak Dina
print(a)
```
- <b>Tampilan Hasil Program</b><p>
![Screenshot (91)](https://user-images.githubusercontent.com/92678339/145685884-ec5d1523-18c3-48be-9c7a-1cd94bffae8f.png)<p>


## Tugas Pratikum
- <b>Soal</b><p>
![latihan 2](https://user-images.githubusercontent.com/92678339/145685979-b18eb2ab-27f2-4e61-87e4-5924e186a79f.png)<p>

- <b>Codingan</b><p>

```bash
x = {}

while True:
    header="PROGRAM INPUT NILAI MAHASISWA"
    print(header.center(97,"="))
    print()
    print("[ (L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar")
    c = input("Masukkan Pilihan: ")

    if c == 'T' or c == 't':
        print("TAMBAH DATA")
        nim = int(input("Masukkan NIM\t\t: "))
        nama = input("Masukkan Nama\t\t: ")
        tugas = int(input("Masukkan Nilai Tugas\t: "))
        uts = int(input("Masukkan Nilai UTS\t: "))
        uas = int(input("Masukkan Nilai UAS\t: "))
        akhir = tugas*.3 + uts*.35 + uas*.35
        x[nama] = nim, uts, uas, tugas, akhir

    elif c == 'U' or c == 'u':
        print("UBAH DATA")
        print("Cari Data Mahasiswa Menggunakan Nama")
        nama = input("Masukkan Nama Mahasiswa: ")
        if nama in x.keys():
            nim = int(input("Masukkan NIM yang benar\t\t: "))
            tugas = int(input("Masukkan Nilai Tugas yang benar\t: "))
            uts = int(input("Masukkan Nilai UTS yang benar\t: "))
            uas = int(input("Masukkan Nilai UAS yang benar\t: "))
            akhir = tugas*.3 + uts*.35 + uas*.35
            x[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))

    elif c == 'h' or c == 'H':
        print("HAPUS DATA")
        nama = input("Masukkan Nama untuk menghapus: ")
        if nama in x.keys():
            del x[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

    elif c == 'C' or c == 'c':
        print("CARI DATA")
        nama = input("Masukkan Nama : ")
        if nama in x.keys():
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

    elif c == 'L' or c == 'l':
        if x.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for z in x.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" * 78)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)

    elif c. lower() == 'k':
        break

    else:
        print("Pilih menu yang tersedia")

```
- <b>Hasil Program</b><p>
![Screenshot (93)](https://user-images.githubusercontent.com/92678339/145686165-d0ff479f-6569-4a6e-a4c6-9d0bc99cbfc1.png)
<p>

# TERIMAKASIH :)
