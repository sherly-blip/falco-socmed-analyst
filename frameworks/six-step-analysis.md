# 6-Step Analysis Framework — Kerangka Non-Negotiable Falco

## Prinsip Utama

⚠️ **FILE INI WAJIB DIBACA SETIAP KALI FALCO MELAKUKAN ANALISIS APAPUN.**

Ini adalah kerangka analisis baku Falco. Urutan ini **TIDAK BOLEH DIUBAH** dan **TIDAK BOLEH DI-SKIP**. Setiap step harus dijalankan secara berurutan. Setiap step harus nyambung ke step sebelumnya dan sesudahnya.

**Kenapa urutan ini penting?** Karena tanpa urutan yang runut:
- Loncat dari data ke kesimpulan → kesimpulan tidak grounded
- Skip pattern analysis → saran tidak berbasis pola, hanya tebakan
- Skip detail → ranking tidak punya konteks
- Skip overview → analisis kehilangan gambaran besar

## ⚠️ Prinsip Universalitas: Framework Ini Berlaku untuk SEMUA Konteks

Framework 6-step ini **TIDAK terbatas pada konten organik saja.** Kerangka dan cara berpikirnya bersifat universal — bisa diterapkan ke konteks apapun dalam social media dan digital marketing, selama **variabel dan faktor yang dianalisis disesuaikan** dengan konteksnya.

| Konteks | Unit Analisis | Contoh Faktor Spesifik |
|---------|--------------|----------------------|
| **Konten Organik** | Per konten | Format, durasi, hook, topik, talent, visual, timing, CTA |
| **KOL/Endorsement** | Per KOL | Tier (nano-mega), domisili, tipe konten, karakter audiens, avg performa, relevansi brand |
| **Live Shopping** | Per sesi live | Durasi, GMV, viewers, alur live, host/talent, offering, waktu, conversion funnel |
| **Affiliate** | Per affiliator | Tipe affiliator, jenis konten, gaya komunikasi, hasil penjualan, produk laku |
| **Ads** | Per creative/ad set | CTR, cost per result, conversion rate, ROAS, creative type, audience, placement |

**Alur tetap sama untuk semua konteks:**
1. Overview — gambaran besar performa keseluruhan unit yang dianalisis
2. Detail — breakdown per unit (per konten / per KOL / per sesi / per affiliator / per creative)
3. Ranking — top & worst per metrik yang relevan (10% proporsi, minimal 3 metrik)
4. Pattern — cari pola per faktor yang relevan dengan konteksnya
5. Kesimpulan — tarik benang merah dari pattern
6. Saran — rekomendasi berbasis data, spesifik untuk konteks tersebut

**Yang berubah hanya konteks dan variabelnya. Kerangka berpikirnya TETAP.**

---

## Step 1: OVERVIEW (Gambaran Besar)

### Tujuan
Lihat performa secara keseluruhan dulu sebelum masuk ke detail. Ini memberikan "peta" sebelum zoom in.

### Yang harus ada:
- **Total metrics agregat:** total views, total reach, total engagement, average ER, followers growth, dll (sesuai konteks)
- **Perbandingan dengan periode sebelumnya:** WoW (week-over-week), MoM (month-over-month), atau benchmark yang relevan
- **Tren singkat:** apakah secara umum naik, turun, atau stagnan? Sejak kapan?
- **Anomali yang langsung terlihat di level overview:** ada lonjakan/penurunan drastis? Ada outlier?
- **Jumlah konten/item:** berapa total konten/campaign/sesi yang dianalisis dalam periode ini?
- **⚠️ Distribusi Pareto:** berapa persen konten menyumbang berapa persen total views/engagement — apakah performa concentrated atau terdistribusi? (→ Standar 6 di `standards/standar-analisis-mendalam.md`)
- **⚠️ Anomali struktural:** pattern-pattern di level overview yang langsung terlihat — contoh: "views naik tapi comments turun" atau "growth naik tapi ER juga naik (biasanya berlawanan)" (→ Standar 6)

