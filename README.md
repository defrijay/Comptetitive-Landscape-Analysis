# 🛵 Grab vs Gojek vs Maxim vs inDrive — Competitive Landscape Analysis

> **Portfolio Project 01 · Market Research & Consumer Insight**
> Analisis kompetitif 4 platform ride-hailing terbesar di Indonesia menggunakan survei primer, sentiment analysis, dan social listening, mengidentifikasi positioning gap dan peluang strategis Grab di tengah persaingan dengan incumbents dan challengers berbasis harga.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Looker Studio](https://img.shields.io/badge/Looker_Studio-Dashboard-4285F4?style=flat&logo=google&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-IndoBERT_·_VADER-8A2BE2?style=flat)
![Survey](https://img.shields.io/badge/Survey-150%2B_Respondents-00A67E?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-ongoing?style=flat)

---

## 📌 Executive Summary

| | |
|---|---|
| **Apa yang dilakukan** | Analisis kompetitif 4 platform ride-hailing (Grab, Gojek, Maxim, inDrive) di 5 kota Indonesia menggunakan survei primer (n=150+), sentiment analysis 4.000+ app review, dan Twitter/X social listening |
| **Metode utama** | NPS scoring, 7-dimensi feature rating, VADER + IndoBERT sentiment, LDA topic modeling |
| **Temuan terkuat** | Grab unggul di reliability dan ekosistem superapp, namun terancam oleh Maxim & inDrive yang agresif di segmen price-sensitive kota tier 2–3 |
| **Output bisnis** | Feature gap matrix + 4 rekomendasi strategis dengan estimasi dampak terukur |
| **Tools** | Python · Google Forms · Looker Studio · google-play-scraper · HuggingFace |
| **Relevansi ke Grab GIP** | Langsung mencerminkan tugas role: *"research on products and the market to support new and ongoing programs"* |

---

## 🎯 Background

Pasar ride-hailing Indonesia merupakan salah satu yang paling kompetitif dan terfragmentasi di Asia Tenggara. Empat pemain utama saat ini menempati positioning yang sangat berbeda:

| Platform | Asal | Diferensiasi Utama | Kekuatan Pasar |
|---|---|---|---|
| **Grab** | Singapura | Superapp ekosistem lengkap (ride, food, payment) | Dominan di kota besar, loyal users |
| **Gojek** | Indonesia | Brand lokal kuat, GoPay, integrasi KRL | Market share tertinggi (82.6% pengguna) |
| **Maxim** | Rusia | Tarif sangat murah, ekspansi kota tier 2–3 | Tumbuh cepat di luar Jabodetabek |
| **inDrive** | Rusia | Model negosiasi tarif driver-penumpang, komisi < 10% | Price-sensitive commuters, driver-friendly |

Dinamika ini memunculkan pertanyaan kritis: di tengah tekanan harga dari Maxim dan inDrive, serta dominasi brand Gojek secara lokal, **di mana posisi kompetitif Grab yang paling defensible** — dan dimensi apa yang harus diprioritaskan untuk mempertahankan loyalitas pengguna?

Proyek ini menjawab pertanyaan tersebut melalui pendekatan mixed-method yang menggabungkan data kuantitatif survei, sentiment analysis app review, dan analisis media sosial.

---

## ❓ Problem Statement

> *"Di dimensi mana Grab unggul atau tertinggal dari Gojek, Maxim, dan inDrive — dan strategi produk apa yang paling efektif untuk mempertahankan posisi kompetitif Grab di pasar ride-hailing Indonesia?"*

**Research Questions:**

| # | Research Question |
|---|---|
| RQ1 | Pada dimensi mana (harga, reliability, UX, driver quality, ekosistem layanan, program reward) Grab unggul atau tertinggal dari ketiga kompetitor? |
| RQ2 | Apa trigger utama yang menyebabkan pengguna berpindah ke Maxim atau inDrive, dan segmen pengguna mana yang paling rentan? |
| RQ3 | Bagaimana sentimen publik terhadap masing-masing platform di app store dan media sosial, dan isu apa yang paling sering dibicarakan? |
| RQ4 | Apakah model negosiasi tarif inDrive dan tarif flat Maxim menjadi ancaman nyata terhadap basis pengguna Grab, atau hanya menarik segmen berbeda? |
| RQ5 | Rekomendasi produk dan strategi apa yang memberikan dampak terbesar untuk memperkuat posisi Grab terhadap challenger berbasis harga? |

---

## 💡 Key Findings

### 1. Grab dan Gojek dominan, Maxim & inDrive tumbuh dari bawah
> Grab dan Gojek masih memimpin di kota besar berdasarkan survei, namun **Maxim dan inDrive menunjukkan traksi signifikan di kota tier 2–3** (Bandung, Medan, Semarang). 31% responden dari kota-kota tersebut menyebut Maxim sebagai platform utama untuk perjalanan pendek karena tarif yang 30–45% lebih murah.

### 2. Harga adalah satu-satunya keunggulan Maxim & inDrive
> Analisis feature rating menunjukkan Maxim dan inDrive hanya unggul di 1 dari 7 dimensi: **harga/tarif**. Di semua dimensi lain — reliability, app UX, keamanan, ekosistem layanan, program reward — Grab dan Gojek memimpin secara konsisten. Ini berarti ancaman mereka bersifat *price-driven*, bukan *experience-driven*.

### 3. Model negosiasi inDrive menarik segmen driver, bukan rider
> Dari sisi rider, model negosiasi tarif inDrive justru dipersepsikan sebagai **sumber friction**, bukan keunggulan: 67% responden yang pernah mencoba inDrive menyebut proses tawar-menawar sebagai alasan tidak melanjutkan penggunaan. Ancaman inDrive lebih terasa di sisi supply (driver) dibanding demand (rider).

### 4. Ekosistem superapp adalah moat terkuat Grab
> Pengguna yang menggunakan 3+ layanan Grab (ride + food + payment) memiliki churn rate **4.8x lebih rendah** dari pengguna ride-only. Ini mengkonfirmasi bahwa integrasi ekosistem — bukan harga — adalah diferensiasi yang paling defensible untuk Grab terhadap Maxim dan inDrive.

### 5. App stability Grab lebih baik dari Gojek, namun driver cancellation masih jadi isu
> Sentiment analysis menunjukkan keluhan driver cancellation mendominasi review negatif Grab (38% topik negatif) — jauh di atas Gojek (22%), Maxim (15%), dan inDrive (8%). Di luar itu, app stability Grab secara umum dinilai lebih baik dari Gojek berdasarkan rating dan review tren 6 bulan terakhir.

---

## 👥 Segment Profiles

Berdasarkan survei, pengguna ride-hailing di Indonesia terbagi ke dalam 4 profil berbeda dengan preferensi platform yang berbeda:

| Segmen | Proporsi | Karakteristik | Platform Utama | Switching Risk ke Maxim/inDrive |
|---|---|---|---|---|
| 🏙️ **Urban Loyalist** | 22% | Kota besar, multi-service, GrabPay/GoPay user, income menengah-atas | Grab atau Gojek (eksklusif) | Rendah — ekosistem lock-in kuat |
| 💰 **Price Hunter** | 31% | Sensitif harga, sering bandingkan tarif sebelum order, kota tier 2–3 | Mixed — pilih termurah saat itu | Sangat tinggi — aktif pakai Maxim |
| 🛡️ **Safety-First** | 19% | Perempuan, malam hari, prioritas keamanan driver | Grab atau Gojek | Rendah — tidak mau coba platform baru |
| 🔄 **Pragmatic Switcher** | 28% | Tidak loyal ke satu platform, pilih berdasarkan promo hari itu | Semua platform bergantian | Sedang — sudah pakai inDrive sesekali |

**Insight kritis:** Price Hunters (31%) adalah segmen yang paling aktif trial Maxim dan inDrive. Namun sebagian besar tetap mempertahankan Grab/Gojek untuk perjalanan penting — mengindikasikan *dual-apping* bukan full switching.

---

## 📊 Recommendations

| # | Temuan yang Mendasari | Rekomendasi | Estimated Impact |
|---|---|---|---|
| 1 | Price Hunters aktif dual-app dengan Maxim di kota tier 2–3 | Rancang **"Grab Hemat" tier** dengan tarif kompetitif khusus motor jarak pendek di kota tier 2–3, menggunakan dynamic pricing yang lebih agresif di off-peak hours | Estimasi recovery 25% Price Hunter segment dari dual-app menjadi Grab-primary |
| 2 | Driver cancellation 38% topik negatif di review Grab | Implementasi **automatic driver penalty system** yang lebih transparan + notifikasi real-time ke rider saat driver cancel — kurangi ambiguitas yang menjadi sumber frustrasi utama | Estimasi penurunan cancellation complaint -40% dalam 3 bulan |
| 3 | Ekosistem superapp = moat terkuat vs Maxim & inDrive | Perkuat **cross-service bundling**: "Order GrabFood 3x minggu ini, dapat GrabBike gratis 2x" — dorong pengguna ride-only menjadi multi-service | Pengguna multi-service 4.8x lebih tidak mungkin full-switch ke Maxim |
| 4 | inDrive menarik driver dengan komisi rendah, mengancam supply Grab | Luncurkan **"Grab Driver Loyalty Program"** dengan earning boost untuk driver dengan acceptance rate tinggi — pertahankan supply berkualitas yang menjadi fondasi reliability unggul | Mitigasi driver supply drain yang secara tidak langsung meningkatkan cancellation rate |

---

## 🗂️ Dataset

Proyek ini menggunakan kombinasi **data primer** (survei) dan **data sekunder** (scraping + referensi publik):

### Primary data — Survei (Google Forms)

| Attribute | Detail |
|---|---|
| Jumlah responden | 150+ |
| Target | Pengguna aktif minimal 1 platform dalam 30 hari terakhir |
| Metode distribusi | WhatsApp group mahasiswa, komunitas transportasi & daily commuter, media sosial |
| Durasi pengisian | ~8–10 menit |
| Kota target | Jakarta, Bandung, Medan, Semarang, Surabaya |
| Bahasa | Bahasa Indonesia |

**Struktur survei (5 bagian):**
- **Bagian A:** Screening & profil demografis (kota, usia, frekuensi perjalanan)
- **Bagian B:** Usage pattern — platform yang digunakan & alasan utama
- **Bagian C:** Feature rating 7 dimensi per platform yang pernah digunakan (skala 1–5 Likert)
- **Bagian D:** NPS (0–10) + likelihood mencoba Maxim/inDrive
- **Bagian E:** Switching trigger — open text + checklist alasan berpindah platform

### Secondary data — App Store Reviews

| Sumber | Volume | Periode | Metode |
|---|---|---|---|
| Google Play — Grab | ~1,000 review | 6 bulan terakhir | `google-play-scraper` |
| Google Play — Gojek | ~1,000 review | 6 bulan terakhir | `google-play-scraper` + Kaggle Gojek dataset |
| Google Play — Maxim | ~1,000 review | 6 bulan terakhir | `google-play-scraper` |
| Google Play — inDrive | ~1,000 review | 6 bulan terakhir | `google-play-scraper` |

### Secondary data — Referensi publik

| Sumber | Kegunaan |
|---|---|
| Mordor Intelligence / 6W Research | Market share & competitive landscape ride-hailing Indonesia 2024 |
| ResearchGate — Pratiwi et al. (2024) | Riset akademis: strategi promosi digital Gojek, Grab, inDrive, Maxim |
| UIN Sultan Syarif Kasim Riau (2025) | Sentiment baseline Grab vs Gojek (peer-reviewed, 1.800 review per platform) |
| Google Trends | Search volume trend 4 platform, 2022–2025 |
| Similarweb (free tier) | Web traffic & app engagement proxy |

> **Catatan transparansi:** Data survei primer dikumpulkan dengan persetujuan responden. Data app review digunakan sesuai terms of service Google Play. Tidak ada data internal atau proprietary dari platform manapun yang digunakan dalam proyek ini.

---

## ⚙️ Pipeline Overview

```
┌──────────────────────────────────────────────────┐
│              DATA COLLECTION LAYER                │
│  Google Forms Survey  +  App Store Scraping (4x) │
│  Twitter/X snscrape   +  Public Reports & Papers  │
└─────────────────────┬────────────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────────────┐
│              PREPROCESSING LAYER                  │
│  Slang normalization (gak→tidak, dll)             │
│  Duplicate & short review removal (< 10 kata)     │
│  Survey response validation & encoding            │
│  Language detection — split ID vs EN text         │
└─────────────────────┬────────────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────────────────────┐
│                    ANALYSIS LAYER                         │
│                                                           │
│  ┌──────────────────────┐  ┌───────────────────────────┐ │
│  │   Survey Analysis    │  │    Sentiment Analysis     │ │
│  │  · NPS per platform  │  │  · VADER (English text)   │ │
│  │  · 7-dim feature     │  │  · IndoBERT (Indonesian)  │ │
│  │    rating heatmap    │  │  · LDA topic modeling     │ │
│  │  · Switching trigger │  │  · Word cloud per platform│ │
│  │  · Segment profiling │  │  · Sentiment trend 6 bln  │ │
│  └──────────┬───────────┘  └─────────────┬─────────────┘ │
│             └──────────────┬─────────────┘               │
│                            ▼                              │
│             ┌──────────────────────────┐                 │
│             │  Competitive Synthesis   │                 │
│             │  · 7-dim radar chart     │                 │
│             │  · Feature gap matrix    │                 │
│             │  · Platform scorecard    │                 │
│             └──────────────────────────┘                 │
└──────────────────────┬───────────────────────────────────┘
                       │
                       ▼
┌──────────────────────────────────────────────────┐
│                  OUTPUT LAYER                     │
│  Executive Report PDF  ·  Looker Studio Dashboard │
│  Companion Slide Deck  ·  GitHub Repo             │
└──────────────────────────────────────────────────┘
```

---

## 📓 Notebooks

| Notebook | Deskripsi | Output utama |
|---|---|---|
| `01_data_collection.ipynb` | Scraping Google Play reviews untuk 4 platform menggunakan `google-play-scraper` | `grab_reviews.csv`, `gojek_reviews.csv`, `maxim_reviews.csv`, `indrive_reviews.csv` |
| `02_survey_analysis.ipynb` | Analisis survei primer: NPS, feature rating, switching trigger, segment profiling | NPS scorecard, radar chart 4 platform, segment distribution |
| `03_sentiment_analysis.ipynb` | Text cleaning → VADER/IndoBERT → LDA topic modeling → word cloud per platform | `sentiment_scores.csv`, topic clusters, sentiment heatmap |
| `04_competitive_synthesis.ipynb` | Integrasi semua sumber: feature gap matrix, competitive scorecard, rekomendasi | Final gap matrix, competitive heatmap, executive tables |

---

## 🤖 Model Performance

### Sentiment Analysis Accuracy

| Model | Language Target | Approach | Accuracy |
|---|---|---|---|
| VADER | English reviews | Lexicon-based | ~78% |
| IndoBERT (HuggingFace) | Indonesian reviews | Pretrained transformer | ~85% |
| LDA Topic Model | All text (4 platform) | Unsupervised | Coherence score: 0.54 |

### NPS Hasil Survei — 4 Platform

| Platform | NPS | Promoters | Passives | Detractors | Interpretasi |
|---|---|---|---|---|---|
| Grab | +34 | 52% | 30% | 18% | Positif kuat |
| Gojek | +29 | 48% | 33% | 19% | Positif |
| Maxim | +11 | 35% | 41% | 24% | Netral-positif |
| inDrive | +4 | 31% | 42% | 27% | Netral |

> NPS dihitung sebagai % Promoters (9–10) — % Detractors (0–6). Grab memimpin NPS, namun gap dengan Gojek sempit — mengindikasikan loyalitas yang rentan terhadap pergeseran promosi.

---

## 🛠️ Tech Stack

```
Language        Python 3.10+
Scraping        google-play-scraper, snscrape
NLP             VADER (vaderSentiment), IndoBERT (transformers · HuggingFace)
Topic Modeling  gensim (LDA)
Data            pandas, numpy
Visualization   matplotlib, seaborn, wordcloud, plotly
Dashboard       Looker Studio (interactive, shareable link)
Survey          Google Forms + Google Sheets
Version control GitHub
```

---

## 📁 Project Structure

```
grab-ridehailing-competitive-analysis/
│
├── data/
│   ├── raw/
│   │   ├── grab_reviews.csv              # Scraped Google Play reviews — Grab
│   │   ├── gojek_reviews.csv             # Scraped Google Play reviews — Gojek
│   │   ├── maxim_reviews.csv             # Scraped Google Play reviews — Maxim
│   │   ├── indrive_reviews.csv           # Scraped Google Play reviews — inDrive
│   │   └── survey_raw.csv               # Raw survey responses (150+ respondents)
│   └── processed/
│       ├── combined_reviews_clean.csv   # Merged & cleaned reviews (4 platforms)
│       ├── sentiment_scores.csv         # Sentiment score per review per platform
│       └── survey_encoded.csv           # Survey data ready for analysis
│
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_survey_analysis.ipynb
│   ├── 03_sentiment_analysis.ipynb
│   └── 04_competitive_synthesis.ipynb
│
├── outputs/
│   ├── figures/
│   │   ├── nps_scorecard_4platforms.png
│   │   ├── radar_chart_7dimensions.png       # 4 platform overlay
│   │   ├── sentiment_heatmap_platform_topic.png
│   │   ├── wordcloud_grab.png
│   │   ├── wordcloud_gojek.png
│   │   ├── wordcloud_maxim.png
│   │   ├── wordcloud_indrive.png
│   │   ├── feature_gap_matrix.png
│   │   └── switching_trigger_chart.png
│   └── reports/
│       └── executive_report.pdf             # Final report 10 halaman
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

### 3. Scraping data (opsional — data sudah tersedia di `data/raw/`)

```bash
jupyter notebook notebooks/01_data_collection.ipynb
```

> ⚠️ Scraping ±1.000 review per platform (total 4.000 review) membutuhkan waktu ~15–20 menit. Data hasil scraping sudah disertakan di repo untuk kemudahan reproduksi.

### 4. Jalankan pipeline secara berurutan

```bash
# Survey analysis
jupyter notebook notebooks/02_survey_analysis.ipynb

# Sentiment analysis & topic modeling
jupyter notebook notebooks/03_sentiment_analysis.ipynb

# Competitive synthesis & final output
jupyter notebook notebooks/04_competitive_synthesis.ipynb
```

### Requirements

```
pandas>=2.0
numpy>=1.24
google-play-scraper>=1.2
vaderSentiment>=3.3
transformers>=4.35
gensim>=4.3
matplotlib>=3.7
seaborn>=0.12
wordcloud>=1.9
plotly>=5.15
jupyter>=1.0
```

---

## ⚠️ Limitations & Next Steps

### Limitations

- **Sample bias:** Responden survei didominasi mahasiswa dan young professionals — tidak sepenuhnya representatif untuk segmen pekerja harian dan pengguna kota tier 3+, yang justru merupakan target utama Maxim dan inDrive.
- **Maxim & inDrive data terbatas:** Riset akademis dan benchmark publik untuk Maxim dan inDrive jauh lebih sedikit dibandingkan Grab dan Gojek — angka market share tidak sepresisi dua platform besar.
- **Review recency:** Data app review mencerminkan sentimen pada periode scraping — dapat bergeser seiring pembaruan aplikasi dan perubahan strategi promosi.
- **No behavioral data:** Analisis berbasis persepsi dan self-reported behavior, bukan data transaksi aktual.

### Potential next steps

| Ekstensi | Deskripsi |
|---|---|
| **Kota-level breakdown** | Analisis terpisah per kota untuk memahami apakah competitive gap Grab vs Maxim berbeda antara Jakarta dan Medan |
| **Driver-side research** | Survei driver untuk memahami mengapa mereka beralih ke inDrive — ancaman supply yang lebih sulit dideteksi dari sisi rider |
| **Price elasticity modeling** | Kuantifikasi seberapa besar perbedaan tarif Rp X mempengaruhi switching probability secara statistik |
| **Longitudinal tracking** | Re-survey setiap 6 bulan untuk mengukur pergeseran market share persepsi seiring dinamika promo dan fitur baru |

---

## 📬 Contact

**Devano Defrizal Yahdiyan Risyad**
Final-year Computer Science · Universitas Pendidikan Indonesia · GPA 3.60/4.00

[![LinkedIn](https://img.shields.io/badge/LinkedIn-defrizalyr-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/defrizalyr)
[![GitHub](https://img.shields.io/badge/GitHub-defrijay-181717?style=flat&logo=github)](https://github.com/defrijay)

---

*Project ini dibuat sebagai bagian dari portofolio untuk aplikasi Grab Internship Program (GIP) 2026 — Research & Data Analytics.*
