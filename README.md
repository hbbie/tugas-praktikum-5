# tugas-praktikum-5
# Tugas Pertemuan 9
# Biodata
Nama  :Dhani Naufal Habibie
NIM   :312410300
Kelas :TI.24.A.4



# Latihan 1

![Screenshot 2024-11-16 193431](https://github.com/user-attachments/assets/577c5552-78e9-49c7-aa84-bb3f1a7d1a24)


```python 
daftar_kontak = {}

# menampilkan semua kontak
def tampilkan_kontak():
    print("\nDaftar Kontak:")
    if daftar_kontak:
        print("Nama  | No Telpon")
        print("===================")
        for nama, nomor in daftar_kontak.items():
            print(f"{nama}    | {nomor}")
    else:
        print("Tidak ada kontak dalam daftar.")

# Tambah kontak
def tambah_kontak():
    nama = input("Masukkan nama kontak: ")
    nomor = input("Masukkan nomor telepon: ")
    daftar_kontak[nama] = nomor
    print(f"Kontak {nama} berhasil ditambahkan.")

# Ubah kontak
def ubah_kontak():
    nama = input("Masukkan nama kontak yang ingin diubah: ")
    if nama in daftar_kontak:
        nomor_baru = input(f"Masukkan nomor baru untuk {nama}: ")
        daftar_kontak[nama] = nomor_baru
        print(f"Kontak {nama} berhasil diubah.")
    else:
        print(f"Kontak {nama} tidak ditemukan.")

# Hapus kontak
def hapus_kontak():
    nama = input("Masukkan nama kontak yang ingin dihapus: ")
    if nama in daftar_kontak:
        del daftar_kontak[nama]
        print(f"Kontak {nama} berhasil dihapus.")
    else:
        print(f"Kontak {nama} tidak ditemukan.")

# Tampilkan semua nama
def tampilkan_semua_nama():
    print("\nSemua Nama:")
    for nama in daftar_kontak.keys():
        print(nama)

# Tampilkan semua nomor
def tampilkan_semua_nomor():
    print("\nSemua Nomor:")
    for nomor in daftar_kontak.values():
        print(nomor)

# menu utama
while True:
    print("\nMenu:")
    print("1. Tampilkan semua kontak")
    print("2. Tambah kontak")
    print("3. Ubah kontak")
    print("4. Hapus kontak")
    print("5. Tampilkan semua nama")
    print("6. Tampilkan semua nomor")

    pilihan = input("Masukkan pilihan (1-7): ")

    if pilihan == "1":
        tampilkan_kontak()
    elif pilihan == "2":
        tambah_kontak()
    elif pilihan == "3":
        ubah_kontak()
    elif pilihan == "4":
        hapus_kontak()
    elif pilihan == "5":
        tampilkan_semua_nama()
    elif pilihan == "6":
        tampilkan_semua_nomor()
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
    ````

Penjelasan Bagian-bagian Program:
1. Inisialisasi Dictionary kosong
```python
daftar_kontak = {}
````
Pada awalnya, kita membuat sebuah Dictionary kosong yang akan digunakan untuk menyimpan data kontak. Di dalam dictionary ini, key adalah nama kontak, dan value adalah nomor telepon dari kontak tersebut.

2. Fungsi Menampilkan Semua Kontak
```python
def tampilkan_kontak():
    print("\nDaftar Kontak:")
    if daftar_kontak:
        print("Nama  | No Telpon")
        print("===================")
        for nama, nomor in daftar_kontak.items():
            print(f"{nama}    | {nomor}")
    else:
        print("Tidak ada kontak dalam daftar.")
````

Fungsi ini digunakan untuk menampilkan seluruh kontak yang ada di dalam dictionary. Fungsi items() digunakan untuk mendapatkan pasangan key (nama) dan value (nomor). Jika dictionary kosong, akan menampilkan pesan "Tidak ada kontak dalam daftar."

3. Fungsi Menambah Kontak Baru
```python
def tambah_kontak():
    nama = input("Masukkan nama kontak: ")
    nomor = input("Masukkan nomor telepon: ")
    daftar_kontak[nama] = nomor
    print(f"Kontak {nama} berhasil ditambahkan.")
````
Fungsi ini meminta pengguna untuk menginputkan nama dan nomor telepon kontak yang ingin ditambahkan ke dalam daftar. Nilai-nilai ini kemudian disimpan ke dalam dictionary dengan nama sebagai key dan nomor sebagai value.

4. Fungsi Mengubah Kontak
```python
def ubah_kontak():
    nama = input("Masukkan nama kontak yang ingin diubah: ")
    if nama in daftar_kontak:
        nomor_baru = input(f"Masukkan nomor baru untuk {nama}: ")
        daftar_kontak[nama] = nomor_baru
        print(f"Kontak {nama} berhasil diubah.")
    else:
        print(f"Kontak {nama} tidak ditemukan.")
````
Fungsi ini memungkinkan pengguna untuk mengubah nomor telepon kontak yang sudah ada. Pertama, program meminta nama kontak yang ingin diubah. Jika kontak tersebut ditemukan dalam dictionary, maka nomor lama akan digantikan dengan nomor baru yang dimasukkan oleh pengguna.

5. Fungsi Menghapus Kontak
```python
def hapus_kontak():
    nama = input("Masukkan nama kontak yang ingin dihapus: ")
    if nama in daftar_kontak:
        del daftar_kontak[nama]
        print(f"Kontak {nama} berhasil dihapus.")
    else:
        print(f"Kontak {nama} tidak ditemukan.")
````
Fungsi ini memungkinkan pengguna untuk menghapus kontak dari daftar. Pengguna diminta memasukkan nama kontak yang ingin dihapus. Jika nama ditemukan dalam dictionary, maka entri tersebut dihapus menggunakan perintah del.

6. Fungsi Menampilkan Semua Nama Kontak
```python
def tampilkan_semua_nama():
    print("\nSemua Nama:")
    for nama in daftar_kontak.keys():
        print(nama)
````
Fungsi ini menampilkan semua nama yang ada dalam daftar kontak. Fungsi keys() digunakan untuk mengambil semua key (nama) yang ada dalam dictionary dan menampilkannya satu per satu.

7. Fungsi Menampilkan Semua Nomor Kontak
```python
def tampilkan_semua_nomor():
    print("\nSemua Nomor:")
    for nomor in daftar_kontak.values():
        print(nomor)
````
Fungsi ini menampilkan semua nomor telepon yang ada dalam daftar kontak. Fungsi values() digunakan untuk mengambil semua value (nomor telepon) yang ada dalam dictionary dan menampilkannya satu per satu.

# Hasil
![Screenshot 2024-11-16 195840](https://github.com/user-attachments/assets/b61214ce-cef9-4eec-835b-6c5801128b34)

Di gambar tersebut terdapat hasil dari
Tampilkan kontaknya Ari
Tambah kontak baru dengan nama Riko, nomor 087654544
Ubah kontak Dina dengan nomor baru 088999776

![Screenshot 2024-11-16 195946](https://github.com/user-attachments/assets/c23aced0-12b4-4488-a9a3-9a65152bdd4e)

Tampilkan semua Nama
Tampilkan semua Nomor
Tampilkan daftar Nama dan nomornya

![Screenshot 2024-11-16 200057](https://github.com/user-attachments/assets/1a4de6db-bc80-465b-bc75-26fa557ef1df)

Hapus Kontak Dina



# Latihan 2

![Screenshot 2024-11-16 202502](https://github.com/user-attachments/assets/7522e3f9-f186-4ade-a74d-789553f8c2e6)


```python
# Dictionary untuk menyimpan data mahasiswa
data_mahasiswa = {}

# Fungsi untuk menghitung nilai akhir
def hitung_nilai_akhir(tugas, uts, uas):
    return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

# Fungsi untuk menambah data mahasiswa
def tambah_data():
    nim = input("Masukkan NIM: ")
    nama = input("Masukkan Nama: ")
    tugas = float(input("Masukkan Nilai Tugas: "))
    uts = float(input("Masukkan Nilai UTS: "))
    uas = float(input("Masukkan Nilai UAS: "))
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
    data_mahasiswa[nim] = {"Nama": nama, "Tugas": tugas, "UTS": uts, "UAS": uas, "Nilai Akhir": nilai_akhir}
    print(f"Data mahasiswa dengan NIM {nim} berhasil ditambahkan.")

# Fungsi untuk mengubah data mahasiswa
def ubah_data():
    nim = input("Masukkan NIM mahasiswa yang akan diubah: ")
    if nim in data_mahasiswa:
        print(f"Data saat ini: {data_mahasiswa[nim]}")
        nama = input("Masukkan Nama baru: ")
        tugas = float(input("Masukkan Nilai Tugas baru: "))
        uts = float(input("Masukkan Nilai UTS baru: "))
        uas = float(input("Masukkan Nilai UAS baru: "))
        nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
        data_mahasiswa[nim] = {"Nama": nama, "Tugas": tugas, "UTS": uts, "UAS": uas, "Nilai Akhir": nilai_akhir}
        print(f"Data mahasiswa dengan NIM {nim} berhasil diubah.")
    else:
        print(f"Data dengan NIM {nim} tidak ditemukan.")

# Fungsi untuk menghapus data mahasiswa
def hapus_data():
    nim = input("Masukkan NIM mahasiswa yang akan dihapus: ")
    if nim in data_mahasiswa:
        del data_mahasiswa[nim]
        print(f"Data mahasiswa dengan NIM {nim} berhasil dihapus.")
    else:
        print(f"Data dengan NIM {nim} tidak ditemukan.")

# Fungsi untuk menampilkan semua data mahasiswa
def tampilkan_data():
    if data_mahasiswa:
        print("\nDaftar Nilai Mahasiswa:")
        print("=" * 75)
        print(f"{'NIM':<10} {'Nama':<15} {'Tugas':<10} {'UTS':<10} {'UAS':<10} {'Nilai Akhir':<10}")
        print("=" * 75)
        for nim, data in data_mahasiswa.items():
            print(f"{nim:<10} {data['Nama']:<15} {data['Tugas']:<10} {data['UTS']:<10} {data['UAS']:<10} {data['Nilai Akhir']:<10.2f}")
    else:
        print("Belum ada data mahasiswa.")

# Fungsi untuk mencari data mahasiswa
def cari_data():
    nim = input("Masukkan NIM mahasiswa yang ingin dicari: ")
    if nim in data_mahasiswa:
        data = data_mahasiswa[nim]
        print(f"\nData Mahasiswa dengan NIM {nim}:")
        print(f"Nama        : {data['Nama']}")
        print(f"Nilai Tugas : {data['Tugas']}")
        print(f"Nilai UTS   : {data['UTS']}")
        print(f"Nilai UAS   : {data['UAS']}")
        print(f"Nilai Akhir : {data['Nilai Akhir']:.2f}")
    else:
        print(f"Data dengan NIM {nim} tidak ditemukan.")

# Program utama dengan menu pilihan
while True:
    print("\nMenu:")
    print("1. Tambah Data")
    print("2. Ubah Data")
    print("3. Hapus Data")
    print("4. Tampilkan Data")
    print("5. Cari Data")
    print("6. Keluar")
    pilihan = input("Masukkan pilihan (1-6): ")

    if pilihan == "1":
        tambah_data()
    elif pilihan == "2":
        ubah_data()
    elif pilihan == "3":
        hapus_data()
    elif pilihan == "4":
        tampilkan_data()
    elif pilihan == "5":
        cari_data()
    elif pilihan == "6":
        print("Program selesai. Terima kasih!")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
````

![Screenshot 2024-11-16 203616](https://github.com/user-attachments/assets/76814bee-1f18-4fbd-8536-86108f3d3aa7)


Penjelasan
1. Struktur Data (Dictionary)
Data mahasiswa disimpan dalam dictionary dengan format:

```python
data_mahasiswa = {
    "NIM": {
        "Nama": "Nama Mahasiswa",
        "Tugas": nilai_tugas,
        "UTS": nilai_uts,
        "UAS": nilai_uas,
        "Nilai Akhir": nilai_akhir
    }
}
````
Key utama adalah NIM.
Value adalah dictionary lain yang berisi data mahasiswa (nama, nilai tugas, UTS, UAS, dan nilai akhir).

2. Fungsi Hitung Nilai Akhir
```python
def hitung_nilai_akhir(tugas, uts, uas):
    return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
````
Fungsi ini menerima nilai tugas, UTS, dan UAS sebagai input, lalu menghitung nilai akhir berdasarkan bobot:

Tugas: 30%
UTS: 35%
UAS: 35%

3. Menambah Data Mahasiswa
```python
def tambah_data():
    nim = input("Masukkan NIM: ")
    nama = input("Masukkan Nama: ")
    tugas = float(input("Masukkan Nilai Tugas: "))
    uts = float(input("Masukkan Nilai UTS: "))
    uas = float(input("Masukkan Nilai UAS: "))
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
    data_mahasiswa[nim] = {"Nama": nama, "Tugas": tugas, "UTS": uts, "UAS": uas, "Nilai Akhir": nilai_akhir}
    print(f"Data mahasiswa dengan NIM {nim} berhasil ditambahkan.")
````
Fungsi ini meminta input pengguna untuk data NIM, nama, tugas, UTS, dan UAS. Nilai akhir dihitung menggunakan fungsi hitung_nilai_akhir(), lalu data dimasukkan ke dalam dictionary.

4. Mengubah Data Mahasiswa
```python
def ubah_data():
    nim = input("Masukkan NIM mahasiswa yang akan diubah: ")
    if nim in data_mahasiswa:
        print(f"Data saat ini: {data_mahasiswa[nim]}")
        nama = input("Masukkan Nama baru: ")
        tugas = float(input("Masukkan Nilai Tugas baru: "))
        uts = float(input("Masukkan Nilai UTS baru: "))
        uas = float(input("Masukkan Nilai UAS baru: "))
        nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
        data_mahasiswa[nim] = {"Nama": nama, "Tugas": tugas, "UTS": uts, "UAS": uas, "Nilai Akhir": nilai_akhir}
        print(f"Data mahasiswa dengan NIM {nim} berhasil diubah.")
    else:
        print(f"Data dengan NIM {nim} tidak ditemukan.")
````
Fungsi ini memungkinkan pengguna memperbarui data mahasiswa berdasarkan NIM. Jika NIM ditemukan, pengguna dapat memasukkan data baru.

6. Menghapus Data Mahasiswa
```python
def hapus_data():
    nim = input("Masukkan NIM mahasiswa yang akan dihapus: ")
    if nim in data_mahasiswa:
        del data_mahasiswa[nim]
        print(f"Data mahasiswa dengan NIM {nim} berhasil dihapus.")
    else:
        print(f"Data dengan NIM {nim} tidak ditemukan.")
````
Fungsi ini menghapus data mahasiswa berdasarkan NIM yang diberikan.

7. Menampilkan Semua Data
```python
def tampilkan_data():
    if data_mahasiswa:
        print("\nDaftar Nilai Mahasiswa:")
        print("=" * 50)
        print(f"{'NIM':<10} {'Nama':<15} {'Tugas':<10} {'UTS':<10} {'UAS':<10} {'Nilai Akhir':<10}")
        print("=" * 50)
        for nim, data in data_mahasiswa.items():
            print(f"{nim:<10} {data['Nama']:<15} {data['Tugas']:<10} {data['UTS']:<10} {data['UAS']:<10} {data['Nilai Akhir']:<10.2f}")
    else:
        print("Belum ada data mahasiswa.")
````
Fungsi ini mencetak daftar semua mahasiswa dalam format tabel.

# Hasil

![Screenshot 2024-11-16 203616](https://github.com/user-attachments/assets/31128f1d-08f1-4bc8-ad36-13ee7e6ea6b9)


# Flowchart
![image](https://github.com/user-attachments/assets/36afe717-4fea-466b-b51a-93ea6b740b26)


# Penjelasan Flow Chart
Pertama mulai
kedua kita akan melist data data mahasiswa
ketiga masukkan nama
keempat masukan nim
kelima masukan nilai tugas
keenam masukkan nilai uts
ketujuh masukkan nilai uas
kedelapan menghitung nilai akhir (nilai tugas * 0.30)(nilai uts * 0.35)(nilai uas * 0.35)jika sudah lanjut
kesembilan tambahkan ke list data
kesepuluh ada dua pilihan jika ingin menambahkan data pilih iya dan kita akan kembali ke langkah ke tiga jika tidak tampilkan tabel data dan terakhir selesai
