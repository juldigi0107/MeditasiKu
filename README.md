# MeditasiKu V24 — GitHub Frontend + Cloudflare Workers/D1

Deployment source untuk MeditasiKu V24.

- Frontend shell dipublikasikan melalui GitHub Pages.
- Authentication, membership, payment, recipe, entitlement, dan artwork protected dilayani Cloudflare Worker + D1.
- Repository ini sengaja **tidak** menyimpan 500 recipe canonical, 500 full artwork, atau category artwork protected.
- Private D1 seed diimpor terpisah melalui Admin → Konten D1 setelah backend live.

Akses default:
- Admin awal: `superadmin`
- Password awal: `superadmin123`
- Wajib diganti segera pada login pertama.

Plan:
- Free: 1 Dose per kategori dapat dibuka, semua Dose tetap terlihat dengan lock.
- Pro: 5 Dose per kategori dapat dibuka.
- Premium: seluruh Dose.
- Admin: seluruh Dose + Admin Settings.

Release: V24 D1 protected content.
