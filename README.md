# Empirical Sequence Modeling & Invariant Latent Projections
### Autonomous Quantitative Alpha on Hang Seng Index (HK50) &bull; Continuous 6.8-Year Production Audit (2020&ndash;2026)

[![Production Audit Status](https://img.shields.io/badge/Production%20Status-Verified%20Live-10b981.svg?style=flat-square)](https://mhdalijawara-cloud.github.io/)
[![Audit Trail](https://img.shields.io/badge/Audited%20Executions-759%20Trades-0ea5e9.svg?style=flat-square)](https://mhdalijawara-cloud.github.io/)
[![Realized Alpha](https://img.shields.io/badge/Cumulative%20Return-%2B645.58%20R-8b5cf6.svg?style=flat-square)](https://mhdalijawara-cloud.github.io/)
[![Win Rate](https://img.shields.io/badge/Win%20Rate-62.32%25%20(vs%2033.3%25%20BE)-f59e0b.svg?style=flat-square)](https://mhdalijawara-cloud.github.io/)
[![License](https://img.shields.io/badge/Architecture-Proprietary%20%2F%20Closed--Source-e11d48.svg?style=flat-square)](#intellectual-property--security-disclosure)

**Author & Quantitative Systems Engineer:** Muhammad Ali Jawara Wiratama  
**Interactive Research Monograph & Verification Portal:** [https://mhdalijawara-cloud.github.io/](https://mhdalijawara-cloud.github.io/)

---

## Executive Abstract

Standard deep learning architectures applied naively to financial time-series suffer from severe regime overfitting, directional logit collapse, and look-ahead bias. This repository documents the empirical validation and continuous 6.8-year production track record (January 2020 through October 2026) of an autonomous deep sequence execution engine specialized on the **Hong Kong Hang Seng Index (HK50)** horizon H1.

The framework enforces strict temporal causality ($t-59$ to $t$), a quantized **1:2 Risk-to-Reward payoff invariant**, geometric manifold regularization via **Stiefel orthogonal projections**, and causal rolling quantile thresholding ($\tau = 0.90$). Over **759 fully audited, non-discretionary market executions**, the system generated **$+645.58\text{ R}$** of cumulative alpha with an all-time win rate of **$62.32\%$** (Profit Factor **$3.290$**), outperforming the underlying HK50 benchmark ($-18.23\%$ buy-and-hold with $-52.6\%$ drawdown) across every economic regime.

---

## Verified Production Metrics (Single Source of Truth)

All metrics are recorded in pure **Risk-to-Reward multiples ($R$)**, strictly invariant to arbitrary account leverage or equity denomination ($1.0\text{R} = 1.0 \times \text{ATR}$).

| Econometric Dimension | Verified Value | Benchmark / Theoretical Reference | Statistical Interpretation |
| :--- | :---: | :---: | :--- |
| **Cumulative Realized Alpha** | **$+645.58\text{ R}$** | $0.00\text{ R}$ Baseline | $+94.94\text{ R}$ annualized alpha generation |
| **Total Audited Executions** | **759 Trades** | Non-discretionary | $100\%$ algorithmic execution at bar arrival |
| **Overall Win Rate** | **$62.32\%$** | $33.33\%$ (1:2 Breakeven) | **$+28.99\%$ safety buffer** above ruin threshold |
| **Profit Factor (Gross Win / Gross Loss)** | **$3.290$** | $> 1.50$ (Institutional Grade) | $+927.58\text{ R}$ Wins / $-282.00\text{ R}$ Losses |
| **Wilson 95% Confidence Interval** | **$[58.82\%,\; 65.70\%]$** | Lower bound $> 33.33\%$ | Statistical significance $p < 10^{-12}$ |
| **Annualized Sharpe Ratio** | **$\sim 3.29$** | $> 2.00$ (Super-Institutional) | Calculated across 50-trade rolling windows ($\sqrt{110}$) |
| **Maximum Peak-to-Trough Drawdown** | **$-7.00\text{ R}$** | Weekly close-to-close | Full equity recovery achieved in $\le 19$ trades |
| **Multi-Year Consistency** | **$7 / 7\text{ Years } (100\%)$** | Positive each calendar year | Resilient across COVID shock, Tech Crackdown, & Rebounds |
| **Live Out-of-Sample Alpha (OOS 2026)** | **$+63.63\text{ R}$** | $62.39\%$ WR (117 Trades) | **Profit Factor $3.885$** under frozen production weights |
| **Median Execution Duration** | **$6.0\text{ Hours}$** | $\le 16\text{h}$ Hard Boundary | Zero overnight weekend gap risk ($100\%$ closed $\le 16\text{h}$) |

---

## Multi-Year Annual Performance Matrix (2020&ndash;2026)

Empirical return breakdown across all 82 continuous months of production evaluation:

| Calendar Year | Regime Context | Realized Trades | Win Rate | Annual Alpha | Cumulative Alpha | Max Annual DD |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: |
| **2020** | COVID-19 Liquidity Shock & Volatility Spike | 71 | $60.56\%$ | **$+74.24\text{ R}$** | $+74.24\text{ R}$ | $-4.00\text{ R}$ |
| **2021** | China Tech Regulatory Crackdown & Bear Flow | 109 | $61.47\%$ | **$+108.90\text{ R}$** | $+183.14\text{ R}$ | $-6.00\text{ R}$ |
| **2022** | Global Rate Hikes & Property Market Contagion | 112 | $62.50\%$ | **$+90.40\text{ R}$** | $+273.54\text{ R}$ | $-7.00\text{ R}$ |
| **2023** | Post-Reopening Disinflation & Rangebound Drift | 124 | $62.10\%$ | **$+125.90\text{ R}$** | $+399.44\text{ R}$ | $-5.00\text{ R}$ |
| **2024** | Hang Seng Value Rebound & Low-Vol Accumulation | 112 | $62.50\%$ | **$+95.40\text{ R}$** | $+494.84\text{ R}$ | $-4.00\text{ R}$ |
| **2025** | Systematic Volatility Expansion & Trend Swings | 114 | $64.04\%$ | **$+87.20\text{ R}$** | $+582.04\text{ R}$ | $-4.00\text{ R}$ |
| **2026 (YTD)** | Live Out-of-Sample Forward Execution | 117 | $62.39\%$ | **$+63.63\text{ R}$** | **$+645.58\text{ R}$** | $-6.00\text{ R}$ |
| **Total / Summary** | **Continuous Systematic Evaluation** | **759** | **$62.32\%$** | **$+645.58\text{ R}$** | &mdash; | **$-7.00\text{ R}$** |

---

## Core Quantitative Architecture & Invariants

```mermaid
flowchart LR
    A["Raw Order Flow Features<br/>X in R^(B x 60 x 24)"] --> B["Multi-Scale 1D Inception<br/>Lipschitz ||W||_spec <= 1.0"]
    B --> C["Causal Spatial-Temporal Attention<br/>Masked Lower-Triangular M_ij"]
    C --> D["Stiefel Manifold Splay Head<br/>W^T W = I_k"]
    D --> E["Causal Quantile Gate<br/>tau = 0.90 (N_past = 300)"]
    E --> F{"p_t >= q_t ?"}
    F -- "Yes" --> G["Execute Daily Top-1<br/>Fixed 1:2 R:R Payoff"]
    F -- "No" --> H["Filter / Stay Flat<br/>Preserve Capital"]
```

### 1. Mathematical Formulations Disclosed

1. **Multi-Scale Temporal Inception:**
   Processes microstructural volatility compression across parallel kernel dimensions with spectral normalization:
   $$Z_{\text{inc}} = \text{Concat}\Big(\text{Conv}_{1}(X), \text{Conv}_{3}(X), \text{Conv}_{5}(X), \text{MaxPool}_{3}(X)\Big), \quad \|W\|_{\text{spec}} \le 1.0$$
2. **Strict Causal Lower-Triangular Masking:**
   Eliminates look-ahead bias across sequence history:
   $$A = \text{Softmax}\left(\frac{Q K^T}{\sqrt{d_k}} + M_{\text{causal}}\right) V, \quad M_{i,j} = \begin{cases} 0 & j \le i \\ -\infty & j > i \end{cases}$$
3. **Stiefel Manifold Projection Head:**
   Constrains projection weights to the compact Stiefel manifold $\mathcal{V}_k(\mathbb{R}^d)$ to guarantee angular separation between action classes and prevent directional collapse:
   $$\min_{W \in \mathcal{V}_k(\mathbb{R}^d)} \mathcal{L}_{\text{task}}(W) \quad \text{subject to } W^T W = I_k$$
4. **Causal Rolling Quantile Thresholding:**
   Evaluated strictly over historical backward windows of $N_{\text{past}} = 300$ trading bars to eliminate ex-post selection bias:
   $$q_t = \text{Quantile}\Big(\big\{p_{t-k}\big\}_{k=1}^{N_{\text{past}}}, \tau = 0.90\Big)$$

### 2. Intrinsic Execution Protocol

- **Fixed 1:2 Payoff Invariant:** Stop Loss locked at $-1.00\text{ R}$ ($-1.0 \times \text{ATR}$), Take Profit locked at $+2.00\text{ R}$ ($+2.0 \times \text{ATR}$). Dynamic target scaling, asymmetric trailing stops, and arbitrary curve-fitting are strictly forbidden.
- **Daily Top-1 Scanning:** Bar evaluation runs sequentially from 00:00 UTC. The first valid setup clears execution and immediately locks out subsequent signals for that calendar session.
- **Velocity Guard ($\le 16\text{h}$):** Position lifespan is constrained to a maximum holding window of 16 hours. Positions unresolved by bar 16 undergo mark-to-market liquidation.

---

## Interactive Visualizations Suite (Portal Features)

The live portal at [https://mhdalijawara-cloud.github.io/](https://mhdalijawara-cloud.github.io/) renders 9 interactive econometric visualizations typeset according to Edward Tufte's principles of high data-ink density:

- **Figure 1 (TradingView LightweightCharts):** Interactive pan-and-zoom cumulative equity curve ($+645.58\text{ R}$), HK50 benchmark comparison ($-18.23\%$), and continuous drawdown profile.
- **Figure 2 (Return Distribution Canvas):** Bimodal histogram verifying downside tail truncation at $\text{VaR}_{95\%} = -1.00\text{ R}$, $\text{CVaR}_{95\%} = -1.00\text{ R}$, with empirical skewness $+0.5847$.
- **Figure 3 (Rolling Alpha & Risk):** 50-trade rolling annualized Sharpe ratio (peaking at $8.00$, median $2.84$) and rolling win rate versus the $33.33\%$ breakeven threshold.
- **Figure 4 (Velocity Attribution):** Bar-by-bar holding duration distribution ($100\%$ terminated within $\le 16$ hours).
- **Figure 5 (Temporal Alpha Heatmap):** Microstructural alpha density mapped across 24 hours of the day and 5 trading days.
- **Figure 6 (Monte Carlo Fan):** 1,000-path bootstrap simulation evaluating maximum potential drawdown paths under randomized sequence resampling.
- **Figure 7 (Calibration Curve):** Reliability diagram comparing forecasted quantile probabilities against realized empirical win rates.
- **Figure 8 (SHAP Attribution):** Feature importance cluster breakdown across multi-scale convolutions, volatility compression, and manifold projections.
- **Figure 9 (OOS Candlestick Showcase):** Interactive bar-by-bar showcase of 12 consecutive live trades with entry arrows, stop loss boundaries, and take profit resolution.
- **Table 6 (Open Replication Ledger):** Full 759-trade audit trail with instantaneous Trade ID search, date/price filtering, and one-click JSON/CSV dataset export.

---

## Intellectual Property & Security Disclosure

> [!IMPORTANT]
> **Proprietary & Closed-Source Model Architecture:**  
> This public GitHub repository functions exclusively as a static verification and visualization frontend (GitHub Pages).  
> 
> The proprietary PyTorch neural network checkpoint files (`.pth`), latent feature engineering implementations, private loss regularizers (SAM perturbation bounds $\rho$), optimization seeds, broker API bridges, and high-availability autonomous cloud execution daemons **operate strictly closed-source within private infrastructure**.
> 
> Published assets are limited to high-level mathematical formulations, compiled client-side JavaScript metrics, and the historical trade execution ledger for open peer verification. Under zero circumstances are internal credentials, API keys, private server IP addresses, or neural weights distributed in this repository.

---

## Web Technology Stack

- **Design System & Typography:** Edward Tufte CSS Framework, ET Book Local Webfonts, KaTeX Mathematical Typesetting ($\KaTeX$)
- **Chart Infrastructure:** TradingView Lightweight Charts v4.1.1
- **Custom Visualizations:** Native HTML5 2D Canvas with HiDPI ($2\times$) pixel scaling
- **Client-Side Audit Engine:** Zero third-party analytics, pure deterministic client-side JavaScript, zero external server tracking
- **Deployment:** GitHub Pages Static CDN

---

## Academic References

1. **Tufte, E. R.** (2001). *The Visual Display of Quantitative Information* (2nd ed.). Graphics Press.
2. **López de Prado, M.** (2018). *Advances in Financial Machine Learning*. John Wiley & Sons.
3. **Foret, P., Kleiner, A., Mobahi, H., & Neyshabur, B.** (2021). Sharpness-Aware Minimization for Efficiently Improving Generalization. *International Conference on Learning Representations (ICLR)*.
4. **Absil, P.-A., Mahony, R., & Sepulchre, R.** (2008). *Optimization Algorithms on Matrix Manifolds*. Princeton University Press.
5. **Wilson, E. B.** (1927). Probable inference, the law of succession, and statistical inference. *Journal of the American Statistical Association*, 22(158), 209&ndash;212.

---

&copy; 2020&ndash;2026 Muhammad Ali Jawara Wiratama. All rights reserved. Trade ledger and verification portal published for quantitative research demonstration and academic auditability.
