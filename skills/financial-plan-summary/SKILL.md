---
name: financial-plan-summary
description: Produces a client-facing financial plan summary that translates a technical financial plan into a clear story about where the client is, where they're going, and what needs to happen. Use when asked to write a financial plan, plan summary, financial planning summary, retirement plan summary, client plan review, planning summary, or financial goals review. For plan presentations and annual reviews.
triggers:
  - financial plan
  - plan summary
  - financial planning
  - retirement plan
  - client plan review
  - planning summary
  - financial goals
license: MIT
metadata:
  author: gonzih
  version: "1.0"
---

# financial-plan-summary

Produces a client-facing financial plan summary — translates the technical plan into a clear story about where the client is, where they're going, and what needs to happen. For plan presentations and annual reviews.

## How to Invoke

Say: *"Write a financial plan summary for [client description]"* and provide the client profile, assets, goals, and any existing plan analysis. The skill will structure everything into a readable client document.

## Workflow

### Step 1 — Client Profile

Gather:

- **Age(s)**: individual or couple (e.g., "David, 52; Susan, 49")
- **Life stage**: accumulation / pre-retirement / retirement / estate planning
- **Primary goals**: retirement income, college funding, business exit, legacy/estate, home purchase, debt payoff — ranked by priority
- **Risk profile**: conservative / moderate / aggressive, and why

### Step 2 — Current Financial Snapshot

Advisor provides the numbers; the skill structures the narrative:

- **Assets**: investment accounts (taxable, IRA, Roth, 401k), real estate equity, business interest, other
- **Liabilities**: mortgage balance, other debt
- **Income**: salary, business income, rental income, other
- **Savings rate**: annual savings to investment accounts
- **Insurance**: life, disability, long-term care (note any gaps)

### Step 3 — Goal Analysis

For each goal, produce a structured analysis:

| Goal | Target Amount | Timeline | Current Trajectory | Gap / Surplus |
|------|--------------|----------|--------------------|---------------|
| [Goal 1] | $[X] | [Year] | On track / Behind / Ahead | $[X] gap or $[X] surplus |
| [Goal 2] | $[X] | [Year] | ... | ... |

For any goal that is behind:
- Quantify the gap in plain English ("You need approximately $X more to reach this goal at current savings rate")
- State what closing the gap requires (increase savings by $X/year, adjust timeline by Y years, or accept a lower income in retirement)
- Flag assumptions used (rate of return, inflation, Social Security at age [X])

### Step 4 — Key Recommendations

List the top 3–5 actions in priority order. Each recommendation should:

- State the action clearly and specifically
- Explain the plain-English reasoning ("why this matters")
- Note the approximate impact or urgency
- Avoid jargon (say "Roth conversion" not "§ 408A election")

### Step 5 — The Plan Story

Write a 1-page narrative connecting:

**Where you are today** → **What we're doing together** → **Where you'll be**

This section is what the client reads first. It must be:
- Written in plain English, no financial jargon
- Personal — use the client's name and specific goals
- Honest about gaps without being alarming
- Focused on what's in the client's control
- Readable in under 5 minutes

### Step 6 — Action Items

Produce a clean action checklist split into two columns:

**Your Responsibilities** | **Our Responsibilities**
(Client actions) | (Advisor actions)

Include deadlines where applicable.

---

## Live Data Sources

When modeling projections and return assumptions, reference the following authoritative public datasets rather than hard-coded assumptions:

- **FRED historical return series** — Use FRED series `SP500` for historical S&P 500 levels to compute realized 10-, 20-, and 30-year annualized returns as a cross-check for the long-term equity return assumption used in retirement projections.
  - Endpoint: `https://fred.stlouisfed.org/graph/fredgraph.csv?id=SP500`
  - Compute trailing CAGR over planning-relevant horizons to calibrate the growth rate assumption (typically 6–8% nominal for a balanced portfolio).

- **Damodaran.com public datasets** (`pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/histretSP.html`) — Aswath Damodaran's annual equity risk premium (ERP) and historical return tables, updated every January. Use to:
  - Cross-check the equity risk premium assumption embedded in the plan's discount rate
  - Pull the implied ERP for the current year as a sanity check on forward return assumptions
  - Reference the historical arithmetic vs. geometric return distinction when explaining assumptions to clients

**How to use**: When populating the Goal Analysis assumptions row (*"X% average portfolio return"*), fetch current FRED and Damodaran data to confirm the assumption is within a defensible historical range. If the plan's assumed return is an outlier vs. historical data, flag this to the advisor with suggested language for the client disclosure.

---

## Example Output

**Input**: David (52) and Susan Chen (49). Portfolio $1.2M (60% equities/40% bonds). Income $310K combined. Saving $36K/year to 401ks. Home equity $420K, mortgage $280K remaining. Goals: retire at 65, two kids starting college 2026 and 2028 ($80K/year each for 4 years), leave estate to kids. Conservative-moderate risk. No long-term care insurance.

