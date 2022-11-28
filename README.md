# PRATIKUM 6
### Latihan 1
```
telp = {}
telp['Ari'] = '081267888'
telp['Dina'] = '087677776'
print(telp['Ari'])
telp['Riko'] = '087654544'
telp['Dina'] = '088999776'
print(telp.keys())
print(telp.values())
print(telp.items())
telp.pop('Dina')
print(telp.items())
```
![gambar](gambar/gam1.png)
## Tugas Praktikum
### Daftar Nilai Mahasiswa Menggunakan **Dictionary**
- Pertama kita membuat sebuah dictionary kosong yang nantinya akan diinputkan data ketika program dijalankan.
```
data = {}
```
- Lalu kita membuat kondisi perulangan dan sebuah keterangan untuk pilihan menu yang akan menjalankan program.
```
while True:
    v = input("\n(T)ambah, (U)bah, (H)apus, (C)ari, (L)ihat, (K)eluar: ")
```
- Membuat syntax untuk menambahkan data.
```
if v.lower() == 't':
        print("Tambah Data")
        nama = input("Nama           : ")
        nim = int(input("NIM            : "))
        uts = int(input("Nilai UTS      : "))
        uas = int(input("Nilai UAS      : "))
        tugas = int(input("Nilai Tugas    : "))
        akhir = tugas*30/100 + uts*35/100 + uas*35/100
        data[nama] = nim, uts, uas, tugas, akhir
```
- Di atas merupakan program (t) dibuat untuk menambahkan inputan yang akan kita isi nantinya dimana sudah di inputkan dari ( nama,nim,uts,uas,tugas) lalu dari nilai (uts,uas,tugas) dibuat nilai pembagian yang menjadi hasil akhir dari penginputan nilai.
- Membuat syntax untuk mengubah data.
```
 elif v.lower() == 'u':
        print("Ubah Data")
        nama = input("Masukkan Nama  : ")
        if nama in data.keys():
            nim = int(input("NIM            : "))
            uts = int(input("Nilai UTS      : "))
            uas = int(input("Nilai UAS      : "))
            tugas = int(input("Nilai Tugas    : "))
            akhir = tugas * 30 / 100 + uts * 35 / 100 + uas * 35 / 100
            data[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))

```
- Di atas adalah program  'u' dimana apabila kita ingin mengubah keterangan data dan kita akan diminta untuk menginputkan nama yang mau diubah datanya, apabila nama tidak ada maka outputnya "Nama {} tidak ditemukan". Dimana ```{}``` adalah nama/data yang mau kita ubah.

- Membuat syntax untuk menghapus data.
```
elif v.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama  : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```
- Jika kita menginput 'h' maka kita akan diminta menginput nama yang akan dihapus. Jika nama ada di dalam dictionary, maka system akan menghapus keys/nama tersebut beserta valuesnya pada statement ```del Data[nama]```.

- Membuat syntax untuk mencari data
```
elif v.lower() == 'c':
        print("Cari Data")
        nama = input("Masukkan Nama : ")
        if nama in data.keys():
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
```
- Jika kita menginputkan 'c' maka kita akan diminta untuk memasukkan nama yang akan dicari. Apabila nama yang dicari ada di dalam dictionary maka outputnya akan menampilkan data dari nama tersebut.

- Membuat syntax untuk melihat atau menampilkan data.
```
elif v.lower() == 'l':
        if Data.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for j in Data.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(j[0][:13], j[1][0], j[1][1], j[1][2], j[1][3], j[1][4], no=i))
            print("=" * 78)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)
```
- Jika kita menginput 'l' maka sistem akan menampilkan data - data yang sudah kita masukkan. Jika kita belum memasukkan data maka outputnya menjadi "TIDAK ADA DATA".

- Membuat syntax untuk menghentikan perulangan.
```
 elif v.lower() == 'k':
            break
```
- Jika kita menginput 'k' maka program akan langsung berhenti.

- Membuat syntax untuk apabila memilih pilihan yang tidak ada di menu.
```
 else:
        print("Pilih menu yang tersedia")
```
- Jika kita menginputkan selain yang ada pada menu (t, u, h, c, l, k) maka kita akan diminta untuk memilih menu yang tersedia.
![Gambar1](gambar/gam2.png)
