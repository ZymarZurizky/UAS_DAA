# **Analisis Sistem: Komunitas Jual Beli Barang Bekas**

---

## **1. Latar Belakang**

Dalam beberapa tahun terakhir, kesadaran masyarakat terhadap pentingnya gaya hidup berkelanjutan semakin meningkat. Salah satu upaya yang dilakukan untuk mendukung keberlanjutan adalah dengan mengurangi limbah dan memaksimalkan penggunaan kembali barang-barang yang masih layak pakai. Jual beli barang bekas menjadi salah satu solusi yang dapat membantu mengurangi jumlah sampah yang dihasilkan serta memberikan manfaat ekonomi bagi individu yang ingin menjual atau membeli barang dengan harga lebih terjangkau.

Namun, meskipun terdapat berbagai keuntungan dari sistem jual beli barang bekas, masyarakat masih menghadapi berbagai kendala dalam melakukan transaksi tersebut. Salah satu permasalahan utama adalah sulitnya menemukan platform yang terpercaya dan efisien untuk mempertemukan penjual dan pembeli. Banyak individu yang masih mengandalkan media sosial atau forum online yang belum memiliki sistem keamanan yang memadai untuk memastikan transaksi yang aman dan nyaman.

Selain itu, kurangnya transparansi dalam kondisi barang, harga yang tidak konsisten, serta minimnya sistem rating dan ulasan sering kali membuat pembeli merasa ragu dalam melakukan transaksi. Di sisi lain, penjual juga sering mengalami kesulitan dalam menjangkau calon pembeli yang potensial. Tidak adanya platform yang terpusat untuk jual beli barang bekas juga membuat proses pencarian dan transaksi menjadi tidak efisien.

Oleh karena itu, dibutuhkan sebuah solusi dalam bentuk platform digital yang dapat mempertemukan penjual dan pembeli barang bekas dengan lebih mudah, aman, dan terpercaya. Platform ini diharapkan dapat memberikan berbagai fitur seperti sistem rating dan ulasan, pencarian barang berdasarkan kategori, serta kemudahan dalam berkomunikasi antara penjual dan pembeli. Dengan adanya platform yang lebih terstruktur, transaksi jual beli barang bekas dapat menjadi lebih efisien dan terpercaya, serta turut mendukung ekonomi sirkular yang lebih berkelanjutan.

## **2. Identifikasi Masalah**

Berdasarkan studi awal, masalah utama yang dihadapi adalah:

1. **Kesulitan Menemukan Pembeli/Penjual**: Banyak orang kesulitan menemukan pembeli atau penjual untuk barang bekas mereka.
2. **Kurangnya Kepercayaan**: Transaksi barang bekas seringkali dihambat oleh kurangnya kepercayaan antara pembeli dan penjual.
3. **Tidak Ada Platform Terpusat**: Tidak adanya platform yang memudahkan pencarian dan transaksi barang bekas secara efisien.

4.**Manajemen Transaksi yang Rumit**: Proses transaksi seringkali tidak terorganisir dengan baik.

## **3. Rumusan Masalah**

Berdasarkan identifikasi masalah, rumusan masalahnya adalah:

- Bagaimana cara membuat platform yang memudahkan transaksi barang bekas?
- Bagaimana meningkatkan kepercayaan antara pembeli dan penjual?
- Bagaimana menyediakan fitur yang memudahkan manajemen transaksi?

## **4. Tujuan Penelitian**

Tujuan dari penelitian ini adalah:

1. Membangun platform komunitas jual beli barang bekas yang terpercaya dan efisien.
2. Meningkatkan kepercayaan antara pembeli dan penjual melalui sistem rating dan ulasan.
3. Memudahkan manajemen transaksi dengan fitur yang terintegrasi.

## **5. Metode Analisis**

Metode analisis yang digunakan adalah **Fishbone Diagram (Diagram Tulang Ikan)** untuk mengidentifikasi akar masalah dan solusi.

### **Fishbone Diagram**