### Contoh output Overview yang benar:
```
Periode Maret 2025, akun IG @brandX memproduksi 24 konten (12 Reels, 8 Carousel, 4 Single Image).

Total views: 892K (naik 23% dari Februari yang 725K)
Average views per konten: 37.2K (naik dari 30.2K di Februari)
Total engagement: 45.6K (naik 15% dari Februari)
Average ER: 3.8% (turun dari 4.1% di Februari — reach naik lebih cepat dari engagement)
Followers growth: +2.340 (naik 18% dari +1.980 di Februari)

Highlight: Views naik signifikan (+23%) tapi ER turun (-7%). Ini menunjukkan konten menjangkau lebih banyak orang, tapi proporsi yang engage lebih kecil — kemungkinan reach bertambah dari audience baru yang belum familiar dengan brand.

Anomali: 1 konten Reels (#7) mendapat 189K views, jauh di atas rata-rata 37.2K — ini outlier yang perlu dianalisis lebih dalam.
```

### ❌ Overview yang SALAH:
- "Performa bulan ini cukup baik" — TANPA angka dan benchmark
- Langsung masuk ke detail per konten tanpa overview dulu

---

## Step 2: DETAIL (Breakdown Mendalam)

### Tujuan
Pecah data per konten/per item/per aktivitas dengan deskripsi yang lengkap dan presisi.

### Yang harus ada per konten/item:
- **Identitas konten:** judul/topik, format, durasi (kalau video), content pillar, tanggal posting
- **Metrics lengkap:** views, reach, impressions, likes, comments, shares, saves, ER, completion rate (video), dll
- **Deskripsi konten yang presisi** — baca `standards/standar-deskripsi-data.md` untuk detail:
  - Format & konsep (Reels/Carousel/dll + format naratif)
  - Premis (inti ide konten — spesifik)
  - Hook (3 detik pertama + mekanisme psikologis)
  - Talent/karakter (siapa, karakter seperti apa)
  - Visual style (raw/polished, sudut kamera, setting)
  - CTA (jenis + placement)
- **Kontekstualisasi:** setiap angka di-frame — di atas/bawah rata-rata periode ini, naik/turun dari item sejenis di periode sebelumnya

### Contoh deskripsi per konten yang benar:
```
Konten #7: "5 Kesalahan Masak yang Kamu Lakukan Setiap Hari"
- Format: Reels 28 detik
- Content Pillar: Edukasi
- Tanggal: 12 Maret 2025
- Talent: Talent A (bicara langsung ke kamera, tone casual-authority)
- Hook: Pertanyaan langsung di 3 detik pertama — "Kamu masih pakai api besar terus? Pantesan gosong." (mekanisme: threat/ancaman + identifikasi langsung)
- Visual: Clean, studio lighting, text overlay per poin, transisi cut cepat antar poin
- CTA: "Save buat reminder" di frame terakhir

Metrics:
- Views: 189K (5x rata-rata bulan ini 37.2K — outlier signifikan)
- Reach: 156K
- Likes: 8.2K | Comments: 1.4K | Shares: 3.1K | Saves: 5.7K
- ER: 9.8% (2.6x rata-rata bulan ini 3.8%)
- Completion rate: 78% (di atas rata-rata 52% untuk Reels akun ini)

Konteks: Ini konten dengan views tertinggi bulan ini — 5x rata-rata. Share rate (1.6%) dan save rate (3%) jauh di atas rata-rata akun (0.8% share, 1.2% save), menunjukkan konten ini dianggap valuable oleh audience.
```

### ❌ Detail yang SALAH:
- "Konten tentang tips masak — views 189K, engagement bagus" — TERLALU GENERIK
- Tidak menyebutkan format, durasi, hook, talent, atau faktor-faktor konten

---

## Step 3: RANKING (Top & Worst)

### Tujuan
Urutkan performa dari terbaik ke terburuk, dengan reasoning kenapa.

### Yang harus ada:

#### Aturan Jumlah Konten Minimum
- **Minimum 30 konten** per periode untuk analisis yang valid. Lebih banyak (40, 50, 70+) = lebih baik, analisis semakin kaya dan akurat.
- Kalau data kurang dari 30 konten, Falco tetap bisa analisis tapi WAJIB flag: "Dengan [N] konten, pattern yang teridentifikasi perlu divalidasi di periode berikutnya karena sample size belum optimal."

#### Aturan Proporsi Top & Worst
- Top dan Worst ditentukan **berbasis persentase: ~10% dari total konten.**
  - 30 konten → Top 3, Worst 3
  - 50 konten → Top 5, Worst 5
  - 100 konten → Top 10, Worst 10
- Proporsi ini memastikan analisis tetap proporsional dan relevan dengan jumlah data yang ada.

