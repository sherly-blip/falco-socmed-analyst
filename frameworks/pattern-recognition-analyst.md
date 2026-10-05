# Pattern Recognition Framework — Untuk Analyst

## Prinsip Utama

Pattern recognition adalah **skill inti** yang membedakan analyst yang hanya compile angka dari analyst yang melihat insight di balik angka. Analisis yang baik bukan menyajikan data satu per satu, tapi **mencari POLA** — pola dari performa, pola dari faktor konten, pola dari timing, pola dari audience behavior.

**Pola = insight yang bisa direplikasi atau dihindari.**

---

## 4 Jenis Pola yang Dicari

### 1. Recurring Pattern (Pola Berulang)
Faktor yang muncul **MINIMAL di 3 data points** berbeda secara konsisten.

**Cara menemukan:**
- Setelah ranking top dan worst, cek: apa kesamaan di antara top? Apa kesamaan di antara worst?
- Hitung frekuensi: "X dari Y [top/worst] content punya [kesamaan]"

**Contoh:**
- "3 dari 5 top content berdurasi di bawah 30 detik"
- "4 dari 5 worst content tidak punya hook di 3 detik pertama"
- "Semua top content bulan ini menampilkan Talent A"

**Tingkat keyakinan:**
- 3 dari 5 = pattern moderat, worth noting
- 4 dari 5 = pattern kuat, confident
- 5 dari 5 = pattern sangat kuat, tingkat keyakinan tinggi

### 2. Correlation Pattern (Pola Korelasi)
Hubungan antara **dua variabel** yang konsisten terlihat.

**Cara menemukan:**
- Cari pasangan faktor yang selalu muncul bersamaan di top/worst content
- Cross-tabulate: apakah faktor A + faktor B selalu menghasilkan performa tinggi?

**Contoh:**
- "Reels dengan talent + durasi < 30 detik → selalu masuk top 5 (3 dari 3 bulan terakhir)"
- "Carousel + CTA save → save rate 3x rata-rata"
- "Konten di-posting jam 7 AM + hari kerja → completion rate lebih tinggi"

**⚠️ PENTING — Korelasi ≠ Kausalitas:**
Falco harus **selalu transparent** — "data menunjukkan korelasi antara X dan Y, tapi belum tentu kausalitas. Perlu di-test secara isolated untuk konfirmasi."

**Cara membedakan:**
- **Relasional (kemungkinan kausal):** Ada mekanisme logis yang menghubungkan (durasi pendek → completion rate tinggi → algorithm push → views tinggi — mekanismenya jelas)
- **Non-relasional (mungkin coincidence):** Tidak ada mekanisme logis yang obvious (posting Rabu → views tinggi — kenapa Rabu? Belum jelas)

### 3. Anomaly Pattern (Pola Anomali)
Sesuatu yang **BERBEDA dari mayoritas** — ini sering jadi insight paling menarik dan unexpected.

**Cara menemukan:**
- Cari outlier: data point yang jauh di atas atau di bawah rata-rata
- Cari kontradiksi: konten yang seharusnya perform baik tapi tidak, atau sebaliknya
- Tanya: "apa yang BERBEDA dari konten ini dibanding yang lain?"

**Contoh:**
- "Konten #7 dapat 189K views (5x rata-rata) — outlier signifikan. Apa yang membedakan?"
- "Dari 15 konten Reels, hanya 1 yang gagal — dan yang gagal justru yang paling high-production. Apakah raw/authentic lebih resonance?"
- "KOL terkecil (followers 10K) justru punya CPA terendah — audience quality > audience size?"

**Cara menangani anomali:**
1. **Identifikasi** — tandai bahwa ini anomali, bukan pattern
2. **Analisis** — cari faktor pembeda: apa yang unik dari anomali ini?
3. **Hipotesis** — buat hipotesis kenapa anomali terjadi
4. **Rekomendasi** — apakah anomali ini worth di-replicate/test?
5. **Label** — tandai sebagai "hipotesis, bukan pattern — perlu validasi"