```plaintext

Masalah Utama: Kesulitan dalam Transaksi Barang Bekas

  |

  +---> Manusia (Human)

  |       - Kurangnya kepercayaan antara pembeli dan penjual

  |       - Kurangnya partisipasi aktif

  |

  +---> Metode (Method)

  |       - Tidak ada sistem rating dan ulasan

  |       - Proses transaksi yang rumit

  |

  +---> Material (Material)

  |       - Kualitas barang bekas yang tidak terjamin

  |       - Kurangnya informasi detail tentang barang

  |

  +---> Mesin (Machine)

  |       - Tidak ada platform terpusat

  |       - Kurangnya fitur yang memudahkan transaksi

  |

  +---> Lingkungan (Environment)

          - Kurangnya kesadaran masyarakat tentang ekonomi sirkular

          - Tidak ada dukungan dari komunitas lokal

```

## **6. Perancangan Sistem**

### **a. Arsitektur Sistem**

-**Frontend**: HTML, CSS, JavaScript

-**Backend**: Laravel (PHP)

-**Database**: MySQL

-**Admin Panel**: Filament

### **b. Use Case Diagram**

```plaintext

+-------------------+

|      Actors       |

+-------------------+

| - Penjual         |

| - Pembeli         |

| - Admin           |

+-------------------+

        |

        v

+-------------------+

|    Use Cases      |

+-------------------+

| - Login/Register  |

| - Unggah Barang   |

| - Cari Barang     |

| - Transaksi       |

| - Kelola Platform |

+-------------------+

```

### **c. Entity Relationship Diagram (ERD)**

```plaintext

+-----------------+       +-----------------+       +-----------------+

|     Users       |       |     Products    |       |   Transactions  |

+-----------------+       +-----------------+       +-----------------+

| user_id (PK)    |<------| product_id (PK) |       | transaction_id  |

| username        |       | user_id (FK)    |       | product_id (FK) |

| password        |       | name            |       | buyer_id (FK)   |

| email           |       | description     |       | seller_id (FK)  |

| phone_number    |       | price           |       | status          |

| role            |       | category        |       | date            |

+-----------------+       | status          |       +-----------------+

                          +-----------------+

```

## **7. Implementasi Teknologi**

* **Frontend**: Menggunakan React.js untuk antarmuka pengguna yang interaktif.
* **Backend**: Menggunakan Laravel untuk logika bisnis dan API.
* **Database**: MySQL untuk menyimpan data pengguna, produk, dan transaksi.

-**Admin Panel**: Menggunakan Filament untuk manajemen data oleh admin.

## **8. Implementasi Fitur Berdasarkan Studi Kasus**

### **a. Fitur untuk Penjual**

1. **Unggah Barang**: Penjual dapat mengunggah informasi barang yang ingin dijual.
2. **Kelola Barang**: Penjual dapat mengedit atau menghapus barang yang sudah diunggah.
3. **Chat dengan Pembeli**: Penjual dapat berkomunikasi langsung dengan pembeli.

### **b. Fitur untuk Pembeli**

1. **Cari Barang**: Pembeli dapat mencari barang berdasarkan kategori, lokasi, atau harga.
2. **Transaksi**: Pembeli dapat melakukan transaksi dan memberikan ulasan.
3. **Chat dengan Penjual**: Pembeli dapat berkomunikasi langsung dengan penjual.

### **c. Fitur untuk Admin**

1. **Kelola Pengguna**: Admin dapat mengelola data pengguna (penjual/pembeli).
2. **Kelola Produk**: Admin dapat memantau dan mengelola produk yang diunggah.
3. **Kelola Transaksi**: Admin dapat memantau dan mengelola transaksi.

## **9. Kesimpulan**

Platform komunitas jual beli barang bekas ini dirancang untuk memudahkan transaksi, meningkatkan kepercayaan, dan mempromosikan gaya hidup berkelanjutan. Dengan fitur-fitur yang terintegrasi, platform ini diharapkan dapat menjadi solusi efektif bagi masyarakat.
