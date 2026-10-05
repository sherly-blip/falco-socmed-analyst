# Standar Deskripsi Data & Konten dalam Analisis

## Prinsip Utama

⚠️ **FILE INI WAJIB DIBACA setiap kali Falco mendeskripsikan konten atau data dalam output analisis.**

Dalam konteks analisis performa, setiap konten dan data point harus dideskripsikan dengan presisi yang cukup untuk:
1. Pembaca bisa **memahami konten tanpa melihat langsung**
2. Pattern analysis bisa dilakukan dengan **faktor yang teridentifikasi jelas**
3. Saran yang dihasilkan bisa **spesifik dan actionable**

**Prinsip:** Deskripsi yang generik menghasilkan pattern yang dangkal, yang menghasilkan kesimpulan yang lemah, yang menghasilkan saran yang tidak actionable. **Presisi di deskripsi = presisi di analisis.**

---

## Standar Deskripsi Konten dalam Analisis (8 Layer Analyst)

Diadaptasi dari standar deskripsi berlapis yang biasa digunakan dalam riset konten — disesuaikan untuk konteks **analisis performa**. Falco tidak perlu se-mendalam researcher di setiap layer (karena fokus Falco adalah performa, bukan riset mendalam tentang konten itu sendiri), tapi presisi dasar harus terjaga.

### Layer 1: Identitas Konten
**Yang harus ada:**
- Format teknis: Reels, Carousel, Single Image, Story, dll
- Durasi (kalau video): dalam detik/menit
- Tanggal posting
- Content pillar/kategori

❌ "Konten video di Instagram"
✅ "Reels 28 detik, di-posting 12 Maret 2025, pillar edukasi"

### Layer 2: Premis/Topik
**Yang harus ada:**
- Inti konten — tentang APA secara spesifik
- Angle/sudut pandang — dari perspektif apa

❌ "Konten tentang skincare"
✅ "Carousel 7 slide tentang 5 kesalahan skincare routine untuk kulit berminyak — angle: common mistakes yang sering tidak disadari"

### Layer 3: Hook
**Yang harus ada:**
- Deskripsi 3 detik pertama (atau slide pertama untuk Carousel)
- Mekanisme psikologis hook: kenapa ini bikin orang stop scroll?

Mekanisme hook yang umum:
- **Curiosity gap** — memicu rasa penasaran
- **Threat/pain point** — memicu rasa terancam atau "aku harus tahu ini"
- **Pertanyaan langsung** — memicu keinginan menjawab
- **Kontras/ketidakselarasan** — dua hal yang harusnya tidak nyambung
- **Visual surprise** — sesuatu yang tidak terduga secara visual
- **Identifikasi langsung** — "ini gue banget" moment
- **Aspirasi** — sesuatu yang orang inginkan
- **Statement kontroversial** — memicu keinginan untuk agree/disagree

❌ "Hook-nya menarik"
✅ "Hook: pertanyaan langsung di 3 detik pertama — 'Kamu cuci muka pakai air panas? Stop.' Mekanisme: threat/ancaman + identifikasi langsung (banyak orang melakukan ini)"

### Layer 4: Talent/Karakter
**Yang harus ada:**
- Siapa yang tampil (atau tidak ada talent)
- Karakter/perannya — presentasi seperti apa

❌ "Ada talent"
✅ "Talent A, bicara langsung ke kamera, tone casual-authority (seperti teman yang expert)"

### Layer 5: Visual & Eksekusi
**Yang harus ada:**
- Style visual: clean/raw/cinematic/text-heavy/dll
- Elemen eksekusi kunci: text overlay, transisi, lighting, setting

❌ "Visual yang bagus"
✅ "Visual clean studio lighting, text overlay per poin, transisi cut cepat antar poin, produk muncul 2x sebagai prop"

### Layer 6: CTA
**Yang harus ada:**
- Jenis CTA: follow, save, comment, share, link, beli
- Placement: di mana CTA muncul
- Atau: tidak ada CTA eksplisit

❌ "Ada CTA"
✅ "CTA 'Save buat reminder' di frame terakhir + 'Tag teman yang butuh ini' di caption"

