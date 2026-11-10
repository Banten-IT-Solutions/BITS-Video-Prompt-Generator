# Dengan Model — Iklan Video 10 Detik

Ubah **1 foto produk + 1 foto model** menjadi **satu video iklan 10 detik** langsung di Google Flow.

Tanpa CapCut. Tanpa edit manual.

Model yang Anda upload dipakai sebagai acuan wajah, rambut, warna kulit, proporsi tubuh, dan wardrobe. Produk tetap mengikuti foto produk.

Folder ini adalah versi One Shot. File storyboard dan video lama ada di `References/`, tetapi bukan bagian dari alur ini. Yang masuk Flow hanya 3 gambar bersih tanpa teks tambahan.

Prompt ini sengaja panjang dan rinci. Google Flow tidak mempublikasikan batas karakter, dan detail tambahan justru menaikkan kontrol. Yang membuat hasil melenceng bukan panjangnya, tetapi instruksi yang berulang, saling bertentangan, atau terlalu banyak ide dalam satu beat.

---

## Yang Anda butuhkan

- 1 foto produk yang jelas.
- 1 foto model yang jelas.
- ChatGPT yang bisa generate image.
- Akun Google Flow.

Yang **tidak** perlu:

- Storyboard.
- Foto dari banyak sudut.
- Software editing.

---

## Cara pakai

### 1. Siapkan dua foto

**Foto produk:**

- Produk terlihat utuh.
- Satu varian saja.
- Tanpa harga, rating, badge, watermark, atau UI marketplace.
- Label terlihat jelas. Kalau tidak terbaca, AI akan membuatnya generik.
- Semakin bersih fotonya, semakin akurat hasilnya.

**Foto model:**

- Satu orang saja.
- Wajah terlihat jelas.
- Tubuh terlihat cukup untuk membaca proporsi.
- Pencahayaan wajar, tanpa filter berat.
- Pakaian sederhana lebih mudah dijaga konsisten.
- Hindari pakaian dengan tulisan, logo, atau motif ramai.

Kalau foto model berisi beberapa orang, AI akan memilih yang paling dominan. Lebih aman crop ke satu orang.

### 2. Upload dua foto + paste `PROMPT.md`

1. Buka chat baru di ChatGPT.
2. Upload **1 foto produk** terlebih dahulu, lalu **1 foto model**.
3. Paste seluruh isi `PROMPT.md`.
4. Kirim.

ChatGPT langsung mengembalikan dua hal:

**A. Satu master prompt** di dalam code block — tinggal klik copy. Di dalamnya ada `CINEMATIC NOTES` per beat: camera, effect, transition.

**B. Tiga gambar** — tinggal download.

| Gambar | Fungsi |
|---|---|
| `flow-1-product.png` | Produk di background polos. Acuan bentuk, warna, material, dan label. |
| `flow-2-hero.png` | Master frame. Model + produk di environment. Acuan wajah, wardrobe, komposisi, dan lighting. |
| `flow-3-lifestyle.png` | Dibuat dari `flow-2-hero.png`. Acuan interaksi, skala, dan real-world use. |

Urutan generate: **1 → 2 → 3**. Gambar 2 adalah master frame. Gambar 3 dibuat dari gambar 2, bukan dari foto model asli. Ini yang menjaga wajah dan wardrobe tidak berubah.

Tidak ada manifest, storyboard, tabel, atau setting Flow.

### 3. Generate di Flow

1. Upload 3 gambar di atas ke Flow Ingredients.
2. Paste master prompt.
3. Atur Flow sesuai selera Anda.
4. Generate 3–4 variasi.
5. Pilih yang wajah modelnya paling konsisten dan produknya paling utuh.

Jangan upload foto model asli ke Flow. Identitas model sudah dibawa oleh `flow-2-hero.png` dan `flow-3-lifestyle.png`.

---

## Yang dikunci di prompt

| Bagian | Isi |
|---|---|
| `PRODUCT LOCK` | Deskripsi konkret bentuk, warna, material, finish, logo, dan komponen. Satu unit produk. Label asli dipertahankan. |
| `MODEL LOCK` | Deskripsi konkret wajah, warna kulit, mata, rambut, dan proporsi. Identitas dipertahankan; pakaian ditangani `WARDROBE LOCK`. Tidak ada orang lain atau hewan. |
| `WARDROBE LOCK` | Produk yang dipakai (apparel) menjadi wardrobe utama: panjang lengan, hem, dan neckline persis produk. Bagian pendek menampilkan kulit. Rambut dan hijab mengikuti kategori produk. |
| `INGREDIENT ROLES` | Gambar 2 adalah master frame. Gambar 3 harus sama persis dengan gambar 2. |
| `REFERENCE USE` | Gambar hanya referensi. Tidak boleh dianimasikan, di-pan, di-zoom, atau dipakai sebagai frame diam. |
| `STYLE` | Lighting konkret: soft diffused window light from upper left, 5200K. Lensa 50mm f/2.8. Tekstur kulit natural. |
| `ON-SCREEN GRAPHICS` | 3 overlay. Tidak boleh menutup wajah, mata, atau logo. |
| `TIMELINE` | Frame pertama sudah menampilkan produk + model. Closing ditahan 0.5–1.0 detik. |
| `CINEMATIC NOTES` | Camera, effect, transition per beat. Hanya gerakan sederhana dan hard cut. |
| `NEGATIVE` | Larangan produk ganda, produk melayang, kulit plastik, HDR, wide-angle distortion, dan efek visual berlebihan. |

