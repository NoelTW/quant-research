# Purged Walk-Forward Ensembles, Kyle's Lambda Microstructure Impact, and Cross-Market Regime Governance

[![Working Paper](https://img.shields.io/badge/Working_Paper-2026--11_(Post--Audit_Edition)-0284c7?style=flat-square)](https://noeltw.github.io/quant-research/)
[![Purged OOS](https://img.shields.io/badge/Purged_Walk--Forward_&_3--Phase_Audited-Validated-059669?style=flat-square)](https://noeltw.github.io/quant-research/)
[![Read Paper](https://img.shields.io/badge/Interactive_Paper-GitHub_Pages-black?style=flat-square&logo=github)](https://noeltw.github.io/quant-research/)

**Author:** Noel Yang  
*Senior Data Scientist @ Micron Technology (Singapore) &bull; Autonomous AI & Systematic Quantitative Systems*  
Correspondence: `noelyang0208@gmail.com` | [GitHub: @NoelTW](https://github.com/NoelTW)

---

### 📖 [Read the Full Interactive Research Whitepaper (Distill / Academic Format) ↗](https://noeltw.github.io/quant-research/)

---

## 📌 Executive Summary & Anti-Overfitting Audit Note

> **Methodological Revision (November 2026 — EXP-026 / EXP-029 / EXP-030 / EXP-031):**  
> Earlier single-cutoff tree ensembles in emerging markets are susceptible to subtle lookahead contamination, thin-liquidity micro-cap fills, and rebalance-weekday calendar luck. This revised working paper documents a rigorous **first-principles anti-overfitting purge** across 130+ multi-phase stress tests—enforcing **Purged Walk-Forward Cross-Validation**, a **NT\$30M 20-day average turnover floor**, **Kyle's Lambda volume-normalized institutional impact**, **3-Phase (`P0/P1/P2`) staggered parallel-universe evaluation**, and **online-offline PSI serving-skew telemetry (`Rank-Norm PSI = 0.0020`)**.

Rather than forcing a single model across incompatible market microstructures, our production architecture exploits **Tax-and-Friction Asymmetry** across two orthogonal engines:

1. **Engine I — Taiwan Mid-Cap Value-Growth (`Titan-4S` / `TWSE & TPEx`)**:  
   Given Taiwan's round-trip transaction friction (~`0.395%` including `0.30%` statutory disposal tax), alpha is harvested on a **3-week low-churn horizon** among liquid mid-cap hidden champions (`Price <= NT$250`, `20d Turnover >= NT$30M`). A double-neutralized (28 sub-sectors + log-cap) multi-task GBDT ensemble + **Left-Tail Crash Risk Head** is paired with **Kyle's Lambda institutional flow normalization** ($\overline{Q}_{3d} / \overline{V}_{20d}$) and structural moving-average ribbon hysteresis (`MA20 > MA70 > MA120`).
2. **Engine II — US Leveraged Macro Gearbox (`TQQQ-007 M14-Apex` / `NASDAQ-100`)**:  
   In zero-stamp-tax US ETF markets (`0%` transaction tax, `0%` Singapore capital gains), global mega-cap AI/tech beta is captured via an **Asymmetric 180-SMA Hysteresis Gate (`+1.0% / -0.5%`)**, a **4-Speed Realized Volatility Gearbox**, and a **3D Cross-Asset Credit/Duration/FX Shield** (`HYG/IEF`, `IEF/TLT`, `FXY` Yen-carry unwind, `CBOE VIX/VIX3M` term structure), parking defensive capital in `0.07%`-fee `SGOV` T-Bills (with an optional temporally orthogonal `GLD/UUP` Crisis-Alpha sleeve).

---

## 📊 Audited Performance Attribution (Net of Full Taxes, Commissions & Slippage)

### Table 1A: Taiwan Equities Engine (`Titan-4S`, Unlevered Cash Equities)

| Performance Metric | Double-Ortho Linear White-Box | High-Price (`>NT$250`) AI Moat | **`Titan-4S` (Purged + Kyle's $\lambda$)** | TAIEX Benchmark |
| :--- | :---: | :---: | :---: | :---: |
| **Full-Cycle Audited CAGR** | +23.83% | +9.71% | **+53.08%** | +13.48% |
| **Strict Post-Freeze OOS CAGR (`2024–2026`)** | +30.15% | +45.63% | **+68.77%** | +21.40% |
| **3-Phase (`P0/P1/P2`) Staggered Mean CAGR** | +19.86% | +14.57% | **+42.17%** | +13.48% |
| **Daily Sharpe Ratio** | 1.15 | 0.43 | **2.34** | 0.68 |
| **Maximum Drawdown (Full / OOS)** | -26.63% | -64.12% | **-12.13% / -10.75%** | -32.50% |
| **Calmar Ratio ($\text{CAGR} / \|\text{MDD}\|$)** | 0.89 | 0.15 | **4.38** | 0.41 |
| **2022 Tightening Bear Market** | -18.24% | -46.33% | **+5.23% (Cash Lock)** | -22.40% |

### Table 1B: US Macro Volatility Gearbox (`TQQQ-007 M14-Apex`, `±15%` Tolerance Band + `D+1` Execution)

| Performance Metric (`2016–2026`) | Buy & Hold `TQQQ` | Pure Price Vol-Targeting | **`TQQQ-007` (`TQQQ + SGOV`)** | **`TQQQ-007` + Crisis Sleeve (`GLD/UUP`)** |
| :--- | :---: | :---: | :---: | :---: |
| **Full-Cycle Audited CAGR** | +38.40% | +31.76% | **+55.10%** | **+56.41%** |
| **`2022–2026` Out-of-Sample CAGR** | +14.20% | +27.42% | **+43.65%** | **+48.77%** |
| **Maximum Drawdown (MDD)** | -81.65% | -32.98% | **-29.88%** | **-30.34%** |
| **Daily Sharpe / Calmar Ratio** | 0.76 / 0.47 | 0.95 / 0.96 | **1.30 / 1.84** | **1.33 / 1.86** |
| **2022 Rate-Shock Bear Market** | -79.08% | -12.78% | **-6.10% (`SGOV` Shelter)** | **+1.07% (Positive Crisis Alpha)** |

---

## 📈 Empirical Figures

### Figure 1: Audited Cumulative Wealth Trajectories (Log Scale)
![Cumulative Out-of-Sample Performance](fig_performance.svg)

### Figure 2: Comparative Underwater Drawdown Profile
![Underwater Drawdown Profile](fig_drawdown.svg)

### Figure 3: Cross-Market Regime & Volatility Governance Automaton
![State Machine](fig_state_machine.svg)

### Figure 4: Microstructure Asymmetry & Continuous Cap-Rank Weighting
![Size Adaptive Weights](fig_size_weights.svg)

---

## 🔬 Key First-Principles Findings & Falsified Hypotheses

* **Dimensional Flaw in Raw Institutional Share Counts (Kyle's Lambda Fix)**: Ranking net institutional buying by raw share counts overweights cheap mega-float stocks (`1,000` lots of a `NT$15` stock `< 1%` ADV) over genuine institutional accumulation in mid-caps (`400` lots of a `NT$180` stock `= 25%` ADV). Normalizing 3-day institutional flow by 20-day volume ($\overline{Q}_{3d} / \overline{V}_{20d}$) lifted OOS CAGR by **`+2.07%`** and 3-phase staggered CAGR by **`+1.49%`** with zero extra parameters.
* **Why High-Priced (`> NT$250`) Taiwan AI Leaders Fail Unhedged**: Although a `> NT$250` high-multiple moat portfolio returned `+45.63%` during `2024–2026`, it suffered a **`-64.12%` MDD (`-46.33%` in 2022)** because crowded foreign-owned long-duration equities collapse during global rate shocks. Allocating long-duration tech beta to the tax-free, macro-hedged US `TQQQ-007` engine while restricting Taiwan to `<= NT$250` value-growth champions is strictly Pareto-dominant.
* **Eliminating Rebalance-Day Overfitting via 3-Phase Parallel Universes**: Testing every structural change across all 3 staggered 3-week rebalance phases (`P0`, `P1`, `P2`) prevented calendar-phase overfitting and validated `4` equal-weighted positions with an `8`-rank retention buffer as the global Pareto optimum.

---

## 📚 Citation

```bibtex
@article{yang2026dualengine,
  title   = {Purged Walk-Forward Ensembles, Kyle's Lambda Microstructure Impact, and Cross-Market Regime Governance},
  author  = {Yang, Noel},
  journal = {Working Paper Series in Quantitative Finance},
  year    = {2026},
  number  = {2026-11},
  url     = {https://noeltw.github.io/quant-research/}
}
```