### Layer 7: Metrics (Lengkap + Kontekstual)
**Yang harus ada:**
- Semua metrics yang tersedia: views, reach, likes, comments, shares, saves, ER, completion rate, dll
- Kontekstualisasi: setiap angka di-frame — di atas/bawah rata-rata, naik/turun vs periode sebelumnya

❌ "Views 45K, likes 2K"
✅ "Views 45K (40% di atas rata-rata bulan ini 32K), likes 2.1K, comments 340, shares 890 (share rate 2% — 2.5x rata-rata akun 0.8%), saves 1.5K (save rate 3.3% — 2.7x rata-rata). ER 10.7% (2.8x rata-rata bulan ini 3.8%)"

### Layer 8: Konteks Khusus
**Yang harus ada (kalau relevan):**
- Apakah konten ini bagian dari campaign?
- Apakah ada faktor eksternal? (trending moment, hari libur, ads boost)
- Apakah ada anomali yang perlu di-note?

❌ (skip tanpa penjelasan)
✅ "Konten ini di-posting bersamaan dengan trending topic skincare di TikTok — kemungkinan mendapat boost dari search traffic"
ATAU: "Tidak ada faktor eksternal khusus yang teridentifikasi"

---

## Standar Deskripsi Ads dalam Analisis

Per ads creative/ad set/campaign:

| Elemen | Yang Harus Ada |
|--------|---------------|
| Creative type | Image/Video/Carousel/Collection |
| Hook (video) | 3 detik pertama + mekanisme |
| Headline & copy | Pesan utama, angle, ada urgency/social proof? |
| CTA button | Jenis (Shop Now, Learn More, dll) |
| Audience | Targeting: broad/lookalike/retargeting/custom |
| Placement | Feed/Story/Reels/Explore/dll |
| Metrics | Impressions, reach, CTR, CPC, CPM, CPA, ROAS — semua dikontekskan |
| Budget | Berapa allocated, sudah keluar learning phase? |

---

## Standar Deskripsi KOL dalam Analisis

Per KOL:

| Elemen | Yang Harus Ada |
|--------|---------------|
| Identitas | Nama/username, tier (mega/macro/micro/nano), followers, platform |
| Niche | Beauty/lifestyle/food/tech/dll |
| Content format | Review/unboxing/tutorial/storytelling/dll |
| Brief compliance | Sesuai brief atau deviate? Kalau deviate, di bagian mana? |
| Metrics | Reach, views, ER, link clicks, kode promo usage, attributed sales — dikontekskan |
| Cost efficiency | CPR, CPE, CPC, CPA — dibandingkan dengan KOL lain |
| Audience response | Sentiment komentar, buying signals, pertanyaan tentang produk |

---

## Standar Deskripsi Live dalam Analisis

Per sesi live:

| Elemen | Yang Harus Ada |
|--------|---------------|
| Identitas | Tanggal, platform, durasi |
| Host/talent | Siapa, karakter, engagement style |
| Waktu | Hari + jam mulai |
| Produk | Jumlah produk, hero product, urutan showcase |
| Offering | Diskon, flash deal, free gift, bundling |
| Metrics | Total viewers, peak viewers, avg watch time, engagement, products clicked, ATC, transactions, GMV — dikontekskan |
| Conversion funnel | Viewer → click → ATC → checkout — di mana drop-off? |

---

## Prinsip Adaptif

Daftar di atas adalah standar MINIMUM. Falco harus adaptif:
- Kalau ada elemen tambahan yang relevan untuk analisis → tambahkan
- Kalau ada elemen yang benar-benar tidak tersedia datanya → flag: "data [X] tidak tersedia — analisis di area ini terbatas"
- Jangan pernah skip elemen tanpa penjelasan — selalu note apa yang tersedia dan apa yang tidak

**Tujuan akhir:** Setiap konten/item yang dideskripsikan dalam analisis Falco harus **cukup presisi** sehingga:
1. Pattern analysis bisa dilakukan dengan benar (faktor-faktor teridentifikasi)
2. Pembaca tahu persis konten mana yang perform dan kenapa
3. Saran yang dihasilkan bisa spesifik (karena detail faktor sudah jelas)
