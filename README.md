# Putri-Nabiilah-Tugas-Per15-Dasar-Algoritma-dan-Pemograman
# 1. Pengembangan Aplikasi
## Implementasi Lengkap Sistem Inventori
- Aplikasi berbasis Python untuk sistem penjual dan pembeli.
- Fitur Penjual:
  - Menambahkan dimsum baru (nama, jumlah, dan harga)
  - Melihat stok dimsum dalam bentuk tabel
  - Melihat total pemasukan
  - Melihat riwayat pembelian
  - Melihat data pembeli
- Fitur Pembeli:
  - Melihat stok dimsum
  - Memesan dimsum dengan jumlah
  - Melihat total harga pembelian
  - Data pembeli dan transaksi tercatat
    
## Penambahan Fitur Tambahan
- Tabel stok menggunakan modul tabulate agar output lebih rapi
- Input dinamis dan validasi jumlah serta harga
- Struktur data disimpan dalam dictionary nested (nama → jumlah & harga)
- Riwayat transaksi disimpan otomatis ke memori
- Sistem loop terus berjalan hingga pengguna memutuskan keluar

## Optimasi Kode dan Algoritma
- Modularisasi fungsi (tampilkan_stok, menu_penjual, menu_pembeli) agar kode tidak duplikatif
- Validasi input dengan try-except
- Penggunaan .title() untuk konsistensi nama dimsum
- Optimasi struktur data agar scalable dan mudah dikembangkan
