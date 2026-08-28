# MeditasiKu — GitHub Pages V15 (Premium App Graphics Checkpoint)

Build transisi untuk pengujian personal melalui GitHub Pages/PWA dengan 50 kategori dan 500 Dose.

- Katalog tetap berisi 500 Dose dan 50 kategori.
- 60 Dose pertama memakai artwork WebP premium individual 768×960.
- 140 Dose lama masih memakai placeholder SVG individual dari V6.
- 300 Dose baru memakai fallback gerbang Sanctuary sampai artwork individual tersedia.
- Data memakai adapter field kanonis Master Prompt V3.
- Status publikasi diturunkan menjadi `DRAFT` karena reviewed audio master belum tersedia.
- Realtime Web Audio DSP tetap dapat diuji, tetapi bukan audio master produksi.

Build ini adalah checkpoint pengujian personal sampai 500 artwork raster dan audio master selesai direview.

## Integrasi grafis V14

- `meditasiku-graphics.js` mencoba artwork Dose premium, cover dan simbol
  kategori, serta background halaman berdasarkan manifest grafis V14.
- Bila file grafis baru belum tersedia atau gagal dimuat, aplikasi otomatis
  kembali ke artwork/background lama. Navigasi, player, katalog, dan offline
  recipe tidak dihentikan oleh kegagalan aset visual.
- Unggah hasil generate dengan path dan nama file persis dari master prompt V14.
- Aset yang berhasil dimuat aktif otomatis tanpa perlu mengedit HTML kembali.

## Grafis aplikasi V15

- 24 background aplikasi termasuk splash, Gate, tujuh tahap onboarding, Home,
  Explore, Detail, Player, Create, Library, Profile, Settings, Search, Offline,
  Premium, Technical Details, dan Blackout.
- Logo mark, wordmark, tiga ikon instalasi PWA, tiga tekstur tombol, tiga overlay,
  player orb, waveform, dan 33 ikon UI raster transparan.
- Onboarding memilih background berdasarkan langkah yang sedang tampil.
- Tombol memakai ikon premium hanya jika file terkait tersedia; fallback teks dan
  fungsi lama tetap dipertahankan.
- Cache shell memakai `meditasiku-release-v15-premium-app-graphics`.
- 19 ikon UI dan 50 simbol kategori masih menunggu reset kuota generator; aplikasi
  tetap menggunakan fallback lama untuk file yang belum ada.

## Perubahan V8

- 200 recipe dibangun ulang berdasarkan kata kunci judul, fungsi kategori, dan sound palette.
- 200 design signature dan fingerprint recipe unik.
- Player menjalankan ambient, colored noise, tonal, stereo, EQ, limiter, dan fade dari recipe aktual.
- Evidence dan sumber ditampilkan pada Dose Detail.
- Klaim binaural, colored noise, sleep, focus, dan natural sound dibuat konservatif.
- Review audio master tidak dipalsukan: seluruh Dose berstatus `NOT_REVIEWABLE_NO_MASTER` sampai file WAV/FLAC/AAC tersedia.
- Lihat `RECIPE_RESEARCH_AUDIT.md` untuk hasil audit dan sumber.
- Player memiliki Theme Mixer adaptif: hujan, angin, pantai, api unggun, hutan, aliran air, malam, dan kafe tenang hanya ditampilkan bila sesuai dengan Dose.
- Explore menampilkan seluruh 50 kategori dan 500 Dose.
- Detail utama memakai bahasa sederhana; recipe, DSP, evidence, dan status audio master berada di tombol **Buka Technical Details**.

## Perubahan V13

- Tepat 50 kategori dan 500 Dose; setiap kategori berisi 10 Dose.
- 30 kategori tambahan tersimpan di `meditasiku-extra-300.js` dan dimuat sebelum database utama.
- Kategori dibagi menjadi Core Sanctuary, Functional Journeys, Soundscape Worlds, dan Emotional & Perceptual Journeys.
- Pemilihan kategori menampilkan resume fungsi, karakter suara, target pengguna, perhatian keselamatan, lalu 10 Dose dengan ringkasan individual.
- Seluruh recipe memiliki design signature unik dan menjalankan jalur adapter/validator yang sama.
- Auditory Illusion Lab tidak memuat voice, perintah tersembunyi, infrasonik, atau ultrasonik.

Paket ini memakai path relatif sehingga dapat dipasang pada repository GitHub Pages dengan nama apa pun.

## Cara upload dari iPhone atau browser

1. Masuk ke https://github.com dan buat repository baru, misalnya `meditasiku-pwa`.
2. Pilih **Public**, lalu tekan **Create repository**.
3. Pilih **Add file → Upload files**.
4. Ekstrak ZIP ini, lalu unggah **semua isi foldernya**. `index.html` wajib berada di root repository, bukan dalam folder tambahan.
   Pastikan folder `assets/app`, `assets/doses`, dan `assets/doses-raster` ikut terunggah.
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

- `meditasiku-dose-data.js`: database lokal 500 Dose / 50 kategori, metadata editorial, recipe DSP, evidence, safety, setup, lima tips kontekstual, dan pemetaan artwork.
- `assets/doses/`: 200 SVG legacy; 60 Dose pertama menggunakan raster WebP, sedangkan 300 Dose tambahan menggunakan fallback gerbang sampai artwork final tersedia.
- `assets/app/sanctuary-gateway.webp`: environment utama Sanctuary untuk splash dan atmosfer global.
- `meditasiku-production.js`: detail Dose Sanctuary tunggal untuk Home, Explore/kategori, Search, dan Library; player DSP; timer 1–480 menit; favorite; history; playlist; download offline; settings.
- `meditasiku-sw.js`: cache shell PWA dan cache artwork ketika Dose disimpan offline.

## Setelah memperbarui repository

GitHub Pages dapat memerlukan 1–5 menit untuk menerbitkan commit. Service Worker build ini memakai cache `meditasiku-release-v13-50-categories-500-dose`, sehingga cache versi lama akan dibuang setelah Service Worker baru aktif. Jika Safari masih menampilkan versi lama, tutup PWA dari app switcher, buka URL GitHub Pages sekali di Safari, lalu jalankan kembali PWA.

## Batas paket statis

Realtime Web Audio DSP, data lokal, artwork, dan offline PWA bekerja tanpa backend. Authentication cloud, pembelian App Store/Google Play, entitlement lintas perangkat, CDN audio master, serta CMS tetap berstatus **BLOCKED** sampai layanan produksi dan kredensial resminya tersedia; aplikasi tidak memalsukan layanan tersebut.