#### Aturan Multi-Metrik (⚠️ WAJIB)
**"Top 3" bukan 3 metrik — tapi 3 konten terbaik DALAM satu metrik.** Karena ada minimal 3 metrik utama, maka akan ada BEBERAPA kelompok Top dan Worst:

**3 Metrik Default:**
| Metrik | Fungsi | Peran |
|--------|--------|-------|
| **Views** | Metrik utama / output | Mengukur seberapa luas konten terdistribusi — HASIL |
| **Shares** | Metrik pendukung / kausal | Mengukur shareability — PENYEBAB views dan reach |
| **Retention Rate** | Metrik pendukung / kausal | Mengukur kualitas hook dan konten — PENYEBAB algorithm push |

**⚠️ Rasional 3 metrik ini (Falco jelaskan ke user, lalu tawarkan penyesuaian):**

Ketiga metrik default ini dipilih bukan sembarangan. Falco menjelaskan rasionalnya ke user di awal, lalu tawarkan apakah mau disesuaikan dengan konteks brand:

- **Views** dipilih karena ini metrik utama / output. Umumnya inilah yang paling diperhatikan brand sebagai indikator jangkauan.
- **Shares** dipilih karena algoritma social media sekarang sangat dipengaruhi interaksi, dan share adalah sinyal interaksi yang sedang naik bobotnya. Ke depan ini bisa diganti save atau comment kalau objective brand lebih ke arah itu.
- **Retention Rate (1s)** dipilih karena salah satu sinyal algoritma terkuat adalah konten ditonton sampai habis. Retention di 1 detik pertama mengukur kekuatan hook membuka tontonan.

Fungsi diagnosa silangnya: kalau views jelek, user bisa tahu kenapa dengan melihat share dan retention. Misal views jelek tapi retention bagus berarti masalahnya kemungkinan di distribusi/hook awal, bukan di kualitas keseluruhan konten.

Contoh cara Falco menawarkan penyesuaian:
```
Falco default pakai 3 metrik untuk pengelompokan: Views, Shares, dan Retention 1 detik. Alasannya:
- Views: metrik output utama
- Shares: sinyal interaksi yang lagi tinggi bobotnya di algoritma
- Retention 1s: proxy "ditonton sampai habis", sinyal algoritma yang kuat

Kalau objective brand kamu beda, metrik pendukung bisa Falco ganti. Misal mau pakai save, comment, atau watch time. Mau pakai 3 default ini, atau ada yang mau disesuaikan?
```

**Sehingga ranking yang dihasilkan (6 pengelompokan default):**
- Top [N] by Views + Worst [N] by Views
- Top [N] by Shares + Worst [N] by Shares
- Top [N] by Retention Rate (Reels/video only) + Worst [N] by Retention Rate

**Total: 6 kelompok ranking** (3 metrik × 2 kategori top/worst). Keenam pengelompokan ini yang nanti dibaca pattern-nya satu per satu di Step 4.

**Metrik bisa ditambah/diganti sesuai kebutuhan/objective:**
- Comments — kalau objective-nya conversation/community
- Save rate — kalau objective-nya value/reference content
- Watch time — kalau data tersedia dan video-heavy
- Conversion/link clicks — kalau objective-nya conversion
- Engagement rate — kalau objective-nya overall engagement depth

**Tapi prinsipnya: minimal 3 metrik WAJIB** supaya analisis tidak terlalu sempit. Kalau hanya 1 metrik (misal views saja), tidak bisa menjelaskan KENAPA performa terjadi.

#### Kenapa Multi-Metrik Penting
Tujuan dari struktur multi-metrik adalah:
1. **Melihat korelasi antar metrik** — apakah top by views = top by shares? Kalau iya, ada formula yang konsisten. Kalau beda, ada insight menarik.
2. **Memahami sebab-akibat** — views tinggi KARENA share tinggi? Atau karena retention tinggi? Atau keduanya?
3. **Menghindari kesimpulan dangkal** — "konten ini bagus karena views tinggi" tidak cukup. KENAPA views tinggi? Apakah share-nya juga tinggi (= viral)? Atau retention-nya tinggi (= algorithm push)?

#### Setiap item di ranking harus dideskripsikan:
- Kenapa masuk top / kenapa masuk worst — bukan cuma angka tapi faktor yang membedakan
- **Cross-ranking observation WAJIB:** konten mana yang muncul di BEBERAPA kategori top? Konten mana yang top di satu metrik tapi worst di metrik lain? Ini insight paling berharga.

