# Quantitative Systems Research Portfolio & Verification Portal

[![Live Portal](https://img.shields.io/badge/Live_Portal-mhdalijawara--cloud.github.io-blue?style=for-the-badge&logo=google-chrome&logoColor=white)](https://mhdalijawara-cloud.github.io/)
[![Asset Focus](https://img.shields.io/badge/Asset_Focus-Hang_Seng_Index_(HK50)-orange?style=for-the-badge)](https://mhdalijawara-cloud.github.io/)
[![Payoff Structure](https://img.shields.io/badge/Risk_Reward-1:2_Fixed_R:R-emerald?style=for-the-badge)](https://mhdalijawara-cloud.github.io/)
[![Validation](https://img.shields.io/badge/Verification-7/7_Years_Consistent-purple?style=for-the-badge)](https://mhdalijawara-cloud.github.io/)

Official interactive performance showcase and track record verification portal for deep quantitative sequence modeling on index futures.

🌐 **Interactive Portal:** [https://mhdalijawara-cloud.github.io/](https://mhdalijawara-cloud.github.io/)

---

## ⚠️ Proprietary Intellectual Property & Repository Scope Notice

> **IMPORTANT NOTICE REGARDING CODEBASE AND MODEL WEIGHTS:**
> 
> Repositori publik ini **hanya berfungsi sebagai portal statis visualisasi dan verifikasi rekam jejak (Track Record Verification Portal)** yang di-host via GitHub Pages.
> 
> * **Model Weights & Checkpoints:** Seluruh bobot model (`.pth`), arsitektur neural network inti (Transformer latent representations, manifold projections, Stiefel regularization), dan skrip pelatihan machine learning bersifat **PROPRIETARY & CLOSED-SOURCE**. File model tidak disimpan dan tidak dipublikasikan di repositori publik ini.
> * **Execution & Data Infrastructure:** Pipeline inferensi real-time, live execution router, serta feed data frekuensi tinggi beroperasi secara terisolasi pada lingkungan infrastruktur privat.
> * **Public Scope:** Kode pada repositori ini terbatas pada antarmuka pengguna interaktif (*client-side UI*), visualisasi chart/heatmap, kalkulasi verifikasi audit di sisi browser, dan rendering KaTeX untuk kebutuhan transparansi rekam jejak.

---

## 🔬 Research Focus: HK50 H1 Sequence Specialist

Sistem kuantitatif ini difokuskan secara spesifik pada instrumen **Hang Seng Index (HK50)** pada horizon per jam (**H1**). Seluruh proses pemodelan, rekayasa fitur, dan kalibrasi inferensi dirancang di bawah protokol keilmuan kuantitatif yang ketat:

1. **100% Kausalitas Murni (Zero Look-Ahead Bias):** Seluruh input tensor diekstraksi strictly dari jendela masa lalu ($t-59$ s.d. $t$). Ambang batas seleksi logit dihitung menggunakan *Rolling Past Quantile* kausal ($N_{\text{past}}$ bar historis) tanpa peeking ke masa depan.
2. **Ketetapan Sakral Payoff 1:2 R:R:** Setiap posisi terikat pada parameter risiko terkuantisasi pasti: Stop Loss $-1.0\text{R}$ dan Take Profit $+2.0\text{R}$. Tidak ada modifikasi rasio sepihak atau trailing asimetris.
3. **Daily Top-1 Execution:** Memindai bar secara kronologis dari awal hari (00:00 UTC) dan langsung mengeksekusi sinyal valid pertama yang melampaui ambang batas kausal, mengunci sisa hari untuk membatasi *turnover* dan biaya transaksi.
4. **Velocity Guard ($\le 16\text{ Jam}$):** Seluruh posisi dibatasi dengan *Hard Time-Exit Mark-to-Market* maksimal di jam ke-16, melindungi portofolio dari *overnight holding decay* dan fluktuasi multi-hari yang tidak diinginkan.

---

## 📊 Summary Track Record (2020 – 2026)

| Metric | Verified Empirical Track | Standard Benchmark / Edge |
| :--- | :---: | :--- |
| **All-Time Realized Return** | **+643.85 R** | Akumulasi unit Risk-to-Reward murni |
| **Annual Consistency** | **7 / 7 Years (100%)** | Positif setiap tahun berturut-turut (2020–2026) |
| **All-Time Win Rate** | **62.38%** | Jauh di atas titik breakeven payoff 1:2 ($33.33\%$) |
| **Wilson 95% Confidence Interval** | **[58.87%, 65.75%]** | Lower bound $> 33.33\%$ ($p < 10^{-12}$) |
| **Annualized Sharpe Ratio** | **~3.30** | Dihitung dari distribusi performa mingguan |
| **Out-of-Sample (OOS 2026)** | **+61.91 R (52.2% WR)** | Profit Factor $2.183$ pada data un-seen |
| **Max Drawdown (All-Time)** | **-7.00 R** | Weekly close-to-close drawdown terkontrol |
| **Average Holding Duration** | **6.2 Jam** | 100% posisi tuntas dalam $\le 16$ jam |

*Catatan: Seluruh data metrik di atas bersumber langsung dari audit historis bar-demi-bar yang dapat diverifikasi secara interaktif di [portal web](https://mhdalijawara-cloud.github.io/).*

---

## 💻 Tech Stack Portal Web

* **Visual UI:** HTML5, Tailwind CSS, Heroicons
* **Rendering & Charts:** Chart.js, KaTeX (LaTeX math typography)
* **Hosting:** GitHub Pages

---

## 📬 Contact & Inquiries

Untuk diskusi riset kuantitatif, kolaborasi profesional, atau verifikasi metodologi, hubungi melalui profil GitHub resmi atau kontak profesional yang tertera pada portal.
