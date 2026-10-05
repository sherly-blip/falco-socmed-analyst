# Metrics Glossary — Definisi Metrics per Platform

## Tujuan
Konsistensi terminologi. Falco harus menggunakan definisi yang tepat saat menganalisis dan menjelaskan metrics ke user.

---

## Universal Metrics

| Metric | Definisi | Catatan |
|--------|---------|--------|
| **Views** | Jumlah kali konten dilihat/ditonton | Definisi "view" berbeda per platform (lihat di bawah) |
| **Reach** | Jumlah akun UNIK yang melihat konten | 1 orang = 1 reach, walau lihat berkali-kali |
| **Impressions** | Total berapa kali konten DITAMPILKAN | 1 orang bisa = beberapa impressions |
| **Engagement** | Interaksi aktif dengan konten | Likes + comments + shares + saves (definisi bisa bervariasi) |
| **Engagement Rate (ER)** | Persentase engagement terhadap reach/followers | Formula bervariasi — selalu jelaskan formula yang dipakai |
| **Likes** | Jumlah likes/hearts | Basic approval signal |
| **Comments** | Jumlah komentar | Deeper engagement signal |
| **Shares** | Jumlah kali konten di-share | Viral potential signal |
| **Saves** | Jumlah kali konten di-save/bookmark | Value/reference signal |
| **Followers** | Jumlah pengikut akun | Ukuran audience base |
| **Followers Growth** | Perubahan jumlah followers per periode | Growth trajectory |

---

## Platform-Specific: Instagram

| Metric | Definisi IG |
|--------|------------|
| Views (Reels) | Jumlah kali Reels diputar (termasuk autoplay) |
| Views (Story) | Jumlah akun yang melihat Story |
| Reach | Jumlah akun unik yang melihat konten di feed, Story, Reels, atau Explore |
| Impressions | Total tampilan (reach × frekuensi) |
| ER Formula | (Likes + Comments + Shares + Saves) / Reach × 100% |
| ER Alternatif | (Likes + Comments) / Followers × 100% — lebih mudah dihitung dari luar |
| Completion Rate | % viewers yang menonton Reels sampai habis |
| Share Rate | Shares / Reach × 100% |
| Save Rate | Saves / Reach × 100% |
| Profile Visits | Kunjungan ke profil dari konten |
| Website Clicks | Klik ke link di bio dari konten |

## Platform-Specific: TikTok

| Metric | Definisi TikTok |
|--------|----------------|
| Views | Jumlah kali video diputar (termasuk replay) |
| Reach | Tidak langsung tersedia — estimasi dari views |
| ER Formula | (Likes + Comments + Shares + Saves) / Views × 100% |
| Completion Rate | % viewers yang menonton sampai habis |
| Average Watch Time | Rata-rata durasi tonton per viewer |
| For You Page (FYP) | Distribusi ke halaman FYP — indikator algorithm push |
| Profile Visits | Kunjungan ke profil dari konten |

## Platform-Specific: YouTube

| Metric | Definisi YouTube |
|--------|-----------------|
| Views | Jumlah kali video ditonton (dihitung setelah ~30 detik) |
| Watch Time | Total jam tonton — metric terpenting YouTube |
| Average View Duration | Rata-rata durasi tonton per viewer |
| CTR Thumbnail | Click-through rate dari thumbnail di browse/search |
| Subscribers gained | Subscribers baru dari konten |
| Impressions | Jumlah kali thumbnail ditampilkan |

---

## Ads-Specific Metrics

| Metric | Definisi | Platform |
|--------|---------|---------|
| CTR | Click-through rate: clicks / impressions × 100% | All |
| CPC | Cost per click: total spend / clicks | All |
| CPM | Cost per mille: cost per 1000 impressions | All |
| CPA | Cost per acquisition: total spend / conversions | All |
| ROAS | Return on ad spend: revenue / ad spend | All |
| Frequency | Average impressions per person | Meta |
| ThruPlay | Video views ≥15 sec or completed | Meta |
| Cost per ThruPlay | Total spend / ThruPlays | Meta |

---

## Catatan Penting Falco

1. **ER formula harus SELALU disebutkan** — "ER 4.2% (dihitung dari likes+comments+shares+saves / reach)" — karena formula berbeda menghasilkan angka berbeda
2. **Views ≠ Reach** — satu orang bisa nonton berkali-kali. Views bisa lebih tinggi dari reach.
3. **Impressions ≠ Reach** — impressions selalu ≥ reach (satu orang bisa melihat beberapa kali)
4. **Share rate dan save rate lebih informatif dari angka mentah** — 1000 shares dari reach 10K (10% share rate) lebih impresif dari 5000 shares dari reach 1M (0.5% share rate)
5. **ER dari followers vs dari reach** — ER dari followers cenderung lebih rendah (karena tidak semua followers melihat). ER dari reach lebih akurat tapi tidak selalu tersedia dari luar.
