# cashier-self-service-project

## Latar Belakang Masalah

Andi adalah seorang pemilik supermarket. Beliau ingin memperbaiki proses bisnis di supermarket miliknya, yaitu dengan membuat sistem kasir self-service agar customer bisa langsung menginputkan barang yang dibelinya saat ingin melakukan pembayaran secara mandiri. Hal ini dilakukan agar customer yang berada di luar kota juga bisa membeli barang dari supermarket tersebut.

Untuk memecahkan masalah tersebut adalah dengan membuat program Cashier Self-Service untuk memperbaiki proses bisnis di supermarket milik Andi. 

## Objective

Tujuan dari pembuatan projek ini adalah membuat sistem kasir self-service yang dapat melakukan beberapa metode yaitu:

1. Customer dapat menginput barang, jumlah barang, dan juga harga barang dengan metode tambah_barang. 
2. Jika customer salah input, ia dapat mengubah salah satu inputanya:
   - mengubah nama barang dengan metode update_nama_barang. 
   - mengubah jumlah barang dengan metode update_jumlah_barang.
   - mengubah harga barang dengan metode update_harga_barang.
3. Jika customer ingin menghapus salah satu barang dari daftar barang belanjanya, dapat menggunakan metode hapus_barang.
4. Jika customer ingin menghapus semua barang dari daftar belanjanya, dapat menggunakan metode reset_transaction.
5. Sebelum dapat menghitung total belanjanya, isi dari daftar belanja customer dicek dulu dengan metode cek_order. Metode ini mengecek apakah ada inputan yang masih salah pada daftar barang belanja customer.
6. Sistem dapat menghitung semua total belanja dan juga diskon yang didapatkannya dengan metode total_belanja.
7. Ketentuan untuk memperoleh diskon:
   - Jika total belanja diatas Rp.500.000, maka diskon 10%
   - Jika total belanja diatas Rp.300.000, maka diskon 8%
   - Jika total belanja diatas Rp.200.000, maka diskon 5%
    
## Method yang digunakan

1. **tambah_barang()**    
  Metode ini digunakan untuk memasukkan barang ke daftar barang belanja.

2. **update_nama_barang()**    
  Metode ini digunakan untuk merubah nama barang yang sudah ada dalam daftar barang belanja.

3. **update_jumlah_barang()**  
  Metode ini digunakan untuk merubah jumlah barang berdasarkan nama barang yang ada didalam daftar barang belanja. 

4. **update_harga_barang()**
  Metode ini digunakan untuk merubah harga barang berdasarkan nama barang yang ada didalam daftar barang belanja. 

5. **hapus_barang()**  
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

# Tes Case

# Saran / Improvement