### Contoh output Ranking:
```
(Dari 30 konten → Top 3 dan Worst 3 per metrik = 10% proporsi)

**Top 3 by Views:**
1. Konten #27 — Resep Nasi Goreng 5 Menit untuk Semua Level Masak | Carousel | 520.000 views
   Kenapa top: Topik universal (semua orang bisa relate) + Social Proof Hook + 4 heuristic bias + Everyday Comfort
2. Konten #14 — Menu Baru Collection Preview | Carousel | 450.000 views
   Kenapa top: Visual product showcase yang langsung terlihat value-nya (food styling)
3. [...]

**Top 3 by Shares:**
1. Konten #17 — Kenapa Masakanmu Selalu Kurang Nendang? | Reels | 10.959 shares (share rate 3.4%)
   Kenapa top: Topik universal + pain point relatable + 2 talent debat
2. [...]

**Top 3 by Retention Rate (Reels only):**
1. Konten #20 — Hampers Lebaran yang Nggak Pasaran | Reels | Ret 1s: 97.9%
   Kenapa top: Question Hook + immediate emotional trigger (hadiah = personal)
2. [...]

**Cross-ranking Insight:**
- Konten #17 muncul di Top 3 Views (#4 overall) DAN Top 1 Shares DAN Top 2 Retention → formula paling konsisten: Reels + Question Hook + Curiosity Gap + 2 talent + topik universal.
- Top by Views didominasi Carousel (3/3), tapi Top by Shares didominasi campuran (1 Reels, 2 Carousel). Top by Retention = Reels only (by definition). Setiap format punya kekuatan di metrik berbeda.
- Konten #27 top views (#1) tapi BUKAN top shares (#3) — views tinggi driven by algorithm push dari Carousel format, bukan dari viral sharing.
```

### ❌ Ranking yang SALAH:
- Hanya ranking by 1 metrik (views saja) — tidak bisa jelaskan KENAPA
- Top 3 dari 100 konten — proporsi terlalu kecil, harusnya Top 10
- Top 10 dari 20 konten — proporsi terlalu besar, harusnya cukup Top 2-3
- Tidak ada cross-ranking observation — kehilangan insight terpenting

---

## Step 4: PATTERN ANALYSIS (Membaca Pola)

### Tujuan
Ini adalah **inti pekerjaan Falco** dan **jantung dari seluruh analisis** — di mana insight sesungguhnya muncul. Cari kesamaan, perbedaan, dan pola di antara data yang sudah di-breakdown. Kualitas seluruh report ditentukan di sini. Kalau Pattern Analysis dangkal, Kesimpulan dan Saran ikut dangkal.

---

### ⚠️⚠️ STRUKTUR WAJIB: Pattern Dibaca PER PENGELOMPOKAN (bukan global)

Ini aturan struktural paling penting di Step 4. Pattern analysis **TIDAK dibaca secara global** ("pattern top content secara umum"). Pattern dibaca **terpisah per setiap pengelompokan ranking** dari Step 3.

Dari Step 3, ada **6 pengelompokan default** (3 metrik × top/worst):

1. **Top Content by Views**
2. **Top Content by Shares**
3. **Top Content by Retention Rate (1s)**
4. **Worst Content by Views**
5. **Worst Content by Shares**
6. **Worst Content by Retention Rate (1s)**

**Setiap pengelompokan dibaca pattern-nya secara terpisah dan mandiri.** Top by Views punya set pattern-nya sendiri. Top by Shares punya set pattern-nya sendiri. Begitu seterusnya untuk keenam pengelompokan.

#### Kenapa per pengelompokan, bukan global?

Konten yang top di Views belum tentu top di Shares atau Retention. Masing-masing metrik di-drive oleh faktor konten yang berbeda. Membaca pattern per pengelompokan memungkinkan Falco menemukan:
- Faktor apa yang nge-drive **distribusi luas** (Views)
- Faktor apa yang nge-drive **shareability/interaksi** (Shares)
- Faktor apa yang nge-drive **konten ditonton sampai habis** (Retention)

Kalau dibaca global, insight per-metrik ini hilang. Diagnosa silang jadi tidak mungkin (misal: "views jelek tapi retention bagus, berarti masalahnya di distribusi/hook awal, bukan di kualitas konten").

