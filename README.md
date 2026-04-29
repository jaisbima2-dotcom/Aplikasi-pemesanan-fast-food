# Aplikasi-pemesanan-fast-food
Nama Anggota :
1. Fahra Nuzul Azizah
2. Jaisyulusrah Ali Muqtadir
3. Muhamad Zanjaya Fitra

Trigger

1. Trigger Update Subtotal Pembayaran
Tabel: Detail_Pesanan
Waktu: AFTER INSERT, UPDATE

Penjelasan:
Trigger ini berfungsi untuk menghitung nilai subtotal secara otomatis setiap kali data pesanan ditambahkan atau diperbarui. Subtotal diperoleh dari hasil perkalian antara jumlah menu yang dipesan dengan harga menu. Dengan adanya trigger ini, sistem dapat menghindari kesalahan perhitungan manual.

2. Trigger Update Total Harga Pesanan
Tabel: Detail_Pesanan
Waktu: AFTER INSERT, UPDATE, DELETE

Penjelasan:
Trigger ini digunakan untuk memperbarui total harga pada tabel Pesanan berdasarkan seluruh item yang terdapat dalam Detail_Pesanan. Setiap terjadi perubahan data, seperti penambahan, pengubahan, atau penghapusan item pesanan, maka total harga akan dihitung ulang secara otomatis.

3. Trigger Insert Nomor Antrian
Tabel: Pesanan
Waktu: INSTEAD OF INSERT

Penjelasan:
Trigger ini berfungsi untuk menghasilkan nomor antrian secara otomatis setiap kali pelanggan membuat pesanan baru. Dengan menggunakan trigger ini, nomor antrian tidak dapat diinput secara manual oleh pengguna, sehingga urutan antrian tetap terjaga dan konsisten.

4. Trigger Update Stok Menu
Tabel: Detail_Pesanan
Waktu: AFTER INSERT

Penjelasan:
Trigger ini digunakan untuk mengurangi jumlah stok menu secara otomatis ketika terjadi penambahan data pesanan. Setiap menu yang dipesan akan langsung mengurangi stok yang tersedia, sehingga data stok selalu terupdate secara real-time.

5. Trigger Update Status Pembayaran
Tabel: Pembayaran
Waktu: AFTER INSERT, UPDATE

Penjelasan:
Trigger ini berfungsi untuk memperbarui status pesanan menjadi “diproses” ketika pembayaran telah berhasil atau berstatus “lunas”. Dengan demikian, sistem dapat secara otomatis memberi sinyal kepada bagian kitchen bahwa pesanan siap untuk diproses.
