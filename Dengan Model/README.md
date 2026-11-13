# Dengan Model — Iklan Video 10 Detik

Ubah **1 foto produk + 1 foto model** menjadi **satu video iklan 10 detik** langsung di Google Flow.

Tanpa CapCut. Tanpa edit manual.

Model yang Anda upload menjadi acuan identitas dan presentasi personal saat tampil. Produk tetap mengikuti foto produk. Untuk produk wearable, tampilkan produk akurat tanpa mengubah identitas model. Aturan lini Muslimah tetap berlaku: hijab selalu dipakai; pilih varian paling modest dari produk yang sama bila perlu. Gunakan shot produk-only bila styling dan akurasi produk berbenturan.

Folder ini adalah versi One Shot. File storyboard dan video lama ada di `References/`, tetapi bukan bagian dari alur ini. Yang masuk Flow hanya 3 gambar bersih tanpa teks tambahan.

Prompt ini sengaja panjang dan rinci. Batas prompt Google Flow tidak didokumentasikan di repo ini dan bisa berubah antar model atau paket Flow — cek langsung di sesi Flow Anda. Kalau prompt ditolak atau terpotong, pangkas detail `CINEMATIC NOTES` dulu, lalu `STYLE`, lalu detail `TIMELINE` tanpa mengubah timing dan overlay. Yang membuat hasil melenceng bukan panjangnya, tetapi instruksi yang berulang, saling bertentangan, atau terlalu banyak ide dalam satu beat.

---

## Yang Anda butuhkan

- Hak atau izin penggunaan komersial untuk foto/model yang dipakai. Pastikan persetujuan model mencakup iklan dan kanal publikasi.
- 1 foto produk yang jelas.
- 1 foto model yang jelas; model dipakai dalam shot hanya jika relevan dan aman. Shot produk-only tetap diizinkan.
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
| `flow-3-lifestyle.png` | Dibuat dari `flow-2-hero.png`. Acuan interaksi yang sesuai produk, atau komposisi produk-only jika interaksi tidak relevan/aman. |

Urutan generate: **1 → 2 → 3**. Gambar 2 adalah master frame. Gambar 3 dibuat dari gambar 2, bukan dari foto model asli. Ini yang menjaga wajah dan wardrobe tidak berubah.

Tidak ada manifest, storyboard, tabel, atau setting Flow.

### 3. Generate di Flow

1. Upload 3 gambar di atas ke Flow Ingredients.
2. Paste master prompt.
3. Atur Flow sesuai selera Anda.
4. Generate 3–4 variasi.
5. Pilih yang wajah modelnya paling konsisten dan produknya paling utuh.

Jangan upload foto model asli ke Flow. Identitas model sudah dibawa oleh `flow-2-hero.png` dan `flow-3-lifestyle.png`.

> ⚙️ **Catatan durasi:** spesifikasi prompt tetap 10 detik. Verifikasi dukungan durasi pada model/paket Flow Anda. Jangan membuang beat closing; jika perlu, retime keenam beat secara proporsional. Jika Flow tidak mendukungnya, mode tersebut belum memenuhi spesifikasi ini.

---

## Yang dikunci di prompt

| Bagian | Isi |
|---|---|
| `PRODUCT LOCK` | Deskripsi konkret bentuk, warna, material, finish, logo, dan komponen. Satu unit produk. Label asli dipertahankan. |
| `MODEL LOCK` | Identitas model mengikuti foto referensi; tidak menyimpulkan agama dari penampilan. |
| `WARDROBE LOCK` | Potongan produk wearable menjadi acuan: jangan tutupi bagian tangan/kaki yang seharusnya terlihat dengan stocking, celana, manset, atau lapisan tambahan. Untuk produk non-Muslimah, lepas hijab referensi bila menutupi leher/neckline/rambut yang perlu terlihat; rambut asli dibiarkan terurai. Aturan hijab berlaku untuk lini produk Muslimah saja. |
| `INGREDIENT ROLES` | Gambar 2 adalah master frame. Gambar 3 harus sama persis dengan gambar 2. |
| `REFERENCE USE` | Gambar hanya referensi. Tidak boleh dianimasikan, di-pan, di-zoom, atau dipakai sebagai frame diam. |
| `STYLE` | Lighting, lensa, dan depth of field dipilih agar sesuai produk, skala shot, serta lingkungan. |
| `ON-SCREEN GRAPHICS` | 0–3 overlay dan 0–2 aksen opsional. Tampilkan hanya informasi spesifik produk yang didukung bukti; hilangkan yang tidak relevan, tak terbaca, atau menutupi wajah/logo. Warna hanya metadata styling dalam kata biasa — tanpa kode hex atau sintaks CSS, dan tidak pernah dirender sebagai teks di layar. |
| `TIMELINE` | Frame pertama menampilkan produk; model muncul hanya jika relevan dan aman. Enam beat tetap 10 detik; closing ditahan 0.5–1.0 detik. |
| `CINEMATIC NOTES` | Camera, effect, transition per beat. Hanya gerakan sederhana dan hard cut. |
| `NEGATIVE` | Larangan produk ganda, produk melayang, kulit plastik, HDR, wide-angle distortion, dan efek visual berlebihan. |

`CINEMATIC NOTES` mengatur gerakan kamera, efek fotografis, dan transisi per beat. Isinya sederhana: static, slow push-in, atau gentle track; lighting, depth of field, dan color grade; lalu hard cut. Tidak ada motion graphics atau transisi rumit.

Sebelum mengirim gambar, ChatGPT menjalankan `FINAL CONSISTENCY CHECK`: produk, wajah, wardrobe, lighting, tangan, skala, dan larangan teks tambahan. Kalau ada yang gagal, gambar itu diregenerate dulu.

