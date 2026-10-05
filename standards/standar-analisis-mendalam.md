# Standar Analisis Mendalam — 8 Standar Wajib di Atas Baseline

## Prinsip Utama

⚠️ **FILE INI WAJIB DIBACA SETIAP KALI FALCO MENGHASILKAN ANALISIS ATAU ME-REVIEW ANALISIS USER.**

File ini meng-codify 8 standar yang WAJIB dipenuhi di atas baseline report (`references/contoh-report-baseline.md`). Baseline report sudah punya struktur dan alur yang benar — tetapi standar Falco harus MELAMPAUI baseline di 8 area berikut.

**Prinsip:** Baseline = kerangka minimum yang sudah benar. Standar ini = kedalaman yang membedakan analisis biasa dari analisis yang benar-benar insightful.

---

## Standar 1: Setiap Pattern WAJIB Punya Mekanisme "Kenapa"

### Aturan
Setiap pattern yang diidentifikasi di Step 4 (Pattern Analysis) TIDAK BOLEH berhenti di level observasi ("X dari Y punya Z"). Harus ada penjelasan KENAPA pattern itu terjadi — mekanisme algoritmik, psikologis, atau praktis.

### Level Kedalaman

| Level | Contoh | Status |
|-------|--------|--------|
| **Observasi saja** | "3 dari 3 top retention menggunakan Curiosity Gap" | ❌ Belum cukup |
| **Observasi + Mekanisme** | "3 dari 3 top retention menggunakan Curiosity Gap. **Mekanisme:** CG menciptakan information gap di otak — otak otomatis ingin menutup gap ini, sehingga penonton bertahan menonton untuk mendapatkan jawaban. Ini bekerja di level System 1 (bawah sadar), berbeda dengan hook informatif yang butuh keputusan sadar." | ✅ Standar Falco |
| **Observasi + Mekanisme + Implikasi** | [sama seperti di atas] + "**Implikasi:** Untuk meningkatkan retention, prioritaskan hook yang memicu respons otomatis (curiosity, threat, surprise) di atas hook yang meminta komitmen sadar (tutorial promise, educational teaser)." | ✅✅ Ideal |

### Jenis Mekanisme yang Bisa Digunakan

**Mekanisme Algoritmik:**
- Completion rate tinggi → signal positif ke algoritma → distribusi lebih luas → views tinggi
- Save rate tinggi → signal "valuable content" → prioritas di Explore → reach luas
- Share → distribusi ke network baru → reach non-followers
- Carousel swipe → signal engagement → algorithm push

**Mekanisme Psikologis:**
- **Curiosity Gap** — otak ingin menutup information gap → retention
- **Threat/Loss Aversion** — ancaman kehilangan/salah → stop scroll + watch to completion
- **Social Proof** — "banyak orang sudah..." → trust + FOMO → engagement
- **Scarcity** — kelangkaan → urgensi → action (click, save, buy)
- **Identifikasi langsung** — "ini gue banget" → emotional connection → share
- **Contrast/Ketidakselarasan** — ekspektasi vs realita → surprise → watch + share
- **Bandwagon** — "semua orang sedang..." → FOMO → engagement
- **Anchoring** — angka/fakta pertama menjadi acuan → framing persepsi

**Mekanisme Praktis:**
- Durasi pendek → time investment rendah → lebih shareable
- Visual produk (swatches, before-after) → langsung terlihat value → save for reference
- Talent yang sudah dikenal → parasocial relationship → built-in audience
- Topik universal → relatable ke banyak orang → reach luas
- CTA spesifik ("save buat nanti") → memberikan alasan konkret untuk action

### Kalau Mekanisme Belum Jelas
Tidak semua pattern punya mekanisme yang jelas. Kalau belum jelas, Falco HARUS:
1. Tetap tulis observasinya
2. Label sebagai **"Mekanisme belum teridentifikasi — butuh data lebih lanjut"** atau **"Hipotesis: [kemungkinan mekanisme]"**
3. JANGAN memaksakan mekanisme yang tidak masuk akal hanya supaya terlihat dalam

---

## Standar 2: Cross-Pattern Analysis WAJIB Ada

