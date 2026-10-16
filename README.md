# Quantitative Systems Research Portfolio & Verification Portal

Portal verifikasi web publik untuk rekam jejak model runtun waktu kuantitatif pada Hang Seng Index (HK50).

Live Portal: [https://mhdalijawara-cloud.github.io/](https://mhdalijawara-cloud.github.io/)

---

## Scope & Proprietary Architecture

Repositori ini berfungsi secara eksklusif sebagai antarmuka web statis (GitHub Pages) bergaya monograf riset Edward Tufte untuk memvisualisasikan dan mengaudit rekam jejak performa secara transparan di sisi browser klien.

> **Batasan Lisensi & Kekayaan Intelektual (Proprietary / Closed-Source):**  
> Seluruh bobot checkpoint neural PyTorch (`.pth`), pipeline rekayasa 24 fitur laten, benih optimasi (*optimization seeds*), serta daemon eksekusi live beroperasi secara tertutup (*strictly closed-source*) pada infrastruktur server privat. Kode dalam repositori publik ini terbatas pada visualisasi antarmuka pengguna, format audit ekonometrika, dan tipografi matematika KaTeX.

---

## Metodologi Pemodelan & Protokol Eksekusi

Model difokuskan pada instrumen Hang Seng Index (HK50) horizon H1 di bawah empat protokol kuantitatif:

1. **Kausalitas Murni (Zero Look-Ahead Bias):** Fitur input diekstraksi strictly dari jendela observasi $t-59$ s.d. $t$. Ambang batas seleksi dihitung menggunakan *rolling past quantile* tanpa parameter masa depan.
2. **Ketetapan Payoff 1:2 R:R:** Setiap posisi terikat pada batasan terkuantisasi: Stop Loss $-1.0\text{R}$ dan Take Profit $+2.0\text{R}$.
3. **Daily Top-1 Scanning:** Evaluasi bar berjalan kronologis dari 00:00 UTC. Sinyal valid pertama yang melampaui ambang batas langsung dieksekusi dan mengunci sisa hari perdagangan.
4. **Velocity Guard ($\le 16\text{ Jam}$):** Durasi holding posisi dibatasi maksimal 16 jam dengan *hard time-exit mark-to-market*.

---

## Ringkasan Verifikasi Rekam Jejak (2020 – 2026)

*Update Terkini: 16 Oktober 2026 (759 Trades Terverifikasi)*

| Metrik | Nilai Terverifikasi | Keterangan / Benchmark |
| :--- | :---: | :--- |
| **All-Time Realized Return** | **+645.58 R** | Akumulasi unit Risk-to-Reward murni (759 trades) |
| **Konsistensi Tahunan** | **7 / 7 Tahun (100%)** | Positif setiap tahun berturut-turut (2020–2026) |
| **All-Time Win Rate** | **62.32%** | 473 Menang / 286 Kalah (Titik breakeven payoff 1:2 adalah $33.33\%$) |
| **Profit Factor** | **3.290** | Gross Win / Gross Loss murni dalam satuan R |
| **Wilson 95% Confidence Interval** | <nobr>**[58.82%,&nbsp;65.70%]**</nobr> | Lower bound jauh di atas $33.33\%$ ($p < 10^{-12}$) |
| **Annualized Sharpe Ratio** | **~3.29** | Rerata Sharpe rolling 50-trade terskalakan $\sqrt{110}$ |
| **Out-of-Sample (OOS 2026)** | **+63.63 R (62.39% WR)** | Profit Factor $3.885$ pada data un-seen 2026 (117 trades) |
| **Max Drawdown (All-Time)** | **-7.00 R** | Trough drawdown terdalam sepanjang 6.8 tahun |
| **Rerata Durasi Holding** | **6.5 Jam** | $100.0\%$ posisi selesai tuntas dalam $\le 16$ jam |

---

## Stack Teknologi Web

- **Desain & Tipografi:** Edward Tufte CSS Framework, ET Book Local Webfonts, KaTeX Mathematical Typesetting
- **Grafik Finansial:** TradingView Lightweight Charts v4.1.1 (Interaktif: Equity, Underwater Drawdown, HK50 Benchmark)
- **Visualisasi Ekonometrika 2D Canvas:**
  - Figure 2: Empirical Return Distribution (Bimodal Payoff & VaR 95%)
  - Figure 3: 50-Trade Rolling Win Rate vs Breakeven & Rolling Sharpe
  - Figure 4: Trade Duration Velocity Attribution
  - Figure 5: 24-Hour $\times$ 5-Day Alpha Microstructure Heatmap
  - Figure 6: Monte Carlo 1,000-Path Drawdown Fan
  - Figure 7: Signal Calibration / Reliability Diagram
  - Figure 8: Feature Attribution Cluster Importance
  - Figure 9: OOS Live Candlestick Trade Execution Showcase
- **Hosting:** GitHub Pages
