BACKGROUND PROJECT

Andi adalah seorang pemilik supermarket besar di salah satu kota di Indonesia. Andi memiliki rencana untuk melakukan perbaikan proses bisnis, yaitu Andi akan membuat sistem kasir self-service di supermarket miliknya, sehingga customer bisa langsung memasukkan item yang dibeli, jumlah yang dibeli, dan harga item yang dibeli serta sejumlah fitur lainnya.
Dengan demikian, customer yang berada di kota tersebut bisa membeli barang dari supermarket tersebut. Setelah Andi melakukan riset, ternyata Andi memiliki masalah, yaitu Andi membutuhkan seorang Programmer untuk membuat fitur-fitur sistem kasir self-service di supermarket itu agar bisa berjalan dengan lancar.
Project ini dibuat untuk menyelesaikan permasalahan yang dihadapi Andi, dengan membuat sistem kasir self service dengan nama Super Cashier, dan juga sebagai bagian dari penyelesaian course Python Programming dari Pacmann.






FEATURE SISTEM SUPER CASHIER

Berikut adalah customer journey penggunaan sistem Super Cashier:

<img width="504" alt="image" src="https://user-images.githubusercontent.com/128900454/232229059-70a9e371-719a-4d45-beeb-3395681f9ce2.png">

1.	Saat sistem dijalankan, customer akan mendapatkan pesan konfirmasi apakah ingin bertransaksi sebagai berikut:
   <img width="360" alt="image" src="https://user-images.githubusercontent.com/128900454/232229045-27396a75-58af-4484-856b-cd77fab673d5.png">
   
   Jika customer tidak ingin bertransaksi, maka sistem akan menampilkan pesan berikut:
   "Terima kasih telah menggunakan aplikasi Super Cashier"

2.	Jika customer memilih bertransaksi, maka sistem akan membuat ID transaksi customer secara otomatis dengan membuat objek dari class:
trx123 = Transaksi()

3.	Kemudian, customer diminta memasukkan nama item, jumlah item, dan harga barang untuk dimasukkan ke dalam keranjang belanjanya.
Setelah memasukkan item pertama, customer akan ditampilkan pilihan apakah ingin menambahkan item bar uke dalam keranjang atau tidak.
<img width="363" alt="image" src="https://user-images.githubusercontent.com/128900454/232229125-b7f33a08-57f9-4f7f-84bc-894000ffab84.png">

    a.	Jika customer memilih "Y", maka sistem akan kembali menjalankan fungsi menambahkan item ke keranjang
    b.	Jika customer memilih "N", maka sistem akan memberikan daftar menu transaksi utama