### Aturan
Setelah analisis per faktor selesai, Falco WAJIB menambahkan section **Cross-Pattern** — kombinasi 2+ faktor yang secara bersamaan selalu muncul di top atau worst content.

### Kenapa Ini Penting
Pattern per faktor hanya melihat satu dimensi. Cross-pattern melihat INTERAKSI antar faktor — ini yang menghasilkan "formula" yang actionable. "Reels perform" dan "Question Hook perform" adalah dua observasi terpisah. "Reels + Question Hook + Curiosity Gap + durasi < 45 detik = selalu masuk top 5" adalah formula yang langsung bisa di-briefkan.

### Format Wajib

```
### Cross-Pattern Analysis

**Formula Top Content:**
"[Faktor A] + [Faktor B] + [Faktor C]"
→ Muncul di X dari Y top content [metrik] periode ini
→ Validasi historis: [muncul juga di X dari Y top content periode sebelumnya / belum ada data historis]
→ Keyakinan: [TINGGI / SEDANG / RENDAH]
→ Mekanisme: [kenapa kombinasi ini bekerja — bagaimana faktor-faktor ini saling memperkuat]

**Formula Worst Content:**
"[Faktor D] + [Faktor E] + [Faktor F]"
→ Muncul di X dari Y worst content [metrik] periode ini
→ Keyakinan: [TINGGI / SEDANG / RENDAH]
→ Mekanisme: [kenapa kombinasi ini gagal]

**Formula Contrast (Top vs Worst):**
"Top selalu punya [X], worst tidak pernah punya [X]"
→ [X] adalah differentiator kunci
```

### Contoh (dari data baseline report)

```
**Formula Top Views:**
"Carousel + 7 slides + Social Proof Hook + Everyday Comfort + ≥4 heuristic bias"
→ Muncul di 2 dari 3 top views. Yang ke-3 (#16) punya profil serupa minus 1 elemen.
→ Keyakinan: SEDANG (perlu validasi di bulan berikutnya)
→ Mekanisme: Carousel visual-heavy + Social Proof menciptakan "ini dipercaya banyak orang" framing → Everyday Comfort membuat audiens merasa "ini juga cocok untuk aku" → multiple bias memperkuat dari berbagai angle psikologis.

**Formula Top Retention:**
"Question Hook + Curiosity Gap + Real Transformation"
→ Muncul di 2 dari 3 top retention (#20 dan #17)
→ Keyakinan: SEDANG
→ Mekanisme: Question Hook memicu respons otomatis untuk mencari jawaban + Curiosity Gap mempertahankan tension sepanjang video + Real Transformation memberikan payoff yang memuaskan di akhir. Ketiga elemen ini membentuk arc: hook (buka pertanyaan) → tension (gap) → payoff (transformasi).

**Formula Worst Retention:**
"Hook berbasis janji (Tutorial Promise / Myth Buster) + tanpa Curiosity Gap + opening narasi/pengantar"
→ Muncul di 2 dari 3 worst retention
→ Keyakinan: SEDANG-TINGGI (diperkuat oleh 3/3 worst retention yang tidak pakai Curiosity Gap)
→ Mekanisme: Hook janji meminta commitment tanpa memberikan stimulus emosional → opening narasi terlalu lambat membangun tension → tanpa Curiosity Gap tidak ada "tarikan" untuk tetap menonton.

**Differentiator Kunci:**
- Top retention SELALU punya Curiosity Gap (3/3). Worst retention TIDAK PERNAH punya (0/3). Ini korelasi paling kuat di seluruh analisis.
- Top views SELALU punya Everyday Comfort (3/3). Worst views TIDAK PERNAH punya kombinasi Everyday Comfort + Real Transformation (0/3).
```

---

## Standar 3: Absence Pattern WAJIB Ada

### Aturan
Setiap analisis Falco WAJIB menyertakan section **Absence Pattern** — identifikasi apa yang TIDAK ADA dari data yang dianalisis. Ini sering menjadi peluang terbesar yang terlewat.

### 5 Area Absence yang Harus Dicek

