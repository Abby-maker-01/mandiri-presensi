# Absensi SMK Mandiri Haurgeulis

## Perubahan pada versi ini
- Pilihan akun hanya **Guru** dan **Admin**; Guru berada di kiri dan Admin di kanan.
- Pendaftaran akun mandiri hanya untuk Guru dan tetap menunggu persetujuan Admin.
- Akun dengan peran Murid tidak dapat masuk melalui antarmuka ini.
- Rekap Admin menampilkan absensi Guru saja.
- Rekap dipisahkan berdasarkan bulan. Bulan berjalan otomatis dipilih; pilih bulan sebelumnya untuk membuka arsipnya.
- Saat berganti bulan, rekap bulan baru dimulai dari 0 karena hanya data pada bulan terpilih yang dihitung.
- Unduhan CSV mengikuti bulan yang sedang dipilih.

## Riwayat dan data
Perubahan ini tidak menghapus dokumen apa pun dari koleksi Firestore `attendance`. Riwayat lama tetap tersimpan; tampilan hanya memfilter berdasarkan bulan dan peran Guru. Jangan menghapus koleksi Firestore jika ingin mempertahankan arsip.

## Struktur proyek
- `index.html`, `style.css`, `app.js` — aplikasi web.
- `firebase-config.js` — konfigurasi Firebase yang sudah ada.
- `firestore.rules` — aturan Firestore yang disertakan.
- `.github/workflows/build-apk.yml` — workflow GitHub Actions yang disertakan.
- `manifest.json`, `logo.png` — aset aplikasi.

## Memasang lewat GitHub di HP
1. Ekstrak ZIP.
2. Buka repository GitHub dan pastikan branch yang dipakai benar (biasanya `main`).
3. Unggah dan timpa file proyek dengan versi dari ZIP ini, termasuk `.github/workflows/` dan `www` jika ada di proyek tujuan. Untuk proyek ini, file web berada langsung di root.
4. Pastikan `firebase-config.js` tetap berisi konfigurasi Firebase milik proyekmu.
5. Commit perubahan.

## Catatan build
ZIP ini berisi source code proyek dan workflow yang disertakan, bukan APK hasil build. APK baru hanya tersedia setelah workflow berhasil berjalan dan menghasilkan artifact/release. Periksa tab Actions untuk status build.
