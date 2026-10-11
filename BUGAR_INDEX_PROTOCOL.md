# Protokol Index Bugar

## Status saat ini
- `index.html` menampilkan halaman **Server Dorman** selama layanan sementara tidak aktif.
- Versi aplikasi kasir aktif yang sebelumnya ada di `index.html` disimpan utuh di `index.active.html`.

## Trigger pemulihan
Jika Dimas mengatakan **"perbaiki index bugar"**, pulihkan versi aplikasi aktif dari `index.active.html` ke `index.html` dan langsung commit/push ke branch `main` tanpa meminta konfirmasi ulang.

## Batasan
- Jangan mengubah file lain di luar permintaan.
- Sebelum pemulihan, cek apakah `index.active.html` memang versi aktif yang dimaksud; jika pengguna telah menyetujui versi aktif yang lebih baru, gunakan versi terbaru tersebut.
- Laporkan hasil push dan tautan commit setelah selesai.
