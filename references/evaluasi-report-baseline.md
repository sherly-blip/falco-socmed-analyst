# Evaluasi Report Baseline & Panduan Penggunaan

## Tujuan File Ini

File `contoh-report-baseline.md` adalah contoh analytics report yang menjadi **acuan struktur dan alur berpikir** Falco. Falco WAJIB menggunakan report ini sebagai:

1. **Pegangan saat membuat report dari nol** — ikuti alur dan kerangka berpikirnya
2. **Checklist saat mengecek/mengoreksi report user** — kalau report user lebih dangkal dari ini, Falco WAJIB kritik
3. **Baseline kedalaman minimum** — output Falco harus MINIMAL setara ini, idealnya LEBIH TAJAM

---

## Apa yang KUAT dari Report Ini (Dipertahankan & Dijadikan Standar)

### 1. Alur 6-Step yang Runut dan Tidak Loncat
Report mengikuti urutan: Overview → Strategic Pillar Context → Content Detail → Top & Worst Ranking → Pattern Analysis → Kesimpulan → Saran. Tidak ada step yang di-skip. Kesimpulan bisa di-trace ke pattern. Saran bisa di-trace ke kesimpulan. **Ini standar non-negotiable Falco.**

### 2. Overview yang Kontekstual
- Semua metrics punya benchmark (vs target, vs bulan sebelumnya, vs 2 bulan sebelumnya)
- Tren 3 bulan ditunjukkan
- Anomali dan concern langsung di-flag (comments turun, shares turun — dengan hipotesis kenapa)
- Tidak ada angka yang berdiri sendiri tanpa konteks

### 3. Strategic Pillar sebagai Lens Analisis
Report memperkenalkan strategic pillar sebagai lens untuk membaca performa. Ini bukan sekadar "content pillar" tapi **DNA brand yang bisa diukur kehadirannya per konten.** Falco harus selalu mempertimbangkan apakah ada "lens" serupa yang bisa digunakan di setiap analisis — entah itu strategic pillar, brand values, atau framework lain yang sudah dimiliki brand.

### 4. Content Detail yang Terstruktur per Konten
Setiap konten dideskripsikan dengan:
- Topik, format, konsep, content pillar, strategic pillar
- Heuristic bias yang digunakan
- Talent, durasi/jumlah slide, jenis hook, CTA/TTA
- Performa lengkap (views, likes, comments, shares, saves)
- Retention rate per detik (untuk Reels)

**Ini standar minimum deskripsi per konten.** Falco harus ensure setiap konten yang dianalisis punya detail setara ini.

### 5. Multi-Metric Ranking
Report tidak hanya ranking by satu metric — ada Top/Worst by Views, by Shares, DAN by Retention Rate. Ini penting karena top by views ≠ top by shares ≠ top by retention. Cross-ranking insight ini sangat berharga.

### 6. Pattern Language "Berapa dari Berapa"
Pattern analysis konsisten menggunakan format "X dari Y top/worst content punya [kesamaan]". Ini membuat setiap pattern bisa dinilai kekuatannya. **Ini signature Falco yang harus selalu digunakan.**

### 7. Multi-Faktor Pattern Analysis
Pattern dianalisis dari berbagai sudut: format, hook, heuristic bias, strategic pillar, topik, talent, durasi, CTA. Tidak hanya 1-2 faktor tapi komprehensif. Dan dilakukan untuk SETIAP ranking category (top views, top shares, top retention, worst views, worst shares, worst retention).

### 8. Kesimpulan yang Runut dari Pattern
Setiap kesimpulan bisa di-trace balik ke pattern yang teridentifikasi. Contoh: "Hook adalah faktor paling krusial" — bisa di-trace ke pattern "2 dari 3 top retention pakai Question Hook" dan "2 dari 3 worst retention pakai hook berbasis janji." Tidak ada kesimpulan yang muncul tiba-tiba.

### 9. Saran Dibedakan: Data-Based vs Eksploratif
Report memisahkan saran berbasis data (didukung pattern yang kuat) dari saran eksploratif (hipotesis yang perlu di-test). Ini level transparansi yang Falco harus selalu terapkan.

---

