# Standar Penulisan Pattern Analysis — Cara Menulis Pattern yang Tajam

## Prinsip Utama

⚠️ **FILE INI WAJIB DIBACA setiap kali Falco menulis pattern analysis (Step 4).**

Pattern analysis adalah **inti pekerjaan Falco** — di sinilah angka berubah menjadi insight. Pattern yang ditulis dengan tajam bisa langsung memandu keputusan. Pattern yang ditulis generik hanya menambah panjang laporan tanpa nilai.

---

## ⚠️⚠️ Aturan Struktural: Pattern Dibaca PER PENGELOMPOKAN

Pattern analysis dibaca **terpisah per setiap pengelompokan ranking**, bukan global. Dari Step 3 ada 6 pengelompokan default:

1. Top Content by Views
2. Top Content by Shares
3. Top Content by Retention Rate (1s)
4. Worst Content by Views
5. Worst Content by Shares
6. Worst Content by Retention Rate (1s)

Setiap pengelompokan punya set pattern-nya sendiri yang dibaca dari berbagai aspek konten.

### ⚠️ Quality Gate Keras (Minimum Wajib)

| Item | Minimum |
|------|---------|
| Poin pattern per pengelompokan | **8-10 poin** (boleh lebih) |
| Total pattern (6 pengelompokan) | **48-60 poin** |

Ini minimum wajib, bukan target. Kalau data belum cukup untuk 8-10 poin per pengelompokan, Falco TIDAK menurunkan standar. Falco flag kekurangan data dan tawarkan pengayaan konteks ke user.

### Aspek Konten yang Dibaca

Tiap poin = satu aspek konten. Gunakan yang relevan, gali yang lain dari data: hook, talent, durasi, platform, jumlah slide, heuristic bias (psikologis), konsep konten, topik konten, rasio share vs likes, penggunaan sound, content flow, pola skrip/copywriting, struktur storytelling, CTA, caption, visual style, timing, dan aspek lain yang muncul dari data.

### Contoh Penulisan Pattern per Pengelompokan

```
**Pattern: Top Content by Views**

- 2 dari 3 Top Content by Views dari segi hook menggunakan hook headline 2 baris di atas talent + hook suara orang teriak
- 3 dari 3 Top Content by Views dari segi talent itu laki-laki
- 3 dari 3 Top Content by Views dari segi durasi itu di atas 60 detik
- 2 dari 3 Top Content by Views dari segi heuristic bias mengandung pattern interrupt di awal + cognitive dissonance lewat narasi
- 2 dari 3 Top Content by Views dari segi konsep konten adalah interview
- 1 dari 3 Top Content by Views dari segi sound tidak menggunakan sound
- [lanjut sampai minimal 8-10 poin dari aspek berbeda]
```

Ulangi untuk keenam pengelompokan. Untuk report mendalam, tiap poin diperkaya dengan mekanisme "kenapa" dan label keyakinan (lihat struktur 4 elemen di bawah).

---

## Struktur Penulisan Pattern (Per Faktor)

Setiap faktor yang dianalisis harus mengandung 4 elemen:

### 1. Observasi + Frekuensi (APA yang terlihat)
Gunakan pattern language standar: **"X dari Y [top/worst] content punya [kesamaan Z]"**

Frekuensi WAJIB ada — tanpa frekuensi, observasi tidak bisa dinilai kekuatannya.

### 2. Data Pendukung (BUKTI)
Sebutkan konten spesifik yang mendukung observasi. Bukan claim tanpa referensi.

### 3. Mekanisme/Reasoning (KENAPA)
Jelaskan kenapa pola ini terjadi — mekanisme algoritmik, psikologis, atau praktis. Kalau mekanisme belum jelas, label sebagai hipotesis.

### 4. Label Keyakinan (Seberapa YAKIN)
- **RELASIONAL (mekanisme jelas)** — ada hubungan kausal yang masuk akal
- **NON-RELASIONAL (perlu validasi)** — korelasi tanpa mekanisme yang jelas
- **HIPOTESIS (data belum cukup)** — baru 1-2 data points

---

## Contoh Penulisan Pattern yang BENAR vs SALAH

### Faktor Format

❌ SALAH:
```
Reels perform lebih baik dari Carousel.
```

✅ BENAR:
```
*Faktor Format:* 3 dari 5 top content by views adalah Reels (#7, #12, #19), 2 sisanya Carousel (#18, #22). Untuk top by ER, distribusinya terbalik: 3 dari 5 adalah Carousel, 2 Reels.

Pattern: Reels mendominasi reach/views, Carousel mendominasi engagement rate. Ini konsisten dengan data 2 bulan sebelumnya.

Mekanisme: Reels didistribusikan lebih luas oleh algoritma IG (reach ke non-followers), sementara Carousel memicu save dan swipe (engagement lebih dalam dari audience yang sudah follow). [RELASIONAL — mekanisme algoritmik jelas]

Implikasi: Kedua format punya peran berbeda — Reels untuk acquisition, Carousel untuk deepening. Bukan "Reels lebih baik dari Carousel" tapi "fungsinya berbeda."
```

### Faktor Hook

❌ SALAH:
```
Hook yang kuat menghasilkan views tinggi.
```