### 4. Absence Pattern (Pola Ketidakhadiran)
Sesuatu yang **SEHARUSNYA ADA tapi TIDAK ADA** — ini sering jadi peluang terbesar.

**Cara menemukan:**
- Cek checklist faktor: ada faktor yang belum pernah dicoba/digunakan?
- Cek data historis: ada format/topik/approach yang belum pernah di-test?
- Cek vs kompetitor: ada hal yang kompetitor lakukan tapi brand ini tidak?
- Cek vs audience demand: ada yang audiens minta tapi belum dibuat?

**Contoh:**
- "Dalam 3 bulan terakhir, brand belum pernah membuat konten storytelling — semua informatif/edukatif. Apakah storytelling bisa jadi untapped format?"
- "Tidak ada konten yang memanfaatkan trending audio — padahal di akun kompetitor, konten trending audio perform 2x rata-rata"
- "Belum pernah test Carousel dengan CTA 'share ke teman' — padahal share rate adalah blind spot akun ini"
- "Tidak ada konten yang tampilkan user/customer — UGC/testimonial belum dicoba"

---

## Metode Mencari Pola

### Step 1: Siapkan Data yang Cukup
- Pola TIDAK bisa dilihat dari 1-2 data points. Minimum:
  - Weekly analysis: 5-10 konten
  - Bi-weekly: 10-20 konten
  - Monthly: 15-30 konten
  - Kalau data kurang dari minimum, Falco harus flag: "dengan [N] data points, pattern belum bisa di-validate secara kuat"

### Step 2: Tag Setiap Data Point
- Beri label per faktor: format, durasi, hook type, topic, talent, visual, timing, CTA
- Kelompokkan berdasarkan label yang sama
- Mapping: faktor mana yang muncul di top? Faktor mana yang muncul di worst?

### Step 3: Hitung Frekuensi
- Faktor mana yang paling sering muncul di top? → Recurring pattern
- Faktor mana yang selalu muncul bersamaan? → Correlation pattern
- Faktor mana yang jarang tapi menonjol? → Anomaly pattern
- Faktor mana yang seharusnya ada tapi tidak muncul? → Absence pattern

### Step 4: Validasi Pola
- Apakah pola ini muncul di MINIMAL 3 data points? (kalau < 3, label sebagai hipotesis)
- Apakah ada mekanisme logis yang menjelaskan pola ini?
- Apakah pola ini konsisten dengan data periode sebelumnya? (kalau ada historis)
- Label: RELASIONAL (mekanisme jelas) vs NON-RELASIONAL (perlu validasi)

### Step 5: Artikulasikan Pola
Gunakan pattern language standar Falco:
- "X dari Y [top/worst] content punya [kesamaan Z]"
- "[Faktor A] berkorelasi kuat dengan [metrics B] — [mekanisme/reasoning]"
- "Anomali: [deskripsi] — hipotesis: [penjelasan]"
- "Absence: [apa yang tidak ada] — peluang: [apa yang bisa dicoba]"

---

## Cross-Pattern Analysis

Setelah menganalisis faktor per faktor, Falco harus mencari **cross-pattern** — kombinasi faktor yang secara bersamaan menghasilkan performa tertentu.

**Cara menemukan:**
- Overlay top content: faktor apa saja yang secara bersamaan muncul?
- Overlay worst content: faktor apa saja yang secara bersamaan muncul?
- Apakah ada "formula" yang terlihat? (misal: Reels + durasi pendek + hook threat + Talent A = selalu top)

**Contoh cross-pattern:**
```
Cross-pattern Top Content:
"Reels < 40 detik + hook emotional + Talent A"
→ Muncul di 3 dari 3 top content bulan ini
→ Muncul di 4 dari 5 top content bulan lalu
→ Tingkat keyakinan: TINGGI — formula ini konsisten

Cross-pattern Worst Content:
"Carousel promosi + tanpa hook + tanpa talent"
→ Muncul di 3 dari 3 worst content bulan ini
→ Tingkat keyakinan: TINGGI — formula ini konsisten underperform
```

---

## Anti-Pattern (Apa yang BUKAN Pola)

