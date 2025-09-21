# Charlie Munger Investment Analysis — Agent Operating Guide

Purpose: a concise, actionable standard for producing consistent, high‑quality fundamental equity research rooted in Charlie Munger’s principles. Use this guide end‑to‑end on every ticker.

## Core Principles
- Circle of Competence: analyze only what you truly understand.
- Mental Models: apply multidisciplinary thinking (psychology, economics, math, biology, etc.).
- Margin of Safety: buy quality at clear discounts to intrinsic value.
- Long‑Term: optimize for decade‑long compounding, not quarters.
- Quality over Quantity: concentrate in a few excellent businesses.

## Workflow (Happy Path)
1) Define Scope
   - [ ] Confirm the business is within circle of competence.
   - [ ] Write 2–3 sentences on “how the company makes money.”
2) Gather Primary Sources (save to `/data/`)
   - [ ] 10‑K/20‑F, 10‑Q, transcripts, investor deck, shareholder letters.
   - [ ] Industry publications/trade data; relevant regulatory filings.
3) Business Quality Assessment
   - [ ] Moat (brand, network effects, cost, regulation, switching).
   - [ ] Management (competence, integrity, capital allocation, skin‑in‑game).
   - [ ] Financial strength (liquidity, leverage, covenants, maturity wall).
   - [ ] Earnings quality (cash conversion, volatility through cycles).
   - [ ] Pricing power and unit economics.
4) Valuation
   - [ ] Intrinsic value via DCF with explicit assumptions and ranges.
   - [ ] Multiples cross‑check (P/E, EV/EBITDA, P/B vs history/peers).
   - [ ] Margin of safety: target entry ≥ 30–50% discount.
   - [ ] Opportunity cost versus watchlist alternatives.
5) Risk Assessment
   - [ ] Permanent loss risks; disruption; secular vs cyclical.
   - [ ] Leverage/refinancing; key person; regulatory/geo.
   - [ ] Disconfirming evidence collected and addressed.
6) Decision & Sizing
   - [ ] Clear Buy/Sell/Hold with triggers and invalidation.
   - [ ] Position size based on conviction, liquidity, and risk.
7) Save & Journal
   - [ ] Save analysis file (see Deliverables) and update journal.
   - [ ] If bought/sold, update portfolio files.

## Deliverables (Required)
- File: `/analysis/[TICKER]_analysis_[YYYYMMDD].md`
- Must include sections: Executive Summary, Business Quality, Valuation, Risks, Decision & Sizing, Key Metrics, Sources, Change Log.
- Journal entry: `/analysis/journal/[YYYYMMDD]_[TICKER].md` (decision, reasoning, emotions, lessons).
- Data artifacts saved to: `/data/financials/`, `/data/market/`, `/data/reports/`.

## Templates

### Executive Summary (one page)
```
Ticker: XYZ | Sector: <sector> | Market Cap: <>
Thesis: <2–3 sentences>  
Edge: <why mispriced>  
Moat: <type + durability>  
Management: <capital allocation + incentives>  
Valuation: IV range <low–base–high> | MOS target <price>  
Catalysts: <near/mid‑term>  
Key Risks: <top 3 and mitigants>  
Decision: BUY/SELL/HOLD | Size: <x%> | Triggers: <add/trim/exit levels>
```

### Detailed Analysis Outline
1. Business Overview: products, customers, geographies, revenue mix, unit economics.
2. Moat Analysis: brand, network effects, cost, regulation, switching costs (evidence + metrics).
3. Management & Incentives: track record, capital allocation, comp alignment, ownership.
4. Financials: growth, margins, FCF conversion, ROIC, leverage, liquidity, covenants.
5. Valuation: DCF (assumptions, WACC, terminal), multiples vs history/peers, scenario table.
6. Risks & Disconfirming Evidence: what breaks the thesis; severity x likelihood; mitigants.
7. Decision & Sizing: entry range, adds/trims, invalidation, expected return vs alternatives.
8. Appendix: sources, data tables, key charts.

### Decision Summary Block (embed near top)
```
BUY/SELL/HOLD — Confidence: <low/med/high> — Time horizon: <yrs>
Entry: <$> | Adds: <$> | Trims: <$> | Exit: <$>
IV (L/B/H): <$ / $ / $> | MOS: <≥30–50%>
Thesis Invalidates If: <conditions>
```

### Journal Entry
```
[YYYY‑MM‑DD] — [TICKER] — Action: <initiate/add/trim/exit/hold>
What I believed: <>
What changed: <>
What I learned: <>
Next check‑ins: <dates/events>
```

## Checklists

### Business Quality
- [ ] Moat exists and is widening (evidence/metrics documented).
- [ ] Management is competent and aligned (owner‑operators preferred).
- [ ] Balance sheet can survive a severe recession.
- [ ] Earnings quality high; FCF durable through cycles.
- [ ] Pricing power present; low customer churn; favorable unit economics.

### Valuation
- [ ] DCF with conservative inputs and sensitivity table.
- [ ] Multiples cross‑checked vs history and peers.
- [ ] MOS quantified; target entry ≥ 30–50% below IV.
- [ ] Explicit comparison to top watchlist idea (opportunity cost).

### Risk
- [ ] Permanent impairment scenarios enumerated.
- [ ] Disruption/regulatory risks analyzed with base/bear/severe.
- [ ] Leverage/refi schedule vetted; covenant headroom.
- [ ] Key person/operational concentration addressed.
- [ ] Disconfirming evidence actively sought and logged.

## Key Metrics
- ROIC, ROCE, FCF margin, FCF yield.
- Net debt/EBITDA, interest coverage, maturity ladder.
- Revenue growth, gross/EBIT margins, cash conversion.
- Market share and customer/employee retention.

## Red Flags
- Frequent accounting changes; aggressive non‑GAAP; auditor churn.
- High executive turnover; poor capital allocation track record.
- Declining margins despite scale; growth via serial M&A masking organics.
- Rising DSOs/inventory; channel stuffing; off‑balance‑sheet liabilities.

## Position Sizing (Guideline)
- Top 5 positions: 60–80% of portfolio; size by conviction and downside.
- Never risk permanent capital impairment; consider liquidity and volatility.
- Rebalance on thesis change, valuation stretch, or superior opportunity.

## File & Directory Standards
- Naming: `[TICKER]_analysis_[YYYYMMDD].md` (analysis) and `[YYYYMMDD]_[TICKER].md` (journal).
- Directories:
  - `/analysis/` — current stock analyses
  - `/analysis/archive/` — prior versions
  - `/analysis/journal/` — decision logs
  - `/data/financials/` — statements and metrics
  - `/data/market/` — price/volume/benchmarks
  - `/data/reports/` — research and external notes
  - `/portfolio/positions/` — current holdings
  - `/portfolio/watchlist/` — candidates and notes

## Update Cadence & Quality Gates
- Update analyses at least quarterly or upon material events.
- Before marking “complete,” confirm:
  - [ ] All required sections filled and sources cited.
  - [ ] Numbers tie to saved data artifacts.
  - [ ] Risks include disconfirming evidence.
  - [ ] Decision & sizing explicit with triggers.
  - [ ] Files saved in correct locations and formats.

> “It is remarkable how much long‑term advantage people like us have gotten by trying to be consistently not stupid, instead of trying to be very intelligent.” — Charlie Munger
