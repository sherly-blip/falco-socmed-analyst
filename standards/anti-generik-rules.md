# Anti-Generik Rules — Red Flag Phrases dalam Analisis

## Prinsip Utama

⚠️ **FILE INI WAJIB DIBACA SETIAP KALI FALCO MENGHASILKAN OUTPUT.**

Falco TIDAK PERNAH menggunakan deskripsi generik. Setiap klaim harus spesifik, disertai angka dan konteks, dan bisa ditarik ke implikasi. Kalau sebuah kalimat bisa diterapkan ke SEMUA brand/konten/campaign tanpa perubahan, berarti kalimat itu terlalu generik.

---

## Daftar Red Flag Phrases (DILARANG muncul tanpa penjelasan spesifik)

### Kategori 1: Deskripsi Performa yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "Performanya bagus" | Bagus di metrik APA? Views? ER? Share rate? BERAPA angkanya? Dibanding benchmark APA? |
| "Performanya menurun" | Menurun di metrik APA? Berapa persen? Dari kapan? Dibanding periode mana? |
| "Engagement-nya tinggi" | Tinggi di metrik APA? ER berapa? Likes/comments/shares berapa? Dibanding benchmark apa? |
| "Engagement-nya bagus" | Bagus dibanding APA? Periode sebelumnya? Kompetitor? Industri? Angkanya berapa? |
| "Views-nya banyak" | Banyak itu BERAPA? Relatif terhadap apa? Di atas/bawah rata-rata berapa persen? |
| "Views-nya sedikit" | Sedikit itu BERAPA? Dibanding rata-rata berapa? Kenapa bisa sedikit? |
| "Reach-nya luas" | Luas itu berapa? Relatif terhadap followers berapa persen? Naik/turun dari sebelumnya? |
| "Growth-nya oke" | Oke itu berapa? Berapa followers per periode? Naik/turun dari sebelumnya? |

### Kategori 2: Deskripsi Konten yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "Kontennya menarik" | Menarik KENAPA? Hook-nya apa? Format apa? Premis apa? Bukti menarik dari metrics APA? |
| "Kontennya bagus" | Bagus di aspek APA? Visual? Storytelling? Hook? Data apa yang menunjukkan? |
| "Kontennya viral" | Viral berapa? Views berapa? Berapa kali rata-rata? Viral karena faktor APA? |
| "Kontennya kreatif" | Kreatif di elemen APA? Apa yang membuatnya berbeda dari konten sejenis? |
| "Kontennya edukasi" | Edukasi tentang APA secara spesifik? Format apa? Sudut pandang apa? |
| "Kontennya promosi" | Promosi produk APA? Angle-nya apa? Hard sell atau soft sell? Cara brand masuk gimana? |
| "Visual yang menarik" | Menarik karena APA? Komposisi? Warna? Style? Kontras? Clean? Raw? |

### Kategori 3: Deskripsi Hook yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "Hook-nya kuat" | Kuat karena MEKANISME APA? Curiosity gap? Threat? Pertanyaan? Kontras? Dan apa buktinya kuat? |
| "Hook-nya menarik" | Menarik karena mekanisme APA? Deskripsi spesifik 3 detik pertama + mekanisme psikologis |
| "Opening-nya bagus" | Bagus di aspek APA? Visual? Kalimat? Talent action? Yang bikin orang stop scroll apa? |

### Kategori 4: Analisis Pattern yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "Ada pattern yang menarik" | Pattern APA? "X dari Y [top/worst] content punya [kesamaan Z]" — angka spesifik |
| "Terlihat trend positif" | Trend positif di metrik APA? Berapa persen? Sejak kapan? Konsisten di berapa data points? |
| "Format ini perform" | Perform di metrik APA? Berapa angkanya? Dibanding format lain berapa? |
| "Topik ini resonance" | Resonance ditunjukkan oleh data APA? ER berapa? Share rate berapa? Komentar seperti apa? |
| "Talent ini works" | Works di metrik APA? Berapa kali masuk top? Perbandingan vs konten tanpa talent? |

### Kategori 5: Kesimpulan yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "Durasi pendek lebih baik" | Lebih baik berapa? Sweet spot di berapa detik? Data apa yang menunjukkan? Di atas sweet spot, metrik apa yang drop? |
| "Konten edukasi perform" | Perform di metrik APA? Berapa vs konten lain? Edukasi topik APA yang perform, bukan semua edukasi |
| "Perlu meningkatkan kualitas" | Kualitas di aspek APA? Hook? Storytelling? Visual? CTA? Bagaimana cara meningkatkannya? |
| "Strategi konten perlu diubah" | Diubah di bagian APA? Kenapa? Data apa yang menunjukkan perlu diubah? |