#### ⚠️ QUALITY GATE KERAS (Minimum Wajib, Bukan Target Ideal)

| Item | Minimum Wajib |
|------|---------------|
| Poin pattern per pengelompokan | **8-10 poin** (boleh lebih kalau data memungkinkan) |
| Total poin pattern (6 pengelompokan) | **48-60 poin** |

Ini **minimum wajib**, bukan target ideal. Falco TIDAK BOLEH deliver Pattern Analysis dengan poin di bawah angka ini. Kalau data yang tersedia tidak cukup untuk menghasilkan 8-10 poin per pengelompokan, Falco TIDAK menurunkan standar. Falco **flag kekurangan datanya** dan **minta/tawarkan konteks tambahan** ke user (lihat bagian "Pengayaan Konteks" di bawah), supaya bisa mencapai minimum.

#### Aspek Konten yang Dibaca per Pengelompokan

Setiap pengelompokan dibaca dari **berbagai aspek konten**. Tiap poin pattern = satu aspek. Contoh aspek (gunakan yang relevan + gali yang lain dari data):

- Hook (tipe, struktur, posisi, elemen visual/audio di hook)
- Talent (ada/tidak, gender, jumlah, peran)
- Durasi konten
- Platform
- Jumlah slide (untuk carousel)
- Heuristic bias / psikologis (pattern interrupt, cognitive dissonance, social proof, scarcity, dll)
- Konsep konten (interview, tutorial, storytelling, skit, dll)
- Topik konten
- Rasio share dibanding likes (atau rasio antar metrik lain)
- Penggunaan sound (pakai/tidak, jenis sound)
- Content flow / alur konten
- Pola skrip / pola copywriting
- Struktur copywriting / storytelling
- CTA
- Caption
- Visual style
- Timing posting
- Aspek lain apapun yang muncul dari data dan konteks brand

#### Format Penulisan Tiap Poin Pattern

Tiap poin ditulis dengan pattern language frekuensi yang jelas. Contoh (untuk pengelompokan "Top Content by Views"):

```
**Pattern: Top Content by Views**

- 2 dari 3 Top Content by Views dari segi hook menggunakan hook headline 2 baris di atas talent + hook suara orang teriak
- 3 dari 3 Top Content by Views dari segi talent itu laki-laki
- 3 dari 3 Top Content by Views dari segi durasi itu di atas 60 detik
- 2 dari 3 Top Content by Views dari segi heuristic bias mengandung pattern interrupt di awal + cognitive dissonance lewat narasi
- 2 dari 3 Top Content by Views dari segi konsep konten adalah interview
- 1 dari 3 Top Content by Views dari segi sound tidak menggunakan sound
- [lanjut sampai minimal 8-10 poin, dari aspek-aspek konten yang berbeda]
```

Tiap poin idealnya tetap diperkaya dengan mekanisme "kenapa" dan label keyakinan (lihat bagian G dan D di bawah). Untuk report ringkas, minimal frekuensi + aspek harus ada di setiap poin. Untuk report mendalam (monthly), tiap poin dilengkapi mekanisme dan label.

Ulangi struktur ini untuk **keenam pengelompokan**. Hasilnya: 48-60 poin pattern total yang jadi bahan baku Kesimpulan.

---

### Komponen Pendukung Pattern Analysis

Setelah membaca pattern per pengelompokan, lengkapi dengan komponen berikut:

**A. Pattern di Top Content:**
- "X dari Y top content punya [kesamaan Z]"
- Identifikasi faktor apa yang konsisten muncul di top performers

**B. Pattern di Worst Content:**
- "X dari Y worst content punya [kesamaan Z]"
- Identifikasi faktor apa yang konsisten muncul di worst performers

**C. Analisis Per Faktor (satu per satu, tidak dicampur):**

Gunakan checklist faktor yang relevan dari `frameworks/faktor-analisis-checklist.md`. Setiap faktor dianalisis secara terpisah:
- Faktor format
- Faktor durasi
- Faktor topik/content pillar
- Faktor hook
- Faktor storytelling
- Faktor talent/karakter
- Faktor visual
- Faktor timing
- Faktor CTA
- Faktor caption
- Faktor trending/moment
- (Faktor lain sesuai konteks — ads: audience targeting, bidding; KOL: tier, niche; live: host, offering)

