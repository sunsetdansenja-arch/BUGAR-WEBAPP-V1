# Protokol Dorman dan Recovery Bugar

## Status saat ini
Semua halaman aplikasi berakhiran `.html` di root repo sedang menampilkan halaman **Server Dorman**:
- `index.html`
- `index.active.html`
- `keuangan.html`
- `logistik.html`
- `owner.html`
- `review.html`
- `stocking.html`
- `supervisor.html`
- `test.html`

Halaman dorman hanya menampilkan status layanan sementara tidak aktif dan tidak menjalankan fitur aplikasi atau request ke backend.

## Pemicu recovery
Anggap semua instruksi berikut sebagai permintaan pemulihan yang sama:
- **"recover bugar"**
- **"perbaiki index bugar"**
- **"pulihkan Bugar"**
- **"aktifkan kembali Bugar"**
- Instruksi serupa yang jelas bermaksud mengembalikan aplikasi Bugar dari mode dorman.

## Prosedur recovery — langsung eksekusi
1. Baca protokol ini dan cek file HTML yang ada saat instruksi diterima.
2. Pulihkan kode aplikasi asli untuk **seluruh sembilan file HTML** di daftar atas, bukan hanya `index.html`.
3. Gunakan blob kode asli yang disimpan di riwayat Git sebelum file-file diganti menjadi halaman dorman. Blob SHA versi asli:
   - `index.html`: `291a18d2714e9c666385b28d71a3a6266c24b7eb`
   - `index.active.html`: `291a18d2714e9c666385b28d71a3a6266c24b7eb`
   - `keuangan.html`: `4419b6db4f2ec795e93d587f78488bb5fda560d9`
   - `logistik.html`: `83f65a1ec8f16163124edbb60e25fbea3d91f77a`
   - `owner.html`: `d454d65ab0da005028b646be043ab47cbb6f198f`
   - `review.html`: `f054db5c32d704fb797e7699a76719cdefbbf258`
   - `stocking.html`: `8f67f6a65dee289ddb0ce22f0c5005b015573745`
   - `supervisor.html`: `674a4be0b2b7e4f51672167928e9c674adf362b5`
   - `test.html`: `291a18d2714e9c666385b28d71a3a6266c24b7eb`
4. Ambil isi blob dari GitHub, lalu update file yang cocok dengan SHA terbaru masing-masing. Jangan mengarang atau menulis ulang isi HTML dari ingatan.
5. Pertahankan file logo, workflow/backend, dan file non-HTML lainnya. Jangan mengubah scope di luar pemulihan ini.
6. Commit/push perubahan ke branch `main` tanpa meminta konfirmasi ulang, karena trigger recovery merupakan otorisasi pengguna.
7. Verifikasi isi file hasil pemulihan dan laporkan daftar file, commit, serta tautan repo. Jangan mengklaim deployment sudah selesai kecuali benar-benar diverifikasi.

## Prosedur dorman ulang
Jika pengguna meminta Bugar dijadikan dorman lagi, simpan referensi/blob aplikasi aktif terbaru terlebih dahulu, lalu ganti semua halaman HTML di daftar tersebut dengan halaman status dorman. Update protokol dan commit ke `main`.

## Batasan
- Jangan menghapus data atau workflow backend.
- Jangan mengubah file selain HTML target dan protokol kecuali diperlukan untuk menjaga pemulihan.
- Jika ada perubahan aplikasi yang lebih baru dan secara eksplisit disetujui pengguna setelah SHA di atas, prioritaskan versi terbaru yang disetujui; perbarui daftar blob sebelum melakukan recovery.
