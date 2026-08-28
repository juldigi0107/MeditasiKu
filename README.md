# MeditasiKu V17 — Clean Modular Rebuild

Build ini mengganti shell lama yang memuat React inline dan gambar Base64. UI utama sekarang tersusun dari file HTML, CSS, JavaScript, dan aset eksternal yang terpisah.

## Upload ke GitHub Pages

1. Ekstrak ZIP.
2. Upload **seluruh isi** folder ke root repository `MeditasiKu`.
3. Pastikan `index.html`, semua file `.js`/`.css`, `manifest.webmanifest`, `meditasiku-sw.js`, dan folder `assets` berada di root yang sama.
4. Commit perubahan dan tunggu proses Pages selesai.
5. Buka `https://juldigi0107.github.io/MeditasiKu/?v=17`.

Untuk memastikan versi lama tidak tertahan di iPhone, hapus PWA lama dan data situs `juldigi0107.github.io` dari **Settings → Safari → Advanced → Website Data**, lalu buka ulang URL V17.

## File aktif

- `index.html` — shell kecil tanpa bundle UI tertanam.
- `meditasiku-app.css` — seluruh sistem visual utama.
- `meditasiku-app.js` — navigasi dan renderer layar utama.
- `meditasiku-production.css` / `meditasiku-production.js` — detail Dose, kategori, player, Create Studio, dan penyimpanan lokal.
- `meditasiku-dose-data.js` / `meditasiku-extra-300.js` — katalog kanonis 500 Dose dalam 50 kategori.
- `assets/` — artwork dan ikon eksternal.
- `meditasiku-sw.js` — cache PWA V17.

File legacy seperti `meditasiku-sanctuary*.css/js`, `meditasiku-graphics.*`, `meditasiku-dose.css`, dan `meditasiku-uiux-v16.*` tidak lagi dipanggil. Jika masih ada di repository lama, file tersebut boleh dihapus setelah V17 berhasil berjalan.

## Perilaku yang dipertahankan

- 500 Dose / 50 kategori.
- Detail Dose dan technical details.
- Player DSP, timer, kontrol transport, ambience tematik, volume, intensitas, repeat, shuffle, favorite, dan offline recipe.
- Create Studio.
- Library/Profile berbasis data lokal.
- Splash, onboarding, Home, Explore, kategori, dan dock yang responsif.