---

### The Plan Story (1-Page Narrative)

**David & Susan Chen | Financial Plan Summary**
*Prepared by [ADVISOR NAME] | [DATE]*

---

**Where You Are Today**

You've built a strong foundation. At 52 and 49, you have $1.2 million invested, meaningful home equity, and a solid combined income. You're saving consistently — $36,000 per year to retirement accounts — and you've got time on your side.

The picture isn't perfect, and that's what planning is for. Two college tuitions starting in two years will create a significant near-term cash demand. And while your retirement savings are healthy, retiring at 65 on your current trajectory requires some adjustments to stay on track given rising healthcare costs and a retirement that could span 30+ years.

**What We're Doing Together**

Our plan focuses on three things in parallel:

1. **Getting ready for college costs** — We're redirecting a portion of current savings to fund two tuitions starting in 2026. The goal is to cover this without touching your retirement accounts or taking on debt.

2. **Keeping retirement on track** — After the college years, we'll step up retirement contributions aggressively to close the gap created by the college funding phase. We're also planning for Social Security timing — waiting until 70 for the higher earner meaningfully increases lifetime income.

3. **Protecting what you've built** — You have a gap in long-term care coverage. With assets at this level, an LTC event is the single biggest risk to your retirement plan. We're recommending you address this in the next 12 months while premiums are still favorable.

**Where You'll Be**

If the plan is executed as designed, you retire at 65 with an estimated sustainable income of $[ADVISOR TO CALCULATE] per year (inflation-adjusted), both kids' education funded, your home paid off, and a projected estate of $[ADVISOR TO CALCULATE] at life expectancy. That's the goal. Here's how we get there.

---

### Goal Analysis

| Goal | Target | Timeline | Status | Notes |
|------|--------|----------|--------|-------|
| Retire at 65 | ~$3.8M portfolio | 2038 | **Slightly Behind** | ~$180K gap at current savings rate; addressable by increasing 401k + IRA contributions post-college |
| College — Child 1 | $320K total | 2026–2030 | **Needs Funding** | ~$85K available in 529; gap of ~$235K; recommend redirecting $30K/year starting now |
| College — Child 2 | $320K total | 2028–2032 | **Needs Funding** | Funded in parallel with Child 1 plan |
| Estate / Legacy | Preserve estate | Long-term | **On Track** | Estate projected at $[X] at life expectancy; beneficiary review needed |

*Assumptions: 6.5% average portfolio return, 2.5% inflation, Social Security at age 70 for David ($[X]/mo estimated), age 67 for Susan ($[X]/mo estimated). Actual results will vary.*

---

### Top 5 Recommendations

**1. Fund college without raiding retirement (Priority: Immediate)**
Redirect $30,000/year from taxable savings to a 529 plan for each child starting this year. This avoids depleting the $1.2M retirement portfolio and captures the remaining tax-advantaged growth before tuitions begin.

**2. Max both 401(k)s + back-door Roth IRA (Priority: This tax year)**
At your income level, both 401(k)s should be maxed ($23,000 each + $7,500 catch-up for David = $53,500 total). Additionally, a back-door Roth IRA for each of you adds $14,000/year in tax-free growth. This alone closes approximately 60% of the retirement gap.

**3. Delay Social Security — David to 70 (Priority: Plan now, act at 62)**
David delaying Social Security to age 70 vs. 62 increases monthly benefit by approximately 77%. At joint life expectancy, this generates an estimated $[X] more in lifetime income. Factor this into the drawdown plan.

**4. Purchase long-term care insurance (Priority: Within 12 months)**
You have no LTC coverage. A hybrid life/LTC policy at your ages is still reasonably priced (~$[X]/year) and protects your portfolio from a $200K–$500K LTC event that would derail the retirement plan. This is the single biggest unaddressed risk in your plan.

**5. Review beneficiary designations and estate documents (Priority: Within 6 months)**
Your wills, powers of attorney, and beneficiary designations may not reflect your current wishes or assets. A review with an estate attorney is recommended. Cost: $[X]–$[X].

---

### Action Checklist

| Your Responsibilities | Our Responsibilities |
|---|---|
| ☐ Increase 401(k) contributions to max ($53,500 combined) — by [DATE] | ☐ Open 529 accounts and set up automatic transfers — by [DATE] |
| ☐ Gather LTC insurance application materials; complete health questionnaire | ☐ Run LTC insurance quotes from 3 carriers — by [DATE] |
| ☐ Schedule appointment with estate attorney | ☐ Provide estate attorney with current beneficiary summary |
| ☐ Confirm Social Security earnings history at SSA.gov | ☐ Model Social Security timing scenarios and present options |
| ☐ Review and sign updated investment policy statement | ☐ Schedule 6-month check-in to review college funding progress |

*This plan summary is for educational and planning purposes only. All projections are estimates based on assumptions that may not be realized. Consult your advisor, tax professional, and legal counsel before making financial decisions.*
