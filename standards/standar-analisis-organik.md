# Standar Analisis Performa Konten Organik

## Kapan Dipakai
- Weekly/bi-weekly/monthly content performance review
- Evaluasi content pillar mana yang perform
- Identifikasi formula konten winning
- Diagnosa kenapa performa turun/naik
- A/B testing analysis (konten reguler vs eksperimental)

## Metrics Wajib Dianalisis

### Primary Metrics (Harus Ada)
| Metric | Definisi | Kenapa Penting |
|--------|---------|---------------|
| Views | Jumlah tampilan konten | Indikator reach/distribusi |
| Reach | Jumlah akun unik yang melihat | Seberapa luas jangkauan |
| Engagement Rate (ER) | (likes+comments+shares+saves)/reach × 100% | Seberapa resonant konten dengan audience |
| Likes | Jumlah likes | Indikator basic approval |
| Comments | Jumlah komentar | Indikator conversation/deeper engagement |
| Shares | Jumlah share | Indikator viral potential — "ini worth spreading" |
| Saves | Jumlah save | Indikator value — "ini worth revisiting" |

### Secondary Metrics (Kalau Tersedia)
| Metric | Definisi | Kenapa Penting |
|--------|---------|---------------|
| Impressions | Total tampilan (termasuk repeated views) | Seberapa sering muncul |
| Completion Rate (video) | % orang yang nonton sampai habis | Indikator content quality & retention |
| Watch Time | Total waktu tonton | Algorithm signal yang kuat |
| Share Rate | Shares/reach × 100% | Indikator shareworthiness (lebih informatif dari angka share mentah) |
| Save Rate | Saves/reach × 100% | Indikator value depth |
| Profile Visits | Kunjungan profil setelah lihat konten | Indikator curiosity/interest |
| Website Clicks | Klik ke link | Indikator conversion intent |
| Followers Growth | Pertumbuhan followers per periode | Indikator brand growth |

### Derived Metrics (Falco Hitung Sendiri Kalau Data Cukup)
- **Average views per konten** — total views / jumlah konten
- **Average ER per format** — ER rata-rata per Reels, Carousel, dll
- **Share rate per konten** — shares / reach × 100%
- **Save rate per konten** — saves / reach × 100%
- **Views distribution** — berapa konten di atas rata-rata, berapa di bawah

## Jumlah Konten & Proporsi Top/Worst

### Jumlah Konten Minimum
- **Minimum 30 konten** per periode untuk analisis yang valid
- 40-50 konten = lebih baik, 70+ = semakin kaya dan akurat
- Kalau < 30 konten: Falco tetap analisis tapi flag bahwa pattern perlu divalidasi

### Proporsi Top & Worst
- **~10% dari total konten** per kategori
- 30 konten → Top 3, Worst 3
- 50 konten → Top 5, Worst 5
- 100 konten → Top 10, Worst 10

### 3 Metrik Default untuk Ranking (WAJIB)
| Metrik | Fungsi | Peran |
|--------|--------|-------|
| **Views** | Output / hasil | Seberapa luas konten terdistribusi |
| **Shares** | Kausal / pendukung | Penyebab views & reach — shareability |
| **Retention Rate** | Kausal / pendukung | Penyebab algorithm push — kualitas hook & konten |

→ Menghasilkan **6 kelompok ranking**: Top by Views + Worst by Views, Top by Shares + Worst by Shares, Top by Retention + Worst by Retention

### Metrik Tambahan (sesuai kebutuhan)
- Comments — kalau objective-nya conversation
- Save rate — kalau objective-nya reference content
- Watch time, conversion, ER — sesuai konteks
- **Prinsip: minimal 3 metrik WAJIB** supaya bisa menjelaskan sebab-akibat, bukan hanya hasil

## Faktor yang Harus Dianalisis
→ Lihat `frameworks/faktor-analisis-checklist.md` bagian "Faktor Konten Organik"

## Benchmark yang Harus Dicari
1. **Internal benchmark:** rata-rata metrics periode sebelumnya (WoW/MoM)
2. **Cross-format benchmark:** rata-rata per format (Reels vs Carousel vs dll)
3. **Cross-pillar benchmark:** rata-rata per content pillar (edukasi vs promosi vs dll)
4. **Industry benchmark (kalau tersedia):**
   - ER rata-rata IG: 1-3% (tergantung tier followers)
   - ER rata-rata TikTok: 3-6% (tergantung tier)
   - Minta ke user kalau ada benchmark industri spesifik

## Alur Analisis
1. **Overview:** Total metrics periode + comparison + anomali + distribusi Pareto
2. **Detail:** Deskripsi per konten (8 layer analyst) + metrics kontekstual
3. **Ranking:** Top [10%] by views + Top [10%] by shares + Top [10%] by retention + Worst per masing-masing + cross-ranking observation
4. **Pattern:** Analisis per faktor per metrik ranking (format, durasi, hook, topik, talent, visual, timing, CTA) + mekanisme + cross-pattern + absence + label keyakinan
5. **Kesimpulan:** Benang merah + traceable ke pattern + label kuat vs hipotesis
6. **Saran:** Level 3 actionable + prioritized + metrik ukur + target

## Khusus A/B Testing Analysis
Kalau ada konten yang sengaja di-A/B test (misalnya: test durasi berbeda, test hook berbeda, test format berbeda):
- **Isolate variabel:** Pastikan hanya 1 variabel yang berbeda antar konten A dan B
- **Compare apple-to-apple:** Konten A dan B harus di-posting dalam kondisi yang comparable (hari mirip, jam mirip, audience overlap)
- **Minimum sample:** Idealnya 3+ pair A/B test untuk conclude
- **Reporting format:** "A vs B: [variabel yang ditest] → A menghasilkan [metrics] vs B [metrics]. Perbedaan: [angka]. Kesimpulan: [A/B lebih baik] karena [reasoning]. Confidence: [tinggi/sedang/rendah berdasarkan jumlah pair]"
