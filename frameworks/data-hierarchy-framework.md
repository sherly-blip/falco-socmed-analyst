# Data Hierarchy Framework — Dari Angka Mati ke Saran Hidup

## Prinsip Utama

Ini adalah hirarki yang WAJIB dipegang Falco dalam setiap proses analisis. Output analisis **TIDAK BOLEH** berhenti di level bawah. Setiap analisis harus mendorong data naik sampai level tertinggi yang dimungkinkan oleh data yang tersedia.

```
Level 1: DATA MENTAH        → Angka, fakta, metrics tanpa konteks
Level 2: INFORMASI           → Data + konteks (angka yang diberi makna awal)
Level 3: PATTERN             → Pola yang teridentifikasi dari kumpulan informasi
Level 4: INSIGHT             → Mekanisme di balik pattern — "kenapa pola ini terjadi"
Level 5: SARAN               → Tindakan yang harus diambil berdasarkan insight
```

---

## Detail Per Level

### Level 1: Data Mentah (BUKAN OUTPUT — Ini baru bahan baku)
**Apa:** Angka murni, metrics tunggal, fakta tanpa interpretasi.
**Contoh:** "Views: 45.000" / "ER: 3.8%" / "Posting 4x seminggu"
**Status:** Ini BUKAN output analisis. Ini bahan baku yang harus diproses.

### Level 2: Informasi (BOLEH ada di output sebagai pendukung)
**Apa:** Data yang sudah diberi konteks sehingga punya makna awal.
**Contoh:** "Views 45K, di atas rata-rata bulan ini yang 32K, naik 40% dari rata-rata" / "ER 3.8%, turun dari 4.1% bulan lalu"
**Status:** Boleh ada di laporan (di step Overview dan Detail), tapi BUKAN output utama.

### Level 3: Pattern (TARGET MINIMUM Step 4)
**Apa:** Pola yang ditemukan dari kumpulan informasi — kesamaan, korelasi, anomali, atau absence yang teridentifikasi dari data.
**Contoh:** "3 dari 5 top content berdurasi < 30 detik" / "Carousel konsisten punya ER 2x lebih tinggi dari Reels"
**Status:** Ini target minimum di Step 4 Pattern Analysis. Setiap pattern harus di-label frekuensinya ("X dari Y").

### Level 4: Insight (TARGET Step 5 Kesimpulan)
**Apa:** Mekanisme di balik pattern — KENAPA pola ini terjadi. Insight menghubungkan pattern dengan penjelasan kausal atau mekanisme.
**Contoh:** "Durasi pendek (< 30 detik) konsisten perform tinggi karena: (1) completion rate tinggi → signal positif ke algoritma, (2) match dengan attention span audience akun ini yang didominasi Gen Z, (3) lebih shareable karena tidak meminta time investment besar"
**Status:** Ini yang membedakan analyst biasa dari analyst yang punya depth. Tidak semua pattern bisa ditarik ke level insight — dan Falco harus transparent tentang ini.

### Level 5: Saran (TARGET Step 6)
**Apa:** Tindakan konkret yang harus diambil berdasarkan insight. Actionable, spesifik, dan bisa langsung dieksekusi.
**Contoh:** "Produksi 3-4 Reels per minggu dengan durasi 20-35 detik, prioritaskan hook emotional di 3 detik pertama, gunakan Talent A. Track: views, completion rate, share rate."
**Status:** Output akhir yang membuat analisis ACTIONABLE. Harus bisa langsung di-briefkan ke tim.

---

## Cara Naik Level

### Data Mentah → Informasi
**Tambahkan konteks:**
- Bandingkan dengan benchmark (periode sebelumnya, kompetitor, rata-rata industri)
- Berikan kerangka waktu (trend naik/turun/stagnan)
- Berikan kerangka perbandingan (di atas/bawah rata-rata)

### Informasi → Pattern
**Cari pola:**
- Apakah ada faktor yang berulang di minimal 3 data points?
- Apakah ada korelasi antara dua variabel?
- Apakah ada anomali yang menunjukkan sesuatu unexpected?
- Apakah ada absence — sesuatu yang seharusnya ada tapi tidak ada?

### Pattern → Insight
**Jelaskan mekanisme:**
- KENAPA pola ini terjadi? (mekanisme algoritmik, psikologis, sosial)
- Apakah mekanismenya relasional (kausal) atau non-relasional (coincidence)?
- Apakah insight ini bisa diprediksi/direplikasi?

### Insight → Saran
**Terjemahkan ke aksi:**
- Berdasarkan insight, apa yang harus DILAKUKAN? (dengan detail eksekusi)
- Berdasarkan insight, apa yang harus DIHENTIKAN? (dengan reasoning kenapa)
- Berdasarkan insight, apa yang harus DI-TEST? (eksperimental, dengan metrik ukur)
- Prioritaskan: mana yang paling impactful?

---

## Self-Check Level Output

Sebelum finalize output, Falco tanya:

| Pertanyaan | Kalau Jawabannya Ya |
|---|---|
| Apakah output ini masih di level data mentah? | → Tambahkan konteks, naikkan ke informasi |
| Apakah output masih kumpulan informasi tanpa pattern? | → Cari pola, naikkan ke pattern |
| Apakah pattern ini belum ada mekanisme? | → Jelaskan kenapa pola ini terjadi, naikkan ke insight |
| Apakah insight ini belum ada saran? | → Terjemahkan ke aksi spesifik, naikkan ke saran |
| Apakah saran ini masih generik? | → Tambahkan detail eksekusi (apa, bagaimana, berapa, ukur apa) |

---

## Indikator Level Output

| Level | Ciri Kalimat | Status |
|---|---|---|
| Data Mentah | "Views-nya 45.000" | ❌ Belum selesai |
| Informasi | "Views-nya 45K, 40% di atas rata-rata" | ⚠️ Boleh sebagai pendukung |
| Pattern | "3 dari 5 top content berdurasi < 30 detik" | ✅ Minimum di Step 4 |
| Insight | "Durasi pendek perform karena completion rate tinggi yang memicu algorithm push" | ✅ Target di Step 5 |
| Saran | "Produksi 3-4 Reels/minggu, 20-35 detik, hook emotional, Talent A. Track: completion rate" | ✅ Target di Step 6 |

**⚠️ WARNING:** Kalimat "Menurut Falco..." atau "Sepertinya..." → ini masih opini, BUKAN insight. Insight harus ditarik dari data dan pattern, bukan dari pendapat.
