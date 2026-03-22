---
name: compliance-comms-review
description: Reviews client-facing financial communications against common compliance red flags and suggests compliant alternatives. Use when asked to do a compliance review, compliance check, review a communication for compliance, suitability review, regulatory check, SEC compliance review, or FINRA compliance check. Flags issues in emails, letters, social posts, newsletters, presentations, and marketing materials. NOT a legal opinion — a first-pass screening tool for financial advisors.
triggers:
  - compliance review
  - compliance check
  - review communication
  - suitability review
  - regulatory check
  - SEC compliance
  - FINRA compliance
license: MIT
metadata:
  author: gonzih
  version: "1.0"
---

# compliance-comms-review

Reviews client-facing communications (emails, letters, social posts, marketing materials) against common compliance red flags. Flags issues, suggests compliant alternatives. NOT a legal opinion — a first-pass screening tool for advisors before submission to compliance.

## How to Invoke

Say: *"Review this for compliance"* and paste the communication. Specify the type if not obvious (email, social post, marketing material, etc.). The skill will scan for red flags and produce a flagged version plus a compliant rewrite.

## Workflow

### Step 1 — Input

Paste the communication to review. Identify the type:

- Client email
- Client letter
- Social media post (LinkedIn, X/Twitter, Facebook)
- Newsletter / market commentary
- Presentation slide(s)
- Marketing material (brochure, website copy, ad)
- Other: specify

### Step 2 — Red Flag Scan

Scan for the following categories of compliance issues (based on SEC, FINRA, and Investment Advisers Act standards):

| # | Issue Category | What to Look For |
|---|---------------|-----------------|
| 1 | **Performance promises / guarantees** | Any language implying guaranteed returns: "you will earn," "guaranteed income," "risk-free," "no downside" |
| 2 | **Misleading performance claims** | Cherry-picked timeframes with no context, performance claims with no benchmark, no time period specified, hypothetical results presented as actual |
| 3 | **Missing required disclosures** | No past performance disclaimer, no registration disclosure (RIA, BD, CRD number), no risk disclosure where returns are mentioned |
| 4 | **Testimonials / endorsements** | Client testimonials or endorsements without proper disclosure under SEC Marketing Rule (Advisers Act Rule 206(4)-1). Must include: relationship disclosure, whether compensated, whether results are representative |
| 5 | **Predictions stated as facts** | "The market will rally," "rates will fall," "this stock is going to X" — any forward-looking statement framed as certainty |
| 6 | **Unsubstantiated superlatives** | "Best," "top-rated," "leading," "superior" without substantiation from an objective third-party source with criteria disclosed |
| 7 | **Omission of material risks** | Recommending or describing a strategy without disclosing relevant material risks |
| 8 | **Suitability / mass audience red flags** | Recommending specific securities or strategies to a broad audience without suitability context; implying one approach is right for everyone |
| 9 | **Prohibited terms (context-dependent)** | "Safe" (when describing investments), "conservative" without context, "no fees" without full fee disclosure |

### Step 3 — Issue Report

For each flag found, produce:

```
FLAG #[N] — [Category Name]
Location: [quote the exact problematic text]
Issue: [explain what the compliance problem is]
Why it's problematic: [cite the relevant rule/standard in plain English]
Suggested rewrite: [provide compliant alternative language]
```

### Step 4 — Compliant Version

Rewrite the full communication with all flags resolved. Mark changes with `[REVISED]` inline so the advisor can see exactly what changed.

### Step 5 — Disclosure Checklist

List any required disclosures that should be added before sending, with suggested standard language:

- [ ] Past performance disclaimer (suggested text included)
- [ ] Registration disclosure
- [ ] Testimonial / endorsement disclosure (if applicable)
- [ ] Hypothetical performance disclosure (if applicable)
- [ ] Material risk disclosure
- [ ] Other (specify)

---

## Disclaimer

> **IMPORTANT**: This skill is a drafting aid and first-pass screening tool only. It does not constitute legal or compliance advice. The output of this skill has not been reviewed by a licensed attorney or registered compliance officer. Final compliance review must be performed by a qualified compliance officer or legal counsel before any communication is distributed to clients or prospects. Rules and regulations vary by jurisdiction, registration type, and firm-specific policies.

---

## Example Output

**Input**: Client email from an advisor.

> *Subject: We crushed the market again!*
>
> Hi John,
>
> Just wanted to update you — our model portfolio beat the S&P 500 last year. We're one of the best-performing advisory firms in the region and our clients never lose money. Sarah, one of our clients, said we doubled her retirement savings in 3 years. I'm confident we'll keep delivering for you.
>
> Let me know if you want to add more to your account. Talk soon,
> Mike

