# 📘 Panduan Cepat Golang (Cheat Sheet)
*Khusus untuk peserta seleksi Divisi Akademik*

Dokumen ini adalah panduan dasar bagi Anda untuk menyelesaikan tantangan *Live Coding*. Fokuslah pada alur logika (**Input -> Proses -> Output**).

---

### 1. Dasar Output & Input
Digunakan untuk berinteraksi dengan pengguna di dalam aplikasi.
* `fmt.Println` : Perintah untuk menampilkan teks atau hasil ke layar (Output).
* `fmt.Scan` : Perintah untuk mengambil data yang diketik oleh pengguna (Input).

**Contoh Kode & Penjelasan:**
```go
fmt.Println("Masukkan Nama Anda:") // Menampilkan pesan ke layar
fmt.Scan(&namaVariabel)            // Menunggu input dan menyimpannya ke variabel
```

---

### 2. Variabel
Variabel digunakan untuk menyimpan data sementara dalam program.
* `var namaVariabel tipeData` : Mendeklarasikan variabel dengan tipe data tertentu.

**Contoh Kode & Penjelasan:**
```go
// Menyiapkan kotak bernama 'nama' khusus untuk menyimpan tulisan/teks
var nama string     

// Menyiapkan kotak bernama 'umur' khusus untuk menyimpan angka bulat
var umur int        

// Menyiapkan kotak bernama 'harga' khusus untuk menyimpan angka desimal
var harga float64
```

---

### 3. Kondisi (If-Else)
Kondisi digunakan untuk membuat keputusan berdasarkan nilai tertentu.
* `if kondisi { ... } else { ... }` : Mengecek kondisi dan menjalankan blok kode sesuai.

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
```

---

### 4. Loop (For)
Loop digunakan untuk mengulang eksekusi kode sampai kondisi tertentu terpenuhi.
* `for kondisi { ... }` : Mengulang selama kondisi benar.

**Contoh Kode & Penjelasan:**
```go
// Memeriksa kondisi: "Selama saldo masih kurang dari target, teruslah mengulang"
for saldo < target {
    // Meminta input setoran secara berulang
    fmt.Print("Masukkan jumlah setoran Anda: ")
    fmt.Scan(&setoran)

    // Menambahkan setoran ke saldo agar uang terus bertambah
    saldo = saldo + setoran
}
// Jika saldo sudah mencapai target, program otomatis berhenti mengulang
```

---

### 5. Fungsi
Fungsi digunakan untuk mengelompokkan kode yang dapat dipanggil berulang kali.
* `func namaFungsi(parameter) returnType { ... }` : Mendefinisikan fungsi.

**Contoh Kode & Penjelasan:**
```go
// Membuat mesin bernama 'hitungSisa' yang butuh dua bahan (target & skrg)
func hitungSisa(target float64, skrg float64) float64 {
    // Jalankan proses pengurangan di dalam mesin untuk cari selisih
    hasil := target - skrg

    // Mengeluarkan hasil akhir dari mesin (Output) untuk dipakai di program
    return hasil
}

// Cara pakai: sisa := hitungSisa(1000, 400)
```

---

### 6. Operator Aritmatika
Operator digunakan untuk melakukan operasi matematika.
* `+` : Penjumlahan
* `-` : Pengurangan
* `*` : Perkalian
* `/` : Pembagian

**Contoh Kode & Penjelasan:**
```go
// 1. TAMBAH (+): Digunakan untuk akumulasi atau menambah nilai
total := saldoLama + setoranBaru

// 2. KURANG (-): Digunakan untuk mencari selisih atau sisa kekurangan
sisa := target - totalSekarang

// 3. KALI (*): Digunakan untuk menghitung persentase (Contoh: 0.1 = 10%)
potongan := hargaAwal * 0.1

// 4. BAGI (/): Digunakan untuk membagi nilai menjadi beberapa bagian
rataRata := totalNilai / jumlahPeserta
```


