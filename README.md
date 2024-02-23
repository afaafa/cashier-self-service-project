# cashier-self-service-project

## Latar Belakang Masalah

Andi adalah seorang pemilik supermarket. Beliau ingin memperbaiki proses bisnis di supermarket miliknya, yaitu dengan membuat sistem kasir self-service agar customer bisa langsung menginputkan barang yang dibelinya saat ingin melakukan pembayaran secara mandiri. Hal ini dilakukan agar customer yang berada di luar kota juga bisa membeli barang dari supermarket tersebut.

Untuk memecahkan masalah tersebut, yaitu dengan membuat program cashier Self-Service untuk memperbaiki proses bisnis di supermarket milik Andi. 

## Requirement / Objective

Tujuan dari pembuatan projek ini adalah membuat sistem kasir self-service yang dapat mempermudah customer melakukan transaksi pembelian barang secara mandiri, serta memperbaiki proses bisnis supermarket milik Andi.
Customer nantinya dapat melakukan beberapa metode saat pembelian barangyaitu:

1. Customer dapat menginput barang, jumlah barang, dan juga harga barang dengan metode tambah_barang. 
2. Jika customer salah input, ia dapat mengubah salah satu inputannya:
   - mengubah nama barang dengan metode **update_nama_barang**. 
   - mengubah jumlah barang dengan metode **update_jumlah_barang**.
   - mengubah harga barang dengan metode **update_harga_barang**.
3. Jika customer ingin menghapus salah satu barang dari daftar barang belanjanya, dapat menggunakan metode **hapus_barang**.
4. Jika customer ingin menghapus semua barang dari daftar belanjanya, dapat menggunakan metode **reset_transaction**.
5. Sebelum dapat menghitung total belanjanya, isi dari daftar belanja customer dicek dulu dengan metode **cek_order**. Metode ini mengecek apakah ada inputan yang masih salah pada daftar barang belanja customer.
6. Sistem dapat menghitung semua total belanja dan juga diskon yang didapatkannya dengan metode **total_belanja**.
7. Ketentuan untuk memperoleh diskon:
   - Jika total belanja diatas **Rp.500.000**, maka diskon **10%**.
   - Jika total belanja diatas **Rp.300.000**, maka diskon **8%**.
   - Jika total belanja diatas **Rp.200.000**, maka diskon **5%**.
    
## Class & Method yang digunakan

1. **Transaction()**
   Membuat kelas transaksi untuk menghimpun data transaksi dan membuat fungsi/method sehingga menghasilkan objek
   
1. **tambah_barang(self, nama_barang, jumlah_barang, harga_barang)**    
  Metode ini digunakan untuk memasukkan barang ke daftar barang belanja.

2. **update_nama_barang(self, nama_barang, nama_barang_baru)**    
  Metode ini digunakan untuk merubah nama barang yang sudah ada dalam daftar barang belanja.

3. **update_jumlah_barang(self, nama_barang, jumlah_barang_baru)**  
  Metode ini digunakan untuk merubah jumlah barang berdasarkan nama barang yang ada didalam daftar barang belanja. 

4. **update_harga_barang(self, nama_barang, harga_barang_baru)**  
  Metode ini digunakan untuk merubah harga barang berdasarkan nama barang yang ada didalam daftar barang belanja. 

5. **hapus_barang(self, nama_barang)**     
  Metode ini digunakan untuk menghapus salah satu barang yang diinginkan berdasarkan nama barang yang ada didalam daftar barang belanja

6. **reset_transaction()**  
  Metode ini digunakan untuk menghapus semua barang didalam daftar barang belanjaan.

7. **cek_order()**  
  Mwtode ini digunakan untuk memastikan data yang diinputkan sudah benar atau belum.
  
8. **total_belanja()**  
  Metode ini digunakan untuk menghitung total harga dari daftar barang belanja customer. 

## Flowchart
 <p>
<img align="center" src="src/flowchart.jpg" width="800" height="1200" />
</p>

## Alur Program
1. Customer membuat ID transaksi dengan membuat objek dari class `trnsct_123 = Transaction()`
2. Customer memasukkan nama barang, jumlah, barang, dan harga barang
3. kemudian dicek apakah ada kesalahan inputan, jika ada kesalahan inputan tapi tidak ingin menghapus barangnya, maka customer dapat melakukan salah satu dari method dibawah:
   - update nama barang dengan method `update_nama_barang()`
   - update jumlah barang dengan method `update_jumlah_barang()`
   - update harga barang dengan method `update_harga_barang()`
4. Jika customer ingin membatalkan salah satu barang, customer dapat menghapus salah satu barang dengan method `hapus_barang`, ketika menghapus salah satu item maka jumlah barang dan harga barang ikut terhapus.
5. Jika customer ingin menghapus semua barang di daftar barang, yaitu menggunakan method `reset_transaction()`
6. Apabila customer sudah selesai belanja online, tapi masih ragu apakah inputannya sudah benar atau belum, maka customer dapat menggunakan method `cek_order` dan mengeluarkan pesan "pemesanan sudah benar" jika tidak ada kesalahan input. Jika ada kesalahan input maka mengeluarkan pesan "terdapat kesalahan input data.
7. Setelah melakukan pengecekan, customer dapat menghitung total belanja dengan method `total_belanja()` dengan ketentuan:
   - jika total belanja > 500_000 maka dapat diskon 10%
   - jika total belanja > 300_000 maka dapat diskon 8%
   - jika total belanja > 200_000 maka dapat diskon 5%

## Tes Case
### Tes 1:
Customer ingin menambahkan dua 4 barang baru dengan method `tambah_barang()`. Barang yang diinputkan:
 - nama barang: apel, jumlah: 20, harga: 3000
 - nama barang: jambu, jumlah: 25, harga: 2500
 - nama barang: mangga, jumlah: 25, harga: 5000
 - nama barang: jeruk, jumlah: 33, harga: 3500
Expected Output:
 <p>
<img align="center" src="src/method tambah_barang.png" width="500" height="100" />
</p>

### Tes 2:
Customer ingin mengubah nama barang `apel` menjadi `duku` dengan method `update_nama_barang()`.
Expected Output:
 <p>
<img align="center" src="src/method update_nama_barang.png" width="800" height="300" />
</p>

### Tes 3:
Customer ingin mengubah jumlah barang `mangga` menjadi `17 buah` dengan method `update_jumlah_barang()`.
Expected Output:
 <p>
<img align="center" src="src/method update_jumlah_barang.png" width="800" height="300" />
</p>

### Tes 3:
Customer ingin mengubah harga barang `jambu` menjadi `3000` dengan method `update_harga_barang()`.
Expected Output:
 <p>
<img align="center" src="src/method update_harga_barang.png" width="800" height="300" />
</p>

### Tes 4:
Customer ingin menghapus barang `duku` dengan method `hapus_barang()`.
Expected Output:
 <p>
<img align="center" src="src/method hapus_barang.png" width="800" height="300" />
</p>

### Tes 5:
Customer ingin menghitung barang total belanja dengan method `total_belanja()`.
Expected Output:
 <p>
<img align="center" src="src/method total_belanja.png" width="800" height="300" />
</p>

### Tes 6:
Customer ingin menghapus seluruh barang dengan method `reset_transaction()`.
Expected Output:
 <p>
<img align="center" src="src/method reset_transaction.png" width="800" height="300" />
</p>

## Saran Pengembangan
Saran pengembangan selanjutnya, program ini dapat ditambahkan fitur-fitur yang user friendly, dapat menghitung jika ada pajak transaksi, dapat membuat history transaksi, cek stok barang, serta menyimpan data-data transaksi kedalam database.
