# Praktikum 5

### Programnya 

![Gambar1](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/ss1.png?raw=true)

### berikut penjelasan dari bagian brogram tersebut

Program di atas adalah sebuah sistem sederhana untuk menampilkan data nilai mahasiswa yang tersimpan dalam variabel data_nilai. Penjelasan rinci dari program tersebut adalah sebagai berikut:

### Variabel data_nilai

Variabel data_nilai dideklarasikan sebagai list kosong, yang akan digunakan untuk menyimpan data mahasiswa. Data yang disimpan berupa dictionary, dengan setiap elemen dictionary mencakup informasi seperti NIM, nama, nilai tugas, UTS, UAS, dan nilai akhir.

### Fungsi lihat_data()

Fungsi ini berfungsi untuk menampilkan data mahasiswa yang ada di dalam data_nilai dalam format tabel.

Fungsi dimulai dengan mengecek apakah data_nilai kosong menggunakan kondisi if len(data_nilai) == 0. Jika list kosong, fungsi akan mencetak pesan "Tidak Ada Data" dan tidak melanjutkan ke proses berikutnya.

Jika data_nilai tidak kosong, fungsi akan menampilkan data dalam format tabel dengan kolom yang berisi nomor urut, NIM, nama, nilai tugas, nilai UTS, nilai UAS, dan nilai akhir. Header tabel dipisahkan oleh garis pembatas yang ditampilkan menggunakan "-" * 60, untuk memastikan tampilan yang rapi.

### Perulangan untuk Menampilkan Data

Data ditampilkan menggunakan perulangan for yang mengiterasi setiap elemen dalam data_nilai. Fungsi enumerate() digunakan agar setiap elemen memiliki nomor urut (i) yang dimulai dari 1. Setiap elemen dictionary ditampilkan dalam format tertentu:

Nomor urut ditampilkan dengan lebar 2 karakter.

NIM dengan lebar minimal 7 karakter.

Nama dengan lebar minimal 8 karakter.

Nilai Tugas, UTS, dan UAS ditampilkan dalam kolom masing-masing.

Nilai akhir ditampilkan dengan format dua angka desimal untuk memberikan presisi.

### Format Tampilan

Seluruh data dicetak dengan format yang rapi menyerupai tabel, di mana setiap kolom disejajarkan menggunakan padding (lebar karakter yang ditentukan). Setelah data selesai dicetak, garis pembatas ditampilkan kembali untuk menutup tabel.

![Gambar2](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/ss2.png?raw=true)

### Lalu selanjutnya penjelasan dari pogram tersebut

Program yang ditampilkan adalah fungsi tambah_data() yang berfungsi untuk menambahkan data mahasiswa ke dalam variabel data_nilai. Berikut adalah penjelasan rinci dari program tersebut:

### 1. Pengumpulan Input dari Pengguna

Fungsi meminta input dari pengguna untuk mengisi data mahasiswa:

### Baris 17: NIM = input("NIM: ")

Pengguna diminta memasukkan NIM mahasiswa, disimpan dalam variabel NIM.

### Baris 18: Nama = input("Nama: ")

Pengguna diminta memasukkan nama mahasiswa, disimpan dalam variabel Nama.

### Baris 19-21: Tugas, UTS, dan UAS

Pengguna diminta memasukkan nilai tugas, UTS, dan UAS dalam bentuk angka (integer). Nilai-nilai ini disimpan dalam variabel Tugas, UTS, dan UAS.

### 2. Perhitungan Nilai Akhir

### Baris 22: Akhir = (Tugas * 0.3) + (UTS * 0.35) + (UAS * 0.35)

*Nilai akhir dihitung dengan rumus berbobot:

*Nilai tugas memiliki bobot 30%,

*Nilai UTS memiliki bobot 35%,

*Nilai UAS memiliki bobot 35%. Hasil perhitungan disimpan dalam variabel Akhir.

### 3. Menambahkan Data ke data_nilai

### Baris 23:

data_nilai.append({
    "NIM": NIM, 
    "Nama": Nama, 
    "Tugas": Tugas, 
    "UTS": UTS, 
    "UAS": UAS, 
    "Akhir": Akhir
})

Data yang baru dimasukkan pengguna disimpan dalam bentuk dictionary dengan key (NIM, Nama, Tugas, UTS, UAS, Akhir) dan nilai yang sesuai. Dictionary ini kemudian ditambahkan ke list data_nilai menggunakan metode append().

### 4. Konfirmasi Penambahan Data

### Baris 24: print('Data berhasil ditambahkan!')

Setelah data berhasil dimasukkan ke dalam data_nilai, program mencetak pesan konfirmasi bahwa data berhasil ditambahkan.

![Gambar3](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/ss3.png?raw=true)

### Berikut penjelasan dari program di atas

### Penjelasan Fungsi

### 1. Memanggil Fungsi lihat_data()

### Baris 27: lihat_data()