| Area | Pertanyaan | Contoh |
|------|-----------|--------|
| **Format/Approach** | Ada format atau pendekatan yang belum pernah dicoba? | "Belum ada Collab Post, belum ada konten UGC/testimonial customer" |
| **Kombinasi Faktor** | Ada kombinasi yang secara teori menjanjikan tapi belum pernah di-test? | "Belum pernah test Reels + Social Proof Hook (selama ini hanya Carousel yang pakai Social Proof Hook)" |
| **Topik/Angle** | Ada topik yang audiens minta tapi belum dibuat? Ada angle yang belum di-explore? | "Komentar banyak tanya soal sensitive skin tapi belum ada konten dedicated untuk itu" |
| **Audience Segment** | Ada segmen audiens yang belum ter-address? | "Semua konten fokus ke ibu rumah tangga — padahal data menunjukkan 30% followers adalah laki-laki yang juga suka masak" |
| **Distribusi/Channel** | Ada channel atau metode distribusi yang belum dimanfaatkan? | "Belum pernah test posting di Reels tab vs Feed first, belum ada cross-posting ke TikTok" |

### Format Wajib

```
### Absence Pattern — Yang Belum Ada

1. **[Area]: [Apa yang tidak ada]**
   - Observasi: [kenapa ini teridentifikasi sebagai absence]
   - Potensi: [kenapa ini worth exploring — data atau reasoning apa yang mendukung]
   - Rekomendasi: [apa yang bisa di-test]

2. [...]
```

---

## Standar 4: Setiap Pattern WAJIB Punya Label Keyakinan

### Aturan
Setiap pattern yang ditulis Falco WAJIB diberi label keyakinan. Tidak boleh semua pattern di-treat sama — ada yang kuat, ada yang masih hipotesis.

### 3 Level Label

| Label | Kriteria | Cara Menulis |
|-------|---------|-------------|
| **RELASIONAL (Keyakinan Tinggi)** | ≥3 data points konsisten + mekanisme kausal yang jelas + (idealnya) validasi lintas periode | `[RELASIONAL — mekanisme: ...]` |
| **KORELASI (Keyakinan Sedang)** | ≥3 data points konsisten TAPI mekanisme belum sepenuhnya jelas, ATAU mekanisme jelas tapi baru 2 data points | `[KORELASI — perlu validasi: ...]` |
| **HIPOTESIS (Keyakinan Rendah)** | 1-2 data points ATAU mekanisme tidak jelas ATAU baru muncul di periode ini saja | `[HIPOTESIS — baru X data points, perlu test: ...]` |

### Contoh Penerapan

```
*Faktor Hook:*
4 dari 5 top content by views punya hook yang memicu emotional response (Question Hook, Social Proof Hook, Shock Statement).
[RELASIONAL — mekanisme psikologis jelas: emotional hook memicu System 1 response yang lebih cepat dari rational hook. Konsisten dengan data 2 bulan terakhir.]

*Faktor Timing:*
2 dari 3 top content di-posting pagi (7-8 AM).
[HIPOTESIS — baru 2 data points di 1 periode. Bisa jadi coincidence karena konten pagi kebetulan juga punya hook dan topik yang lebih kuat. Perlu controlled test.]

*Faktor Jumlah Slide:*
2 dari 3 top Carousel punya 7 slides.
[KORELASI — muncul konsisten di data bulan ini, tapi mekanismenya belum jelas. Apakah 7 slides memang optimal, atau karena konten 7 slides kebetulan juga punya topik yang lebih menarik? Perlu isolasi variabel.]
```

### Implikasi ke Saran
- Pattern RELASIONAL → saran dengan confidence tinggi ("lakukan ini")
- Pattern KORELASI → saran dengan confidence sedang ("lakukan sambil monitor")
- Pattern HIPOTESIS → saran eksperimental ("test ini dengan design yang jelas")

---

## Standar 5: Deskripsi Hook WAJIB Spesifik + Mekanisme

### Aturan
Setiap kali Falco mendeskripsikan hook (di Step 2 Detail maupun Step 4 Pattern), hook TIDAK BOLEH hanya disebut jenisnya. Harus ada:
1. **Jenis hook** — Question Hook, Social Proof Hook, Shock Statement, dll
2. **Deskripsi spesifik** — kalimat/visual pembuka yang SEBENARNYA digunakan
3. **Mekanisme psikologis** — kenapa hook ini membuat orang stop scroll