✅ BENAR:
```
*Faktor Hook:* 4 dari 5 top content by views punya hook yang memicu emotional response di 3 detik pertama:
- #7: "Kamu cuci muka pakai air panas? Stop." → threat/ancaman
- #12: Close-up Talent A langsung bicara ke kamera → personal connection
- #19: "3 bahan ini ada di produk kamu — dan harusnya nggak" → fear/curiosity
- #22: Before-after di slide pertama → visual surprise/kontras

1 dari 5 top content (#18 Carousel) tidak punya hook video tapi slide pertama punya headline bold yang memicu curiosity gap.

Pattern: Hook berbasis emotional trigger (threat, fear, curiosity, personal connection) konsisten di top content. Hook informatif murni ("Ini cara pakai...") tidak muncul di top 5.

Mekanisme: Emotional hook memicu stop-scroll response lebih kuat dari rational hook — otak memproses ancaman dan curiosity lebih cepat dari informasi. [RELASIONAL — mekanisme psikologis jelas]

Catatan: 3 dari 3 worst content (#5, #9, #14) punya hook yang informatif/deskriptif tanpa emotional trigger — memperkuat pattern bahwa hook emosional > hook informatif untuk akun ini.
```

### Faktor Timing

❌ SALAH:
```
Posting pagi hari lebih baik.
```

✅ BENAR:
```
*Faktor Timing:* 2 dari 5 top content di-posting antara jam 7-8 AM hari kerja (#7 Selasa 7:15, #12 Kamis 7:30). 3 sisanya di-posting siang/sore (12-17 PM).

Pattern: Belum bisa di-conclude. Dengan 2 dari 5 di pagi dan 3 di siang/sore, distribusinya tidak cukup kuat untuk menyatakan timing pagi lebih baik. [NON-RELASIONAL — baru korelasi lemah, perlu data lebih banyak]

Rekomendasi: Test lebih systematic di periode berikutnya — 50% konten di-posting pagi, 50% siang. Track views per time slot.
```

---

## Pattern di Top Content vs Worst Content

Falco harus analisis pattern di KEDUA sisi — bukan hanya top tapi juga worst. Sering kali, pattern di worst content sama informatifnya (atau bahkan lebih informatif) dengan pattern di top content.

### Cara Analisis Dual-Side:
1. Identifikasi faktor yang KONSISTEN di top → ini "resep sukses"
2. Identifikasi faktor yang KONSISTEN di worst → ini "resep gagal"
3. Bandingkan: apakah faktor top = kebalikan dari faktor worst? (kalau iya, pattern sangat kuat)
4. Cari faktor yang muncul di top DAN worst → faktor ini mungkin tidak berpengaruh

### Contoh:
```
Cross-analysis Top vs Worst:

| Faktor | Top 3 | Worst 3 | Insight |
|--------|-------|---------|---------|
| Hook | 3/3 emotional trigger | 3/3 informatif/deskriptif | Hook tipe = differentiator kuat |
| Durasi | 2/3 < 30 detik, 1/3 = 45 detik | 2/3 > 60 detik, 1/3 = 50 detik | Durasi < 50 detik perform lebih baik |
| Talent | 2/3 Talent A | 2/3 tanpa talent | Talent A punya resonance kuat |
| Format | 2/3 Reels, 1/3 Carousel | 2/3 Single Image, 1/3 Reels | Single Image konsisten underperform |
| Pillar | 3/3 edukasi | 2/3 promosi, 1/3 edukasi (generic) | Promosi heavy = worst performer |

Pattern terkuat: Hook emotional + durasi < 50 detik = formula top content. Hook informatif + durasi > 60 detik = formula worst content.
```

---

## Cross-Pattern (Kombinasi Faktor)

Setelah analisis per faktor, Falco WAJIB mencari cross-pattern — kombinasi 2+ faktor yang secara bersamaan selalu muncul di top atau worst content.

### Format penulisan:
```
Cross-Pattern Top:
"[Faktor A] + [Faktor B] + [Faktor C]"
→ Muncul di X dari Y top content [periode ini]
→ Muncul di X dari Y top content [periode sebelumnya, jika ada]
→ Tingkat keyakinan: [TINGGI/SEDANG/RENDAH]
→ Implikasi: [apa artinya untuk strategi konten]
```

---

## Absence Pattern (Apa yang Tidak Ada)

Falco WAJIB juga mencari apa yang TIDAK ADA — faktor yang seharusnya ada tapi tidak muncul. Ini sering jadi peluang terbesar.

### Cara menulis:
```
Absence yang teridentifikasi:
- Dalam 3 bulan terakhir, belum ada konten yang menggunakan [format/approach X]. Padahal di akun kompetitor, [format X] perform [data kalau ada].
- Belum ada test [variabel tertentu] — ini blind spot yang bisa di-explore.
- Audiens sering bertanya tentang [topik Y] di komentar, tapi belum ada konten yang menjawab.
```

---

## Red Flags Pattern Analysis yang Lemah

- ❌ Pattern dibaca global, tidak per pengelompokan — harusnya 6 pengelompokan terpisah
- ❌ Poin pattern di bawah minimum — kurang dari 8-10 per pengelompokan / 48-60 total
- ❌ Data belum cukup tapi standar diturunkan — harusnya flag + tawarkan pengayaan konteks
- ❌ Pattern tanpa frekuensi — "Reels perform lebih baik" tanpa "X dari Y"
- ❌ Pattern tanpa data pendukung — claim tanpa menyebut konten mana yang mendukung
- ❌ Pattern tanpa mekanisme — "durasi pendek lebih baik" tanpa menjelaskan kenapa (untuk report mendalam)
- ❌ Pattern hanya dari top — tidak analisis worst content
- ❌ Pattern yang terlalu luas — "konten bagus perform bagus" (ini bukan pattern, ini tautologi)
- ❌ Tidak ada label keyakinan — semua di-treat sama padahal ada yang baru hipotesis
- ❌ Tidak ada cross-pattern — hanya analisis faktor per faktor tanpa mencari kombinasi
- ❌ Tidak ada absence — hanya melihat apa yang ada, tidak melihat apa yang tidak ada
