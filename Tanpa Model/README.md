# Tanpa Model — Iklan Video 10 Detik

Ubah **satu foto produk** menjadi **satu video iklan 10 detik** langsung di Google Flow.

Tanpa model. Tanpa wajah. Tanpa CapCut. Tanpa edit manual.

Versi ini hanya memakai **1 foto produk**. Tidak ada foto model yang diupload. Kalau video butuh tangan untuk menunjukkan skala atau cara pakai, prompt membatasi hanya **satu tangan tanpa wajah**. Kalau tidak ingin tangan sama sekali, shot produk saja juga didukung.

Prompt ini sengaja panjang dan rinci. Google Flow tidak mempublikasikan batas karakter, dan detail tambahan justru menaikkan kontrol. Yang membuat hasil melenceng bukan panjangnya, tetapi instruksi yang berulang, saling bertentangan, atau terlalu banyak ide dalam satu beat.

---

## Yang Anda butuhkan

- 1 foto produk yang jelas.
- ChatGPT yang bisa generate image.
- Akun Google Flow.

Yang **tidak** perlu:

- Foto model.
- Foto dari banyak sudut.
- Storyboard.
- Software editing.

---

## Cara pakai

### 1. Siapkan satu foto produk

Cukup **satu** foto.

- Produk terlihat utuh.
- Satu varian saja.
- Tanpa harga, rating, badge, watermark, atau UI marketplace.
- Label terlihat jelas. Kalau tidak terbaca, AI akan membuatnya generik.
- Semakin bersih fotonya, semakin akurat hasilnya.

Jangan upload foto model. Folder ini memang untuk produk saja.

### 2. Upload foto + paste `PROMPT.md`

1. Buka chat baru di ChatGPT.
2. Upload **1 foto produk**.
3. Paste seluruh isi `PROMPT.md`.
4. Kirim.

ChatGPT langsung mengembalikan dua hal:

**A. Satu master prompt** di dalam code block — tinggal klik copy. Di dalamnya ada `CINEMATIC NOTES` per beat: camera, effect, transition.

**B. Tiga gambar** — tinggal download.

| Gambar | Fungsi |
|---|---|
| `flow-1-product.png` | Produk di background polos. Acuan bentuk, warna, material, dan label. |
| `flow-2-hero.png` | Master frame. Produk di environment, kondisi awal video. |
| `flow-3-lifestyle.png` | Dibuat dari `flow-2-hero.png`. Produk dipakai dengan satu tangan. Acuan skala. |

Urutan generate: **1 → 2 → 3**. Gambar 2 adalah master frame. Gambar 3 dibuat dari gambar 2, bukan dari foto produk asli. Ini yang menjaga produk, lighting, dan environment tidak berubah.

Tidak ada manifest, storyboard, tabel, atau setting Flow.

### 3. Generate di Flow

1. Upload 3 gambar di atas ke Flow Ingredients.
2. Paste master prompt.
3. Atur Flow sesuai selera Anda.
4. Generate 3–4 variasi.
5. Pilih yang produknya paling konsisten dan teksnya paling terbaca.

Jangan upload foto produk asli ke Flow. Bentuk dan label produk sudah dibawa oleh ketiga gambar ingredient.

---

## Yang dikunci di prompt

| Bagian | Isi |
|---|---|
| `PRODUCT LOCK` | Deskripsi konkret bentuk, warna, material, finish, logo, dan komponen. Satu unit produk. Label asli dipertahankan. |
| `HAND LOCK` | Tidak ada wajah, kepala, torso, atau orang kedua. Kalau ada tangan: satu tangan kanan dan sebagian lengan bawah, warna kulit, kuku, dan sleeve yang sama di setiap shot. |
| `INGREDIENT ROLES` | Gambar 2 adalah master frame. Gambar 3 harus sama persis dengan gambar 2. |
| `REFERENCE USE` | Gambar hanya referensi. Tidak boleh dianimasikan, di-pan, di-zoom, atau dipakai sebagai frame diam. |
| `STYLE` | Lighting konkret: soft diffused window light from upper left, 5200K. Lensa 50mm f/2.8. Material dan kulit tangan natural. |
| `ON-SCREEN GRAPHICS` | 3 overlay gaya sticker TikTok: outline tebal, offset shadow, swipe warna aksen dari palette produk. Pop-in sekali lalu statis. Tidak boleh menutup logo produk. |
| `TIMELINE` | Frame pertama sudah menampilkan produk. Closing ditahan 0.5–1.0 detik. |
| `CINEMATIC NOTES` | Camera, effect, transition per beat. Hanya gerakan sederhana dan hard cut. |
| `NEGATIVE` | Larangan wajah, orang, tangan ganda, produk ganda, produk melayang, kulit plastik, HDR, wide-angle distortion, dan efek visual berlebihan. |

`CINEMATIC NOTES` mengatur gerakan kamera, efek fotografis, dan transisi per beat. Isinya sederhana: static, slow push-in, atau gentle track; lighting, depth of field, dan color grade; lalu hard cut. Tidak ada motion graphics atau transisi rumit.

