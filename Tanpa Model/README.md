# Tanpa Model — Iklan Video 10 Detik

Ubah **satu foto produk** menjadi **satu video iklan 10 detik** langsung di Google Flow.

Tanpa model. Tanpa wajah. Tanpa CapCut. Tanpa edit manual.

Versi ini hanya memakai **1 foto produk**. Tidak ada foto model yang diupload. Kalau video butuh tangan untuk menunjukkan skala atau cara pakai, prompt membatasi hanya **satu tangan tanpa wajah**. Kalau tidak ingin tangan sama sekali, shot produk saja juga didukung.

Prompt ini sengaja panjang dan rinci. Batas prompt Google Flow tidak didokumentasikan di repo ini dan bisa berubah antar model atau paket Flow — cek langsung di sesi Flow Anda. Kalau prompt ditolak atau terpotong, pangkas detail `CINEMATIC NOTES` dulu, lalu `STYLE`, lalu detail `TIMELINE` tanpa mengubah timing dan overlay. Yang membuat hasil melenceng bukan panjangnya, tetapi instruksi yang berulang, saling bertentangan, atau terlalu banyak ide dalam satu beat.

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

**B. Tiga gambar** — tinggal download; frame lifestyle dapat tanpa tangan jika interaksi tidak relevan.

| Gambar | Fungsi |
|---|---|
| `flow-1-product.png` | Produk di background polos. Acuan bentuk, warna, material, dan label. |
| `flow-2-hero.png` | Master frame. Produk di environment, kondisi awal video. |
| `flow-3-lifestyle.png` | Dibuat dari `flow-2-hero.png`. Menunjukkan penggunaan/skalanya; tangan opsional, produk-only juga valid. |

Urutan generate: **1 → 2 → 3**. Gambar 2 adalah master frame. Gambar 3 dibuat dari gambar 2, bukan dari foto produk asli. Ini yang menjaga produk, lighting, dan environment tidak berubah.

Tidak ada manifest, storyboard, tabel, atau setting Flow.

### 3. Generate di Flow

1. Upload 3 gambar di atas ke Flow Ingredients.
2. Paste master prompt.
3. Atur Flow sesuai selera Anda.
4. Generate 3–4 variasi.
5. Pilih yang produknya paling konsisten dan teksnya paling terbaca.

Jangan upload foto produk asli ke Flow. Bentuk dan label produk sudah dibawa oleh ketiga gambar ingredient.

> ⚙️ **Catatan durasi:** spesifikasi prompt tetap 10 detik. Verifikasi dukungan durasi pada model/paket Flow Anda. Jangan membuang beat closing; jika perlu, retime keenam beat secara proporsional. Jika Flow tidak mendukungnya, mode tersebut belum memenuhi spesifikasi ini.

---

## Yang dikunci di prompt

| Bagian | Isi |
|---|---|
| `PRODUCT LOCK` | Deskripsi konkret bentuk, warna, material, finish, logo, dan komponen. Satu unit produk. Label asli dipertahankan. |
| `HAND LOCK` | Tidak ada wajah, kepala, torso, atau orang kedua. Kalau ada tangan: satu tangan kanan dan sebagian lengan bawah, warna kulit, kuku, dan sleeve yang sama di setiap shot. |
| `INGREDIENT ROLES` | Gambar 2 adalah master frame. Gambar 3 harus sama persis dengan gambar 2. |
| `REFERENCE USE` | Gambar hanya referensi. Tidak boleh dianimasikan, di-pan, di-zoom, atau dipakai sebagai frame diam. |
| `STYLE` | Lighting, lensa, dan depth of field dipilih agar sesuai produk, skala shot, serta lingkungan. |
| `ON-SCREEN GRAPHICS` | 0–3 overlay dan 0–2 aksen opsional. Tampilkan hanya informasi spesifik produk yang didukung bukti; hilangkan yang tidak relevan, tak terbaca, atau menutupi logo. Warna hanya metadata styling dalam kata biasa — tanpa kode hex atau sintaks CSS, dan tidak pernah dirender sebagai teks di layar. |
| `TIMELINE` | Frame pertama sudah menampilkan produk. Closing ditahan 0.5–1.0 detik. |
| `CINEMATIC NOTES` | Camera, effect, transition per beat. Hanya gerakan sederhana dan hard cut. |
| `NEGATIVE` | Larangan wajah, orang, tangan ganda, produk ganda, produk melayang, kulit plastik, HDR, wide-angle distortion, dan efek visual berlebihan. |

