# Relational-Database-Pacmann---Penjualan-Mobil-Bekas
Pada project kali ini untuk membangun relational database untuk sebuah website yang menawarkan penjualan mobil bekas. Untuk detail fitur dan kebutuhan dari website ini adalah sebagai berikut:

1. Setiap user aplikasi dapat menawarkan lebih dari satu produk mobil bekasnya.
2. Sebelum menjual produk mobil, user harus melengkapi data dirinya terlebih dahulu, seperti nama, kontak, dan domisili lokasi.
3. User menawarkan produknya melalui iklan yang akan ditampilkan oleh website.
4. Iklan ini berisikan judul, detail informasi produk yang ditawarkan, serta kontak penjual. Beberapa informasi yang harus ditulis dalam iklan adalah sebagai berikut
   - Merek mobil: Toyota, Daihatsu, Honda, dll
   - Model: Toyota Camry, Toyota Corolla Altis, Toyota Vios, Toyota Camry Hybrid, dll
   - Jenis body mobil: MPV, SUV, Van, Sedan, Hatchback, dll
   - Tipe mobil: manual atau automatic
   - Tahun pembuatan mobil: 2005, 2010, 2011, 2020
   - Deskripsi lain, seperti warna, jarak yang telah ditempuh, dsb, boleh ditambahkan sesuai kebutuhan.
5. Setiap user bisa mencari mobil yg ditawarkan berdasarkan lokasi user penjual, merk mobil, dan jenis body mobil.
6. Jika calon pembeli tertarik terhadap sebuah mobil, ia dapat menawar (bid) harga produk jika penjual mengizinkan fitur tawar.
7. Transaksi pembelian dilakukan di luar aplikasi sehingga tidak dalam scope project

# # Mendesain Database
Untuk mendesain database kita perlu mendefinisikan terlebih dahulu kebutuhan tabel yang akan dibangun. Berikut merupakan gambar ERD dari database, terdapat 5 tabel yang akan dibuat dalam project ini, yaitu:
1. Tabel cities
Tabel ini merupakan tabel yang akan menyimpan kota domisili dari pengguna yang dalam hal ini penjual maupun pembeli. Tabel ini terdiri dari kolom id_city, city_name, longitude, dan latitude.
2. Tabel users
Tabel ini merupakan tabel yang akan menyimpan data pengguna dari website, yang dalam hal ini bisa penjual maupun pembeli. Tebel ini terdiri dari kolom id_user, fullname, phone_number, email, dan id_city.
3. Tabel ads
tabel ads merupakan tabel yang akan menyimpan data iklan yang telah dibuat oleh pengguna atau user. Tabel ini terdiri dari kolom id_ads, title, detail_ads, availability, created_At, price, bid_allowed, id_product, dan id_user. availability disini nantikan akan digunakan untuk mennadkaan apakah sebuah iklan yang dipasang masih tersedia atau sudah laku dijual, begitu pula untu kolom bid_allowed sama dengan availability.
4. Tabel products
Tabel product sendiri adalah tabel yang menyimpan data produk apa yang diiklankan oleh pengguna attau user. Tabel ini terdiri dari kolom id_product, model, body_type, brand, vehicle_year, price, distance, dan color.
5. Tabel bids
Tabel bids merupakan tabel yang menyimpan data hasil bid yang diajukan oleh pengguna atau user pada sebuah iklan yang ditawarkan dalam website. Tabel ini terissri dari kolom id_bid, created_At, bid_price, status, id_user, dan id_ads. Status disini berisi nilai accept dan reject untuk menandakan apakah bid yang diajukan diterima atau tidak.

# # Implementasi DDL

ERD setelah tabel dibuat pada postgresql


# # Populating Database

Pada proses selanjutnya adalah menambahkan data pada tabel yang telah dibuat, pada kesempatan kali ini untuk isi dari tabel tersebut akan didapatkan dengan membuat file datta dummy menggunaka bantuan faker pada python. Berikut ini merupakan code python yang digunakan untuk membuat data dummy.