### Format Wajib per Konten (di Step 2)

```
- Hook: [Jenis Hook] — "[Kalimat/deskripsi visual spesifik di 3 detik pertama atau slide pertama]"
  Mekanisme: [Kenapa ini bekerja — trigger psikologis apa yang diaktifkan]
```

### Contoh

❌ **Baseline (belum cukup):**
```
- Jenis Hook: Question Hook
```

✅ **Standar Falco:**
```
- Hook: Question Hook — "Kenapa masakanmu selalu kurang nendang padahal udah ikutin resep?"
  Mekanisme: Pertanyaan langsung yang menyerang pain point universal → memicu self-reflection ("iya ya, aku juga gitu") + curiosity gap (mau tahu jawabannya) → double trigger yang membuat stop scroll sangat kuat.
```

✅ **Standar Falco (Carousel):**
```
- Hook: Social Proof Hook — Slide pertama: foto swatch 8 shade di tangan dengan headline "SHADE YANG PALING BANYAK DICARI" + badge "500K+ terjual"
  Mekanisme: Social proof (banyak orang sudah beli) + visual yang langsung menunjukkan value (swatch = bisa langsung lihat warna) + scarcity implication (kalau banyak dicari, mungkin limited) → triple trigger awareness + FOMO + interest.
```

### Untuk Pattern Analysis (Step 4)
Saat menganalisis pattern hook di top/worst content, Falco harus tidak hanya menghitung "berapa yang pakai hook X" tapi juga menjelaskan:
- **Apa kesamaan mekanisme** dari hook-hook di top content? (misal: semua trigger System 1 / emotional response)
- **Apa kesamaan mekanisme** dari hook-hook di worst content? (misal: semua butuh System 2 / deliberate decision)
- **Kontras:** mekanisme top vs worst → ini jadi insight

---

## Standar 6: Overview WAJIB Include Distribusi & Anomali Struktural

### Aturan
Overview (Step 1) harus include tidak hanya total metrics + benchmark + tren, tapi juga:
1. **Distribusi Pareto** — berapa persen konten menyumbang berapa persen total views/engagement
2. **Anomali struktural** — pattern-pattern di level overview yang langsung terlihat sebelum deep dive

### Format Wajib (ditambahkan ke Overview)

```
**Distribusi performa:**
- [X] konten ([Y]% dari total) menyumbang [Z]% dari total views. Distribusi Pareto [kuat/moderat/lemah].
- Implikasi: [apa artinya — apakah performa terlalu concentrated di few konten, atau terdistribusi sehat?]

**Anomali struktural:**
- [Anomali 1]: [deskripsi — contoh: "Comments turun 10.5% padahal views naik 12.7% — kemungkinan pergeseran CTA atau content type"]
- [Anomali 2]: [...]
```

### Contoh (dari baseline report)

```
**Distribusi performa:**
6 konten (20% dari 30 total) menyumbang ~80% total views bulan ini. Distribusi Pareto sangat kuat — artinya performa akun sangat bergantung pada beberapa "hit besar," bukan konsistensi merata.
Implikasi: Strategi perlu mencakup both "swinging for the fences" (ciptakan konten dengan viral potential) DAN "base hits" (konten konsisten yang maintain engagement).

**Anomali struktural:**
- Views naik 12.7% tapi comments turun 10.5% dan shares turun 15.4% — gap ini signifikan. Hipotesis: pergeseran CTA ke follow/save mengorbankan interaksi langsung.
- New followers naik 23% (tertinggi 3 bulan) tapi ER juga naik — biasanya growth cepat menurunkan ER karena audience baru belum engaged. Ini anomali positif yang worth diinvestigasi.
```

---

## Standar 7: Saran WAJIB Level 3 dengan Metrik Ukur & Target

### Aturan
Setiap saran berbasis data WAJIB mengandung komponen Level 3 ini:

| Komponen | Wajib? | Penjelasan |
|----------|--------|-----------|
| Apa yang dilakukan | ✅ WAJIB | Aksi spesifik |
| Data pendukung | ✅ WAJIB | Pattern/kesimpulan yang mendukung — "X dari Y..." |
| Eksekusi detail | ✅ WAJIB | Format, hook, talent, visual, durasi, dll |
| Frekuensi/Volume | ✅ WAJIB | Berapa per periode |
| Metrik ukur | ✅ WAJIB | KPI yang harus di-track |
| Target angka | ⚠️ IDEALNYA | Target kuantitatif kalau bisa di-estimasi dari data |
| Prioritas | ✅ WAJIB | High / Medium / Eksperimental |
| Reasoning | ✅ WAJIB | Kenapa saran ini — koneksi ke data |
| Constraint | ⚠️ KALAU ADA | Risiko, limitasi, dependency |

### Contoh Saran Level 3 Lengkap

```
**Prioritas 1 (High Impact — RELASIONAL, didukung 3 bulan data):**
Standardisasi Question Hook + Curiosity Gap sebagai kombinasi default Reels.

- Data pendukung: 2 dari 3 top retention pakai Question Hook, 3 dari 3 top retention pakai Curiosity Gap. 3 dari 3 worst retention TIDAK pakai Curiosity Gap. Korelasi paling kuat di seluruh analisis.
- Eksekusi: Buat hook library berisi 15-20 template Question Hook + Curiosity Gap untuk berbagai topik. Contoh template: "Kenapa [pain point]? Ternyata [unexpected answer]..." / "[Angka mengejutkan]% orang melakukan [kesalahan]. Kamu salah satunya?"
- Frekuensi: Apply ke minimal 70% Reels (12-13 dari ~18 Reels/bulan). Sisanya 30% untuk variasi hook (Shock Statement, Controversial Opinion) supaya tidak monoton.
- Ukur: Retention rate detik ke-1 (target: >85%), retention detik ke-5 (target: >40%), views per Reels (target: naik 20% dari rata-rata current).
- Reasoning: Curiosity Gap bekerja di level System 1 thinking — memicu respons otomatis yang membuat penonton bertahan. Ini lebih reliable dari hook yang butuh keputusan sadar.
- Constraint: Hook yang sama berulang bisa fatigue setelah 2-3 bulan — perlu refresh template setiap quarter.
```

### Untuk Saran Eksploratif: Harus Ada Design Test

```
**Eksperimental (HIPOTESIS — perlu validasi):**
Test format "2 talent debat" sebagai format baru untuk shareability.

- Data pendukung: Konten #17 (2 talent pria & wanita) punya share tertinggi (10.959). Baru 1 data point — belum bisa conclude, tapi worth testing.
- Design test: Produksi 3 konten "debat ringan" di bulan depan dengan variasi:
  - Konten A: 2 talent debat tentang cara masak nasi goreng (30 detik)
  - Konten B: 2 talent debat tentang ingredient (30 detik)
  - Konten C: 2 talent debat tentang food myth (45 detik)
- Ukur: Share rate (target: >2% = di atas rata-rata akun), share-to-views ratio, komentar yang memilih sisi.
- Evaluasi setelah: 3 konten cukup untuk pola awal. Kalau 2 dari 3 punya share rate >2%, format ini layak di-adopt.
```

---

## Standar 8: Retention Analysis WAJIB Mendalam (Reels/Video)

### Aturan
Kalau data retention per detik tersedia, Falco WAJIB analisis lebih dalam dari sekadar menyajikan angka. Retention curve adalah data paling kaya untuk memahami QUALITY konten.

### Yang Harus Dianalisis

**A. Drop Point Analysis:**
- Di detik berapa drop TERBESAR terjadi per konten?
- Apa yang terjadi di detik itu? (transisi, narasi, visual change, dll)
- Apakah ada pattern: drop terbesar selalu di detik yang sama?

**B. Retention Recovery:**
- Apakah ada konten yang retention-nya NAIK setelah drop? (contoh: drop di detik 3 tapi naik lagi di detik 4-5)
- Kalau ya, apa yang terjadi di momen recovery itu? (twist, reveal, surprise, visual hook baru)
- Ini insight berharga tentang apa yang "menarik kembali" penonton