- ❌ **1 konten viral = bukan pattern.** Bisa jadi kebetulan, trending moment, atau outlier. Note sebagai anomali, bukan pattern.
- ❌ **Korelasi tanpa mekanisme = belum bisa disebut insight.** "Top content di-posting Selasa" bukan insight kalau tidak ada mekanisme kenapa Selasa.
- ❌ **"Semua konten bagus/jelek" = bukan pattern.** Ini generik. Harus ada diferensiasi: bagus di metrics APA, jelek dibanding APA.
- ❌ **Observasi tanpa frekuensi = bukan pattern.** "Ada konten dengan talent" → berapa dari berapa? Tanpa frekuensi, ini bukan pattern tapi deskripsi.

---

## Bedah Heuristik, Retention, dan Disiplin QC

### Peluru Heuristik: Satu Konten, Banyak Bias
Konten yang perform biasanya memuat bukan satu, melainkan tiga sampai empat pemicu psikologis sekaligus. Setiap pemicu diperlakukan seperti peluru: makin banyak peluru yang tepat sasaran, makin kuat kontennya. Saat membedah konten viral, hitung berapa pemicu yang bekerja dan di bagian mana masing-masing muncul.

### Heuristik yang Paling Sering Muncul
Dari pengamatan konten yang perform, beberapa pemicu paling sering berulang:
- **Kontras.** Membandingkan dua hal, dua generasi, dulu dan sekarang, atau dua tipe produk.
- **Novelty.** Sesuatu yang baru, "gue baru lihat ada begini".
- **In-group.** Memecah audiens jadi dua kubu (A versus B) sehingga komentar mengalir. Sering muncul lewat statement yang cukup tegas.
- **Curiosity gap.** Membuka rasa penasaran lewat headline atau tebakan sehingga ditonton sampai habis.
- **Negativity bias.** Pilihan kata yang lebih menohok (durhaka lebih kena daripada tidak berbakti).
- **Empati.** Menyentuh rasa kasihan, haru, atau sedih.
- **Pattern interrupt.** Sesuatu yang mengagetkan atau janggal di detik awal.
- **Salience.** Sesuatu yang mencolok, terlalu besar, terlalu kecil, atau berlebihan.

Pemicu lain tetap ada dan valid, tapi kelompok di atas yang paling sering menjelaskan kenapa sebuah konten naik.

### Retention Detik per Detik
Analisis retention dibaca per detik, bukan rata-rata. Detik nol selalu 100 persen. Titik rawan ada di detik pertama sampai kelima, di situ penonton paling banyak rontok. Fokus perhatian analisis ada di 5 detik pertama, karena di situ nasib sebuah konten sebagian besar ditentukan. Kalau retention jeblok di detik satu sampai dua, itu sinyal hook yang perlu diperbaiki, dan temuan ini disimpan sebagai learning.

### Disiplin QC: Habiskan Waktu di Awal
Saat me-review konten sebelum tayang, alokasi waktu tidak dibagi rata. Sebagian besar waktu QC dihabiskan memutar ulang 5 detik pertama berkali-kali sambil membayangkan diri sebagai audiens yang sedang scroll. Sisanya baru untuk bagian lain. Bahkan satu detik yang terasa terlalu lambat atau basa-basi layak ditandai untuk dipangkas.

### Evaluasi adalah Membaca Pola
Evaluasi bukan sekadar melihat sudah sesuai target atau belum. Inti evaluasi adalah membaca pola: apa yang berulang di konten yang perform, faktor apa yang berpengaruh, apa yang layak di-improve. Celah yang sering kosong dalam analisis adalah lompatan dari angka langsung ke kesimpulan tindakan, tanpa lebih dulu menjelaskan polanya. Selalu jembatani dari data ke pola, baru ke rekomendasi.

### Konteks Menyertai Angka
Data tanpa konteks berhenti di "naik sekian, turun sekian". Yang memberi makna adalah pola winning, faktor yang berpengaruh, dan konteks di baliknya. Gabungkan data dengan konteks supaya analisis tidak berhenti di permukaan.
