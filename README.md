##PRAKTIKUM 6
```py
mahasiswa = {}

def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
            .format (a[0][: 14],a[1][0],a[1][1],a[1][2],a[1][3],a[1][4], no = i))
        print("=================================================================================")
        
    else:
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                                TIDAK ADA DATA                                 |")
        print("=================================================================================")

def add():
    print("Tambah Data")
    nama = input("Nama\t : ")
    nim = input("NIM\t : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir

def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")
    
    if nama in mahasiswa.keys():
        del mahasiswa[nama]
    
    else:
        print("Nama tidak ditemukan")

def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")

def search():
    print("Cari Data")
    a = input("Masukkan Nama : ")
    if a in mahasiswa.keys():
        print("===========================================================================")
        print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
        print("===========================================================================")
        print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
            .format (a , mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4] ))
        print("===========================================================================")

    else:
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                          DATA TIDAK DITEMUKAN                                 |")
        print("=================================================================================")

def menu():
    print("\n")
    print("================================")
    print("      Program input nilai       ")
    print("================================\n")

    x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
    print("\n")

    if x == 'L':
        show()
    elif x == 'T':
        add()
    elif x == 'U':
        update()
    elif x == 'H':
        delete()
    elif x == 'C':
        search()
    elif x == 'K':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")

while True:

    menu()
```
Output : 
        ![Screenshot_20221128_121145](https://user-images.githubusercontent.com/115573041/204199401-0f05f9f9-15b2-4dfa-a8e1-1c2007469051.png)
        

## LATIHAN 1
```py        
print("========== LATIHAN 1 - DICTIONARY ==========")
print()
r = {'Ari' : '081267888', 'Dina' : '087677776'}
print("# Daftar Kontak :\n", r)
print()

#Menampilkan Kontak
print("# Menampilkan kontak Ari : 081267888")
print("~~~~~~~~~~~~~~~~~~~~~~~~~")

#Menambahkan kontak baru
print("# Menambahkan kontak baru\n", r)
print("Daftar kontak sebelumnya :\n", r)
r['Riko']= '087654544';
print("Daftar kontak setelah ditambahkan :\n", r)
print("~~~~~~~~~~~~~~~~~~~~~~~~~")

#Mengubah kontak Dina
print("# Mengubah Kontak Dina\n")
print("Daftar Kontak Dina Sebelumnya :\n", r)
r['Dina'] = '088999776'
print("Daftar Kontak Dina Setelah Diubah :\n", r)
print("~~~~~~~~~~~~~~~~~~~~~~~~~")

#Menampilkan semua nama
print("# Menampilkan Semua Nama Kontak :\n")
print(r.keys())
print("~~~~~~~~~~~~~~~~~~~~~~~~~")

#Menampilkan semua nomor
print("# Menampilkan Semua Nomor :\n")
print(r.values())
print("~~~~~~~~~~~~~~~~~~~~~~~~~")

#Menampilkan Keseluruhan
print("# Daftar Kontak Keseluruhan :\n")
print(r.items())
print("~~~~~~~~~~~~~~~~~~~~~~~~~")

#Menghapus Kontak Dina
print("# Menghapus Kontak Dina\n")
print("Daftar Kontak Sebelumnya :\n", r)
del r['Dina'];
print("Daftar Kontak Setelah Dihapus :\n", r)
```
![Screenshot_20221122_013100](https://user-images.githubusercontent.com/115573041/204199614-6a6dd671-666d-4ae9-89ec-1f9a2f6b3f3c.png)
