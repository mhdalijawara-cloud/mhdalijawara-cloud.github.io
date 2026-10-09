# Quantitative Systems Research Portfolio & Verification Portal

Portal verifikasi web publik untuk rekam jejak model runtun waktu kuantitatif pada Hang Seng Index (HK50).

Live Portal: [https://mhdalijawara-cloud.github.io/](https://mhdalijawara-cloud.github.io/)

---

## Scope & Proprietary Architecture

Repositori ini berfungsi secara eksklusif sebagai antarmuka web statis (GitHub Pages) untuk memvisualisasikan dan memverifikasi rekam jejak performa secara transparan di sisi browser.

Arsitektur model machine learning, bobot checkpoint PyTorch (`.pth`), pipeline pelatihan fitur laten, serta router eksekusi live beroperasi secara tertutup (*closed-source*) pada infrastruktur privat. Kode dalam repositori ini terbatas pada rendering visual antarmuka pengguna, kalkulasi metrik audit di sisi klien, dan tipografi matematika KaTeX.

---

## Metodologi Pemodelan & Protokol Eksekusi

Model difokuskan pada instrumen Hang Seng Index (HK50) horizon H1 di bawah empat protokol kuantitatif:

1. **Kausalitas Murni (Zero Look-Ahead Bias):** Fitur input diekstraksi strictly dari jendela observasi $t-59$ s.d. $t$. Ambang batas seleksi logit dihitung menggunakan *rolling past quantile* tanpa parameter masa depan.
2. **Ketetapan Payoff 1:2 R:R:** Setiap posisi terikat pada batasan terkuantisasi: Stop Loss $-1.0\text{R}$ dan Take Profit $+2.0\text{R}$.
3. **Daily Top-1 Scanning:** Evaluasi bar berjalan kronologis dari 00:00 UTC. Sinyal valid pertama yang melampaui ambang batas langsung dieksekusi dan mengunci sisa hari perdagangan.
4. **Velocity Guard ($\le 16\text{ Jam}$):** Durasi holding posisi dibatasi maksimal 16 jam dengan *hard time-exit mark-to-market*.

---

## Ringkasan Verifikasi Rekam Jejak (2020 – 2026)

| Metrik | Nilai Terverifikasi | Keterangan / Benchmark |
| :--- | :---: | :--- |
| **All-Time Realized Return** | **+643.85 R** | Akumulasi unit Risk-to-Reward murni |
| **Konsistensi Tahunan** | **7 / 7 Tahun (100%)** | Positif setiap tahun berturut-turut (2020–2026) |
| **All-Time Win Rate** | **62.38%** | Titik breakeven payoff 1:2 adalah $33.33\%$ |
| **Wilson 95% Confidence Interval** | **[58.87%, 65.75%]** | Lower bound $> 33.33\%$ ($p < 10^{-12}$) |
| **Annualized Sharpe Ratio** | **~3.30** | Distribusi performa mingguan |
| **Out-of-Sample (OOS 2026)** | **+61.91 R (52.2% WR)** | Profit Factor $2.183$ pada data un-seen |
| **Max Drawdown (All-Time)** | **-7.00 R** | Weekly close-to-close drawdown |
| **Rerata Durasi Holding** | **6.2 Jam** | 100% posisi tuntas dalam $\le 16$ jam |

---

## Stack Teknologi Web

- UI & Styling: HTML5, Tailwind CSS
- Visualisasi: Chart.js
- Tipografi Matematika: KaTeX
- Hosting: GitHub Pages
