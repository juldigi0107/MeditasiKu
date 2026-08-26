# MeditasiKu — Paket GitHub Pages

Paket ini memakai path relatif sehingga dapat dipasang pada repository GitHub Pages dengan nama apa pun.

## Cara upload dari iPhone atau browser

1. Masuk ke https://github.com dan buat repository baru, misalnya `meditasiku-pwa`.
2. Pilih **Public**, lalu tekan **Create repository**.
3. Pilih **Add file → Upload files**.
4. Ekstrak ZIP ini, lalu unggah **semua isi foldernya**. `index.html` wajib berada di root repository, bukan dalam folder tambahan.
5. Isi commit message `Upload MeditasiKu PWA`, lalu tekan **Commit changes**.
6. Buka **Settings → Pages**.
7. Pada **Build and deployment**, pilih **Deploy from a branch**.
8. Pilih branch **main**, folder **/(root)**, lalu tekan **Save**.
9. Tunggu sampai muncul URL `https://USERNAME.github.io/NAMA-REPOSITORY/`.

## Memasang di iPhone

1. Buka URL GitHub Pages menggunakan Safari.
2. Tekan **Share → Add to Home Screen**.
3. Jalankan MeditasiKu dari ikon Home Screen.

## Jika versi lama masih muncul

Refresh URL di Safari. Jika masih lama, hapus ikon PWA, buka **Settings iPhone → Safari → Advanced → Website Data**, hapus data domain GitHub Pages terkait, lalu pasang kembali.

## Catatan

- Gunakan HTTPS GitHub Pages; jangan membuka `index.html` langsung dari aplikasi Files.
- Favorit, riwayat, custom Dose, settings, dan data offline tersimpan lokal di perangkat.
- Penyimpanan PWA iOS dapat dihapus oleh sistem atau pengguna.
- Backend, pembayaran asli, dan sinkronisasi akun belum merupakan layanan produksi dalam paket statis ini.