4.	Customer masuk ke menu transaksi utama dimana customer dapat melakukan beberapa aktivitas berikut:
   <img width="258" alt="image" src="https://user-images.githubusercontent.com/128900454/232229346-c44e70b7-efe5-495f-b56a-934e26952cb9.png">

    a.	Lihat isi keranjang belanja:
       Fungsi tampilkan_keranjang(self):
       sistem akan menampilkan seluruh isi keranjang belanja customer serta langsung kembali ke menu utama
       <img width="354" alt="image" src="https://user-images.githubusercontent.com/128900454/232229152-eb28ecac-b883-4a4f-b408-c4e41c313b81.png">

    b.	Tambah item baru:
       Fungsi add_item(self):
       Menjalankan fungsi untuk menambahkan item baru ke keranjang, fungsi dasarnya sama dengan langkah 3.

    c.	Update nama item:
       Fungsi update_item_name(self):
       Customer dapat mengubah nama item yang ada di keranjang belanja. Saat memilih opsi ini, customer akan memperoleh informasi daftar keranjang belanja sebagai referensi:
       <img width="349" alt="image" src="https://user-images.githubusercontent.com/128900454/232229163-060b5c9b-df64-4894-bf4b-3c8dca842702.png">

       Customer akan diminta memasukkan nama barang yang akan diubah (case insensitive), jika item tersebut ada di keranjang, customer akan diminta memasukkan nama barang yang baru dan kembali ke menu utama
       Jika nama yang dimasukkan tidak ada di keranjang, maka sistem akan menginformasikan bahwa item tersebut tidak ada dan kembali ke menu utama.

    d.	Update jumlah item:
      Fungsi update_item_qty(self):
      Customer dapat mengubah jumlah item yang ada di keranjang belanja. Saat memilih opsi ini, customer akan memperoleh informasi daftar keranjang belanja sebagai referensi (sama dengan Langkah 4. C)
      Customer akan diminta memasukkan nama barang yang akan diubah (case insensitive), jika item tersebut ada di keranjang, customer akan diminta memasukkan jumlah barang yang baru (input hanya berupa integer) dan kembali ke menu utama
      Jika tidak ditemukan, maka sistem akan memberikan output item tidak ditemukan dan kembali ke menu utama

    e.	Update harga item:
       Fungsi update_item_price(self):
       Customer dapat mengubah harga item yang ada di keranjang belanja. Saat memilih opsi ini, customer akan memperoleh informasi daftar keranjang belanja sebagai referensi (sama dengan Langkah 4. C)
       Customer akan diminta memasukkan nama barang yang akan diubah (case insensitive), jika item tersebut ada di keranjang, customer akan diminta memasukkan harga barang yang baru (input hanya berupa integer) dan kembali ke menu utama
       Jika tidak ditemukan, maka sistem akan memberikan output item tidak ditemukan dan kembali ke menu utama

    f.	Hapus salah satu item di keranjang belanja:
       Fungsi delete_item(self):
       Customer dapat menghapus salah satu item yang ada di keranjang belanja. Saat memilih opsi ini, customer akan memperoleh informasi daftar keranjang belanja sebagai referensi (sama dengan Langkah 4. C)
       Customer akan diminta memasukkan nama barang yang akan dihapus (case insensitive), jika item tersebut ada di keranjang, maka sistem akan menghapus item tersebut dan kembali ke menu utama.
       Jika tidak ditemukan, maka sistem akan memberikan output item tidak ditemukan dan kembali ke menu utama

    g.	Hapus seluruh item di keranjang belanja:
       Fungsi reset_transaction(self):
       Customer akan masuk ke menu konfirmasi untuk menghapus seluruh isi keranjang dan selanjutnya kembali ke menu utama
       <img width="401" alt="image" src="https://user-images.githubusercontent.com/128900454/232229179-c2cf6476-3055-496d-82ef-1c42e89eca3c.png">


    h.	Keranjang belanja sudah sesuai:
       Fungsi konfirmasi_transaksi(self):
       Ini adalah pilihan checkout keranjang. Customer akan memperoleh tampilan seluruh isi keranjang serta total nilai transaksi sebelum transaksi, serta pilihan konfirmasi untuk checkout atau kembali ke menu utama
       <img width="342" alt="image" src="https://user-images.githubusercontent.com/128900454/232229192-fea2d99a-4451-437f-ba2e-ab95268551a8.png">

       Jika nasabah memilih checkout transaksi, maka sistem akan menampilkan nilai total belanja customer, termasuk rincian diskon sebagai berikut:
       <img width="376" alt="image" src="https://user-images.githubusercontent.com/128900454/232229205-442bb2ab-a116-4740-9d71-fcd017e9aa03.png">

    i.	Cek ketentuan diskon:
       Fungsi table_diskon:
       Fungsi ini akan menampilkan ketentuan diskon yang berlaku saat ini
       <img width="303" alt="image" src="https://user-images.githubusercontent.com/128900454/232229218-65ca8e9d-1e50-4edf-96c2-c6d69413fa5b.png">


    j.	Batalkan transaksi:
       Fungsi konfirmasi_batal(self):
       Customer akan masuk ke menu konfirmasi, jika nasabah memilih Y, makan sistem akan berakhir, jika tidak, maka customer akan kembali ke menu utama

5.	Terkait ketentuan diskon, pemilik supermarket dapat melakukan penyesuaian ketentuan diskon yang berlaku pada line code berikut:
   <img width="468" alt="image" src="https://user-images.githubusercontent.com/128900454/232229245-feb3bcc1-3beb-44e4-ad75-f9cc4ac000bc.png">

 
SARAN PENGEMBANGAN

1. membuat database item-item yang dijual oleh Supermarket milik Andi yang meliputi nama item, jumlah item tersedia, dan harga per item.
Nantinya, customer dapat memilih item dari database tersebut sehingga tidak perlu memasukkan harga item. Hal ini juga memitigasi kemungkinan item yang diinput customer ternyata tidak ada dalam stok supermarket.
Jika customer melakukan checkout, makan database item akan terupdate berupa pengurangan jumlah item tersedia.
2.	Memastikan agar nama item tidak dapat berupa numerik atau diawali dengan angka
