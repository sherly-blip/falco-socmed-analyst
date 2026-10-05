# Falco Skill, Folder Structure

```
falco-skill/
│
├── SYSTEM-PROMPT.md                  # System prompt utama Falco (LOAD PERTAMA KALI)
├── SKILL.md                          # Skill detail Falco (BACA SETELAH SYSTEM PROMPT)
│
├── standards/                        # Standar analisis per konteks + quality gates (13 file)
│   ├── standar-humanize-writing.md   # ⚠️ WAJIB BACA SELALU, protokol anti-pattern AI (em dash, antitesis, dll). Override semua file lain dalam hal gaya penulisan.
│   ├── standar-analisis-mendalam.md  # ⚠️⚠️ MASTER STANDARD, 8 standar wajib di atas baseline (WAJIB BACA SELALU)
│   ├── standar-audit-socmed.md       # ⚠️ Standar social media audit 360°, 9 blok wajib (WAJIB BACA saat audit)
│   ├── standar-analisis-organik.md   # Standar analisis performa konten organik
│   ├── standar-analisis-ads.md       # Standar analisis performa ads/paid content
│   ├── standar-analisis-kol.md       # Standar analisis performa KOL/affiliate campaign
│   ├── standar-analisis-live.md      # Standar analisis performa liveshopping
│   ├── standar-analisis-kompetitor.md # Standar analisis kompetitor & creator benchmarking
│   ├── standar-reporting-periodik.md # Standar laporan periodik (weekly/bi-weekly/monthly)
│   ├── standar-deskripsi-data.md     # ⚠️ Standar presisi deskripsi data & konten dalam analisis (WAJIB BACA)
│   ├── standar-penulisan-pattern.md  # ⚠️ Cara menulis pattern analysis yang tajam (WAJIB BACA)
│   ├── standar-penulisan-saran.md    # ⚠️ Standar saran berbasis data, Level 3 actionable (WAJIB BACA)
│   └── anti-generik-rules.md         # ⚠️ Red-flag phrases + standar presisi analisis (WAJIB BACA)
│
├── frameworks/                       # Framework analisis & evaluasi (4 file)
│   ├── six-step-analysis.md          # ⚠️ 6-Step Analysis Framework (NON-NEGOTIABLE)
│   ├── faktor-analisis-checklist.md  # Checklist faktor analisis per konteks (organik, ads, KOL, live)
│   ├── pattern-recognition-analyst.md # Pattern recognition untuk analyst: recurring, correlation, anomaly, absence
│   └── data-hierarchy-framework.md   # Hirarki: Data Mentah, Informasi, Pattern, Insight, Saran
│
└── references/                       # Referensi konteks & benchmark (9 file)
    ├── brand-profile-overheard-beauty.md  # ⚠️ Konteks brand permanen Overheard Beauty: fondasi semua analisis
    ├── template-input-analisis.md    # Template input siap-isi (Overview + Content Detailed) untuk user
    ├── metrics-glossary.md           # Definisi metrics per platform (reach vs impressions, ER, dll)
    ├── benchmark-reference.md        # Benchmark metrics per platform & per tier followers
    ├── contoh-analisis-pattern.md    # Contoh pattern analysis mendalam (referensi kedalaman)
    ├── contoh-report-baseline.md     # ⚠️ Contoh analytics report lengkap, ACUAN STRUKTUR & ALUR
    ├── contoh-audit-baseline.md      # ⚠️ Contoh social media audit 360° lengkap, ACUAN AUDIT
    ├── evaluasi-report-baseline.md   # ⚠️ Evaluasi baseline: apa yang kuat, apa yang harus di-improve
    └── interaction-examples.md       # Contoh interaksi Falco di berbagai skenario
```

## Total Files: 30
- Core: 2 (SYSTEM-PROMPT.md, SKILL.md)
- Standards: 13
- Frameworks: 4
- References: 9
- Documentation: 1 (FOLDER-STRUCTURE.md)

## Urutan Baca

1. **SYSTEM-PROMPT.md**, di-load pertama kali. Berisi identitas Falco, prinsip berpikir, personality, tone, cara kerja, arsenal, kemampuan, dan batasan.
2. **standards/standar-humanize-writing.md**, ⚠️ WAJIB BACA SELALU sebelum output apapun (protokol anti-pattern AI).
3. **SKILL.md**, dibaca setelah system prompt. Berisi detail teknis: 6 capabilities, mode kerja, brand context setup, brief collection, standar output, format laporan.
4. **standards/**, ⚠️ WAJIB dibaca sebelum mengerjakan jenis analisis tertentu. Berisi standar minimum per konteks analisis.
5. **frameworks/**, ⚠️ WAJIB dibaca saat analisis. 6-Step Framework adalah NON-NEGOTIABLE.
6. **references/**, dibaca saat perlu konteks brand, benchmark, atau contoh kedalaman analisis.

## Prinsip

- SYSTEM-PROMPT.md: siapa Falco dan cara berpikir
- SKILL.md: cara bekerja (6 capabilities, mode, brief collection, standar output, format)
- Standards: quality gate (standar minimum per jenis analisis yang TIDAK BOLEH dilanggar)
- Frameworks: model (kerangka analisis yang WAJIB diikuti, terutama 6-Step)
- References: konteks (brand context setup, benchmark, contoh kedalaman)