## Apa yang BISA DI-IMPROVE (Falco Harus Melampaui Baseline Ini)

### 1. Pattern Analysis Belum Ada Mekanisme "Kenapa"
Report mengidentifikasi pattern dengan baik ("3 dari 3 top retention menggunakan Curiosity Gap"), tapi belum menjelaskan KENAPA Curiosity Gap bekerja. Falco harus menambahkan mekanisme:

**Baseline (report ini):**
> "3 dari 3 top content berdasarkan retention itu mengandung Curiosity Gap sebagai heuristic bias."

**Standar Falco (harus lebih dalam):**
> "3 dari 3 top content by retention menggunakan Curiosity Gap. Mekanisme: Curiosity Gap menciptakan 'information gap' di otak audiens — otak secara otomatis ingin menutup gap ini, sehingga penonton tetap menonton untuk mendapatkan jawaban. Ini mempengaruhi retention secara langsung karena mekanismenya bekerja di level bawah sadar (System 1 thinking), berbeda dengan hook informatif yang membutuhkan keputusan sadar untuk terus menonton."

### 2. Cross-Pattern Belum Eksplisit
Report menganalisis faktor per faktor tapi belum secara eksplisit menulis cross-pattern — kombinasi faktor yang secara bersamaan muncul di top/worst content. Falco harus menambahkan:

**Contoh cross-pattern yang bisa ditarik dari data report ini:**
> "Cross-pattern Top Content: 'Carousel + 7 slides + Social Proof Hook + strategic pillar utama + 4 heuristic bias' → muncul di 2 dari 3 top views content. Formula ini konsisten."
>
> "Cross-pattern Top Retention: 'Question Hook + Curiosity Gap + transformation pillar' → muncul di 2 dari 3 top retention. Formula hook + bias + pillar ini saling memperkuat."

### 3. Absence Pattern Belum Ada
Report tidak mengidentifikasi apa yang TIDAK ADA — format/approach yang belum dicoba. Ini sering jadi peluang terbesar. Falco harus menambahkan section absence, misalnya:
- Format apa yang belum pernah dicoba? (Collab Post, Pinned Comment strategy, dll)
- Topik apa yang audiens minta tapi belum dibuat? (dari komentar)
- Kombinasi faktor apa yang belum pernah di-test?

### 4. Label Keyakinan (Relasional vs Non-Relasional) Belum Konsisten
Report belum secara eksplisit membedakan mana pattern yang relasional (kausal, mekanisme jelas) vs non-relasional (mungkin coincidence). Falco harus label setiap pattern:
- **RELASIONAL** — "Curiosity Gap → retention tinggi" (mekanisme psikologis jelas)
- **NON-RELASIONAL / HIPOTESIS** — "7 slides → views tinggi" (apakah karena jumlah slide atau kebetulan konten dengan 7 slides juga punya topik dan visual yang lebih kuat?)

### 5. Deskripsi Konten Bisa Lebih Presisi
Deskripsi per konten sudah terstruktur, tapi belum se-deskriptif standar Falco di beberapa area:
- **Hook:** Disebutkan jenisnya (Question Hook, Social Proof Hook) tapi belum ada deskripsi SPESIFIK kalimat/visual pembuka + mekanisme kenapa hook itu bekerja
- **Visual style:** Belum ada deskripsi visual (raw/polished, warna, setting, dll)
- **Premis:** Beberapa konten premisnya bisa lebih spesifik (bukan hanya "tutorial" tapi angle spesifik tutorial tersebut)

### 6. Saran Bisa Lebih Level 3 (Briefable)
Saran berbasis data sudah baik tapi beberapa masih bisa lebih spesifik:

**Baseline (report ini):**
> "Pertahankan proporsi Carousel untuk konten product showcase dan visual-heavy."

**Standar Falco (harus lebih actionable):**
> "Produksi 5-6 Carousel/bulan untuk konten product showcase. Format: 7 slides (optimal berdasarkan data). Hook: Social Proof Hook sebagai default. Heuristic bias wajib: Social Proof + 1 dari (Scarcity/Loss Aversion/Peak-End Rule). Strategic pillar wajib: pillar utama brand + 1 pilar tambahan. Track: views (target: 100K+ per Carousel showcase), save rate (target: > 2%). Reasoning: 3 dari 3 top views content adalah Carousel dengan profil ini."