Sebelum mengirim gambar, ChatGPT menjalankan `FINAL CONSISTENCY CHECK`: produk, label, tangan, sleeve, lighting, skala, dan larangan wajah. Kalau ada yang gagal, gambar itu diregenerate dulu.

---

## Setelah video jadi

- Download 1080p.
- Upload ke TikTok dan Shopee.
- Taruh CTA di caption, bukan di video.
- Tambahkan disclosure affiliate/AI jika diperlukan.

---

## Kalau hasil kurang bagus

| Masalah | Yang dilakukan |
|---|---|
| Muncul wajah atau orang | Pastikan `no faces, no heads, no bodies, no people` tetap ada di prompt. Regenerate gambar yang melenceng. |
| Muncul dua tangan | Pastikan `one hand only, one right hand` tetap ada. Kurangi aksi jadi satu gerakan. |
| Tangan cacat | Ganti beat itu jadi produk saja tanpa tangan. Versi produk-only selalu aman. |
| Tangan menutup logo | Ganti aksi jadi memegang badan produk, bukan bagian depan. |
| Produk ganda atau melayang | Pastikan `one product unit only` dan `no floating product` tetap ada. Kurangi gerakan tangan. |
| Label produk berubah | Regenerate `flow-1-product.png`. Kurangi close-up ekstrem pada label. |
| Kulit tangan seperti plastik | Pertahankan `natural hand skin with visible pores, no beauty filter`. |
| Satu gambar melenceng | Regenerate gambar itu saja di chat yang sama. |
| Teks rusak | Kurangi jadi 2 overlay, atau pakai versi tanpa teks. |
| Produk berubah | Regenerate dengan `flow-1-product.png`, kurangi gerakan kamera. |
| Cut terasa aneh | Minta hard cuts, atau kurangi jumlah beat. |
| Musik muncul | Pastikan `no background music` tetap ada. |
| CTA/logo platform muncul | Hapus lewat video-to-video edit di Flow. |
| Warna aksen tabrakan dengan environment | Fallback otomatis merah-kuning. Aksen harus diambil dari palette produk dan sama di semua beat. |
| Angka di overlay mengada-ada | Angka harus bisa diverifikasi dari foto produk atau demo; kalau tidak, hapus angkanya. |

Jangan pindah ke CapCut. Perbaiki di Flow.

---

## Tips supaya sekali jadi

- Gunakan foto yang tajam dan terang.
- Jangan upload collage atau beberapa varian.
- Jangan upload screenshot marketplace ke Flow.
- Jangan upload gambar dengan teks tambahan seperti caption, harga, atau badge. Label produk sendiri boleh dan harus dipertahankan.
- Generate beberapa variasi. Jangan langsung puas dengan yang pertama.
- Mulai dari produk yang bentuknya sederhana dan matte.
- Kalau tangan sering cacat, pakai shot produk saja. Video produk-only tetap terlihat profesional.

---

## Kalau prompt terasa terlalu panjang

Prompt final sekitar 950–1200 kata. Itu normal untuk 6 beat dengan 3 gambar.

Kalau perlu memangkas:

1. Jangan potong `PRODUCT LOCK`, `HAND LOCK`, `REFERENCE USE`, atau `NEGATIVE`.
2. Potong dulu detail `CINEMATIC NOTES`.
3. Lalu ringkas `STYLE`.
4. Terakhir kurangi detail `TIMELINE`, tetapi jangan ubah timing dan overlay.

Jangan menghapus bagian hanya karena ingin lebih pendek. Panjang bukan masalah utama; instruksi yang berulang dan bertentangan adalah masalahnya.

---

## Batas realistis

| Jenis produk | Peluang berhasil | Catatan |
|---|---|---|
| Bentuk sederhana, matte, tanpa logo | Tinggi | Paling cocok untuk one-shot |
| Logo jelas, tekstur, tangan sederhana | Sedang | Perlu 2–4 variasi |
| Reflektif, transparan, apparel, makanan, skincare | Rendah–sedang | Perlu beberapa percobaan |
| Banyak varian atau logo kecil | Rendah | Pilih 1 varian, hindari close-up logo |
| Produk dengan label kecil dan teks padat | Rendah–sedang | Jaga shot tetap medium, jangan extreme close-up |

---

## Kenapa tanpa CTA dan musik?

Supaya **satu video bisa dipakai di dua platform**.

- CTA ditaruh di caption TikTok atau Shopee.
- Musik platform bisa ditambahkan dari aplikasi masing-masing kalau mau.
- Video tetap bersih dan netral.

---

## File

| File | Fungsi |
|---|---|
| `PROMPT.md` | Prompt yang di-paste ke ChatGPT. Ini yang Anda pakai. |
| `README.md` | Panduan ini. |
| `References/IMAGE-STORYBOARD-GENERATOR.MD` | Referensi lama: generator storyboard gambar. Tidak dipakai di alur One Shot. |
| `References/VIDEO-GENERATOR.MD` | Referensi lama: generator video. Tidak dipakai di alur One Shot. |

Struktur folder:

```text
Tanpa Model/
├── PROMPT.md
├── README.md
└── References/
    ├── IMAGE-STORYBOARD-GENERATOR.MD
    └── VIDEO-GENERATOR.MD
```
