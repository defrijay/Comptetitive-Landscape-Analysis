# 🛵 Grab vs Gojek vs Maxim vs inDrive — Competitive Landscape Analysis

> **Portfolio Project 01 · Market Research & Consumer Insight**
> Analisis kompetitif 4 platform ride-hailing terbesar di Indonesia berbasis **100.000 Google Play reviews** nyata menggunakan NLP, sentiment analysis VADER, keyword-based churn detection, dan feature pain point matrix untuk mengidentifikasi positioning gap dan peluang strategis Grab.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Reviews](https://img.shields.io/badge/Reviews-100K_Google_Play-34A853?style=flat&logo=googleplay&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-VADER_Sentiment-8A2BE2?style=flat)
![Notebooks](https://img.shields.io/badge/Notebooks-6_pipeline_stages-F37626?style=flat&logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat)
![Looker Studio](https://img.shields.io/badge/Looker_Studio-Dashboard-4285F4?style=flat&logo=google&logoColor=white)

## 📌 TL;DR

| | |
|---|---|
| **Apa yang dilakukan** | Scraping 25.000 review per platform (100.000 total) dari Google Play Store, cleaning hingga 66.878 review bersih, EDA 6 analisis, VADER sentiment scoring, dan competitive synthesis dengan 5 rekomendasi strategis |
| **Sumber data** | Google Play Store (real data, bukan simulasi) · `google-play-scraper` · bahasa Indonesia · `lang='id'`, `country='id'` |
| **Metode utama** | NPS Proxy dari star rating, VADER sentiment analysis, keyword-based churn signal detection, feature pain point matrix, developer reply rate analysis |
| **Temuan terkuat** | Maxim memimpin kepuasan pengguna (avg rating 4.27, NPS +60.1); Gojek paling rendah (avg 3.11, NPS -0.1); churn risk tertinggi di Gojek (5.65%); Grab lemah di voucher/promo dan response time |
| **Output bisnis** | 5 rekomendasi strategis IF-THEN-IMPACT + `strategic_recommendations.csv` + 19 visualisasi tersimpan |
| **Tools** | Python · google-play-scraper · VADER · pandas · matplotlib · seaborn · Jupyter |
| **Relevansi ke Grab GIP** | Langsung mencerminkan tugas role: *"research on products and the market to support new and ongoing programs"* |

---

## 🎯 Background

Industri ride-hailing Indonesia merupakan salah satu yang paling kompetitif di Asia Tenggara. Empat pemain utama menempati positioning yang sangat berbeda:

| Platform | Asal | Diferensiasi Utama | App ID Google Play |
|---|---|---|---|
| **Grab** | Singapura | Superapp ekosistem lengkap (ride, food, payment) | `com.grabtaxi.passenger` |
| **Gojek** | Indonesia | Brand lokal kuat, GoPay, integrasi ekosistem | `com.gojek.app` |
| **Maxim** | Rusia | Tarif murah, ekspansi kota tier 2–3 | `com.taxsee.taxsee` |
| **inDrive** | Rusia | Negosiasi tarif driver-penumpang, komisi rendah | `sinet.startup.inDriver` |

Proyek ini menjawab pertanyaan kritis: **di mana posisi kompetitif Grab yang paling defensible**, dan dimensi produk apa yang harus diprioritaskan untuk mempertahankan loyalitas pengguna — berdasarkan bukti langsung dari 66.878 review pengguna nyata.

---

## ❓ Problem Statement

> *"Di dimensi mana Grab unggul atau tertinggal dari Gojek, Maxim, dan inDrive — dan strategi produk apa yang paling efektif untuk mempertahankan posisi kompetitif Grab di pasar ride-hailing Indonesia?"*

**Research Questions:**

| # | Research Question |
|---|---|
| RQ1 | Bagaimana perbandingan rata-rata rating dan NPS proxy keempat platform berdasarkan 66.878 review nyata? |
| RQ2 | Apa topik pain point dan praise yang paling sering muncul di masing-masing platform? |
| RQ3 | Bagaimana tren sentimen bulanan berubah, dan platform mana yang paling fluktuatif? |
| RQ4 | Platform mana yang paling aktif merespons ulasan, dan seberapa cepat? |
| RQ5 | Apa churn risk signal tertinggi per platform, dan trigger switching apa yang paling dominan? |
| RQ6 | Pada dimensi produk mana (harga, driver, app performance, CS) Grab memiliki kelemahan terbesar vs kompetitor? |

---

## 💡 Key Findings

### 1. Maxim memimpin kepuasan, Gojek paling rendah
> Berdasarkan analisis 66.878 review bersih, **Maxim unggul di kedua metrik kepuasan**: avg rating tertinggi **(4.27)** dan NPS Proxy tertinggi **(+60.1)**. Gojek berada di posisi terbawah dengan avg rating **(3.11)** dan NPS Proxy **(−0.1)** — mengindikasikan lebih banyak detractor daripada promotor. Grab dan inDrive berada di tengah dengan rating serupa (3.33–3.37) dan NPS positif tipis (+11.1 hingga +13.0).

### 2. VADER terbatas untuk teks Indonesia — star rating lebih andal
> VADER sentiment analysis mengklasifikasikan **85,3% review sebagai neutral** karena keterbatasan lexicon bahasa Inggris pada teks Indonesia — sebuah limitasi yang didokumentasikan secara transparan. Maxim memiliki compound score tertinggi (0.039) dan negative rate terendah (2.1%); Gojek memiliki negative rate tertinggi (7.9%). Oleh karena itu, analisis kompetitif utama bersandar pada **star rating + keyword analysis** sebagai sinyal yang lebih valid.

### 3. Gojek memiliki churn risk tertinggi, Maxim terendah
> Keyword-based churn signal detection (kata kunci: *uninstall, pindah, kapok, beralih, mending, pakai aplikasi lain*, dll.) menunjukkan bahwa **Gojek memiliki churn signal rate tertinggi (5.65%)**, diikuti inDrive (5.19%) dan Grab (4.45%). **Maxim hanya 1.77%** — kurang dari setengah kompetitor terdekat. Ini mengkonfirmasi bahwa kepuasan pengguna Maxim bukan sekadar rating tinggi, melainkan loyalitas aktif.

### 4. Pricing & voucher adalah pain point terbesar Grab
> Feature pain point matrix dari notebook competitive synthesis mengidentifikasi bahwa **keluhan terkait harga, ongkir, dan voucher mendominasi review negatif Grab**. Ini adalah P1 priority: mekanisme voucher yang tidak konsisten (tiba-tiba tidak bisa digunakan padahal masa berlaku masih ada) adalah trigger paling sering memicu 1-star review.

### 5. Refund & payment issues adalah churn trigger terbesar
> Analisis churn trigger menunjukkan **refund/payment issues menempati posisi tertinggi** dalam switching intent. Tidak adanya SLA yang jelas untuk proses refund mendorong pengguna Grab aktif beralih ke kompetitor yang proses pembayarannya lebih transparan.

### 6. Maxim mengabaikan review, Grab lambat merespons
> Developer reply rate analysis mengungkap disparitas besar: **inDrive paling responsif (56.2%)**, diikuti Grab (46.2%) dan Gojek (43.4%). **Maxim hampir tidak merespons sama sekali (0.8%)**. Namun Grab meskipun reply rate-nya baik, memiliki **median response time 5.8 jam** — jauh lebih lambat dari Gojek yang hanya **0.7 jam**. Kecepatan respons Gojek menjadi competitive advantage yang tersembunyi.

---

## 👥 Segment Profiles

Berdasarkan analisis churn signal dan rating distribution per platform dari 66.878 review bersih:

| Platform | Avg Rating | NPS Proxy | Churn Signal Rate | Reply Rate | Median Reply Time | Profil Pengguna |
|---|---|---|---|---|---|---|
| 🟠 **Maxim** | **4.27** | **+60.1** | **1.77%** | 0.8% | N/A | Sangat puas, sangat loyal, rating-dominant positive |
| 🟢 **Grab** | 3.37 | +13.0 | 4.45% | 46.2% | 5.8 jam | Sedang, terancam oleh voucher/promo issues |
| 🟣 **inDrive** | 3.33 | +11.1 | 5.19% | **56.2%** | N/A | Sedang, tinggi switching risk, paling responsif |
| 🔵 **Gojek** | 3.11 | -0.1 | **5.65%** | 43.4% | **0.7 jam** | Paling rendah, churn risk tertinggi, respons cepat |

---

## 📊 Recommendations

Dihasilkan dari `06_competitive_synthesis.ipynb` → disimpan ke `strategic_recommendations.csv`:

| Prioritas | Temuan (Data-backed) | Aksi yang Direkomendasikan | Expected Impact | KPI |
|---|---|---|---|---|
| **P1** | Pricing & ongkir = pain point terbesar di review negatif Grab | Implement **voucher lock mechanism** — voucher harus dijamin hingga expired, tidak bisa ditarik sepihak | Estimasi reduksi 15–20% churn complaint terkait voucher/promo | % review negatif menyebut "voucher"/"promo" |
| **P1** | Refund/payment issues = churn trigger tertinggi | Enforce **48-hour refund SLA** dengan automated status notification ke user | Kurangi refund-related 1-star reviews ~25% | Median refund resolution time |
| **P2** | App lag/crash sering disebut; pengguna Maxim memuji kecepatan app | Prioritaskan **app performance optimization untuk mid-range Android (RAM < 3GB)** | Improve NPS Proxy +5 hingga +10 poin untuk segmen budget device | Crash-free session rate; frekuensi kata "lag"/"lemot" |
| **P2** | Driver cancellation = recurring pain point vs inDrive | Implement **driver penalty escalation** untuk cancellation berulang di hari yang sama | Kurangi cancellation-related reviews ~20% | Cancellation rate per driver |
| **P3** | CS reply Grab generic dan lambat (5.8 jam median) vs Gojek 0.7 jam | **Personalisasi CS reply template** — hindari copy-paste respons generik | Improve reply sentiment; kurangi follow-up 1-star reviews | Reply thumbs-up count; repeat 1-star rate after reply |

---

## 🗂️ Dataset

### Spesifikasi data yang benar-benar dikumpulkan

| Attribute | Detail |
|---|---|
| **Sumber** | Google Play Store (real data) via `google-play-scraper` |
| **Bahasa** | Indonesia (`lang='id'`, `country='id'`) |
| **Total raw** | **100.000 reviews** (25.000 per platform) |
| **Setelah cleaning** | **66.878 reviews** bersih |
| **Periode** | Hingga Mei 2026 (sorted by newest) |
| **Format raw** | 4 CSV terpisah per platform di `data/raw/google_play_reviews/` |
| **Format clean** | `combined_reviews_clean.csv` di `data/clean/` |

> **Catatan:** Apple App Store scraping (cell ke-2 di notebook 01) sudah disiapkan dengan `app-store-scraper` namun **tidak dieksekusi** dalam pipeline final — proyek ini sepenuhnya berbasis data Google Play Store.

### Kolom raw (9 kolom dari google-play-scraper)

| Kolom | Tipe | Deskripsi |
|---|---|---|
| `reviewId` | string | ID unik review |
| `userName` | string | Nama pengguna |
| `content` | string | Teks review |
| `score` | int | Rating bintang 1–5 |
| `thumbsUpCount` | int | Jumlah thumbs up |
| `reviewCreatedVersion` | string | Versi app saat review ditulis (17.5% null) |
| `at` | datetime | Timestamp review |
| `replyContent` | string | Balasan developer (71.1% null) |
| `repliedAt` | datetime | Timestamp balasan |

### Pipeline cleaning (03_data_cleaning.ipynb)

| Tahap | Sebelum | Sesudah | Keterangan |
|---|---|---|---|
| Raw load | 100.000 | 100.000 | 4 platform × 25.000 |
| Duplicate by `reviewId` | 100.000 | 100.000 | Tidak ada duplikat ID |
| Duplicate by `content + platform` | 100.000 | **67.037** | 32.963 review teks identik dihapus |
| Invalid/empty rows | 67.037 | **66.878** | 159 baris null score/at/content < 3 char |
| **Final clean** | | **66.878** | Siap analisis |

### Kolom tambahan setelah cleaning

Kolom-kolom berikut di-generate selama cleaning dan EDA:
`content_clean`, `content_normalized` (lowercase, hapus URL, normalize whitespace), `review_year`, `review_month`, `review_length`, `sentiment_label` (proxy dari star rating: 4–5 = positive, 3 = neutral, 1–2 = negative), `has_reply`, `churn_signal` (keyword-based binary flag), `vader_label`, `vader_compound`

---

## ⚙️ Pipeline Overview

```
📥 01_data_collection.ipynb
   └── Scraping 25.000 review × 4 platform → data/raw/google_play_reviews/
          (Grab, Gojek, Maxim, inDrive · lang=id · sort=NEWEST · batch 1.000)
       └── delay 3s/batch, 5s/platform untuk hindari IP block

📊 02_data_understanding.ipynb
   └── Load & merge 100.000 rows × 10 cols
   └── Check duplicates, missing values, score distribution
   └── Monthly volume trend, review length distribution
   └── 5 visualisasi → reports/figures/02_*.png

🧹 03_data_cleaning.ipynb
   └── Drop 32.963 same-text duplicates → 67.037
   └── Drop 159 invalid rows → 66.878 final
   └── Rename camelCase → snake_case
   └── Normalize text (lowercase, hapus URL, collapse repetition, preserve emoji)
   └── Tambah: sentiment_label, temporal features, review_length
   └── Output: data/clean/combined_reviews_clean.csv

🔍 04_EDA.ipynb
   └── Avg Rating + NPS Proxy per platform
   └── Stacked rating distribution (100% bar)
   └── Monthly rating trend (line chart)
   └── Top keywords extraction (pain points vs praise)
   └── Developer reply rate + median response time
   └── Keyword-based churn signal detection
   └── 7 visualisasi → reports/figures/04_*.png

🧠 05_sentiment_analysis.ipynb
   └── VADER scoring (compound -1 to +1)
   └── Classification: positive ≥0.05, negative ≤-0.05, neutral
   └── Per-platform VADER scorecard → data/clean/vader_scorecard.csv
   └── Sentiment trend over time (monthly)
   └── VADER vs star rating heatmap (cross-validation)
   └── 3 visualisasi → reports/figures/05_*.png

🏆 06_competitive_synthesis.ipynb
   └── NPS Proxy + aspect mention mapping
   └── 3-metric competitive summary dashboard
   └── Feature pain point matrix (pricing, app, driver, CS, refund)
   └── Feature health radar chart
   └── Churn signal analysis + switching triggers
   └── 5 strategic recommendations → data/clean/strategic_recommendations.csv
   └── 4 visualisasi → reports/figures/06_*.png
   └── Total: 19 figures confirmed
```

---

## 📓 Notebooks

| Notebook | Deskripsi | Input | Output utama |
|---|---|---|---|
| `01_data_collection.ipynb` | Scraping 25.000 review per platform via `google-play-scraper` dengan pagination token dan rate limiting | Google Play Store API | `data/raw/google_play_reviews/*.csv` (4 file) |
| `02_data_understanding.ipynb` | Memahami struktur, kualitas, dan distribusi data sebelum cleaning (12 segmen analisis) | `data/raw/*.csv` | 5 visualisasi: missing values, monthly volume, review length, score distribution, reviews per platform |
| `03_data_cleaning.ipynb` | Deduplikasi 2 pass, rename kolom, type casting, text normalization, feature engineering | `data/raw/*.csv` | `data/clean/combined_reviews_clean.csv` (66.878 baris) |
| `04_EDA.ipynb` | 6 analisis EDA: avg rating + NPS proxy, stacked distribution, trend bulanan, keyword extraction, reply stats, churn signal | `combined_reviews_clean.csv` | 7 PNG figures + kolom `churn_signal` |
| `05_sentiment_analysis.ipynb` | VADER sentiment scoring, per-platform scorecard, trend over time, cross-validation vs star rating | `combined_reviews_clean.csv` | `vader_scorecard.csv` + 3 PNG figures |
| `06_competitive_synthesis.ipynb` | Sintesis kompetitif akhir: NPS, pain point matrix, radar chart, churn analysis, 5 IF-THEN-IMPACT recommendations | `combined_reviews_clean.csv` + `vader_scorecard.csv` | `strategic_recommendations.csv` + 4 PNG figures |

---

## 🤖 Model Performance

### VADER Sentiment Scorecard (per notebook 05)

| Platform | Total Reviews | % Positive | % Neutral | % Negative | Avg Compound |
|---|---|---|---|---|---|
| Maxim | 14.380 | 10.1% | 87.7% | **2.1%** | **0.039** |
| Grab | 16.218 | 8.6% | 84.8% | 6.7% | 0.015 |
| inDrive | 17.979 | 8.0% | 86.2% | 5.8% | 0.014 |
| Gojek | 18.301 | 9.3% | 82.8% | **7.9%** | 0.014 |

> **Catatan metodologi:** VADER adalah lexicon berbasis bahasa Inggris. Pada teks Indonesia, ~85% review terklasifikasi neutral karena kata Indonesia tidak ada di lexicon-nya. Hasil ini **valid sebagai baseline komparatif antar platform**, namun tidak representatif untuk analisis sentimen absolut. Analisis utama menggunakan **star rating + keyword-based approach** sebagai complement yang lebih akurat.

### NPS Proxy & Rating Summary (per notebook 04 & 06)

| Platform | Avg Star Rating | NPS Proxy | Churn Signal Rate | Reply Rate |
|---|---|---|---|---|
| **Maxim** | **4.27** | **+60.1** | **1.77%** | 0.8% |
| Grab | 3.37 | +13.0 | 4.45% | 46.2% |
| inDrive | 3.33 | +11.1 | 5.19% | 56.2% |
| Gojek | 3.11 | -0.1 | 5.65% | 43.4% |

*NPS Proxy = (% bintang 5) − (% bintang 1–2) × 100. Dihitung dari 66.878 review bersih.*

---

## 🛠️ Tech Stack

```
Language         Python 3.10+
Data Collection  google-play-scraper (pagination token, rate limiting)
Data Processing  pandas, numpy, re
NLP/Sentiment    vaderSentiment (VADER)
Visualization    matplotlib, seaborn
Text Analysis    collections.Counter (keyword extraction)
File I/O         pathlib.Path
Notebook         Jupyter Lab / Jupyter Notebook
Version Control  GitHub
```

---

## 📁 Project Structure

```
grab-ridehailing-competitive-analysis/
│
├── data/
│   ├── raw/
│   │   └── google_play_reviews/
│   │       ├── grab_reviews.csv        # 25.000 rows
│   │       ├── gojek_reviews.csv       # 25.000 rows
│   │       ├── maxim_reviews.csv       # 25.000 rows
│   │       └── indrive_reviews.csv     # 25.000 rows
│   └── clean/
│       ├── combined_reviews_clean.csv  # 66.878 rows (final clean)
│       ├── vader_scorecard.csv         # Sentiment summary per platform
│       └── strategic_recommendations.csv  # 5 IF-THEN-IMPACT actions
│
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_understanding.ipynb
│   ├── 03_data_cleaning.ipynb
│   ├── 04_EDA.ipynb
│   ├── 05_sentiment_analysis.ipynb
│   └── 06_competitive_synthesis.ipynb
│
├── reports/
│   └── figures/                        # 19 PNG visualisasi
│       ├── 02_missing_values.png
│       ├── 02_monthly_volume.png
│       ├── 02_review_length.png
│       ├── 02_review_per_platform.png
│       ├── 02_score_distribution.png
│       ├── 04_churn_signal.png
│       ├── 04_monthly_trend.png
│       ├── 04_pain_praise.png
│       ├── 04_rating_nps.png
│       ├── 04_reply_stats.png
│       ├── 04_score_stacked.png
│       ├── 04_top_keywords.png
│       ├── 05_sentiment_heatmap.png
│       ├── 05_sentiment_trend.png
│       ├── 05_vader_sentiment.png
│       ├── 06_churn_analysis.png
│       ├── 06_competitive_summary.png
│       ├── 06_feature_pain_matrix.png
│       └── 06_radar_feature.png
│
├── requirements.txt
└── README.md
```

---

## 🚀 How to Run

### 1. Clone repository

```bash
git clone https://github.com/defrijay/grab-ridehailing-competitive-analysis.git
cd grab-ridehailing-competitive-analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Jalankan pipeline secara berurutan

```bash
# 01 — Scraping data (±30–40 menit, butuh koneksi stabil)
jupyter notebook notebooks/01_data_collection.ipynb

# 02 — Data understanding
jupyter notebook notebooks/02_data_understanding.ipynb

# 03 — Data cleaning
jupyter notebook notebooks/03_data_cleaning.ipynb

# 04 — EDA (termasuk churn signal detection)
jupyter notebook notebooks/04_EDA.ipynb

# 05 — Sentiment analysis VADER
jupyter notebook notebooks/05_sentiment_analysis.ipynb

# 06 — Competitive synthesis & recommendations
jupyter notebook notebooks/06_competitive_synthesis.ipynb
```

> ⚠️ Notebook 01 (scraping) membutuhkan waktu sekitar 30–40 menit untuk 4 platform. Data hasil scraping sudah tersedia di `data/raw/` sehingga kamu bisa skip notebook 01 dan langsung mulai dari notebook 02 jika sudah ada datanya.

### Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
google-play-scraper>=1.2
vaderSentiment>=3.3
pathlib
collections
jupyter>=1.0
```

---

## ⚠️ Limitations & Next Steps

### Limitations

- **VADER terbatas untuk teks Indonesia:** ~85% review terklasifikasi neutral karena VADER adalah lexicon English. Ini limitasi yang sudah diakui dan didokumentasikan di notebook 05. Star rating + keyword approach digunakan sebagai complement yang lebih valid.
- **Hanya Google Play (Android):** Apple App Store scraping sudah disiapkan di notebook 01 namun tidak dieksekusi data iOS tidak termasuk. Mengingat penetrasi Android Indonesia >90% di segmen ride-hailing, ini acceptable.
- **Tidak ada data survei primer:** Analisis sepenuhnya berbasis review app store (observed behavior, bukan stated preference). Switching trigger di sini adalah proxy dari review text, bukan konfirmasi langsung dari pengguna.
- **Review recency:** Data diambil sorted by newest, namun tidak dibatasi rentang waktu spesifik, beberapa review mungkin berasal dari tahun berbeda dengan kondisi yang sudah berubah.

### Potential next steps

| Ekstensi | Deskripsi |
|---|---|
| **IndoBERT sentiment** | Ganti VADER dengan IndoBERT (HuggingFace) untuk akurasi sentimen bahasa Indonesia yang jauh lebih tinggi |
| **Survei primer** | Tambahkan 100–150 responden survei untuk capture stated preference dan switching behavior yang tidak terdeteksi dari review |
| **Topic modeling (LDA)** | Ekstrak topik otomatis dari review text untuk menemukan isu tersembunyi di luar keyword yang sudah didefinisikan |
| **Temporal analysis per versi** | Hubungkan `reviewCreatedVersion` dengan changelog app untuk identifikasi versi mana yang memicu lonjakan review negatif |
| **Geospatial breakdown** | Jika tersedia kota dalam review, pisahkan analisis per kota untuk lihat apakah competitive gap Grab vs Maxim berbeda antara Jakarta dan Medan |

---

## 📬 Contact

**Defrizal Yahdiyan Risyad**

Final-year Computer Science · Universitas Pendidikan Indonesia

[![LinkedIn](https://img.shields.io/badge/LinkedIn-defrizalyr-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/defrizalyr)
[![GitHub](https://img.shields.io/badge/GitHub-defrijay-181717?style=flat&logo=github)](https://github.com/defrijay)