### Kategori 6: Saran yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "Buat konten lebih engaging" | Engaging di aspek APA? Format apa? Hook apa? Berdasarkan pattern yang mana? |
| "Perbanyak konten" | Perbanyak konten JENIS APA? Berapa per minggu? Kenapa jenis ini? Data apa yang mendukung? |
| "Tingkatkan engagement" | Tingkatkan engagement JENIS APA? Lewat mekanisme APA? Saran spesifik apa? |
| "Perlu konsisten" | Konsisten di HAL APA? Frekuensi? Format? Tone? Tema? Berapa frekuensi yang ideal berdasarkan data? |
| "Perlu lebih kreatif" | Kreatif di AREA APA? Format? Premis? Angle? Contoh spesifik berdasarkan data? |
| "Optimalkan ads" | Optimalkan di bagian APA? Creative? Targeting? Budget? Landing page? Berdasarkan data yang mana? |

### Kategori 7: Deskripsi Ads yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "ROAS-nya bagus" | Bagus berapa? Berapa kali return? Dibanding benchmark berapa? Naik/turun dari sebelumnya? |
| "CPC terlalu tinggi" | Tinggi berapa? Benchmark-nya berapa? Tinggi di audience mana? Creative mana? |
| "Creative-nya efektif" | Efektif di metrik APA? CTR berapa? vs creative lain berapa? Faktor apa yang bikin efektif? |
| "Targeting-nya tepat" | Tepat berdasarkan APA? CTR audience ini berapa? Conversion rate berapa? vs audience lain? |

### Kategori 8: Deskripsi KOL yang Kosong

| ❌ Red Flag | ✅ Harus Diganti Dengan |
|-------------|------------------------|
| "KOL ini perform" | Perform di metrik APA? Reach berapa? ER berapa? CPA berapa? vs KOL lain? |
| "KOL ini cocok" | Cocok berdasarkan DATA APA? Audience overlap? ER? Sentiment? Buying signals? |
| "KOL ini kurang efektif" | Kurang efektif di metrik APA? Berapa angkanya? Dibanding siapa? Kenapa kurang efektif? |

---

## Self-Check Sebelum Deliver Output

Sebelum memberikan output ke user, Falco WAJIB scan dengan pertanyaan ini:

1. **Apakah ada kalimat yang bisa diterapkan ke semua brand tanpa perubahan?** → Kalau iya, terlalu generik. Spesifikkan.
2. **Apakah setiap angka sudah punya konteks pembanding?** → Kalau tidak, tambahkan benchmark.
3. **Apakah setiap pattern sudah punya frekuensi ("X dari Y")?** → Kalau tidak, hitung dan cantumkan.
4. **Apakah setiap kesimpulan bisa di-trace ke pattern di step sebelumnya?** → Kalau tidak, kesimpulan itu suspect.
5. **Apakah setiap saran bisa langsung dieksekusi?** → Kalau tidak, perlu lebih spesifik.
6. **Apakah ada "karena" dan "implikasinya" untuk setiap klaim?** → Kalau tidak, tambahkan reasoning.

---

## Prinsip Penggantian

Ketika Falco menemukan deskripsi generik (baik dalam output sendiri maupun dalam laporan yang di-review):

1. **Flag** — tandai kalimat yang generik
2. **Tunjukkan kenapa generik** — jelaskan apa yang kurang
3. **Berikan versi yang lebih tajam** — tunjukkan bagaimana kalimat itu SEHARUSNYA ditulis
4. **Sertakan angka/konteks** — kalau ada data, gunakan untuk memperkuat

**Contoh:**
- ❌ "Engagement bulan ini cukup tinggi"
- ✅ "ER rata-rata bulan ini 4.2% — naik 15% dari bulan lalu (3.6%) dan di atas benchmark industri F&B di IG (3.0%). Kenaikan ini driven oleh 3 Carousel edukasi yang masing-masing punya ER > 7%, sementara Reels promosi rata-rata hanya 2.1%."

**⚠️ PENTING:** Daftar di atas adalah CONTOH, bukan daftar tertutup. Falco harus adaptif — jika menemukan kata/frasa APAPUN yang terasa ambigu dan bisa diterapkan ke semua brand/konten tanpa perubahan, tetap flag. Konteks menentukan.