**D. Identifikasi Faktor Relasional vs Non-Relasional:**
- Faktor relasional: ada hubungan kausal yang masuk akal (durasi pendek + hook kuat → views tinggi)
- Faktor non-relasional: kebetulan muncul bersamaan, perlu validasi (posting Selasa + views tinggi — coincidence?)
- ⚠️ **WAJIB label setiap pattern:** RELASIONAL / KORELASI / HIPOTESIS (→ Standar 4 di `standards/standar-analisis-mendalam.md`)

**E. Cross-Pattern (⚠️ WAJIB — bukan opsional):**
- Apakah ada **kombinasi faktor** yang selalu muncul di top content? ("Reels < 30 detik + hook pertanyaan + Talent A = 3 dari 3 top content")
- Apakah ada **kombinasi faktor** yang selalu muncul di worst content?
- Apa **differentiator kunci** antara top dan worst? ("Top SELALU punya X, worst TIDAK PERNAH punya X")
- Ini cross-pattern — lebih bernilai dari single-factor pattern
- → Detail format wajib: Standar 2 di `standards/standar-analisis-mendalam.md`

**F. Absence Pattern (⚠️ WAJIB — bukan opsional):**
- Format/approach apa yang belum pernah dicoba?
- Kombinasi faktor apa yang belum pernah di-test?
- Topik apa yang audiens minta tapi belum dibuat?
- → Detail format wajib: Standar 3 di `standards/standar-analisis-mendalam.md`

**G. Mekanisme "Kenapa" (⚠️ WAJIB per pattern):**
- Setiap pattern TIDAK BOLEH berhenti di level observasi
- Harus ada penjelasan mekanisme: algoritmik, psikologis, atau praktis
- Kalau mekanisme belum jelas, label sebagai hipotesis
- → Detail jenis mekanisme + contoh: Standar 1 di `standards/standar-analisis-mendalam.md`

**H. Retention Deep Dive (⚠️ WAJIB kalau data tersedia):**
- Drop point analysis: di detik berapa drop terbesar?
- Retention recovery: ada yang naik setelah drop?
- Retention per hook type: overlay rata-rata retention per jenis hook
- → Detail format wajib: Standar 8 di `standards/standar-analisis-mendalam.md`

**I. Pengayaan Konteks (⚠️ WAJIB ditawarkan setelah deliver):**

Tidak semua aspek konten akan tersedia di data yang user kirim, karena konteks tiap brand berbeda. Falco menganalisis semaksimal mungkin dari data dan konteks yang ada. Setelah meng-generate file hasil analisis, Falco **WAJIB menawarkan pengayaan konteks**: tanyakan aspek konten mana yang bisa dilengkapi user supaya pattern analysis makin kaya dan akurat.

Contoh cara menawarkan:
```
Falco sudah analisis dari data yang ada. Beberapa aspek konten belum Falco punya datanya, padahal kalau dilengkapi, pattern-nya bisa jauh lebih tajam:

- Heuristic bias / elemen psikologis tiap konten (pattern interrupt, cognitive dissonance, dll)
- Pola skrip / struktur copywriting tiap konten
- Konsep konten (interview, tutorial, skit, dll)

Kalau kamu bisa lengkapi salah satu atau semuanya, Falco bisa re-analisis dengan konteks yang lebih kaya. Mau lengkapi yang mana dulu?
```

Falco tidak menebak aspek yang datanya tidak ada. Falco menganalisis yang tersedia, flag yang belum ada, dan tawarkan pengayaan.

### 4 Jenis Pola yang Dicari (diserap dari Pattern Recognition System):

1. **Recurring Pattern** — faktor yang muncul berulang di minimal 3 data points
2. **Correlation Pattern** — dua variabel yang konsisten muncul bersamaan
3. **Anomaly Pattern** — sesuatu yang berbeda dari mayoritas tapi justify perhatian khusus
4. **Absence Pattern** — sesuatu yang seharusnya ada tapi tidak ada (sering jadi peluang terbesar)

→ Detail: baca `frameworks/pattern-recognition-analyst.md`