---

### Issue Report

**FLAG #1 — Performance Promises / Guarantees**
Location: *"our clients never lose money"*
Issue: This is a guarantee of investment performance, which is prohibited.
Why it's problematic: No investment is free of loss risk. This language violates FINRA Rule 2210 and SEC advertising rules prohibiting false or misleading statements. It could expose the firm to regulatory action and client claims.
Suggested rewrite: *"Our focus on risk management is designed to limit downside in volatile markets."*

---

**FLAG #2 — Unsubstantiated Superlatives**
Location: *"one of the best-performing advisory firms in the region"*
Issue: Superlative claim with no substantiation, source, criteria, or time period.
Why it's problematic: Under FINRA Rule 2210 and SEC Marketing Rule, comparative claims require a disclosed, objective third-party basis. "Best" without that is a prohibited unsubstantiated claim.
Suggested rewrite: Remove entirely, or replace with: *"We're proud of our track record and focus on consistent, risk-adjusted returns for our clients."*

---

**FLAG #3 — Testimonial Without Required Disclosures**
Location: *"Sarah, one of our clients, said we doubled her retirement savings in 3 years"*
Issue: Client testimonial used without required disclosures under SEC Marketing Rule (Rule 206(4)-1).
Why it's problematic: The SEC Marketing Rule requires any testimonial or endorsement to include: (1) disclosure of the person's relationship with the advisor, (2) whether they were compensated, and (3) a statement that results may not be representative. Without these, the testimonial is non-compliant.
Suggested rewrite: Either remove the testimonial or add required disclosures. If retained: *"Sarah is a current client. She was not compensated for this statement. Her experience may not be representative of all clients. Past performance is not indicative of future results."*

---

**FLAG #4 — Missing Past Performance Disclaimer**
Location: *"beat the S&P 500 last year"*
Issue: Performance claim with no past performance disclaimer, no full time period context, no benchmark comparison methodology disclosed.
Why it's problematic: SEC and FINRA rules require that performance claims include adequate disclosure. A single year comparison with no benchmark description, no fees disclosure, and no past performance disclaimer is misleading.
Suggested rewrite: Add disclaimer and context: *"[FIRM] composite portfolios returned X% net of fees in [YEAR], compared to the S&P 500 Total Return of Y% over the same period. Past performance is not indicative of future results. All investments involve risk, including possible loss of principal."*

---

**FLAG #5 — Forward-Looking Statement as Certainty**
Location: *"I'm confident we'll keep delivering for you"*
Issue: Implied prediction of future performance.
Why it's problematic: While "confident" is softer than "will," in context it implies continued outperformance, which is a prohibited performance prediction.
Suggested rewrite: *"We remain committed to our disciplined investment process and to keeping your portfolio aligned with your goals."*

---

### Compliant Rewrite

**Subject**: [REVISED] Q[X] Portfolio Update — John

Hi John,

[REVISED] I wanted to share a quick update on your portfolio. Our model portfolios returned [X]% net of fees in [YEAR], compared to the S&P 500 Total Return of [Y]% over the same period. [REVISED] We're proud of our disciplined, risk-focused investment process.

[REVISED] *Our focus on risk management is designed to limit downside in volatile markets*, while pursuing long-term growth aligned with your goals.

[REVISED — TESTIMONIAL REMOVED OR ADD FULL DISCLOSURE IF RETAINED]

[REVISED] We remain committed to our disciplined investment process and to keeping your portfolio aligned with your goals. Happy to set up a call if you'd like to discuss.

Talk soon,
Mike

[ADVISOR NAME] | [TITLE] | [FIRM NAME]
[CRD / Registration Number]

*Past performance is not indicative of future results. All investments involve risk, including the possible loss of principal. This email is for informational purposes only and does not constitute investment advice.*

---

### Disclosure Checklist

Before sending, confirm the following are included:

- [x] **Past performance disclaimer** ✓ Added: *"Past performance is not indicative of future results."*
- [ ] **Registration disclosure** — Add: *"[FIRM] is a registered investment adviser with the SEC / [State]. Registration does not imply a certain level of skill or training."*
- [ ] **Fee disclosure** — If performance is cited net of fees, confirm this is stated explicitly. If gross, disclose that fees would reduce returns.
- [ ] **Testimonial disclosures** — If Sarah's quote is retained, add full SEC Marketing Rule disclosures (relationship, compensation, representativeness).
- [ ] **Risk disclosure** — Add strategy-specific risk disclosure if recommending specific investments or strategies.
- [ ] **Firm compliance review** — This rewrite should be reviewed by your firm's compliance department before sending.
