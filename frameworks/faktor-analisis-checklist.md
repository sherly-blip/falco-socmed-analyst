# Faktor Analisis Checklist — Lens per Konteks

## Prinsip Utama

Ini adalah "lens" yang Falco gunakan secara konsisten saat membaca pattern di Step 4 (Pattern Analysis). Falco harus memeriksa faktor-faktor yang RELEVAN sesuai konteks — tidak semua faktor selalu applicable, tapi Falco harus sadar faktor mana yang di-skip dan kenapa.

**Aturan:** Setiap faktor yang dianalisis harus menghasilkan salah satu:
1. **Pattern teridentifikasi** — "X dari Y [top/worst] content punya [kesamaan Z]"
2. **Tidak ada pattern** — "Tidak ditemukan pattern yang konsisten di faktor ini — data terdistribusi merata"
3. **Data tidak cukup** — "Data belum cukup untuk melihat pattern di faktor ini — perlu [data tambahan apa]"

Jangan pernah skip faktor tanpa penjelasan.

---

## Faktor Konten Organik

| Kategori Faktor | Detail yang Dicek | Contoh Pattern Language |
|---|---|---|
| **Format** | Reels/Video, Carousel, Single Image, Story, Live, Thread/Text | "3 dari 5 top content adalah Reels — format ini mendominasi views" |
| **Durasi** (video) | Berapa detik/menit, apakah ada sweet spot, completion rate per durasi | "Sweet spot durasi akun ini: 25-40 detik (completion rate 70%+)" |
| **Topik/Content Pillar** | Pillar apa, sub-topik apa, pilar mana yang konsisten perform | "Pillar edukasi mendominasi top content (4 dari 5), pillar promosi dominasi worst" |
| **Hook** | 3 detik pertama — jenis hook (pertanyaan, statement kontroversial, visual surprise, threat, curiosity gap, identifikasi langsung, dll) + mekanisme psikologis kenapa hook itu bekerja | "Hook berbasis threat/pain point konsisten di top content — mekanisme: memicu urgensi untuk menonton" |
| **Storytelling/Alur** | Struktur narasi (problem-solution, before-after, day-in-life, tutorial, POV, listicle, dll) | "Alur problem-solution perform 2x lebih baik dari alur tutorial murni" |
| **Talent/Karakter** | Siapa yang tampil, karakter seperti apa, apakah konsisten perform, single vs ensemble | "Talent A muncul di 4 dari 5 top content dalam 3 bulan — strong resonance dengan audience" |
| **Visual Style** | Clean/bold/raw/authentic/cinematic/text-heavy, sudut kamera, pencahayaan, setting | "Konten raw/handheld perform lebih baik dari polished studio — selaras dengan preferensi autentisitas" |
| **Audio/Music** | Trending sound, original audio, voiceover, no audio | "Konten dengan voiceover original 2x ER vs trending sound — voice = personal connection" |
| **Caption** | Panjang/pendek, tone, keyword, storytelling di caption, emoji usage | "Caption panjang (storytelling) di Carousel → save rate tinggi. Caption pendek di Reels → tidak berpengaruh signifikan" |
| **CTA** | Jenis CTA (follow, save, comment, link, share), placement, kekuatan | "CTA 'save buat nanti' di Carousel → save rate 3x rata-rata" |
| **Timing** | Hari posting, jam posting | "Pattern belum conclusive — data terdistribusi merata. Perlu test lebih systematic" |
| **Hashtag/SEO** | Jumlah, relevansi, mix (broad vs niche), search visibility | "Konten dengan hashtag niche (5-10) perform lebih baik di reach vs hashtag broad (20+)" |

---

## Faktor Ads/Paid Content

| Kategori Faktor | Detail yang Dicek | Contoh Pattern Language |
|---|---|---|
| **Creative Type** | Image, Video, Carousel, Collection | "Video ads mendominasi CTR (rata-rata 2.3% vs 0.8% image)" |
| **Hook** (video ads) | 3 detik pertama, thumb-stopping factor | "Ads dengan hook pertanyaan → CTR 1.5x vs hook statement" |
| **Headline & Copy** | Pesan utama, angle, urgency, social proof, length | "Headline pendek (< 10 kata) + urgency → CPC 30% lebih rendah" |
| **CTA Button** | Jenis CTA button, kesesuaian dengan objective | "Shop Now vs Learn More — Shop Now punya CPA 20% lebih rendah untuk conversion campaign" |
| **Audience Targeting** | Targeting setting, lookalike, retargeting, custom audience | "Retargeting audience → ROAS 3.2x vs broad targeting ROAS 1.1x" |
| **Placement** | Feed, Story, Reels, Explore, Audience Network, dll | "Reels placement → CPM 40% lebih rendah tapi CTR 15% lebih rendah — net: lebih cost-efficient untuk awareness" |
| **Landing Page** | Kemana diarahkan, kualitas landing page, load time | "Drop-off 60% di landing page — indikasi masalah loading/relevance" |
| **Budget & Bidding** | Alokasi per ad set, strategy bidding, learning phase | "Ad set dengan budget > 500K/hari sudah keluar learning phase — performa stabil" |
| **Frequency** | Berapa kali rata-rata orang melihat ads, ad fatigue signals | "Frequency > 3x → CTR drop 40%. Tanda ad fatigue" |
| **Funnel Position** | TOFU/MOFU/BOFU, warm vs cold audience | "TOFU spend 60% budget tapi hanya 20% conversion — reallocation ke MOFU bisa lebih efisien" |

---

## Faktor KOL/Affiliate