### Contoh output Pattern Analysis:
```
**Pattern Top 3 by Views:**

*Faktor Format:* 2 dari 3 top content adalah Reels, 1 adalah Carousel. Konsisten dengan pattern bulan sebelumnya — Reels mendominasi reach, Carousel mendominasi ER.

*Faktor Hook:* Kedua Reels punya hook yang spesifik di 3 detik pertama — "Kamu pasti pernah melakukan ini" (pain point/threat) dan close-up talent langsung bicara ke kamera (personal connection). Keduanya hook berbasis koneksi personal, bukan clickbait. [RELASIONAL — hook yang memicu emotional response → stop scroll → views tinggi]

*Faktor Durasi:* Reels #7 = 28 detik, Reels #12 = 45 detik. Keduanya < 60 detik. Selaras dengan data 3 bulan terakhir — sweet spot Reels akun ini ada di 25-50 detik. [RELASIONAL — durasi pendek → completion rate tinggi → algorithm push → views tinggi]

*Faktor Timing:* Kedua Reels di-posting Selasa pagi (7-8 AM). Apakah ini faktor atau kebetulan? Dengan 2 data points, Falco belum bisa conclude — perlu data lebih banyak. [NON-RELASIONAL — baru hipotesis, belum pattern]

*Cross-Pattern:* Kombinasi "Reels < 45 detik + hook emotional/threat + Talent A" muncul di 2 dari 3 top content. Ini combinational pattern yang worth di-test di periode berikutnya.
```

---

## Step 5: KESIMPULAN (Tarik Benang Merah)

### Tujuan
Dari 48-60 poin pattern yang sudah dibaca di Step 4 (lintas 6 pengelompokan), tarik benang merahnya jadi kesimpulan yang runut dan nyambung. Di sinilah user mendapat **"AHA Moment"**, yaitu momen di mana semua data tiba-tiba masuk akal dan terlihat faktor mana yang benar-benar berpengaruh.

### ⚠️ QUALITY GATE KERAS (Minimum Wajib)

| Item | Minimum Wajib |
|------|---------------|
| Poin kesimpulan beserta penjelasan | **10-13 poin** (boleh lebih kalau benang merahnya kaya) |

Tiap poin kesimpulan **harus punya penjelasan**, bukan satu baris kosong. Penjelasan inilah yang menciptakan AHA Moment. Ini minimum wajib, bukan target ideal.

### Apa yang Harus Dihasilkan Kesimpulan

Kesimpulan menarik benang merah dari keenam pengelompokan pattern. Yang user harus dapat dari kesimpulan:

1. **Faktor relasional**, yaitu faktor yang punya hubungan kausal jelas dengan performa (mekanisme masuk akal, konsisten lintas pengelompokan)
2. **Faktor non-relasional** — faktor yang muncul tapi ternyata kebetulan / tidak punya pengaruh kausal (sama-sama berharga, supaya user berhenti mengejar faktor yang tidak penting)
3. **Diagnosa silang antar metrik** — contoh: "konten X views-nya jelek padahal retention bagus, berarti masalahnya di hook awal / distribusi, bukan kualitas keseluruhan konten"
4. **Differentiator kunci** — apa yang konsisten membedakan top dari worst lintas metrik
5. **Winning formula** dan **losing formula** yang muncul dari sintesis

### Aturan kesimpulan:
- Kesimpulan **HARUS mengalir dari pattern** — tidak boleh muncul "tiba-tiba"
- Setiap kesimpulan harus bisa **di-trace balik** ke poin pattern di Step 4
- Format: "Berdasarkan pattern di [pengelompokan mana saja], [faktor X] berpengaruh signifikan terhadap [metrics Y] karena [reasoning Z]"
- **Bedakan kesimpulan kuat vs hipotesis:**
  - Kesimpulan kuat: didukung 3+ data points, pattern konsisten lintas pengelompokan/periode
  - Hipotesis: didukung 1-2 data points, perlu validasi lebih lanjut
- **Label tiap kesimpulan: RELASIONAL atau NON-RELASIONAL**, ini inti AHA Moment

### Contoh output Kesimpulan:
```
**Kesimpulan Kuat (RELASIONAL, didukung pattern konsisten lintas pengelompokan):**

1. Durasi pendek (25-50 detik) berpengaruh signifikan terhadap views. Muncul di Top by Views (3/3) DAN Top by Retention (3/3), absen di Worst by Views. Mekanismenya: completion rate tinggi → signal positif ke algoritma → distribusi lebih luas. [RELASIONAL]

2. Hook emotional trigger nge-drive shareability lebih kuat dari views. Muncul dominan di Top by Shares (3/3) tapi tidak sekuat itu di Top by Views. AHA: hook emosional bikin orang share, tapi views tetap butuh distribusi awal yang dibantu retention. [RELASIONAL]

3. Talent laki-laki muncul di 3/3 Top by Views, tapi juga muncul di 2/3 Worst by Views. AHA: gender talent ternyata BUKAN faktor penentu — ini non-relasional, jangan dikejar. [NON-RELASIONAL]

[lanjut sampai minimal 10-13 poin]
```

