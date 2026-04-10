# 📘 Panduan Cepat Golang (Cheat Sheet)
*Khusus untuk peserta seleksi Divisi Akademik*

Dokumen ini adalah panduan dasar bagi Anda untuk menyelesaikan tantangan *Live Coding*. Fokuslah pada alur logika (Input -> Proses -> Output).

---

### 1. Dasar Output & Input
Digunakan untuk berinteraksi dengan pengguna.
- `fmt.Println`: Perintah untuk menampilkan teks ke layar (Output).
- `fmt.Scan`: Perintah untuk mengambil apa yang diketik pengguna (Input).

```go
fmt.Println("Masukkan Nama Anda:") // Output ke layar
fmt.Scan(&namaVariabel)            // Input disimpan ke variabel

### 2. Variabel (Wadah Penyimpanan Data)
Dalam pemrograman, kita perlu menyiapkan "kotak" untuk menyimpan data. Setiap kotak harus diberi nama dan ditentukan jenis isinya.

**Jenis data yang sering digunakan:**
- `string`: Digunakan untuk menyimpan teks seperti nama atau alamat.
- `int`: Digunakan untuk angka bulat (tidak ada koma) seperti umur atau jumlah barang.
- `float64`: Digunakan untuk angka yang memiliki desimal (koma) atau nilai mata uang yang presisi.

**Contoh Kode & Penjelasan:**
```go
// Menyiapkan kotak bernama 'nama' khusus untuk menyimpan tulisan/teks
var nama string     

// Menyiapkan kotak bernama 'umur' khusus untuk menyimpan angka bulat
var umur int        

// Menyiapkan kotak bernama 'harga' khusus untuk menyimpan angka desimal/koma
var harga float64

### 3. Percabangan / Logic Flow (If-Else)
Digunakan agar program bisa mengambil keputusan. Ibarat sebuah gerbang: jika syarat terpenuhi, gerbang terbuka ke arah A, jika tidak, terbuka ke arah B.

**Contoh Kode & Penjelasan:**
```go
// Memeriksa kondisi: "Apakah total belanja lebih dari 100.000?"
if totalBelanja > 100000 {
    // Jalankan kode di dalam kurung ini JIKA KONDISI BENAR
    fmt.Println("Selamat! Anda mendapatkan diskon 10%")
} else {
    // Jalankan kode di dalam kurung ini JIKA KONDISI SALAH
    fmt.Println("Maaf, total belanja belum cukup untuk diskon")
}
4. Perulangan / Loop (Tugas Berulang)
Digunakan agar program bisa melakukan hal yang sama berkali-kali secara otomatis. Ibarat lari di stadion: Anda akan terus berlari selama jumlah putaran belum mencapai target.

Contoh Kode & Penjelasan:

Go
// Memeriksa kondisi: "Selama saldo masih kurang dari target, teruslah mengulang"
for saldo < target {
    // Jalankan kode di dalam kurung ini JIKA KONDISI MASIH BENAR
    fmt.Print("Masukkan jumlah setoran Anda: ")
    fmt.Scan(&setoran)

    // Menambahkan setoran ke saldo agar uang terus bertambah
    saldo = saldo + setoran
}
// Jika saldo sudah mencapai target, program otomatis berhenti mengulang
5. Function / Fungsi (Mesin Pengolah Data)
Digunakan untuk membungkus perintah agar bisa digunakan berulang kali. Ibarat sebuah mesin jus: Anda masukkan buah (Input), mesin bekerja di dalam, lalu mengeluarkan jus (Output).

Contoh Kode & Penjelasan:

Go
// Membuat mesin bernama 'hitungSisa' yang butuh dua bahan (target & skrg)
func hitungSisa(target float64, skrg float64) float64 {
    // Jalankan proses pengurangan di dalam mesin untuk cari selisih
    hasil := target - skrg

    // Mengeluarkan hasil akhir dari mesin (Output) untuk dipakai di program
    return hasil
}

// Cara pakai: sisa := hitungSisa(1000, 400)
6. Operator Aritmatika (Simbol Matematika)
Digunakan untuk memproses data angka menjadi informasi baru. Ibarat tombol pada kalkulator yang memiliki fungsi spesifik untuk menghitung total atau sisa.

Contoh Kode & Penjelasan:

Go
// 1. TAMBAH (+): Digunakan untuk menjumlahkan atau akumulasi nilai
total = saldoLama + setoranBaru

// 2. KURANG (-): Digunakan untuk mencari selisih atau sisa kekurangan
sisa = target - totalSekarang

// 3. KALI (*): Digunakan untuk menghitung diskon atau kelipatan (0.1 = 10%)
potongan = hargaAwal * 0.1

// 4. BAGI (/): Digunakan untuk membagi nilai menjadi beberapa bagian
rataRata = totalNilai / jumlahPeserta