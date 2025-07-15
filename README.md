# Putri-Nabiilah-Tugas-Per15-Dasar-Algoritma-dan-Pemograman
# Aplikasi Toko Dimsum (DIMSUM D'LICIOUS)
# 1. Pengembangan Aplikasi
### Implementasi Lengkap Sistem Inventori
- Aplikasi berbasis Python untuk sistem penjual dan pembeli.
- Fitur Penjual dapat:
  - Menambahkan dimsum baru (nama, jumlah, dan harga)
  - Melihat stok dimsum dalam bentuk tabel
  - Melihat total pemasukan
  - Melihat riwayat pembelian
  - Melihat data pembeli
- Fitur Pembeli dapat:
  - Melihat stok dimsum
  - Memesan dimsum dengan jumlah
  - Melihat total harga pembelian
  - Data pembeli dan transaksi tercatat
    
### Penambahan Fitur Tambahan
- Tabel stok menggunakan modul tabulate agar output lebih rapi
- Input dinamis dan validasi jumlah serta harga
- Input terstruktur dengan validasi angka menggunakan fungsi input_angka()
- Riwayat transaksi disimpan otomatis ke memori
- Sistem loop terus berjalan hingga pengguna memutuskan keluar

### Optimasi Kode dan Algoritma
- Modularisasi fungsi: pemisahan fungsi menu_penjual(), menu_pembeli(), tampilkan_stok(), dan input_angka() agar kode lebih bersih dan mudah dibaca
- Validasi input angka dibuat reusable agar tidak menulis ulang try-except
- Pemakaian dictionary bersarang (nested dict) untuk penyimpanan data dimsum (nama -> jumlah & harga)
- Konsistensi penggunaan f-string dan formatting angka (:,) untuk output harga

# 2. Dokumentasi Teknis
### Dokumen Spesifikasi Sistem
- Aplikasi berbasis terminal menggunakan Python
- Aplikasi CLI (Command Line Interface) dengan dua role: Penjual dan Pembeli
- Menggunakan library tambahan: tabulate

### Code Documentation yang Lengkap
- Komentar diberikan di fungsi penting seperti input_angka() dan pemrosesan pesanan
- Penamaan fungsi dan variabel deskriptif dan konsisten

### Diagram Alur Kerja dan Arsitektur
Saat aplikasi dijalankan, pengguna akan disambut dengan halaman utama yang menampilkan pilihan peran, yaitu sebagai Penjual atau Pembeli. Alur penggunaan sistem kemudian akan menyesuaikan berdasarkan peran yang dipilih:
### 1. Jika pengguna memilih sebagai penjual:
Setelah memilih peran sebagai penjual, pengguna akan diarahkan ke menu khusus yang menyediakan berbagai fungsi manajemen terkait inventori dan transaksi. Menu ini terdiri dari:
- Lihat Pemasukan. Menampilkan total pemasukan toko yang didapat dari semua transaksi pembelian yang telah dilakukan oleh pembeli.
- Tambah Stok Dimsum. Penjual dapat menambahkan data dimsum baru atau memperbarui stok dan harga dimsum yang sudah tersedia. Data yang dimasukkan meliputi nama dimsum, jumlah stok, dan harga per pcs.
- Lihat Stok Dimsum. Menampilkan seluruh daftar dimsum yang tersedia dalam bentuk tabel, lengkap dengan jumlah stok dan harga per satuannya. Tabel ditampilkan dengan format yang rapi menggunakan library tabulate.
- Lihat Riwayat Pembelian. Menampilkan daftar seluruh transaksi yang pernah dilakukan pembeli. Informasi yang ditampilkan meliputi nama pembeli, daftar pesanan yang dibeli beserta jumlahnya, serta total harga pembelian.
- Lihat Riwayat Pembelian. Menampilkan daftar seluruh transaksi yang pernah dilakukan pembeli. Informasi yang ditampilkan meliputi nama pembeli, daftar pesanan yang dibeli beserta jumlahnya, serta total harga pembelian.
- Kembali. Kembali ke menu utama untuk memilih ulang peran atau keluar.

### 2. Jika Memilih Sebagai Pembeli
Pembeli akan masuk ke sub-menu yang terdiri dari:
- Lihat Stok Dimsum. Menampilkan stok dimsum yang tersedia dalam bentuk tabel.
- Pesan Dimsum. Pembeli akan menginput nama mereka dan memilih dimsum dari stok yang tersedia.
  - Input jumlah untuk setiap jenis dimsum.
  - Sistem akan menghitung total harga, menyesuaikan stok, dan menyimpan data pembelian ke riwayat_pembelian serta menambahkan pemasukan ke total_pemasukan.