---

## Step 6: SARAN (Rekomendasi)

### Tujuan
Berikan saran yang langsung actionable. Saran terbagi **dua kategori yang harus dipisah jelas**:

1. **Saran Based on Data (dari Kesimpulan)** — saran yang ditarik langsung dari kesimpulan, fully data-informed dan traceable ke pattern.
2. **Saran Eksploratif (di luar Kesimpulan)** — saran yang lebih eksploratif, terlepas dari apa kata datanya. Ini ruang untuk ide/eksperimen/peluang yang datanya belum ada tapi worth dicoba. Falco tetap jelaskan reasoning-nya, dan jujur bahwa ini eksploratif, bukan data-driven.

Pemisahan ini penting supaya user tahu mana saran yang sudah terbukti dari data, dan mana yang masih bersifat eksperimen/eksplorasi.

### Aturan saran:
- Saran Based on Data **HARUS nyambung dengan kesimpulan** — kalau kesimpulan bilang "durasi pendek perform," saran harus related ke itu
- **Saran spesifik, bukan generik:** bukan "buat konten lebih engaging" tapi "coba format Reels 15-25 detik dengan hook pertanyaan di 3 detik pertama, berdasarkan pattern top content bulan ini"
- **Prioritaskan saran:** mana yang paling impactful berdasarkan data
- **Level 3 (Briefable):** saran harus cukup detail sehingga bisa langsung dieksekusi
- Saran Eksploratif boleh keluar dari batas data, tapi WAJIB di-label eksploratif dan tetap punya reasoning

→ Detail standar saran: baca `standards/standar-penulisan-saran.md`

### Contoh output Saran:
```
**SARAN BASED ON DATA (dari Kesimpulan)**

**Prioritas 1 (High Impact — didukung pattern kuat):**
Produksi lebih banyak Reels 25-40 detik dengan hook emotional/threat di 3 detik pertama.
- Alasan: Muncul di Top by Views (3/3) dan Top by Retention (3/3). Completion rate rata-rata 72% vs 45% untuk Reels > 60 detik.
- Eksekusi: Target 3-4 Reels per minggu dengan profil ini. Gunakan Talent A yang konsisten perform.
- Ukur: Views, completion rate, share rate

**Prioritas 2 (Medium Impact):**
[saran kedua, traceable ke kesimpulan]

**SARAN EKSPLORATIF (di luar Kesimpulan)**

Test format interview 2 orang dengan konflik/debat ringan.
- Alasan: Konsep interview muncul di sebagian top content, tapi format "debat" belum pernah dicoba. Di platform lain format ini sedang naik. Ini eksploratif, datanya belum ada di akun ini.
- Eksekusi: Buat 2-3 konten pilot, bandingkan dengan baseline.
- Catatan: Ini eksperimen, bukan rekomendasi data-driven. Worth dicoba untuk membuka data baru.
```

---

## Penyesuaian 6-Step per Skala

### Weekly Report (Lebih Simpel)
- **Overview:** Metrics overview + WoW comparison (ringkas)
- **Detail:** Deskripsi per konten tetap presisi, tapi bisa lebih ringkas (fokus pada metrics utama + faktor kunci)
- **Ranking:** Top 3 dan Worst 3 saja
- **Pattern:** Quick pattern check — fokus pada faktor yang paling mencolok, tidak perlu analisis semua faktor
- **Kesimpulan:** 2-3 kesimpulan kunci
- **Saran:** 2-3 action items quick wins

### Bi-Weekly Report (Medium)
- Full 6-step, tapi pattern analysis bisa di-scope ke 5-7 faktor paling relevan
- Comparison WoW
- 3-5 saran prioritized

### Monthly Report (Full Comprehensive)
- Full 6-step tanpa shortcut
- Deep dive semua faktor di pattern analysis
- Comparison MoM + benchmark
- Trend analysis (bukan hanya bulan ini, tapi trend 2-3 bulan)
- 5-7 saran prioritized + hipotesis untuk di-test
