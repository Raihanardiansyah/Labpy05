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
