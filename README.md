# Putri-Nabiilah-Tugas-Per15-Dasar-Algoritma-dan-Pemograman
# Aplikasi Toko Dimsum (DIMSUM D'LICIOUS)
# 1. Pengembangan Aplikasi
## Implementasi Lengkap Sistem Inventori
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
    
## Penambahan Fitur Tambahan
- Tabel stok menggunakan modul tabulate agar output lebih rapi
- Input dinamis dan validasi jumlah serta harga
- Input terstruktur dengan validasi angka menggunakan fungsi input_angka()
- Riwayat transaksi disimpan otomatis ke memori
- Sistem loop terus berjalan hingga pengguna memutuskan keluar

## Optimasi Kode dan Algoritma
- Modularisasi fungsi: pemisahan fungsi menu_penjual(), menu_pembeli(), tampilkan_stok(), dan input_angka() agar kode lebih bersih dan mudah dibaca
- Validasi input angka dibuat reusable agar tidak menulis ulang try-except
- Pemakaian dictionary bersarang (nested dict) untuk penyimpanan data dimsum (nama -> jumlah & harga)
- Konsistensi penggunaan f-string dan formatting angka (:,) untuk output harga

# 2. Dokumentasi Teknis
## Dokumen Spesifikasi Sistem
- Aplikasi berbasis terminal menggunakan Python
- Aplikasi CLI (Command Line Interface) dengan dua role: Penjual dan Pembeli
- Menggunakan library tambahan: tabulate

## Code Documentation yang Lengkap
- Komentar diberikan di fungsi penting seperti input_angka() dan pemrosesan pesanan
- Penamaan fungsi dan variabel deskriptif dan konsisten

## Diagram Alur Kerja dan Arsitektur
Saat aplikasi dijalankan, pengguna akan disambut dengan halaman utama yang menampilkan pilihan peran, yaitu sebagai Penjual atau Pembeli. Alur penggunaan sistem kemudian akan menyesuaikan berdasarkan peran yang dipilih:
## 1. Jika pengguna memilih sebagai penjual:
Setelah memilih peran sebagai penjual, pengguna akan diarahkan ke menu khusus yang menyediakan berbagai fungsi manajemen terkait inventori dan transaksi. Menu ini terdiri dari:
- # Lihat Pemasukan
  Menampilkan total pemasukan toko yang didapat dari semua transaksi pembelian yang telah dilakukan oleh pembeli.
- # Tambah Stok Dimsum
  Penjual dapat menambahkan data dimsum baru atau memperbarui stok dan harga dimsum yang sudah tersedia. Data yang dimasukkan meliputi nama dimsum, jumlah stok, dan harga per pcs.

Lihat Stok Dimsum
Menampilkan seluruh daftar dimsum yang tersedia dalam bentuk tabel, lengkap dengan jumlah stok dan harga per satuannya. Tabel ditampilkan dengan format yang rapi menggunakan library tabulate.

Lihat Riwayat Pembelian
Menampilkan daftar seluruh transaksi yang pernah dilakukan pembeli. Informasi yang ditampilkan meliputi nama pembeli, daftar pesanan yang dibeli beserta jumlahnya, serta total harga pembelian.