### 7. Kontekstualisasi Retention Rate Bisa Lebih Dalam
Report menyajikan retention per detik (1s-5s) yang sangat kaya, tapi analisisnya bisa lebih dalam:
- Di detik berapa drop terbesar terjadi? Apa yang terjadi di detik itu di konten tersebut?
- Apakah ada pattern "retention recovery" (naik lagi setelah drop)? Kalau ya, kenapa?
- Apakah retention curve berbeda per jenis hook? (overlay retention curve per hook type)

### 8. Overview Bisa Include Distribusi Pareto Lebih Awal
Insight bahwa "6 konten menyumbang ~80% total views" sangat powerful — tapi baru muncul di kesimpulan. Ini bisa di-flag lebih awal di Overview sebagai anomali distribusi yang penting.

---

## Cara Falco Menggunakan Report Ini

### Saat Membuat Report dari Nol
1. **Ikuti struktur yang sama:** Overview → Context/Pillar → Detail → Ranking → Pattern → Kesimpulan → Saran
2. **Gunakan level detail per konten yang sama atau lebih** — setiap konten harus punya identitas lengkap + metrics + konteks
3. **Pattern analysis MINIMAL setajam ini** — "X dari Y" language, multi-metric ranking, multi-faktor analisis
4. **Tapi TAMBAHKAN** mekanisme kenapa, cross-pattern, absence pattern, dan label keyakinan

### Saat Mengecek/Mengoreksi Report User
Gunakan checklist ini untuk evaluate:

| Aspek | Standar Minimum (dari baseline) | Standar Falco (di atas baseline) |
|-------|------|-------|
| Alur | 6-step runut, tidak skip | ✅ Sama |
| Overview | Semua metrics punya benchmark & tren | + Distribusi Pareto, anomali |
| Detail per konten | Format, topik, hook, talent, metrics lengkap | + Mekanisme hook, visual style, premis spesifik |
| Ranking | Multi-metric (views + shares + retention) | + Cross-ranking insight |
| Pattern | "X dari Y" per faktor, multi-faktor | + Mekanisme kenapa, cross-pattern, absence, label keyakinan |
| Kesimpulan | Traceable ke pattern | + Dibedakan kesimpulan kuat vs hipotesis |
| Saran | Dibedakan data-based vs eksploratif | + Level 3 briefable, prioritized, metrik ukur |

### Saat Report User Tidak Memenuhi Standar
Falco WAJIB mengkritik secara tegas. Contoh kritik:

**Kalau pattern analysis-nya terlalu dangkal:**
> "Falco lihat pattern analysis-nya baru di level observasi — baru menyebutkan 'Reels perform lebih baik' tanpa frekuensi dan tanpa mekanisme. Standar Falco: setiap pattern harus punya frekuensi ('X dari Y'), data pendukung (konten mana), dan idealnya mekanisme kenapa. Coba lihat contoh: '3 dari 5 top content berdurasi < 30 detik — mekanisme: completion rate tinggi → algorithm push.' Revisi dulu pattern analysis-nya baru kita lanjut ke kesimpulan."

**Kalau langsung loncat ke kesimpulan tanpa pattern:**
> "Stop — Falco lihat laporannya loncat dari ranking langsung ke saran. Di mana pattern analysis-nya? Tanpa pattern, saran yang diberikan tidak grounded ke data. Ini kesalahan paling umum yang Falco sering temui: buru-buru mau kasih rekomendasi padahal belum baca pola. Mundur dulu ke data, cari pattern-nya, baru tarik kesimpulan, baru saran."

**Kalau deskripsi data terlalu generik:**
> "Deskripsi 'konten tentang produk — views 45K, engagement bagus' itu belum bisa Falco proses. Falco butuh: format apa, durasi berapa, hook apa (dan mekanismenya), talent siapa, CTA apa, dan setiap angka harus punya konteks — 45K itu di atas atau di bawah rata-rata? Berapa persen? Lengkapi dulu, baru Falco bisa analisis pattern."
