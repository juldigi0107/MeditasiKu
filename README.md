# MeditasiKu — GitHub Pages V9 (Adaptive Themes + Complete Categories)

Build transisi untuk pengujian personal melalui GitHub Pages/PWA.

- Katalog tetap berisi 200 Dose dan 20 kategori.
- 60 Dose pertama memakai artwork WebP premium individual 768×960.
- 140 Dose berikutnya masih memakai placeholder SVG individual dari V6.
- Data memakai adapter field kanonis Master Prompt V3.
- Status publikasi diturunkan menjadi `DRAFT` karena reviewed audio master belum tersedia.
- Realtime Web Audio DSP tetap dapat diuji, tetapi bukan audio master produksi.

Build ini adalah checkpoint pengujian personal sampai 200 artwork raster dan audio master selesai direview.

## Perubahan V8

- 200 recipe dibangun ulang berdasarkan kata kunci judul, fungsi kategori, dan sound palette.
- 200 design signature dan fingerprint recipe unik.
- Player menjalankan ambient, colored noise, tonal, stereo, EQ, limiter, dan fade dari recipe aktual.
- Evidence dan sumber ditampilkan pada Dose Detail.
- Klaim binaural, colored noise, sleep, focus, dan natural sound dibuat konservatif.
- Review audio master tidak dipalsukan: seluruh Dose berstatus `NOT_REVIEWABLE_NO_MASTER` sampai file WAV/FLAC/AAC tersedia.
- Lihat `RECIPE_RESEARCH_AUDIT.md` untuk hasil audit dan sumber.
- Player memiliki Theme Mixer adaptif: hujan, angin, pantai, api unggun, hutan, aliran air, malam, dan kafe tenang hanya ditampilkan bila sesuai dengan Dose.
- Explore menampilkan seluruh 20 kategori dan 200 Dose.
- Detail utama memakai bahasa sederhana; recipe, DSP, evidence, dan status audio master berada di tombol **Buka Technical Details**.

Paket ini memakai path relatif sehingga dapat dipasang pada repository GitHub Pages dengan nama apa pun.

## Cara upload dari iPhone atau browser

1. Masuk ke https://github.com dan buat repository baru, misalnya `meditasiku-pwa`.
2. Pilih **Public**, lalu tekan **Create repository**.
3. Pilih **Add file → Upload files**.
4. Ekstrak ZIP ini, lalu unggah **semua isi foldernya**. `index.html` wajib berada di root repository, bukan dalam folder tambahan.
   Pastikan folder `assets/app` dan `assets/doses` ikut terunggah; folder Dose berisi tepat 200 artwork individual.
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

## Isi build ini

- `meditasiku-dose-data.js`: database lokal 200 Dose / 20 kategori, metadata editorial, recipe DSP, evidence, safety, setup, lima tips kontekstual, dan pemetaan artwork.
- `assets/doses/`: 200 SVG premium individual. Nama file dipetakan satu-ke-satu oleh database dan telah diperiksa tanpa path hilang.
- `assets/app/sanctuary-gateway.webp`: environment utama Sanctuary untuk splash dan atmosfer global.
- `meditasiku-production.js`: detail Dose Sanctuary tunggal untuk Home, Explore/kategori, Search, dan Library; player DSP; timer 1–480 menit; favorite; history; playlist; download offline; settings.
- `meditasiku-sw.js`: cache shell PWA dan cache artwork ketika Dose disimpan offline.

## Setelah memperbarui repository

GitHub Pages dapat memerlukan 1–5 menit untuk menerbitkan commit. Service Worker build ini memakai cache `meditasiku-release-v6-dose-artwork-player`, sehingga cache versi lama akan dibuang setelah Service Worker baru aktif. Jika Safari masih menampilkan versi lama, tutup PWA dari app switcher, buka URL GitHub Pages sekali di Safari, lalu jalankan kembali PWA.

## Batas paket statis

Realtime Web Audio DSP, data lokal, artwork, dan offline PWA bekerja tanpa backend. Authentication cloud, pembelian App Store/Google Play, entitlement lintas perangkat, CDN audio master, serta CMS tetap berstatus **BLOCKED** sampai layanan produksi dan kredensial resminya tersedia; aplikasi tidak memalsukan layanan tersebut.