- Setelah selesai memesan, data pembeli dan pesanannya otomatis tersimpan ke memori (list of dictionaries).
- Kembali. Kembali ke menu utama.

### 3. Jika Memilih Keluar
Program akan menampilkan ucapan terima kasih dan mengakhiri loop utama, sehingga aplikasi selesai dijalankan.

### Arsitektur Logika dan Penyimpanan Data
Struktur utama program dibangun dengan:
- Fungsi modular yang memisahkan tugas penjual dan pembeli.
- Loop yang menjaga agar program terus berjalan sampai pengguna keluar.
- Validasi input untuk mencegah kesalahan seperti memasukkan angka negatif atau teks saat diminta angka.

Struktur data yang digunakan:
- dimsum_stock: menyimpan nama, jumlah, dan harga tiap jenis dimsum.
- riwayat_pembelian: menyimpan riwayat transaksi setiap pembeli, termasuk apa yang mereka beli dan total bayar.
- total_pemasukan: menjumlahkan seluruh pendapatan dari transaksi.
- Fungsi tambahan input_angka() dibuat untuk membantu validasi input angka agar kode tidak perlu menulis ulang try-except berkali-kali.

# 3. User Manual
### Panduan instalasi dan konfigurasi
Persyaratan system:
1. Install Python
2. Terminal/Command Prompt
3. Koneksi internet

Langkah instalasi:
1. Pastikan Python sudah terpasang. Cek dengan perintah di terminal: python --version
2. Install library tabulate (untuk menampilkan tabel stok)
3. Menjalankan program:
   -  Simpan file kode Python dengan nama misalnya: dimsum_app.py
   -  Jalankan dari terminal: python dimsum_app.py

### Tutorial penggunaan aplikasi
Saat program dijalankan kita akan melihat menu utama, yaitu:
1. Penjual
2. Pembeli
3. Keluar

Jika kita sebagai penjual, kita akan melihat dan dapat memilih menu:
1. Lihat pemasukan
2. Tambah stok dimsum
3. Lihat stok dimsum
4. Lihat riwayat pembelian
5. Kembali

Note: Di bagian menu nomor 2 (tambah stok dimsum) akan diminta untuk menginput nama dimsum, jumlah stok, dan harga. Jika dimsum sudah ada, maka stok akan terus bertambah.

Jika kita sebagai pembeli, kita akan melihat dan dapat memilih menu:
1. Lihat stok dimsum
2. Pesan dimsum
3. Kembali

Note: Di bagian menu nomor 2 (pesan dimsum) akan diminta untuk menginput nama pembeli, lalu ada pilih dimsum dari stok yang tersedia, kemudian masukkan jumlah yang ingin dipesan dan sistem akan menghitung total harga. Setelah selesai, data pembelian kamu akan dicatat dan stok akan otomatis berkurang.

### FAQ dan troubleshooting guide
Q: Program tidak bisa dijalankan, muncul error ModuleNotFoundError: No module named 'tabulate'
A: Kamu perlu install modul tabulate dengan perintah:
    - pip install tabulate

Q: Saya sudah pesan dimsum tapi stok tidak berkurang
A: Pastikan kamu menyelesaikan pesanan sampai input "selesai". Jika tidak, data tidak akan diproses.

Q: Bagaimana cara keluar dari aplikasi?
A: Dari menu utama, pilih opsi nomor 3 (Keluar), atau tekan Ctrl + C untuk keluar paksa dari terminal.

# 4. Pengujian dan Evaluasi
### Test suite yang komprehensif
1. Menambah stok dapat berfungsi dengan baik
2. Melihat tabel stok juga rapi dan jelas
3. Input invalid (huruf, negatif) tertolak
4. Pesanan pembeli tercatat
5. Update stok otomatis bisa berjalan

### Laporan Hasil Pengujian:
1. Semua skenario pengujian berjalan dengan hasil sesuai harapan
2. Input yang tidak valid langsung tertolak dan tidak menyebabkan program crash
3. Setiap transaksi langsung memengaruhi pemasukan dan stok
4. Output tabel terlihat rapi, memudahkan pembeli dan penjual

### Analisis kinerja dan optimisasi
1. Waktu eksekusi sangat cepat karena tidak menggunakan database eksternal dan struktur data yang ringan
2. Struktur data efisien untuk operasi baca-tulis
3. Disarankan menyimpan data ke file JSON agar riwayat tidak hilang saat program ditutup
4. Sistem sangat fleksibel dan dapat diintegrasikan ke sistem GUI atau web
