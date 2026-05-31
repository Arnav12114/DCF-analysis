# DCF Valuation Model — FCFF (Free Cash Flow to Firm)
### Built on HCL Technologies | Reusable across IT · FMCG · Pharma · Branded Consumer

---

## What This Is

A clean, fully-functional **2-phase FCFF DCF model** built from scratch in Excel.  
Originally built to value HCL Technologies (NSE: HCLTECH), but structured to be plug-and-play for any **asset-light, cash-generative, low-debt business**.

No macros. No circular references. No fluff — just the model.

---

## What's Inside

| Sheet | What it does |
|---|---|
| 📋 Cover | Key output — intrinsic value, CMP, upside/downside at a glance |
| 📊 Hist Data | 5 years of historical financials pulled from Screener.in |
| 🔑 Assumptions | Every input in one place — growth, margins, WACC, NWC, capex |
| 📈 Projections | 8-year P&L and working capital projection |
| 💰 FCF & Val | FCFF build → discounting → enterprise value → equity bridge → per share |
| 🔬 Sensitivity | Intrinsic value across a WACC × terminal growth rate grid — auto-populates |
| 📐 Beta Calc | Beta computed from weekly price data vs Nifty 50 |

---

## How the Valuation Works

```
Revenue × EBITDA Margin
→ EBIT × (1 − Tax Rate) = NOPAT
→ + D&A  − Capex  − ΔNWC  =  FCFF (Free Cash Flow to Firm)
→ Discount at WACC for 8 explicit years
→ Terminal Value via Gordon Growth Model
→ Enterprise Value = PV of FCFs + PV of Terminal Value
→ Equity Value = EV − Net Debt + Cash + Investments
→ Intrinsic Value per Share = Equity Value ÷ Shares Outstanding
```

**WACC** is built bottom-up: Risk-Free Rate + Beta × ERP (Damodaran) for cost of equity, blended with post-tax cost of debt using market-value weights.

**Working capital** is defined as operating trade-cycle NWC:  
`Trade Receivables + Inventory − Trade Payables − Advances from Customers`  
Charged on incremental revenue only — no base-year distortion.

---

## Sectors Where You Can Use This As-Is
*(change the numbers, not the structure)*

| Sector | Example Names |
|---|---|
| IT Services & Software | TCS, Infosys, Wipro, LTIMindtree, Persistent, Coforge |
| FMCG / Consumer Staples | HUL, Nestlé India, Britannia, Dabur, Marico, Colgate |
| Branded Consumer | Asian Paints, Pidilite, Titan, Page Industries, Berger |
| Pharma & Diagnostics | Sun Pharma, Cipla, Dr Reddy's, Divi's, Dr Lal PathLabs |

**Why these?** All share the same structural DNA this model is built for:
asset-light operations, stable margins, low or zero net debt, and cash flows that scale predictably with revenue.

---

## What to Change When You Switch Companies

| Input | Where |
|---|---|
| Historical financials | 📊 Hist Data — paste from Screener.in |
| Revenue growth (FY27, FY28 consensus) | 🔑 Assumptions → Section A |
| EBITDA margin assumption | 🔑 Assumptions → Section B |
| Capex % of revenue | 🔑 Assumptions → Section C |
| NWC % (operating working capital intensity) | 🔑 Assumptions → Section D |
| Risk-free rate, Beta, ERP | 🔑 Assumptions → Section F (WACC) |
| Current cash, debt, investments | 🔑 Assumptions → balance sheet inputs |
| Shares outstanding | 🔑 Assumptions → linked from Hist Data |
| Beta regression data | 📐 Beta Calc → paste weekly price data |

---

## Key Design Decisions

**Debt schedule removed.** This is an unlevered (FCFF) model — projected debt and interest never touch the valuation. The only debt figure that matters is current net cash in the equity bridge. The debt schedule that appears in many templates adds confusion without adding signal.

**Incremental NWC method.** Working capital is charged on incremental revenue (`NWC% × ΔRevenue`) rather than rebuilding the stock each year. This eliminates the one-time catch-up distortion that appears when the base-year NWC ratio differs from the projected ratio.

**Two-phase WACC.** High-growth phase uses current beta; terminal phase uses a beta-at-maturity of 1.0, reflecting the company converging to market risk over time.

**Sensitivity table auto-populates.** The WACC × terminal growth grid uses direct closed-form formulas — no Excel Data Table setup required. Works in Excel, LibreOffice, and Google Sheets.

---

## Limitations & What This Model Is NOT Suitable For

| Sector | Why it doesn't fit |
|---|---|
| Banks / NBFCs / Insurance | Debt is the raw material, not a financing choice — FCFF is meaningless |
| Metals / Mining / Oil & Gas | Earnings are commodity-price driven — DCF needs mid-cycle normalization |
| Real Estate / REITs | Value lives on the balance sheet — use NAV or cap-rate methods |
| Early-stage / pre-profit companies | Terminal value becomes ~90% of output — guesswork dressed as precision |
| Conglomerates / Holding Companies | Need sum-of-parts, not a blended cash-flow stream |

---

## Data Sources

- Historical financials: [Screener.in](https://www.screener.in)
- Risk-free rate: 10-year Government of India bond yield
- Equity Risk Premium: Damodaran (India ERP)
- Beta: Computed from weekly price returns vs Nifty 50 (3 years)

---

## Disclaimer

This model is for **educational purposes only**. It is not investment advice. All projections are assumptions — outputs are only as good as the inputs. Do your own research before making any investment decision.

---

*Built with ❤️ and a lot of FCFF.*
