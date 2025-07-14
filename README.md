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

# 3. Diagram alur kerja dan arsitektur
START
 └── Pilih Role: Penjual / Pembeli
       ├── Penjual
       │     ├── Lihat Pemasukan
       │     ├── Tambah Stok
       │     ├── Lihat Stok
       │     └── Lihat Riwayat Pembelian
       └── Pembeli
             ├── Lihat Stok
             └── Pesan Dimsum
                    └── Tampilkan Total dan Simpan Riwayat