| Kategori Faktor | Detail yang Dicek | Contoh Pattern Language |
|---|---|---|
| **Tier** | Mega, Macro, Micro, Nano | "Micro KOL punya CPE 5x lebih efisien dari Macro — engagement lebih authentic" |
| **Platform** | Instagram, TikTok, YouTube | "KOL TikTok → views lebih tinggi, KOL IG → conversion lebih tinggi" |
| **Niche** | Beauty, lifestyle, food, tech, parenting, dll | "KOL food niche → ER 2x vs lifestyle niche untuk brand F&B ini" |
| **Content Format** | Review, unboxing, tutorial, storytelling, challenge, GRWM, dll | "Format storytelling → share rate 3x vs format review standar" |
| **Brief Compliance** | Sesuai brief atau deviate, kualitas eksekusi | "KOL yang deviate dari brief (lebih personal) justru perform 2x — over-briefing menurunkan autentisitas?" |
| **Audience Response** | Sentiment komentar, buying signals, pertanyaan tentang produk | "KOL C punya 30% komentar berisi buying signals vs KOL A hanya 5% — audience quality berbeda" |
| **Cost per Result** | CPR, CPE, CPC, CPA per KOL | "KOL D paling cost-efficient: CPA Rp 15K vs rata-rata Rp 45K" |
| **Posting Timing** | Kapan KOL posting, seberapa cepat setelah brief | "Posting di jam prime time KOL sendiri → reach 2x vs posting di jam yang kita tentukan" |

---

## Faktor Liveshopping

| Kategori Faktor | Detail yang Dicek | Contoh Pattern Language |
|---|---|---|
| **Durasi Live** | Total durasi, apakah ada sweet spot | "Live 2-3 jam → GMV tertinggi. Live > 4 jam → GMV per jam menurun (viewer fatigue)" |
| **Host/Talent** | Siapa, karakter, engagement style, product knowledge | "Host B → conversion rate 2x Host A. Perbedaan utama: Host B lebih interaktif menjawab pertanyaan" |
| **Waktu Mulai** | Hari dan jam mulai | "Live jam 19-21 → peak viewers 3x vs live jam 14-16" |
| **Produk** | Jumlah produk, urutan showcase, hero product | "Hero product di 30 menit pertama → 40% total GMV. Di akhir → hanya 15% GMV" |
| **Offering/Promo** | Diskon, flash deal, free gift, bundling | "Flash deal setiap 30 menit → viewers retention naik 25%" |
| **Interaksi** | Cara host engage penonton, games, Q&A, shout-out | "Sesi Q&A produk → add-to-cart spike 40% dalam 5 menit setelah Q&A" |
| **Traffic Source** | Organic discovery, ads, social media push, notification | "Sesi dengan ads pre-live → peak viewers 2x vs organic-only" |
| **Conversion Funnel** | Viewer → click → add to cart → checkout → paid, drop-off per step | "Drop-off terbesar: add to cart → checkout (55%). Kemungkinan: friction di checkout flow" |

---

## Faktor Kompetitor/Creator

| Kategori Faktor | Detail yang Dicek | Contoh Pattern Language |
|---|---|---|
| **Posting Frequency** | Berapa konten per minggu/bulan | "Kompetitor A posting 5x/minggu vs brand kita 3x — tapi ER kompetitor A lebih rendah" |
| **Content Mix** | Proporsi format (Reels/Carousel/dll) | "Kompetitor A heavy Reels (80%), kita balanced — apakah fokus Reels bisa boost reach?" |
| **Content Pillar** | Pilar apa yang mereka mainkan | "Kompetitor A tidak punya pillar edukasi — ini gap yang bisa kita isi" |
| **Top Content Pattern** | Konten mereka yang paling perform, kenapa | "3 dari 5 top content kompetitor A = UGC/testimonial — strategi social proof" |
| **Engagement Quality** | Tipe komentar, sentiment, buying signals | "Komentar kompetitor A 70% emoji/short — komentar brand kita 40% pertanyaan — audience kita lebih engaged" |
| **Growth Trajectory** | Followers growth trend, apakah naik/turun/stagnan | "Kompetitor A tumbuh 8K/bulan vs kita 2.3K — gap signifikan di reach strategy" |
| **Visual Identity** | Konsistensi visual, recognizability | "Kompetitor A punya visual identity sangat konsisten — brand kita berubah-ubah setiap bulan" |
| **Tone & Voice** | Konsistensi tone, differentiasi | "Kompetitor A casual-playful, kompetitor B formal-authority — kita di mana?" |

---

## Cara Menggunakan Checklist Ini

### Saat Full Analysis (Monthly)
- Scan SEMUA faktor yang relevan untuk konteks analisis
- Setiap faktor harus menghasilkan output: pattern teridentifikasi / tidak ada pattern / data tidak cukup
- Prioritaskan faktor yang menunjukkan pattern paling kuat

### Saat Quick Analysis (Weekly)
- Fokus pada 5-7 faktor yang PALING MENCOLOK
- Skip faktor yang tidak menunjukkan perubahan dari minggu lalu
- Tapi tetap flag kalau ada faktor baru yang muncul

### Saat Deep Dive
- Fokus pada 1-3 faktor yang diminta user untuk di-dalami
- Cross-reference dengan faktor lain: apakah ada kombinasi yang menarik?

### Prinsip Adaptif
Daftar faktor di atas adalah CONTOH yang sudah teruji, BUKAN daftar tertutup. Kalau Falco menemukan faktor baru yang berpengaruh (misalnya: kolaborasi dengan brand lain, UGC yang di-repost, timing relatif terhadap competitor posting), tambahkan ke analisis dan jelaskan kenapa faktor ini relevan.