**C. Retention Curve per Hook Type:**
- Overlay rata-rata retention curve per jenis hook
- Contoh: "Question Hook rata-rata retention 1s = 96%, 5s = 66%. Tutorial Promise rata-rata retention 1s = 73%, 5s = 35%. Gap semakin lebar seiring durasi — Question Hook mempertahankan penonton jauh lebih baik."

**D. Retention vs Durasi:**
- Apakah ada hubungan antara durasi total dan retention pattern?
- Contoh: "Reels < 30 detik rata-rata retention 5s = 50%. Reels 30-60 detik rata-rata retention 5s = 40%. Reels > 60 detik rata-rata retention 5s = 33%."

### Format Output

```
**Retention Deep Dive:**

Drop point terbesar rata-rata terjadi di detik ke-[X]. Ini konsisten di [Y dari Z] Reels yang dianalisis. Hipotesis: di detik ke-[X], audiens membuat keputusan sadar apakah akan lanjut menonton — inilah "decision point" krusial.

Retention recovery terdeteksi di [N] konten:
- Konten #[X]: drop dari [A]% ke [B]% di detik [Y], naik kembali ke [C]% di detik [Y+1]. Momen recovery: [apa yang terjadi — twist, reveal, visual surprise].
- Implikasi: struktur konten yang punya "second hook" di detik [Y] bisa mempertahankan penonton yang hampir pergi.

Retention per hook type:
| Hook Type | Avg 1s | Avg 3s | Avg 5s | Drop 1s→5s |
|-----------|--------|--------|--------|------------|
| Question Hook | X% | X% | X% | Xpp |
| Social Proof | X% | X% | X% | Xpp |
| [dst] | | | | |

Insight: [hook mana yang paling mempertahankan retention, dan kenapa]
```

---

## Quality Check: Standar Sebelum Deliver

Sebelum Falco mem-finalize output analisis apapun, jalankan checklist ini:

| # | Standar | Self-Check Question | ✅/❌ |
|---|---------|-------------------|------|
| 1 | Mekanisme | Apakah setiap pattern punya penjelasan "kenapa"? | |
| 2 | Cross-Pattern | Apakah ada section cross-pattern dengan formula top + worst + differentiator? | |
| 3 | Absence | Apakah ada section absence pattern (apa yang belum ada/dicoba)? | |
| 4 | Label Keyakinan | Apakah setiap pattern punya label RELASIONAL / KORELASI / HIPOTESIS? | |
| 5 | Hook Detail | Apakah setiap hook dideskripsikan spesifik + mekanisme, bukan hanya jenis? | |
| 6 | Overview Distribusi | Apakah overview include distribusi Pareto + anomali struktural? | |
| 7 | Saran Level 3 | Apakah setiap saran data-based punya eksekusi + metrik + target + prioritas? | |
| 8 | Retention Depth | (Kalau data ada) Apakah retention dianalisis: drop point, recovery, per hook type? | |

### ⚠️ Quality Gate Angka (KERAS — Minimum Wajib)

Khusus untuk analisis performa konten dengan struktur 6 pengelompokan, tambahan gate ini WAJIB lolos sebelum deliver:

| # | Gate | Minimum | ✅/❌ |
|---|------|---------|------|
| A | Pattern per pengelompokan | Setiap dari 6 pengelompokan punya **8-10 poin** (boleh lebih) | |
| B | Total pattern | **48-60 poin** lintas 6 pengelompokan | |
| C | Poin kesimpulan | **10-13 poin** beserta penjelasan, dengan label relasional/non-relasional | |
| D | Pemisahan saran | Saran dipisah jelas: Based on Data vs Eksploratif | |
| E | Tawaran pengayaan | Setelah deliver, Falco menawarkan pengayaan konteks aspek yang datanya belum ada | |

Ini minimum wajib, bukan target ideal. Kalau data tidak cukup untuk lolos gate A-C, Falco TIDAK menurunkan standar. Falco flag kekurangan datanya dan tawarkan pengayaan konteks ke user supaya bisa mencapai minimum di iterasi berikutnya.

**Kalau ada yang belum ✅ — JANGAN deliver. Lengkapi dulu, atau flag + tawarkan pengayaan kalau penyebabnya data.**
