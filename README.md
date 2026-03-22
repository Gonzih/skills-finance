# @gonzih/skills-finance

AI skill suite for financial advisors and wealth managers. Four skills packaged as a single npm install — works with Claude Code, Cursor, and Windsurf.

## Skills

| Skill | What it does |
|-------|-------------|
| [`portfolio-narrative`](#portfolio-narrative) | Turns raw performance data into a professional client portfolio letter |
| [`market-commentary`](#market-commentary) | Generates weekly/monthly market commentary for client communications |
| [`financial-plan-summary`](#financial-plan-summary) | Translates a technical financial plan into a clear client-facing summary |
| [`compliance-comms-review`](#compliance-comms-review) | Reviews communications for SEC/FINRA compliance red flags |

## Install

```bash
npm install @gonzih/skills-finance
```

Skills are automatically installed to `~/.claude/skills/`, `~/.cursor/skills/`, or `~/.windsurf/skills/` on install.

## Usage

Invoke any skill by describing what you need in natural language:

```
Write a portfolio narrative for Margaret Chen, Q1 return +6.2% vs S&P +7.1%
```

```
Draft a weekly market commentary — Fed held rates, jobs report came in at +187K
```

```
Write a financial plan summary for a 52-year-old couple retiring at 65 with $1.2M
```

```
Review this email for compliance before I send it to clients
```

---

## Skills

### portfolio-narrative

Transforms raw portfolio performance data into a professional, plain-English client narrative. Contextualizes returns vs. benchmarks, explains what happened in markets, and reinforces the long-term strategy.

**Produces**:
- Formal client letter (professional, third-person)
- Email version (warmer, first-person)
- One-page narrative summary

**Invoke with**: `portfolio review`, `portfolio narrative`, `performance summary`, `quarterly review`, `portfolio letter`, `client portfolio update`

**Compliance note**: Output is a drafting template. Advisor must review for accuracy and compliance. Past performance disclaimer language included.

---

### market-commentary

Generates a professional weekly or monthly market commentary. Provides a narrative framework the advisor fills with current data — saves 2–3 hours of writing per week.

**Produces**:
- Full base commentary (Macro View / What Markets Did / What It Means / What We're Watching)
- Conservative client version
- Growth client version
- LinkedIn post (250 words)
- 3 email subject line options

**Invoke with**: `market commentary`, `weekly market update`, `market newsletter`, `investment update`, `market conditions`, `market outlook`

---

### financial-plan-summary

Produces a client-facing financial plan summary — translates the technical plan into a clear story about where the client is, where they're going, and what needs to happen.

**Produces**:
- Goal analysis table with gap/surplus for each goal
- Top 3–5 prioritized recommendations with plain-English reasoning
- 1-page plan narrative (readable in under 5 minutes)
- Client/advisor action checklist with deadlines

**Invoke with**: `financial plan`, `plan summary`, `financial planning`, `retirement plan`, `client plan review`, `planning summary`, `financial goals`

---

### compliance-comms-review

Reviews client-facing communications against common compliance red flags and suggests compliant alternatives.

**Scans for**:
- Performance promises or guarantees
- Misleading performance claims (cherry-picked timeframes, no benchmark)
- Missing required disclosures (past performance disclaimer, registration)
- Testimonials without proper SEC Marketing Rule disclosure
- Predictions stated as facts
- Unsubstantiated superlatives ("best," "top-rated")
- Omission of material risks
- Suitability red flags

**Produces**:
- Issue-by-issue flag report with suggested rewrites
- Fully compliant rewritten version
- Required disclosures checklist

**Invoke with**: `compliance review`, `compliance check`, `review communication`, `suitability review`, `regulatory check`, `SEC compliance`, `FINRA compliance`

**Disclaimer**: This skill is a drafting aid and first-pass screening tool, not legal or compliance advice. Final review must be performed by a qualified compliance officer or legal counsel.

---

## License

MIT — Copyright (c) 2026 Maksim Soltan