`CINEMATIC NOTES` mengatur gerakan kamera, efek fotografis, dan transisi per beat. Isinya sederhana: static, slow push-in, atau gentle track; lighting, depth of field, dan color grade; lalu hard cut. Tidak ada motion graphics atau transisi rumit.

Sebelum mengirim gambar, ChatGPT menjalankan `FINAL CONSISTENCY CHECK`: produk, wajah, wardrobe, lighting, tangan, skala, dan larangan teks tambahan. Kalau ada yang gagal, gambar itu diregenerate dulu.

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
| Wajah model berubah | Regenerate dengan `flow-2-hero.png` sebagai Ingredient 2. Pastikan `flow-3-lifestyle.png` dibuat dari gambar 2. Kurangi close-up wajah. |
| Wardrobe berubah | Regenerate `flow-3-lifestyle.png` dari `flow-2-hero.png`, bukan dari foto model asli. |
| Produk berubah jadi panjang | Pastikan `WARDROBE LOCK` menyebut panjang lengan dan hem persis seperti produk, dan `NEGATIVE` melarang menambah lapisan atau panjang. |
| Hijab tetap dipakai padahal produk pendek/terbuka | Aturan styling: produk terbuka → rambut terurai tanpa hijab; produk modest (gamis, abaya) → hijab dipertahankan. |
| Aksesoris kepala muncul sendiri | Pastikan `no accessories that are not part of the product` tetap ada di prompt. |
| Muncul orang lain atau hewan | Pastikan `no extra people, no background faces, no pets` tetap ada di prompt. |
| Produk ganda atau melayang | Pastikan `one product unit only` dan `no floating product` tetap ada. Kurangi gerakan tangan. |
| Tangan menutup logo | Ganti aksi jadi memegang badan produk, bukan bagian depan. |
| Overlay menutup wajah | Geser ke top-left dan lower-left, atau kurangi jadi 2 overlay. |
| Kulit seperti plastik | Pertahankan `natural skin texture with visible pores, no beauty filter`. |
| Label produk berubah | Regenerate `flow-1-product.png`. Kurangi close-up ekstrem pada label. |
| Satu gambar melenceng | Regenerate gambar itu saja di chat yang sama. |
| Teks rusak | Kurangi jadi 2 overlay, atau pakai versi tanpa teks. |
| Produk berubah | Regenerate dengan `flow-1-product.png`, kurangi gerakan kamera. |
| Tangan cacat | Ganti beat itu jadi produk saja tanpa tangan. |
| Cut terasa aneh | Minta hard cuts, atau kurangi jumlah beat. |
| Model seperti bicara | Pastikan `the model does not speak to camera, no lip-sync` tetap ada. |

Jangan pindah ke CapCut. Perbaiki di Flow.

---

## Tips supaya wajah model konsisten

- Untuk produk pakaian, pakaian di foto model tidak masalah. Produk selalu menjadi wardrobe utama, bukan pakaian referensi.

- Gunakan foto model dengan wajah tajam dan terang.
- Hindari foto wajah tertutup rambut, masker, tangan, atau bayangan keras.
- Pilih wardrobe sederhana: satu warna, tanpa motif atau tulisan.
- Hindari aksesori yang berubah-ubah.
- Jangan upload foto model dari beberapa orang sekaligus.
- Di Flow, gunakan `flow-2-hero.png` sebagai acuan utama wajah.
- Jaga environment di `flow-2-hero.png` tetap sederhana dan tidak ramai. Background yang bersih membantu Flow menyatukan ingredient.
- Pertahankan sudut wajah 3/4 dengan kedua mata terlihat.
- Kalau wajah masih berubah, kurangi durasi close-up dan perbanyak medium shot.

---

## Tips produk

- Jangan upload screenshot marketplace ke Flow.
- Jangan upload gambar dengan teks tambahan seperti caption, harga, atau badge. Label produk sendiri boleh dan harus dipertahankan.
- Produk harus sama di ketiga gambar.
- Satu unit produk saja. Jangan sampai ada produk ganda atau produk melayang.
- Pertahankan label asli. Jangan biarkan AI menambah sertifikasi atau badge.
- Kalau produk punya dua state (terlipat/terbuka), prompt sudah memakai hard cut, bukan animasi mekanisme.

---

## Kalau prompt terasa terlalu panjang

Prompt final sekitar 950–1150 kata. Itu normal untuk 6 beat dengan 3 gambar.

Kalau perlu memangkas:

1. Jangan potong `PRODUCT LOCK`, `MODEL LOCK`, `WARDROBE LOCK`, `REFERENCE USE`, atau `NEGATIVE`.
2. Potong dulu detail `CINEMATIC NOTES`.
3. Lalu ringkas `STYLE`.
4. Terakhir kurangi detail `TIMELINE`, tetapi jangan ubah timing dan overlay.

Jangan menghapus bagian hanya karena ingin lebih pendek. Panjang bukan masalah utama; instruksi yang berulang dan bertentangan adalah masalahnya.

---

## Batas realistis

| Jenis produk + model | Peluang berhasil | Catatan |
|---|---|---|
| Produk sederhana, model dewasa, medium shot | Tinggi | Paling stabil |
| Produk detail, wajah sering close-up | Sedang | Wajah lebih rawan berubah |
| Produk reflektif/transparan, model banyak gerak | Rendah–sedang | Perlu beberapa percobaan |
| Banyak orang dalam foto model | Rendah | Crop ke satu orang dulu |
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
Dengan Model/
├── PROMPT.md
├── README.md
└── References/
    ├── IMAGE-STORYBOARD-GENERATOR.MD
    └── VIDEO-GENERATOR.MD
```
