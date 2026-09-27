# 🌉 Blackstone Bridge

### Read the fine print in 30 seconds.

**Education, not manipulation.** Bridge turns any fund document, fact sheet or investment pitch into a one-page **investment label**. The label shows what you'd own, what it costs *in dollars on your amount*, when you can get your money out, and what could go wrong. **Every line links to the exact sentence it came from.**

> **Blackstone already teaches. Bridge lets you check.**

Built at **ShellHacks** for the **Blackstone challenge**: *reimagine how investors understand their current investments and research new opportunities.*

| | |
|---|---|
| **Run locally** | `pip install -r requirements.txt && python app.py` |
| **Stack** | Python / Flask, vanilla JavaScript, hand-built SVG charts, Claude (AI) |

> ⚠️ Before submitting, open the live demo, click **Share**, and make the link viewable, or judges won't be able to open it.

---

## Table of contents
1. [The problem](#the-problem)
2. [Our solution](#our-solution)
3. [Features](#features)
4. [Why you can trust the label](#why-you-can-trust-the-label)
5. [60-second demo](#60-second-demo)
6. [How it meets the challenge](#how-it-meets-the-challenge)
7. [How it works](#how-it-works)
8. [Data sources](#data-sources)
9. [Design and accessibility](#design-and-accessibility)
10. [Getting started](#getting-started)
11. [Project structure](#project-structure)
12. [Limitations and honesty notes](#limitations-and-honesty-notes)
13. [What's next](#whats-next)
14. [Team](#team)

---

## The problem

### 1. The information exists, but it doesn't turn into understanding
Investors have more information than ever. It's spread across prospectuses, quarterly reports, fact sheets, market data and news, and it's written for lawyers and regulators, not people.

Take a single real term sheet. Blackstone's private equity fund for individuals (BXPE) charges:
- a **1.25%** yearly management fee
- **12.5%** of total return once returns pass a **5%** hurdle

Withdrawals are capped at **3%** of the fund per quarter, and units held **less than two years** face an early repurchase deduction. Each of those facts is public. Almost no first-time investor can turn them into an answer to *"what happens to my $1,000?"*

### 2. Young adults invest the least, and get targeted the most
- Only **44%** of U.S. adults aged 18–29 own stock, compared with **72%** of adults aged 50–64 (Gallup, 2024–25).
- In **44%** of fraud reports from people in their 20s, the person lost money. That's the highest rate of any age group (FTC, 2024).
- Americans reported losing **$7.9 billion** to investment scams in 2025, about half of all reported fraud losses. Many of these scams started on social media (FTC).

The people with the most *time* to grow their money have the least *trust* in finance, and the most exposure to hype.

### 3. Private markets are coming to regular investors, but the fine print isn't getting simpler
Blackstone is actively bringing private markets to individuals:
- **BREIT** (private real estate) has a **$2,500** minimum.
- **BXPE** (private equity) is open to accredited investors.

Meanwhile, **Executive Order 14330 (August 2025)** opened the door for 401(k) plans to hold private equity, private credit and real estate. The Department of Labor proposed a rule in 2026. Soon, young workers may hold private-market investments *inside their retirement plans* without ever choosing them.

These products bring real trade-offs: higher fees, withdrawal limits, and values based on estimates rather than market prices. When BREIT's withdrawal requests exceeded its limits from **November 2022 to February 2024**, investors received only part of what they asked for. People who understood the rules beforehand knew what to expect. Many didn't.

### 4. Education from the seller isn't the same as transparency
Blackstone already runs investor education, including courses on private markets. But when the issuer explains its own product, a skeptical 25-year-old hears marketing.

**The missing piece isn't more education. It's an independent way to *check* the fine print.**

---

## Our solution

**Bridge** is a transparency layer for investing. Its core feature, **Check it**, reads the fine print for you and produces a standardized **investment label**, like a nutrition label for money.

- **Paste anything:** a prospectus section, quarterly report, fact sheet, or a post someone sent you.
- **Get one page:** costs in dollars, access to your money, what you'd own, how the price is set, risks, red flags, and questions to ask.
- **Check every line:** each claim has a numbered **receipt**. Tap it and the exact source sentence lights up in the document.
- **See what's missing:** Bridge scores whether the document answers **6 basic questions**, and names what it *doesn't* say.

Around the label, Bridge helps first-time investors **start small**, understand **what they already own**, and **research what's next**, using real public data.

---

## Features

### 🏷️ Check it: the investment label *(core feature)*
| Section | What it shows |
|---|---|
| **Cost on your amount** | Upfront charge, each yearly fee, performance fee, and early-sale penalty, all **in dollars**, with a "growth before fees" slider. Also shows fees **over 10 years** compared with a 0.03% index fund. |
| **Getting your money out** | A 4-step access meter (any day → monthly → quarterly → locked), plus each withdrawal rule with its receipt. |
| **What you'd own / How the price is set / What could go wrong** | Plain-English rewrites, each backed by a receipt. |
| **Red flags** | Guaranteed returns, pressure to act fast, crypto or gift-card payment, pay-to-withdraw, secrecy. |
| **Does it answer the basics?** | A score out of 6, plus a list of what's missing from the document. |
| **Questions to ask** | 2–3 questions to ask before investing. |
| **Compare** | Up to 3 labels side by side on your amount. |

**Built-in samples** (instant, no AI needed):

| Sample | What the label reveals |
|---|---|
| **Blackstone BREIT** | $65 first-year cost on $1,000 (at 8% growth before fees, with the maximum upfront charge). About $602 in fees over 10 years vs $6 for an index fund. 6 of 6 basics answered. |
| **Blackstone BXPE** | 5 of 6 basics answered. Flags *"Selling early: yes, amount not stated. Ask how much."* |
| **S&P 500 index fund** | $0 upfront, 0.03% a year, sell any business day. |
| **Social media pitch** | **6 red flags**, 1 of 6 basics answered, and "Don't send money" with links to FINRA BrokerCheck and the FTC. |

### 💬 Ask in plain English
A chat assistant ("Chat with my investor") on every page. It answers using your portfolio, the label you're viewing, and the market dataset. It explains trade-offs but **never recommends buying or selling**, never predicts prices, and never asks for passwords. One tap reaches a licensed human.

### 🌱 Start small
*"What could $10 a week become?"* Pick $5–$50 a week, 5–40 years, and stocks, half-and-half, or cash. Bridge replays **every historical stretch since 1928** and shows the **worst, typical and best** outcomes, how often people ended with less than they put in, and **what waiting 5 years costs**.

> Example: $10 a week in a stock index fund for 20 years means $10,400 put in. Across all 79 historical 20-year stretches, the typical result was about **$36,048** (worst $15,725, best $85,884).

### 📊 My portfolio
- **Holdings:** enter your own, or pick a sample mix.
- **Summary:** total value, money you could reach **within a week**, 20-year average growth and worst year, and fees in dollars.
- **Performance history:** your current mix replayed over 5–30 years of real returns, against an all-stocks benchmark.
- **Plain-English signals:** concentration, withdrawal limits, rising rates vs your bonds, cash vs inflation, hot streaks, fee drag.
- **Explain my portfolio:** an AI summary built only from the numbers on screen.

### 🔎 Research
- **Compare** up to 3 asset classes over 5 years to 98 years: growth of $10,000, best and worst year, losing years, biggest drop, and access.
- **What if I added this?** Before and after for *your* portfolio.
- **Trends heatmap:** 10 years of returns, showing that a different investment leads almost every year.
- **What's happening now:** the Fed rate (raised to 3.75–4.00% on Sept. 16, 2026) and inflation (3.4%, Aug. 2026), each with what it means for you.

### 📚 Learn, Stay safe, Money out
- **Learn:** five 4-minute lessons with one-question checks.
- **Stay safe:** scam practice (find the tricks in a fake text) and a pyramid-scheme simulator.
- **Money out:** a withdrawal-limit simulator and the real BREIT 2022–24 story.

---

## Why you can trust the label

Most AI summaries ask you to take them on faith. Bridge doesn't.

1. **Receipts are verified in the browser.** Every quote the AI returns is matched word-for-word against the document you pasted. Anything that doesn't match is marked **"!"** and flagged "not found in the document." The status line reports the result, e.g. *"12 of 13 receipts found word-for-word."*
2. **The AI never does math.** It only extracts the percentages the document states. **Every dollar figure is computed in code.**
3. **It uses only the document.** The AI is told not to use outside knowledge, even about products it recognizes. The label reflects what *you* were actually shown.
4. **It shows what's missing.** Gaps (like an unstated early-sale penalty) become questions to ask, not silence.
5. **It's fair to the issuer.** Growth is labeled "before fees," upfront charges are marked as maximums, and the performance-fee calculation is labeled as simplified.
6. **Every built-in sample is tested.** `labels_data.check()` runs at startup and refuses to start the app if any sample receipt isn't in its document.

---

## 60-second demo

1. **Home.** *"Read the fine print in 30 seconds."* The BREIT mini-label shows $65 first-year cost on $1,000, and $602 of fees over 10 years vs $6 for an index fund.
2. **Check it → Blackstone BXPE.** 5 of 6 basics answered. *"Selling early: yes, amount not stated. Ask how much."* Tap a receipt and the source sentence lights up.
3. **Social media pitch.** 6 red flags, 1 of 6 basics answered.
4. **Paste real text live.** Copy the fee section from a real prospectus on [SEC EDGAR](https://www.sec.gov/edgar/search/), paste it in, and press **Make the label**. The status line reports how many receipts were found word-for-word.
5. **Compare.** BREIT vs the index fund, then change the amount to $10,000.
6. **Ask about this label.** The chat explains it in plain English.

> AI features run on the published claude.ai link (click **Allow** once). The four samples work anywhere, instantly.

---

## How it meets the challenge

| Challenge ask | Where in Bridge |
|---|---|
| Understand current investments | **My portfolio**: mix, access, real history, signals, and each holding linked to its label |
| Research new opportunities | **Check it** (any document) and **Research** (compare, what-if) |
| Performance reports and filings spread across sources | Paste any filing or report and get **one standardized label** |
| Summarize complex information | Investment label, "Explain my portfolio", "Explain this comparison" |
| Compare opportunities | Label comparison (costs, access, clarity, red flags) and asset-class comparison |
| Discover trends and risks | Portfolio signals, "What's happening now", returns heatmap, red flags |
| Visualize performance | Growth charts, heatmap, start-small range bar, access meter |
| Ask questions in natural language | Chat grounded in portfolio, label and data, with page tools for exact numbers |
| **Accessible, actionable, engaging** | Dollars instead of percentages, "questions to ask", start-small tool, 18px+ text, read-aloud, dark mode |

---

## How it works

```
                ┌──────────────────────────────┐
 Pasted text ──▶│  Claude (structured JSON)     │  extracts: plain-English lines (t),
 or screenshot  │  "use ONLY the document"      │  exact quotes (q), stated percentages
                └──────────────┬───────────────┘
                               ▼
                ┌──────────────────────────────┐
                │  Receipt verifier (browser)   │  normalizes whitespace and quotes,
                │                               │  finds each quote in the document,
                │                               │  numbers matches, flags misses
                └──────────────┬───────────────┘
                               ▼
                ┌──────────────────────────────┐
                │  Cost engine (browser)        │  upfront, yearly, performance fee,
                │                               │  early-sale penalty, 10-year fees
                └──────────────┬───────────────┘
                               ▼
               Investment label  +  highlighted source  +  comparison
```

- **Frontend:** a single Jinja template plus vanilla JavaScript (no framework). Charts are hand-built SVG, so there's nothing external to load.
- **Backend:** Flask serves the page and injects all content and data as JSON. `build.py` inlines everything into **one self-contained HTML file** (`dist/blackstone-bridge.html`) for hosting anywhere.
- **AI:** Claude, through the published claude.ai app's built-in AI access. It's used in three places:
  - **Label extraction:** structured JSON output.
  - **Explanations:** streamed text.
  - **Chat:** with two page tools, `what_if_add` and `asset_history`, so answers use exact numbers.
- **Fallback:** without AI, samples, charts and every calculator still work, and the chat switches to scripted answers.
- **Market math:** portfolio history uses yearly-rebalanced weighted returns. Start small replays weekly contributions through every N-year window from 1928 to 2025. The results were cross-checked against an independent Python calculation.

---

## Data sources

All data is public. Every number in the app links to its source.

| Data | Source |
|---|---|
| Annual returns 1928–2025 for large and small U.S. stocks, 10-year Treasuries, Baa corporate bonds, 3-month T-bills, U.S. home prices and gold | [NYU Stern, Prof. Aswath Damodaran: Historical Returns on Stocks, Bonds and Bills](https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/histretSP.html) (updated Jan 2026). Our copy was checked against the source's own cumulative totals. |
| Stock ownership by age and education | [Gallup](https://news.gallup.com/poll/266807/percentage-americans-owns-stock.aspx) |
| Fraud by age; investment-scam losses | [FTC Consumer Sentinel Data Book 2024](https://www.ftc.gov/system/files/ftc_gov/pdf/csn-annual-data-book-2024.pdf); [FTC testimony, March 2026](https://www.ftc.gov/system/files/ftc_gov/pdf/ftc-testimony-jec-hearing-on-the-rising-scam-economy.pdf) |
| Fed interest rate (Sept 2026) | [Federal Reserve](https://www.federalreserve.gov/newsevents/pressreleases/monetary20260916a1.htm) |
| Inflation (Aug 2026) | [Bureau of Labor Statistics, CPI](https://www.bls.gov/news.release/cpi.nr0.htm) |
| BREIT terms, minimum and suitability | [BREIT offering terms](https://www.breit.com/offering-terms/), SEC prospectus supplements |
| BXPE terms and eligibility | SEC filings (10-Q/10-K), [bxpe.com](https://www.bxpe.com/) |
| BREIT withdrawal limits, 2022–24 | [The DI Wire](https://thediwire.com/?p=43137), [Bisnow](https://www.bisnow.com/national/news/capital-markets/breit-fulfills-all-redemption-requests-for-first-time-in-more-than-a-year-123143) |
| 401(k) and alternative assets | Executive Order 14330 (Aug 7, 2025); [DOL rulemaking summary](https://www.shulmanrogers.com/wp-content/uploads/2026/02/Client-Alert-Department-of-Labor-Advances-Proposed-Rule-Expanding-401k-Access-to-Private-Capital.pdf) |

---

## Design and accessibility

**Audience:** Gen Z and young millennials who don't invest yet. The design had to earn trust without feeling like a bank.

**Color psychology:**
| Color | Role | Why |
|---|---|---|
| Violet-blue `#5B3FE0` | Primary buttons and links | Blue is the most trusted color; the violet shift reads modern, not "old bank" |
| Mint / emerald `#12B886` / `#0B7A55` | Growth, gains, "go" | Money and growth |
| Sunny yellow `#FFC93C` | Highlights, selected states | Optimism, used sparingly |
| Ink indigo `#1C1640` | Text, dark surfaces | Grounding and seriousness |
| Coral `#C2410C` | **Losses and warnings only** | Never used to create urgency |

**Accessibility:**
- **Readable type:** Atkinson Hyperlegible body font (designed for low vision), an 18px base, and a 3-step text-size control.
- **Read-aloud** on every page.
- **Keyboard and screen readers:** full support, and every chart has a "Show the numbers" table.
- **Dark mode**, reduced-motion support, and a responsive mobile layout.
- **Contrast:** checked for white text on colored backgrounds.
- **No pressure patterns:** no timers, no streaks, no "limited-time" language.

---

## Getting started

**Requirements:** Python 3.9+

```bash
git clone https://github.com/<your-org>/BridgeIT.git
cd BridgeIT
pip install -r requirements.txt
python app.py            # → http://127.0.0.1:5000
```

**Build a single self-contained file** (for hosting or demos):
```bash
python build.py          # → dist/blackstone-bridge.html
```

**Enable AI features:** publish `dist/blackstone-bridge.html` as a claude.ai artifact with the `sample` capability. When running locally, AI features hide themselves and the chat uses scripted answers.

---

## Project structure

```
BridgeIT/
├── app.py              # Flask app + all content: ASSETS, SNAPSHOT, CONTENT (copy, lessons, sources)
├── labels_data.py      # 4 sample documents + pre-built labels; check() verifies every receipt
├── build.py            # Inlines CSS/JS/data → dist/blackstone-bridge.html
├── requirements.txt
├── data/
│   └── market.json     # NYU Stern annual returns, 1928–2025
├── templates/
│   └── index.html      # Single-page template (tabs switch by URL hash)
├── static/
│   ├── style.css       # Palette tokens, light/dark themes, components
│   ├── app.js          # Routing, lessons, scam tools, login, chat shell
│   ├── insights.js     # Portfolio math, signals, charts, research, start small, AI chat
│   └── labels.js       # Investment label: receipt verifier, cost engine, compare, AI extraction
└── dist/
    └── blackstone-bridge.html
```

**Where to edit:**
- Copy and numbers: `app.py`
- Sample labels: `labels_data.py`
- Current conditions (rates, inflation): `SNAPSHOT` in `app.py`
- Market data: replace `data/market.json` each January

---

## Limitations and honesty notes

- **The samples are not verbatim filings.** The BREIT and BXPE samples are short excerpts we wrote from each fund's verified public terms, to respect copyright. Paste real filing text for live use.
- **You may not be able to buy these funds.** BXPE is limited to accredited investors. BREIT requires a $2,500 minimum and a net worth of at least $250,000 (or $70,000 income plus $70,000 net worth). Bridge explains products; it doesn't sell them.
- **History is not a forecast.** Returns are before fees, taxes and inflation. Portfolio history assumes yearly rebalancing. Private funds have no public yearly price series, so they're excluded from history (the app says so) but included in access calculations.
- **The performance-fee math is simplified.** It ignores catch-up and high-water-mark mechanics. Upfront charges are shown at their stated maximum.
- **AI requires claude.ai.** AI features need the published claude.ai link and the viewer's permission. Everything else works offline.
- **The demo login stays in your browser.** Nothing is sent anywhere, and passwords are never stored.
- **Not investment advice, and not affiliated with Blackstone.** This is an educational concept built for a hackathon.

---

## What's next

- **"Who can buy this?"** A label row for minimums and eligibility (accredited-investor rules, suitability standards), backed by receipts.
- **401(k) labels.** Read plan documents and target-date funds as private markets enter retirement plans (Executive Order 14330).
- **Fetch by name or ticker.** Pull the latest prospectus straight from SEC EDGAR instead of pasting.
- **PDF upload** for full prospectuses, with page-level receipts.
- **Label history.** Show how a fund's terms changed between filings.
- **Español.** Plain-English *and* plain-Spanish labels.
- **Adviser mode.** Advisers generate a label for each client meeting, turning Blackstone's transparency into a shareable, checkable artifact.
- **Issuer-verified labels.** Blackstone could publish its funds' key terms in the label format, so investors can check any document against the official source.

---

## Team

| Name | Role | GitHub |
|---|---|---|
| _Your name_ | _Role_ | _@handle_ |
| _Your name_ | _Role_ | _@handle_ |

*Built at ShellHacks for the Blackstone challenge.*

---

<sub>Blackstone Bridge is an educational concept. It does not provide investment, legal or tax advice, and it is not affiliated with or endorsed by Blackstone Inc. Never share your password, PIN or one-time code with anyone.</sub>