`CINEMATIC NOTES` mengatur gerakan kamera, efek fotografis, dan transisi per beat. Isinya sederhana: static, slow push-in, atau gentle track; lighting, depth of field, dan color grade; lalu hard cut. Tidak ada motion graphics atau transisi rumit.

Sebelum mengirim gambar, ChatGPT menjalankan `FINAL CONSISTENCY CHECK`: produk, label, tangan, sleeve, lighting, skala, dan larangan wajah. Kalau ada yang gagal, gambar itu diregenerate dulu.

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
| Muncul wajah atau orang | Pastikan larangan wajah, kepala, badan, dan orang tetap ada; satu tangan kanan opsional bila berguna. Regenerate gambar yang melenceng.
| Muncul dua tangan | Pastikan `one hand only, one right hand` tetap ada. Kurangi aksi jadi satu gerakan. |
| Tangan cacat | Ganti beat itu jadi produk saja tanpa tangan. Versi produk-only selalu aman. |
| Tangan menutup logo | Ganti aksi jadi memegang badan produk, bukan bagian depan. |
| Produk ganda atau melayang | Pastikan `one product unit only` dan `no floating product` tetap ada. Kurangi gerakan tangan. |
| Label produk berubah | Regenerate `flow-1-product.png`. Kurangi close-up ekstrem pada label. |
| Kulit tangan seperti plastik | Pertahankan `natural hand skin with visible pores, no beauty filter`. |
| Satu gambar melenceng | Regenerate gambar itu saja di chat yang sama. |
| Teks rusak atau tak relevan | Kurangi jumlah overlay sampai 0–3; pertahankan hanya teks terbaca dan didukung bukti. |
| Produk berubah | Regenerate dengan `flow-1-product.png`, kurangi gerakan kamera. |
| Cut terasa aneh | Minta hard cuts, atau kurangi jumlah beat. |
| Musik muncul | Pastikan `no background music` tetap ada. |
| CTA/logo platform muncul | Hapus lewat video-to-video edit di Flow. |
| Warna aksen tabrakan dengan environment | Pilih ulang aksen dari palet produk; jika warnanya tidak jelas, pilih dua warna netral berkontras tinggi. Gunakan sama di semua beat. |
| Overlay tidak sesuai produk atau klaim tidak terbukti | Ganti dengan fitur/benefit spesifik yang didukung foto atau demo. Angka hanya boleh dipakai jika persisnya bisa diverifikasi; jika tidak, gunakan label nonnumerik. |

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

Prompt final harus sesingkat mungkin sambil mempertahankan kunci produk, keselamatan, timing, dan bukti. 950–1200 kata bukan kuota.

Kalau perlu memangkas:

1. Jangan potong `PRODUCT LOCK`, `HAND LOCK`, `REFERENCE USE`, atau `NEGATIVE`. Jumlah beat/durasi tetap 6 beat dan 10 detik; hapus pengulangan, bukan kunci format.
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
| `References/PROMPT.md` | Alur opsional: generate gambar storyboard dan prompt Google Flow siap salin dengan storyboard sebagai referensi. Input: satu foto produk. |
| `References/IMAGE-STORYBOARD-GENERATOR.MD` / `VIDEO-GENERATOR.MD` | Referensi pendukung storyboard dan arahan video. Untuk produksi gunakan `References/PROMPT.md`. |

Struktur folder:

```text
Tanpa Model/
├── PROMPT.md
├── README.md
└── References/
    ├── IMAGE-STORYBOARD-GENERATOR.MD
    └── VIDEO-GENERATOR.MD
```