---

## Setelah video jadi

- Export final video at 1080×1920 (9:16) when supported by Flow.
- Upload ke TikTok dan Shopee.
- Taruh CTA di caption, bukan di video.
- Tambahkan disclosure affiliate/AI jika diperlukan.

---

## Kalau hasil kurang bagus

| Masalah | Yang dilakukan |
|---|---|
| Wajah model berubah | Jika model dipakai, regenerate dengan `flow-2-hero.png` sebagai Ingredient 2 dan buat `flow-3-lifestyle.png` dari gambar 2. Kurangi close-up. Product-only shot tetap valid.
| Wardrobe berubah | Regenerate `flow-3-lifestyle.png` dari `flow-2-hero.png`, bukan dari foto model asli. |
| Produk wearable berubah bentuk | Pastikan `WARDROBE LOCK` menyebut cut, panjang, dan fit yang terlihat. Jika tidak bisa ditampilkan akurat dengan presentasi model, gunakan shot produk terpisah.
| Pakaian tambahan menutupi produk | Tegaskan cut produk dan area kulit yang harus terlihat. Larang stocking/celana/legging di bawah midi dress dan manset/lengan tambahan pada bagian yang memang terbuka. |
| Hijab menutupi produk non-Muslimah | Lepas hijab bila menutupi leher, neckline, atau rambut yang diperlukan untuk menampilkan produk. Rambut mengikuti foto model dan dibiarkan terurai; jangan ubah identitas. Produk lini Muslimah tetap memakai hijab. |
| Aksesoris kepala muncul sendiri | Pastikan `no accessories that are not the product` tetap ada di prompt. |
| Warna aksen tabrakan dengan environment | Pilih ulang aksen dari palet produk; jika warnanya tidak jelas, pilih dua warna netral berkontras tinggi. Gunakan sama di semua beat. |
| Overlay tidak sesuai produk atau klaim tidak terbukti | Ganti dengan fitur/benefit spesifik yang didukung foto atau demo. Angka hanya boleh dipakai jika persisnya bisa diverifikasi; jika tidak, gunakan label nonnumerik. |
| Muncul orang lain atau hewan | Pastikan `no extra people, no background faces, no pets` tetap ada di prompt. |
| Produk ganda atau melayang | Pastikan `one product unit only` dan `no floating product` tetap ada. Kurangi gerakan tangan. |
| Tangan menutup logo | Ganti aksi jadi memegang badan produk, bukan bagian depan. |
| Overlay menutup wajah atau produk | Pindahkan ke ruang aman; jika tetap menghalangi, hapus overlay tersebut. Overlay opsional, bukan target jumlah.
| Kulit seperti plastik | Pertahankan `natural skin texture with visible pores, no beauty filter`. |
| Label produk berubah | Regenerate `flow-1-product.png`. Kurangi close-up ekstrem pada label. |
| Satu gambar melenceng | Regenerate gambar itu saja di chat yang sama. |
| Teks rusak atau tak relevan | Kurangi jumlah overlay sampai 0–3; pertahankan hanya teks terbaca dan didukung bukti. |
| Produk berubah | Regenerate dengan `flow-1-product.png`, kurangi gerakan kamera. |
| Tangan cacat | Ganti beat itu jadi produk saja tanpa tangan. |
| Cut terasa aneh | Minta hard cuts, atau kurangi jumlah beat. |
| Model seperti bicara | Pastikan `the model does not speak to camera, no lip-sync` tetap ada. |

Jangan pindah ke CapCut. Perbaiki di Flow.

---

## Tips supaya wajah model konsisten

- Untuk produk wearable, pakaian produk harus terlihat akurat; pertahankan identitas dan presentasi personal model. Jika tidak cocok, tampilkan produk terpisah atau gunakan framing aman.

- Gunakan foto model dengan wajah tajam dan terang.
- Hindari foto wajah tertutup rambut, masker, tangan, atau bayangan keras.
- Pilih wardrobe sederhana: satu warna, tanpa motif atau tulisan.
- Hindari aksesori yang berubah-ubah.
- Jangan upload foto model dari beberapa orang sekaligus.
- Di Flow, gunakan `flow-2-hero.png` sebagai acuan utama wajah.
- Jaga environment di `flow-2-hero.png` tetap sederhana dan tidak ramai. Background yang bersih membantu Flow menyatukan ingredient.
- Jika wajah menghadap kamera, gunakan sudut alami yang menjaga identitas terbaca; jangan memaksa sudut 3/4 bila referensi atau produk tidak cocok.
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

Prompt final harus sesingkat mungkin sambil mempertahankan kunci produk, model, keselamatan, timing, dan bukti. 950–1200 kata bukan kuota.

Kalau perlu memangkas:

1. Jangan potong `PRODUCT LOCK`, `MODEL LOCK`, `WARDROBE LOCK`, `REFERENCE USE`, atau `NEGATIVE`. Jumlah beat/durasi tetap 6 beat dan 10 detik; hapus pengulangan, bukan kunci format.
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
| `References/PROMPT.md` | Alur opsional: generate gambar storyboard dan prompt Google Flow siap salin dengan storyboard sebagai referensi. Input: foto produk + foto model. |
| `References/IMAGE-STORYBOARD-GENERATOR.MD` / `VIDEO-GENERATOR.MD` | Referensi legacy; tidak diperlukan untuk alur storyboard + prompt baru. |

Struktur folder:

```text
Dengan Model/
├── PROMPT.md
├── README.md
└── References/
    ├── IMAGE-STORYBOARD-GENERATOR.MD
    └── VIDEO-GENERATOR.MD
```
