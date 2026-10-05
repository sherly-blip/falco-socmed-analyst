# Standar Analisis Performa Ads/Paid Content

## Kapan Dipakai
- Campaign ads performance review (mid-campaign atau post-campaign)
- Evaluasi creative mana yang paling cost-efficient
- Optimasi ongoing campaign
- A/B testing analysis untuk ads creative
- Post-campaign analysis & learning extraction

## Metrics Wajib Dianalisis

### Awareness Metrics
| Metric | Definisi | Kenapa Penting |
|--------|---------|---------------|
| Impressions | Total tampilan ads | Seberapa sering muncul |
| Reach | Jumlah orang unik yang melihat | Seberapa luas |
| Frequency | Rata-rata berapa kali per orang | Ad fatigue signal |
| CPM | Cost per 1000 impressions | Efisiensi awareness |

### Engagement/Traffic Metrics
| Metric | Definisi | Kenapa Penting |
|--------|---------|---------------|
| CTR | Click-through rate (clicks/impressions) | Seberapa compelling ads |
| CPC | Cost per click | Efisiensi traffic |
| Video Views | Jumlah views video ads | Reach video |
| ThruPlay | Video ditonton >15 detik atau selesai | Kualitas view |

### Conversion Metrics
| Metric | Definisi | Kenapa Penting |
|--------|---------|---------------|
| Conversions | Jumlah conversion (purchase, lead, dll) | Tujuan akhir |
| CPA | Cost per acquisition/conversion | Efisiensi conversion |
| ROAS | Return on Ad Spend | ROI ads |
| Conversion Rate | Conversions/clicks | Landing page effectiveness |

### Funnel Metrics (Kalau Data Tersedia)
| Step | Metric | Drop-off Analysis |
|------|--------|-------------------|
| Impression → Click | CTR | < 1% = creative lemah |
| Click → Landing | Bounce rate | > 70% = landing page issue |
| Landing → Add to Cart | ATC rate | Kalau rendah = product/price/UX issue |
| ATC → Purchase | Purchase rate | Kalau rendah = checkout friction |

## Faktor yang Harus Dianalisis
→ Lihat `frameworks/faktor-analisis-checklist.md` bagian "Faktor Ads/Paid Content"

## Alur Analisis Ads

### Overview
- Total spend vs total result
- Overall ROAS/CPA
- Comparison dengan campaign sebelumnya (kalau ada)
- Budget utilization: apakah budget habis? Learning phase sudah selesai?

### Detail Breakdown
Per ad set / per creative:
- Creative type, hook, headline, CTA, audience, placement
- Semua metrics: impressions, reach, CTR, CPC, CPM, CPA, ROAS
- Kontekstualisasi: masing-masing dibanding rata-rata campaign

### Ranking
- Top creative by CTR (mana yang paling compelling)
- Top creative by ROAS (mana yang paling profitable)
- Top audience by CPA (audience mana yang paling efisien)
- Worst performers + reasoning

### Pattern Analysis
- Pattern creative: creative type mana yang perform? Hook apa? Headline apa?
- Pattern audience: audience segment mana yang respond?
- Pattern placement: placement mana yang paling efisien?
- Pattern funnel: di mana drop-off terbesar? Kenapa?
- Ad fatigue signals: creative mana yang sudah fatigue (CTR menurun seiring waktu)?

### Kesimpulan
- Creative formula yang work vs yang tidak
- Audience insight: siapa yang respond paling baik
- Budget efficiency: di mana spend paling efisien
- Funnel bottleneck: di mana harus diperbaiki

### Saran
- Creative optimization: apa yang harus diubah, dibuat baru, dihentikan
- Budget reallocation: bagaimana realokasi budget berdasarkan data
- Audience optimization: audience mana yang di-scale, mana yang di-cut
- Funnel fix: apa yang harus diperbaiki di setiap stage
- A/B test recommendations: apa yang perlu di-test selanjutnya

## Khusus Mid-Campaign Optimization
Kalau analisis dilakukan di tengah campaign (masih running):
- Fokus pada **quick wins** — apa yang bisa diubah sekarang
- Identify **underperformers** — matikan atau adjust
- Identify **outperformers** — scale budget
- Budget reallocation recommendation — dari mana ke mana, berapa
- Timeline: kapan harus review lagi