Fungsi lihat_data() dipanggil untuk menampilkan data yang sudah ada di dalam list data_nilai. Hal ini memudahkan pengguna untuk melihat data mana yang ingin diubah.

### 2. Meminta Input Nomor Data yang Akan Diubah

Baris 28: index = int(input("Masukkan nomor data yang akan diubah: ")) - 1

Pengguna diminta untuk memasukkan nomor urut data yang ingin diubah. Nomor tersebut dikurangi 1 agar sesuai dengan indeks list (karena indeks list dimulai dari 0).

### Validasi Indeks

### Baris 29-30:

if index < 0 or index >= len(data_nilai):

    print("Data tidak ditemukan.")
    
Program memeriksa apakah indeks yang dimasukkan pengguna valid (tidak kurang dari 0 atau lebih dari panjang list data_nilai). Jika indeks tidak valid, program mencetak pesan "Data tidak ditemukan" dan keluar dari proses.

### 4. Mengubah Data

### Baris 32-39:

Jika indeks valid, program meminta pengguna memasukkan data baru untuk menggantikan data yang ada pada indeks tersebut. Setiap atribut data (NIM, Nama, Tugas, UTS, dan UAS) diperbarui melalui input baru:

### Baris 33-34: 

Data NIM dan Nama diperbarui berdasarkan input pengguna.

### Baris 35-37: 

Data nilai (Tugas, UTS, UAS) diperbarui berdasarkan input pengguna.

### Baris 38-39: 

Nilai akhir dihitung ulang dengan rumus berbobot:

Nilai Akhir = (Tugas * 0.3) + (UTS * 0.35) + (UAS * 0.35)

Nilai ini disimpan di dalam atribut Akhir.

### Konfirmasi Perubahan

### Baris 41: print("Data berhasil diubah!")

Setelah data berhasil diubah, program mencetak pesan bahwa perubahan berhasil dilakukan.

![Gambar4](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/ss4.png?raw=true)

### berikut penjelasan dari program di atas

Kode yang ditampilkan adalah fungsi Python bernama hapus_data(). Berikut adalah penjelasannya:

### Fungsi hapus_data():

Digunakan untuk menghapus data dari list bernama data_nilai.
Proses yang dilakukan dalam fungsi ini:

*Baris 44: Fungsi lihat_data() dipanggil untuk menampilkan semua data dalam list data_nilai. Hal ini membantu pengguna melihat data yang tersedia sebelum memutuskan data mana yang akan dihapus.

*Baris 45: Program meminta pengguna memasukkan nomor indeks data yang ingin dihapus. Indeks ini dimasukkan melalui fungsi input(), kemudian dikurangi 1 agar sesuai dengan indeks berbasis 0 dalam Python.

*Baris 46: Program memeriksa apakah indeks yang dimasukkan valid, yaitu apakah nilainya tidak negatif dan tidak lebih besar atau sama dengan panjang list data_nilai.

*Jika tidak valid, Baris 47 akan menampilkan pesan "Data tidak ditemukan."

*Baris 49: Jika indeks valid, item dalam list data_nilai pada indeks tersebut dihapus menggunakan perintah del.

*Baris 50: Setelah data berhasil dihapus, program mencetak pesan "Data berhasil dihapus!"

### Fungsi Pendukung

lihat_data(): Fungsi ini (yang tidak terlihat di kode) bertugas menampilkan isi list data_nilai beserta indeksnya. Biasanya digunakan agar pengguna dapat mengetahui data mana yang akan dihapus.

![Gambar5](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/ss5.png?raw=true)

### Penjelasan Baris per Baris

### Baris 52:

keyword = input("Masukkan nama yang dicari: ").lower()
Program meminta pengguna untuk memasukkan nama yang akan dicari, lalu mengonversinya menjadi huruf kecil (menggunakan .lower()) untuk memudahkan pencarian tanpa memperhatikan huruf besar atau kecil.

### Baris 53:

hasil_cari = [data for data in data_nilai if keyword in data['Nama'].lower()]

Ini adalah list comprehension untuk mencari data dalam data_nilai.

Setiap elemen data dalam data_nilai diperiksa apakah keyword ada di dalam data['Nama'].lower().

Jika cocok, data tersebut akan dimasukkan ke dalam list hasil_cari.

### Baris 54-55:

if len(hasil_cari) == 0:

Mengecek apakah list hasil_cari kosong (artinya tidak ada data yang cocok dengan keyword).

Jika kosong, program mencetak "Data tidak ditemukan."

### Baris 57-65:

Else:

Jika ditemukan data yang cocok, program menampilkan hasil pencarian dalam format tabel.

Header tabel dicetak di Baris 59-61 dengan format berikut:

objectivec

Salin kode

| NO | NIM      | NAMA      | TUGAS | UTS | UAS | AKHIR |

### Baris 63-64:

Menggunakan enumerate(hasil_cari, start=1) untuk menghasilkan nomor urut (NO) dimulai dari 1.

Setiap elemen dalam hasil_cari dicetak dalam format yang rapi menggunakan string format:

