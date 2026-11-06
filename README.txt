MBSTORE - Paket aplikasi pembukuan konter pulsa

ISI:
- index.html: aplikasi MBSTORE
- manifest.webmanifest: identitas aplikasi untuk pemasangan PWA
- sw.js: cache offline saat aplikasi diakses melalui HTTPS/localhost

FITUR VERSI 1:
- Dompet Cash, GoPay, DANA, SeaBank, Saldo Pulsa, dan dompet tambahan
- Pengaturan saldo/modal awal tiap dompet
- Penjualan: masukkan harga jual, harga modal, dompet penerima, dan dompet sumber saldo pulsa
- Pengeluaran, tambah modal, pengambilan pribadi, transfer antar-dompet
- Dashboard, riwayat, laporan keuntungan bersih dan saldo akhir
- Backup JSON dan pemulihan backup
- Penyimpanan lokal pada browser/perangkat

CARA PAKAI DI ANDROID:
1. Ekstrak folder MBSTORE.
2. Agar dapat dipasang sebagai aplikasi PWA dan berjalan offline dengan stabil, unggah isi folder ke hosting HTTPS milik sendiri.
3. Buka alamat hosting tersebut menggunakan Chrome Android.
4. Pilih menu Chrome (titik tiga) > Tambahkan ke layar utama / Install app.
5. Buka MBSTORE dari ikon layar utama.
6. Isi saldo awal setiap dompet melalui Atur dompet.
7. Buat backup secara berkala dan simpan di lokasi aman.

CATATAN PENTING:
Paket ini adalah PWA offline-installable, BUKAN APK Android native. Lingkungan pembuatan ini tidak memiliki Android SDK/Gradle untuk membangun dan menandatangani APK. APK native belum dibuat.
Data tidak tersinkron otomatis ke cloud. Pilihan backup saat ini adalah ekspor/impor file JSON manual. Aplikasi tidak membaca saldo GoPay/DANA/SeaBank atau aplikasi pulsa secara otomatis; semua transaksi perlu dicatat oleh pengguna. Data lokal dapat hilang jika data browser dihapus atau perangkat rusak, jadi lakukan backup berkala.

PERHITUNGAN:
- Penjualan menambah harga jual ke dompet penerima.
- Penjualan mengurangi harga modal dari dompet sumber pulsa.
- Laba kotor = harga jual - harga modal.
- Laba bersih = total laba kotor - pengeluaran.
- Transfer hanya memindahkan saldo antar dompet, bukan pemasukan/pengeluaran.
- Tambah modal bukan keuntungan.
- Saldo akhir = saldo awal seluruh dompet + seluruh perubahan saldo dari transaksi.
