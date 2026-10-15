+++
title = "The Case for Quality Factor Investing"
date = 2026-10-15T06:00:00Z
draft = false
slug = 'quality-factor-investing'
tags = ['investing', 'ETFs', 'quality factor', 'AI']
description = "Work in progress: notes and research for a post on quality factor investing."
+++

<!--
SCAFFOLD: write in your own words, then delete the "Points" and "Research" notes.
Preview drafts with: hugo server -D
Set draft = false when it's ready to publish.
-->

> **Note:** not financial advice. Figures as of October 2026.

## Intro

**Points**
- Core idea in one sentence: own good businesses and leave them alone
- Name it: quality factor investing, held via IWFQ
- Roadmap: what quality is, the evidence, how the index picks stocks, why it matters in the AI boom, the trade-offs

## What "quality" means

**Points**
- Definition: high returns on capital, low debt, steady profits
- Examples of quality vs not-quality businesses
- The academic case: why it shouldn't work but does

**Research**
- Asness, Frazzini & Pedersen, *Quality Minus Junk*: profitable, safe, well-run firms earn higher risk-adjusted returns across 24 countries; quality is only modestly priced in; "flight to quality" in crises ([SSRN](https://papers.ssrn.com/abstract=2312432))

## What the numbers say

**Points**
- Long-run record vs MSCI World
- Smaller drawdowns, but not immune
- Be honest about 2022 and back-testing

**Research** (MSCI factsheet, USD, to 30 Sep 2026, [link](https://www.msci.com/documents/10199/255599/msci-world-sector-neutral-quality-index-usd-net.pdf))

| | Quality index | MSCI World |
|---|---|---|
| Annualised return since Nov 1998 | 8.14% | 7.38% |
| Max drawdown (Oct 2007 – Mar 2009) | −54.5% | −57.8% |
| Sharpe ratio since 1998 | 0.45 | 0.39 |
| Beta | 0.95 | 1.00 |

- 2018: quality −7.2% vs World −8.7%
- 2022: quality −19.2% vs World −18.1% (fell *more*, rate shock)
- 2024: 16.8% vs 18.7%; 2025: 15.5% vs 21.1% (lagged)
- Index launched Aug 2014; earlier data is back-tested

## How IWFQ picks its companies

**Points**
- It's rules-based, copying the MSCI World Sector Neutral Quality Index
- Walk through the steps vs the parent MSCI World
- Why sector-neutral matters (compare a bank with banks)
- The three measures check each other (buybacks example)

**Research** ([MSCI methodology, May 2022](https://www.msci.com/eqb/methodology/meth_docs/MSCI_Quality_Indexes_Methodology_May2022.pdf))
1. Parent: MSCI World, ~1,300 large/mid caps, 23 developed countries
2. Measures:
   - ROE = trailing 12m EPS ÷ latest book value per share
   - Debt/equity = latest fiscal-year total debt ÷ book value
   - Earnings variability = std dev of y-o-y EPS growth, last 5 fiscal years
   - No ROE → excluded; needs ROE plus at least one other
3. Winsorise outliers → z-scores (debt and variability flipped) → average
4. Re-standardise within each GICS sector (capped at ±3)
5. Keep a fixed number (~300); buffer: incumbents stay if ranked in the top 360, newcomers need the top 240
6. Weight = market-cap weight × quality score (score = 1 + z if positive); 5% issuer cap
7. Sector weights scaled to match the MSCI World
8. Rebalanced end of May and November

Result vs parent (MSCI factsheet, 30 Sep 2026):

| | MSCI World | Quality index |
|---|---|---|
| Companies | ~1,300 | ~300 |
| Weighting | Size | Size × quality |
| Turnover (12m) | 3% | 26% |
| Price/book | 4.1x | 6.7x |
| P/E | 22.7x | 23.9x |
| Dividend yield | 1.52% | 1.43% |

- IWFQ ongoing charge: ~0.25%

## Why quality matters more in the AI boom

**Points**
- Big Tech used to self-fund; now it's borrowing
- Two of the three measures (debt, earnings stability) are what an AI spending race strains
- Oracle as the extreme example

**Research**
- Alphabet, Amazon, Meta, Microsoft, Oracle: ~$220bn of bonds in 2026 to 10 Aug (BNP Paribas via Reuters, [MLQ](https://mlq.ai/news/hyperscaler-bond-issuance-reaches-about-220-billion-as-ai-financing-costs-rise/)); Goldman expects ~1/3 of hyperscaler capex debt-funded; [CNBC](https://www.cnbc.com/2026/02/23/big-techs-ai-bond-binge-shatters-unspoken-contract-with-investors.html)
- Oracle FY2026 free cash flow −$23.7bn ([8-K](https://www.sec.gov/Archives/edgar/data/0001341439/000119312526265848/orcl-ex99_1.htm))
- Oracle total debt $125–170bn depending on source/leases, up from ~$100bn in late 2024 ([TIKR](https://www.tikr.com/blog/oracle-courts-apollo-and-goldman-for-ai-chip-financing-as-debt-tops-169-billion), [TheStreet](https://www.thestreet.com/investing/stocks/orcl-oracle-stock-junk-bond-bankruptcy-fears-warning-investors))
- Oracle debt/equity >4x; ~$43bn new debt in FY2026; rated BBB, negative outlook
- Oracle is **not** in IWFQ
- Note: the screen doesn't measure cash flow directly

## What IWFQ leaves out

**Points**
- AI-linked S&P 500 names that aren't in IWFQ
- Not all fail on debt: some on erratic earnings or weak returns
- "Not anti-AI, anti-fragile-balance-sheet"

**Research** (iShares holdings, 13 Oct 2026: [IWFQ](https://www.ishares.com/uk/individual/en/products/270054/), [CSPX](https://www.ishares.com/uk/individual/en/products/253743/)). Reasons are inferred; MSCI doesn't publish scores.

| Company | S&P 500 weight | Likely reason |
|---|---|---|
| Amazon | 3.77% | Volatile profits (loss in 2022), heavy capex borrowing |
| Broadcom | 2.53% | VMware debt; net debt ~$55bn ([Eulerpool](https://eulerpool.com/stock/Broadcom-Stock-US11135F1012/netdebt)) |
| Micron | 1.60% | Cyclical, variable earnings |
| Tesla | 1.57% | Profits swung and fell |
| AMD | 1.47% | Low ROE after Xilinx deal |
| Intel | 0.76% | Recent heavy losses |
| Palantir | 0.71% | Short, volatile profit history |
| Oracle | 0.37% | Debt >4x book equity |
| **Total** | **12.78%** | |

- Only 133 of the S&P 500's 504 holdings are in IWFQ; IWFQ holds 289 in total
- CoreWeave (not in S&P 500): ~$30bn debt, negative FCF, junk bonds at 9.75% coupon ([TIKR](https://www.tikr.com/blog/coreweaves-640m-interest-bill-is-growing-faster-than-its-128m-profit-but-management-says-the-burn-is-by-design-heres-what-investors-need-to-know))

## What it owns instead

**Points**
- Still owns AI, the financially strongest end
- "Picks and shovels" chip-equipment makers
- Steady compounders; global (not just US)

**Research** (13 Oct 2026)

| | S&P 500 | IWFQ |
|---|---|---|
| Nvidia | 8.22% | 5.31% |
| Apple | 7.40% | 5.84% |
| Microsoft | 6.00% | 6.66% |
| Alphabet (A+C) | 5.55% | 3.13% |
| Amazon | 3.77% | — |
| Meta | 2.50% | 4.35% |
| Tesla | 1.57% | — |
| **Mag 7 total** | **35.0%** | **25.3%** |

- ASML 2.96%, Lam 1.90%, Applied Materials 1.49%, KLA 1.03%, Advantest 0.79% (~8% combined)
- Visa 3.71%, Mastercard 2.12%, Eli Lilly 2.48%, TJX 1.98%, Caterpillar 1.10%, Costco 0.87%
- ~74% US

## If the AI boom turns to bust

**Points**
- Still lose money, but expect a softer landing
- Same pattern as 2008/2018: not immunity
- The screen's blind spots: Meta, off-balance-sheet debt, rebalancing lag

**Research**
- Meta: $30bn bond Oct 2025 (record non-M&A high-grade deal) + ~$27bn off-balance-sheet SPV for Hyperion data centre ([Silicon Analysts](https://siliconanalysts.com/analysis/hyperscaler-ai-capex-depreciation-wall-2026)); still 4.35% of IWFQ vs 2.50% of S&P 500
- Screen uses reported accounts and rebalances twice a year, so it lags new borrowing

## The trade-offs

**Points**
- Lags speculative rallies (2024, 2025)
- Quality is expensive (P/B 6.7x vs 4.1x); an index can't avoid overpaying
- Not every crash (2022)
- Still concentrated: top 10 = 37% of IWFQ vs 39% of S&P 500
- Costs more than a plain tracker (0.25% vs <0.1%)
- Currency risk for UK investors

## The bottom line

**Points**
- Back to the one-sentence idea
- Why AI makes the discipline more useful, not less
- Win-win framing: benefit if it pays off, sit out the worst if it doesn't

### Sources

- [MSCI factsheet](https://www.msci.com/documents/10199/255599/msci-world-sector-neutral-quality-index-usd-net.pdf) · [MSCI methodology (May 2022)](https://www.msci.com/eqb/methodology/meth_docs/MSCI_Quality_Indexes_Methodology_May2022.pdf) · [latest](https://www.msci.com/indexes/documents/methodology/2_MSCI_Quality_Indexes_Methodology_20250520.pdf)
- [Quality Minus Junk](https://papers.ssrn.com/abstract=2312432)
- [iShares IWFQ](https://www.ishares.com/uk/individual/en/products/270054/) · [iShares CSPX](https://www.ishares.com/uk/individual/en/products/253743/)
- [MLQ/Reuters](https://mlq.ai/news/hyperscaler-bond-issuance-reaches-about-220-billion-as-ai-financing-costs-rise/) · [CNBC](https://www.cnbc.com/2026/02/23/big-techs-ai-bond-binge-shatters-unspoken-contract-with-investors.html) · [Silicon Analysts](https://siliconanalysts.com/analysis/hyperscaler-ai-capex-depreciation-wall-2026)
- [Oracle 8-K](https://www.sec.gov/Archives/edgar/data/0001341439/000119312526265848/orcl-ex99_1.htm) · [TIKR (Oracle)](https://www.tikr.com/blog/oracle-courts-apollo-and-goldman-for-ai-chip-financing-as-debt-tops-169-billion) · [TheStreet](https://www.thestreet.com/investing/stocks/orcl-oracle-stock-junk-bond-bankruptcy-fears-warning-investors)
- [Eulerpool (Broadcom)](https://eulerpool.com/stock/Broadcom-Stock-US11135F1012/netdebt) · [TIKR (CoreWeave)](https://www.tikr.com/blog/coreweaves-640m-interest-bill-is-growing-faster-than-its-128m-profit-but-management-says-the-burn-is-by-design-heres-what-investors-need-to-know)