i adalah nomor urut.

data['NIM'], data['Nama'], data['Tugas'], data['UTS'], data['UAS'], dan data['Akhir'] adalah nilai yang akan ditampilkan.

Format angka seperti 5.2f digunakan untuk membatasi angka desimal pada nilai akhir hingga 2 digit.

![Gambar6](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/ss6.png?raw=true)

### Baris 67: while True:

Program berjalan dalam loop tak berujung sampai pengguna memilih keluar (menu == 'k').

### Baris 68-71: Tampilan Menu

Program mencetak daftar menu:

css
Program Input Nilai
==================
[L]ihat, [T]ambah, [U]bah, [H]apus, [C]ari, [K]eluar

Pengguna diminta untuk memilih menu melalui fungsi input() pada Baris 71, dan input pengguna dikonversi ke huruf kecil menggunakan .lower() agar tidak peka terhadap huruf besar/kecil.

### Logika Pemilihan Menu (Baris 73-87):

### Baris 73-74: if menu == 'l':

Memanggil fungsi lihat_data() untuk menampilkan semua data.

### Baris 75-76: elif menu == 't':

Memanggil fungsi tambah_data() untuk menambahkan data baru ke dalam list.

### Baris 77-78: elif menu == 'u':

Memanggil fungsi ubah_data() untuk mengubah data yang sudah ada.

### Baris 79-80: elif menu == 'h':

Memanggil fungsi hapus_data() untuk menghapus data berdasarkan indeks tertentu.

### Baris 81-82: elif menu == 'c':

Memanggil fungsi cari_data() untuk mencari data berdasarkan nama tertentu.

### Baris 83-85: elif menu == 'k':
Jika pengguna memilih menu K (keluar), program mencetak "Keluar dari program." dan menggunakan break untuk menghentikan loop.

### Baris 86-87: Else
Jika input menu tidak valid, program mencetak pesan "Menu tidak valid."

![GambarRun](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/run.png?raw=true)

Inilah hasil apabila program tersebut di Run, terdapt beberapa pilihan menu yang bisa kalian pilih.

![GambahrHasil](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/hasil.png?raw=true)

seperti inilah apabila kalian telah menginput data data kalian.

![GambarHail2](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/hasil2.png?raw=true)

Dan inilah apabila kalian memilih menu "Lihat" pada program tersebut akan memunculkan data yang telah kalian masukan tadi.

### Berikut flowchart dari program tersebut

![GambarFlowchart](https://github.com/Raihanardiansyah/Labpy05/blob/main/ss/flowchart.png?raw=true)

### Berikut penjelasan dari flowchart tersebut

### Deskripsi Umum:

### 1. Mulai (Start): Proses dimulai dari sini.

### 2. Tampilkan Menu: Sistem akan menampilkan daftar menu dengan opsi:

[L]ihat: Melihat daftar data.

[T]ambah: Menambahkan data baru.

[U]bah: Mengubah data yang ada.

[H]apus: Menghapus data.

[C]ari: Mencari data.

[K]eluar: Keluar dari sistem.

### 3. Input Pilihan Menu (Write(Code Menu)): Pengguna memasukkan kode menu untuk menentukan aksi yang akan dilakukan.

### Penjelasan Alur untuk Tiap Menu:

### 1. [L] Lihat:

Pengguna memilih opsi L.

Sistem akan menampilkan daftar data yang tersedia.

### 2. [T] Tambah:

Pengguna memilih opsi T.

Sistem menampilkan daftar data yang ada (jika ada).

Pengguna diminta untuk memasukkan nomor dan data baru untuk ditambahkan.

### 3. U] Ubah:

Pengguna memilih opsi U.

Sistem menampilkan daftar data yang ada.

Jika data tidak ditemukan, sistem memberi tahu pengguna bahwa data tidak ada.

Jika data ditemukan, pengguna diminta untuk memasukkan nomor data yang ingin diubah, lalu memasukkan data baru.

### 4. [H] Hapus:

Pengguna memilih opsi H.

Sistem menampilkan daftar data.

Pengguna diminta untuk memasukkan nomor data yang akan dihapus.

### 5. [C] Cari:

Pengguna memilih opsi C.

Sistem meminta pengguna untuk memasukkan nama yang ingin dicari.

Jika data ditemukan, sistem menampilkan daftar data tersebut.

### 6. [K] Keluar:

Pengguna memilih opsi K.

Proses berakhir dan sistem keluar.

### Catatan Penting:

* Ada proses pengulangan di setiap akhir alur, yang berarti setelah pengguna menyelesaikan suatu aksi, sistem akan kembali ke menu utama untuk menerima perintah selanjutnya.

* Jika input pengguna tidak sesuai dengan pilihan menu, sistem akan meminta input ulang.

Flowchart ini merepresentasikan alur kerja program berbasis menu dengan kontrol penuh terhadap operasi data, seperti CRUD (Create, Read, Update, Delete).
