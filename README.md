# Research & Valuation Portfolio — SUN Chuanchang

MSc Finance, HKUST (graduating Aug 2027) · seeking **part-time internships, 2–3 days a week** in operations, compliance, settlement support and research · csunaw@connect.ust.hk

**Start here — one-page summary:** [portfolio_summary.pdf](portfolio_summary.pdf)

Three work samples, built to show analytical output rather than coursework: one valuation model, one macro note, one investment memo. Each one states its own assumptions, so a reader can disagree with a number and see exactly where it came from.

| Work sample | What it shows | Format |
|---|---|---|
| [LiNing_2331HK_Valuation_Model.xlsx](LiNing_2331HK_Valuation_Model.xlsx) | 5-year FCFF DCF, WACC build-up, 5×5 sensitivity, trading comparables | Excel, 3 sheets |
| [macro_memo.pdf](macro_memo.pdf) | China PPI vs CPI and Hong Kong's imported rate path: 3 charts, 3 conclusions, monitoring list | 3-page PDF |
| [bolivia_investment_memo.pdf](bolivia_investment_memo.pdf) | Measuring inflation in a pegged economy and sizing a two-factor hedge | 1-page PDF |

## 1. Li Ning (2331.HK) — valuation model
- Base year FY2024A from company annual results; FY2025E–FY2029E are my assumptions, all inputs live in blue cells.
- WACC 9.77% (rf 2.5%, ERP 7.0%, beta 1.20, cost of debt 4.5%, D/V 15%), terminal growth 2.5%.
- Output: EV RMB 41.9bn, equity RMB 50.4bn, **HK$21.17 per share vs HK$18.50 market price (+14.4%)**; the sensitivity grid spans WACC 7.5–9.5% and g 2.0–4.0%, and shows where the thesis breaks.
- Reproduce: `python build_model.py` (openpyxl); recalculate with LibreOffice.

## 2. Macro note — "China reflation is upstream, Hong Kong's policy is imported"
- China Oct-2026 CPI +0.7% y/y against PPI +5.7% y/y: pricing power sits upstream, consumer brands face price parity.
- HKMA base rate 4.25% held with the Fed; the LERS imports US policy even as HK GDP decelerates (5.9% → 4.3% → 5.2%).
- Conclusion: screen China on gross-margin direction and cost pass-through, Hong Kong on domestic demand rather than rate-sensitive sectors.
- Reproduce: `python gen_macro_memo.py` → HTML → PDF. Charts are hand-built SVG, no chart library.

## 3. Bolivia — inflation measurement and hedging
- In a dollarised, pegged economy the CPI understates the inflation an investor actually bears; the adjustment runs through FX access and shortages.
- Method: decompose CPI against the GDP deflator, test transmission through the parallel FX premium and reserve coverage, then size a two-factor hedge.
- Reproduce: `python gen_bolivia_memo.py`; the [markdown version](bolivia_investment_memo.md) is ready to paste into a note.

## How this connects
The three pieces are one chain: how to value a cash-flow stream (Li Ning), what discount rate a Hong Kong investor should demand and why it is imported (macro note), and what happens to that discount rate when the currency is pegged and inflation is measured badly (Bolivia).

## Notes
- Data: National Bureau of Statistics of China (Oct-2026 CPI/PPI release), HKMA base-rate decisions, HK GDP by quarter. Peer multiples and forward assumptions are illustrative and editable.
- These are portfolio exercises, not investment advice.
- Contact: csunaw@connect.ust.hk
