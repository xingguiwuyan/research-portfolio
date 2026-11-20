# When the official price index and the deflator disagree
### Hedging inflation risk in a pegged emerging market — Bolivia

**Thesis.** In a dollarised, pegged economy the CPI understates the inflation an investor actually
bears: part of the adjustment happens through the exchange rate and through shortages, not through
posted prices. A hedge sized on headline CPI mis-measures the risk; the GDP deflator and the parallel
FX rate have to be read together.

## 1. The measurement problem
- CPI = fixed basket at administered prices; GDP deflator = price of everything produced, including
  exports and investment goods. They diverge when fuel/food are subsidised while tradable input
  costs move with the import bill.
- The boliviano is officially pegged near BOB 6.96/USD. When reserve coverage falls, the binding
  constraint appears in FX access and in a parallel-market premium, not in the official rate.
- Rationing and informal mark-ups are inflation without a price: they do not enter the index, but
  they do enter realised returns.

## 2. What I tested
| Step | Method | Finding |
|---|---|---|
| Decompose the gap | CPI vs GDP deflator and components (consumption, investment, exports) | Wedge concentrated in tradables and investment goods; the deflator moves first when the FX constraint tightens |
| Test transmission | Regress deflator changes on parallel FX premium and reserve coverage | FX premium dominates money growth — FX access is the transmission channel |
| Build the hedge | Commodity-input hedge + FX proxy + duration, sized to the deflator | Sizing to CPI leaves the FX part unhedged; sizing to the deflator over-hedges the administered part → two-factor hedge |

## 3. Framework
1. **Factor 1 — administered/CPI component:** slow, political; hedge with local duration only if an
   inflation-linked instrument exists, otherwise price it in.
2. **Factor 2 — FX-access component:** the real risk. Hedge with hard-currency assets, commodity
   options on the export basket, structural long USD; trigger on reserve coverage and parallel premium.
3. **Sizing rule:** weight to the deflator's tradable share, scaled by the estimated pass-through
   coefficient.

## 4. Beyond Bolivia
Same logic for any pegged/managed EM where the official index is a political variable (Argentina
pre-2015, Egypt pre-2016, Nigeria's multiple windows). Practical output: a monitoring dashboard —
deflator-vs-CPI wedge, parallel premium, reserve months, administered-price share.

*Independent project, Mar–Apr 2025. Framework and estimation are my own; figures are illustrative.
Not investment advice.*
