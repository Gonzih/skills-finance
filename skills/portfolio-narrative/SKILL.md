---
name: portfolio-narrative
description: Transforms raw portfolio performance data into a professional, plain-English client narrative. Use when asked to write a portfolio review, portfolio narrative, performance summary, quarterly review, portfolio letter, or client portfolio update. Contextualizes returns vs. benchmarks, explains market context, and reinforces long-term strategy. Replaces hours of report writing for financial advisors and wealth managers.
triggers:
  - portfolio review
  - portfolio narrative
  - performance summary
  - quarterly review
  - portfolio letter
  - client portfolio update
license: MIT
metadata:
  author: gonzih
  version: "1.0"
---

# portfolio-narrative

Transforms raw portfolio performance data into a professional, plain-English client narrative. Contextualizes returns vs. benchmarks, explains what happened in markets, and reinforces the long-term strategy. Replaces hours of report writing.

## How to Invoke

Say: *"Write a portfolio narrative for [client name], [period] return [X%] vs benchmark [Y%]"* — or paste raw data and ask for a portfolio letter. Provide as much or as little detail as you have; the skill will prompt for anything critical that's missing.

## Workflow

### Step 1 — Collect Data

Gather the following inputs (ask the advisor if not provided):

- **Portfolio return**: period return (e.g., +6.2% Q1 2025)
- **Benchmark return**: S&P 500, 60/40 blend, or custom benchmark
- **Asset allocation**: current breakdown (equities %, fixed income %, alternatives %, cash %)
- **Notable holdings / changes**: any significant adds, trims, or sector moves during the period
- **Period**: monthly, quarterly, or annual
- **Client name / type**: individual, family, institution; conservative / balanced / growth

### Step 2 — Market Context

Frame the market narrative for the period. Structure placeholders for the advisor to fill with precise data points:

- Equity market performance (S&P 500, international, small-cap)
- Fixed income / rate environment
- Key macro themes (inflation, Fed policy, earnings, geopolitical events)
- Volatility / sentiment backdrop

### Step 3 — Performance Narrative

- How the portfolio performed vs. benchmark
- Attribution: what contributed positively, what detracted
- If underperformance vs. benchmark: explain it was by design (risk management, positioning, cash buffer, quality tilt)
- If outperformance: credit positioning without making it sound like market-timing

### Step 4 — Strategy Reinforcement

Connect performance to the client's long-term plan:

- Remind client what the portfolio is designed to do (not maximize return in every quarter)
- Anchor to goals: retirement income, capital preservation, legacy, growth
- Resist short-term thinking; reframe volatility as normal

### Step 5 — Forward-Looking View

2–3 sentences on positioning going forward. Mark with `[ADVISOR TO COMPLETE]` placeholders for specific views the advisor will fill in before sending.

### Step 6 — Output Versions

Produce all three versions:

1. **Formal Letter** — professional, third-person, suitable for printing on letterhead
2. **Email Version** — warmer tone, first-person, suitable for direct client email
3. **One-Page Narrative** — condensed plain-English summary, readable in under 3 minutes

---

## Compliance Note

> **IMPORTANT**: This output is a drafting template. The advisor must review all content for factual accuracy and compliance before sending to clients. Past performance disclaimer language is included in each output version but must be reviewed by a qualified compliance officer. This tool does not constitute investment advice.

---

## Example Output

**Input**: Margaret Chen, Q1 2025. Portfolio +6.2%, S&P 500 +7.1%. Overweight investment-grade bonds (40%), underweight large-cap growth. No major changes during quarter. Conservative-moderate profile. Retiring in 8 years.

---

### Formal Letter Version

**[ADVISOR LETTERHEAD]**

April 7, 2025

Dear Ms. Chen,

We are pleased to share your portfolio review for the first quarter of 2025.

**Portfolio Performance**

Your portfolio returned +6.2% during the first quarter of 2025, compared to the S&P 500's return of +7.1% over the same period. This modest difference in return reflects a deliberate positioning choice — your portfolio carries a meaningful allocation to investment-grade fixed income, which provided stability during periods of equity market volatility in the quarter but naturally dampens upside capture relative to an all-equity benchmark.

**What Happened in Markets**

[ADVISOR TO COMPLETE: Briefly describe Q1 2025 market conditions — Fed policy, rate environment, equity sector leadership, any notable volatility events.]

**Your Portfolio in Context**

Your allocation is designed not to track the S&P 500, but to pursue growth while managing downside risk consistent with your goals and timeline. The 0.9% difference versus the benchmark is the expected cost of the risk management structure we've built into your portfolio. In quarters where equity markets decline sharply, this same positioning is designed to protect capital.

**Looking Ahead**

[ADVISOR TO COMPLETE: 2–3 sentences on current positioning and forward outlook.]

We remain focused on keeping your portfolio aligned with your retirement timeline and income goals. As always, we welcome any questions.

Sincerely,
[ADVISOR NAME]
[FIRM NAME] | [REGISTRATION / CRD #]

*Past performance is not indicative of future results. All investments involve risk, including the possible loss of principal. This letter is for informational purposes only and does not constitute investment advice.*

---

### Email Version

**Subject**: Your Q1 2025 Portfolio Review — [Client First Name]

Hi Margaret,

I wanted to share a quick update on your portfolio for the first quarter of 2025.

Your portfolio was up **6.2%** for the quarter. The S&P 500 returned 7.1% over the same period — so we trailed the index slightly, and I want to explain why that's by design.

Your portfolio holds a substantial position in investment-grade bonds. That allocation doesn't keep pace with the S&P 500 in a strong equity quarter, but it's there to cushion the portfolio when markets turn — which, as you know from experience, they eventually do. You're 8 years from retirement, and protecting the capital you've built is just as important as growing it.

[ADVISOR TO COMPLETE: Add 2–3 sentences on market context and forward positioning.]

Happy to jump on a call if you'd like to talk through anything. Talk soon.

[ADVISOR NAME]

*Past performance is not indicative of future results.*

---

### One-Page Narrative

**Margaret Chen | Q1 2025 Portfolio Summary**

| | Q1 2025 |
|---|---|
| Your Portfolio | +6.2% |
| S&P 500 | +7.1% |
| Difference | -0.9% |

**Why the difference?** Your portfolio is built for your goals — not to mirror the S&P 500. The 40% allocation to investment-grade bonds added stability during equity market fluctuations but naturally reduces upside capture vs. a pure equity benchmark. This is intentional.

**What happened this quarter:** [ADVISOR TO COMPLETE]

**What we're doing about it:** Nothing. The portfolio is positioned exactly as planned for someone 8 years from retirement with a conservative-moderate risk profile.

**Looking ahead:** [ADVISOR TO COMPLETE]

*Past performance is not indicative of future results. This document is for informational purposes only.*
