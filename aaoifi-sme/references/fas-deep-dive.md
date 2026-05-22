# AAOIFI FAS — Deep Dive Reference

This file is the working reference for **applying** the AAOIFI Financial Accounting Standards. It assumes you have already consulted `standards-catalogue.md` to identify the right standard number. Here we go one level deeper — recognition triggers, measurement bases, presentation, disclosure, and the most common audit traps.

> Always quote paragraph numbers verbatim from the issued standard text. The structure below is your guide; the standard is the authority.

## Table of contents

1. The FAS framework — overarching principles
2. FAS 1 (Revised 2021) — General Presentation and Disclosures
3. FAS 28 — Murabaha and Other Deferred Payment Sales
4. FAS 30 — Impairment, Credit Losses and Onerous Commitments (AAOIFI ECL)
5. FAS 32 — Ijarah
6. FAS 33 — Investments in Sukuk, Shares and Similar Instruments
7. FAS 35 — Risk Reserves (PER / IRR)
8. FAS 39 — Financial Reporting for Zakah
9. FAS 40 — Financial Reporting for Islamic Finance Windows
10. FAS 42 — Takaful Disclosures
11. FAS 43 — Diminishing Musharakah
12. FAS 44 — Islamic Microfinance Institutions
13. FAS 53 — Istisna-Based Development Contracts (newly approved)
14. The IFRS-to-AAOIFI reconciliation cheat sheet

---

## 1. The FAS framework — overarching principles

The AAOIFI Accounting Board operates under the **Conceptual Framework for Financial Reporting by Islamic Financial Institutions**. The five anchoring principles to keep in mind:

1. **Substance over form, but with a Shari'ah filter.** An Islamic transaction that has the economic substance of conventional financing (e.g., a Murabaha to the Purchase Orderer) is still recognised in the form Shari'ah requires — as a sale, with the embedded financing element distinctly disclosed (FAS 28, para. 7–10).
2. **Risk sharing reflected in classification.** Investment Account Holders (IAH) bear investment risk and are therefore classified separately from depositors (FAS 5, FAS 6, FAS 27, FAS 35).
3. **Profit follows ownership and effort.** Profit allocation between the IFI (as Mudarib) and IAH (as Rabb-al-Mal) must reflect the Mudaraba contract terms, not a fixed-margin convention (FAS 5, FAS 35, SS 40).
4. **Time value of money is recognised as embedded in deferred-price contracts**, not as standalone interest (FAS 28).
5. **Zakah is a financial-reporting concern, not a discretionary item** (FAS 39).

---

## 2. FAS 1 (Revised 2021) — General Presentation and Disclosures

The umbrella standard. Replaces the original FAS 1 (1996). **Effective for periods beginning on or after 1 January 2023.**

Required primary statements for an IFI:

- Statement of Financial Position
- Statement of Income
- Statement of Changes in Owners' Equity
- Statement of Cash Flows
- **Statement of Changes in Equity of Investment Account Holders** *(uniquely IFI)*
- Statement of Sources and Uses of Charity Funds *(uniquely IFI)*
- Statement of Sources and Uses of Qard Hasan Fund *(uniquely IFI, if maintained)*
- Notes to the Financial Statements
- **Report of the Shari'ah Supervisory Board** (governance — not technically an FS component, but presented together)
- Zakah disclosure (per FAS 39)

The IFI-specific statements (changes in IAH equity, charity fund, Qard Hasan fund) are the single biggest presentation difference vs. IFRS conventional banks. An IFI cannot omit them.

Common audit findings: missing Statement of Sources and Uses of Charity Funds (which captures **Shari'ah Non-Compliance Income** — SNCI — accumulated and then donated); missing IAH-specific share of impairment reversals; insufficient disclosure of profit-distribution methodology.

---

## 3. FAS 28 — Murabaha and Other Deferred Payment Sales

The operative standard for Murabaha. **Replaced FAS 2 (Murabaha) and FAS 20 (Deferred Payment Sale).**

### Recognition triggers

A Murabaha is recognised in the IFI's books only after **constructive possession** by the IFI (FAS 28, para. 14; SS 8, clause 2/2/4). Pre-possession, the customer's promise (Wa'd) under Murabaha-to-the-Purchase-Orderer (MPO) is **not** the recognition trigger.

### Bookings — typical sequence

| Step | Entry |
|---|---|
| 1. IFI purchases the asset from supplier | Dr **Murabaha Asset (Inventory)** / Cr Cash / Payable to supplier |
| 2. IFI sells to customer at cost-plus-markup, deferred payment | Dr **Murabaha Receivable** (gross) / Cr Murabaha Asset / Cr **Deferred Murabaha Income** |
| 3. Recognition of profit over the term | Dr Deferred Murabaha Income / Cr **Murabaha Income** (effective profit method) |
| 4. Customer instalment received | Dr Cash / Cr Murabaha Receivable |
| 5. Late payment / default | Late-payment amounts → **Charity Fund** (cannot be recognised as IFI income) per SS 3 |

### Measurement

Murabaha Receivable is measured **at the net amortised cost using the effective profit rate** (FAS 28, para. 20–24). Note the distinction: AAOIFI uses *"effective profit rate"* — not *"effective interest rate"*. Substantively similar to IFRS 9's EIR, but the naming matters in disclosure.

### Common audit traps

- IFI did not take title/risk before sale → not a valid Murabaha (Shari'ah issue, also FAS 28 recognition failure).
- "Murabaha" used as a synthetic loan with no real underlying asset → likely **organised Tawarruq** (SS 30 — debated; many SSBs require explicit board approval).
- Deferred income amortised straight-line rather than via effective-profit-rate → presentation overstatement of early-period income.
- Late-payment charges routed to P&L rather than charity → income contamination; recurring finding in SBP / CBB inspections.

---

## 4. FAS 30 — Impairment, Credit Losses and Onerous Commitments (AAOIFI ECL)

The AAOIFI equivalent of IFRS 9 expected credit losses. **Effective for periods beginning 1 January 2020.**

### Three-stage model

| Stage | Trigger | ECL measurement | Profit recognition |
|---|---|---|---|
| **Stage 1** | Performing — no significant increase in credit risk (SICR) since initial recognition | **12-month ECL** | On gross carrying amount |
| **Stage 2** | SICR has occurred but not yet credit-impaired | **Lifetime ECL** | On gross carrying amount |
| **Stage 3** | Credit-impaired (default, 90+ DPD presumption, evidence of impairment) | **Lifetime ECL** | On **net** carrying amount (gross less ECL) |

### Scope adaptations vs. IFRS 9

- Applies to **Murabaha receivables, Salam receivables, Istisna receivables, Ijarah net investment, Mudaraba/Musharakah financing receivables**, and Sukuk classified at amortised cost.
- For **equity-type Sukuk** (FAS 33), the impairment model is **closer to IAS 36** — significant or prolonged decline triggers impairment.
- For **off-balance-sheet financing commitments** under Islamic contracts (e.g., Wa'd-based purchase undertakings), FAS 30 introduces an **onerous commitment** provision concept that has no direct IFRS 9 analogue.

### PD × LGD × EAD applies — but with Shari'ah-aware overlays

- **PD** — same modelling approach as IFRS 9, but credit policies must respect Shari'ah-defined product limits.
- **LGD** — recovery from collateral can include **Rahn (Shari'ah-compliant pledge)**; recovery from collateral **must not include conventional guarantee fee income**.
- **EAD** — for Murabaha, EAD = outstanding receivable net of deferred profit; for Ijarah, EAD = net investment in the lease.

### Disclosure pack expected by auditors

- Gross carrying amount and ECL by stage
- Movement reconciliation (transfers between stages, new originations, derecognition, write-offs)
- Sensitivity disclosure — at minimum +/- 1 standard deviation on PD; many IFIs disclose macroeconomic-scenario weights
- IAH share of impairment recoveries (per FAS 5 / FAS 35 — IAH bears part of the credit risk on assets funded by IAH equity)

---

## 5. FAS 32 — Ijarah

Operative for Ijarah (operating lease) and Ijarah Muntahia Bittamleek (lease ending in ownership transfer). **Replaced FAS 8.**

### Lessor's books (the IFI is typically the lessor)

- **Operating Ijarah**: leased asset stays on the lessor's balance sheet; rentals are recognised as income over the lease term (typically straight-line unless another basis better reflects the pattern of benefit).
- **Ijarah Muntahia Bittamleek**: the legal transfer can be via gift (Hibah), sale at nominal price, or sale at market value. The economic substance varies — FAS 32 requires disclosure of the transfer mechanism.

### Lessee's books (IFI as lessee or corporate IFI clients)

FAS 32 introduces a **right-of-use (ROU) asset and Ijarah liability** model — broadly analogous to IFRS 16, but with these Shari'ah-driven differences:

- The lease must reflect actual usufruct of an identifiable asset (no synthetic ROU constructions).
- Variable rentals tied to a benchmark (e.g., 3-month KIBOR + 250 bps) are **permitted** under SS 9 with caveats, but **must be disclosed** as a feature.
- The Ijarah liability does not bear a "discount rate" labelled as interest — it is the rate implicit in the Ijarah or the IFI's incremental Ijarah rate.

### Common traps

- IMB transfers via **automatic transfer at end of term** without separate sale/gift contract → Shari'ah non-compliance (SS 9, clause 8/2 requires distinct transfer mechanism).
- Lessor capitalising periodic Ijarah rental into the leased asset cost → presentation error.

---

## 6. FAS 33 — Investments in Sukuk, Shares and Similar Instruments

The Sukuk investor's standard. **Replaced parts of FAS 17 and FAS 25.**

Three classification categories (selected at initial recognition):

| Category | Suitable for | Measurement |
|---|---|---|
| **Investments at Amortised Cost** | Held-to-maturity Sukuk where contractual cash flows are SPPI-equivalent (return = principal + agreed profit) | Amortised cost using effective profit method |
| **Investments at Fair Value through Equity** | Sukuk and shares the IFI intends to hold long-term but may realise | FVTOCI-equivalent — fair value changes through equity, with reclassification rules for Shari'ah-compliant equity-type instruments |
| **Investments at Fair Value through Income Statement** | Trading book, short-term-disposal intent | FVTPL-equivalent — fair value changes through P&L |

### Impairment

- Amortised-cost Sukuk → FAS 30 ECL.
- FV-through-equity equity-type → impairment when significant or prolonged decline below cost.
- FV-through-income → no separate impairment (mark-to-market captures it).

### Common disclosure issues

- Failing to disclose the **Shari'ah classification of Sukuk** alongside the accounting classification — auditors increasingly demand both.
- Misclassifying a Mudaraba Sukuk (equity-type) as Amortised Cost (debt-type) because of practitioner habit.

---

## 7. FAS 35 — Risk Reserves (PER / IRR)

The standard governing the two reserves that IFIs use to smooth IAH returns and absorb credit losses on IAH-funded assets:

- **Profit Equalisation Reserve (PER)** — created from gross income before allocation, smoothes the return to IAH and shareholders together.
- **Investment Risk Reserve (IRR)** — created from IAH share of income only, exclusively absorbs investment losses borne by IAH.

Movements in PER and IRR must be:
- Disclosed in the Statement of Changes in IAH Equity (FAS 1 Revised)
- Approved by the SSB (governance link to GSIFI 2)
- Justified with a documented policy

The most common finding is **opacity** — many IFIs disclose only opening and closing balances. FAS 35 expects more granular disclosure of transfers in/out and the basis.

---

## 8. FAS 39 — Financial Reporting for Zakah

Replaces FAS 9. Mandatory for any IFI that either (a) is required by law to pay Zakah on behalf of shareholders, or (b) administers Zakah collection.

Key requirements:
- A separate **Zakah computation** disclosed in the financial statements.
- Disclosure of the **method** (Net Invested Funds / Net Assets — sometimes called "Shafi'i" vs. "Hanbali" methods; AAOIFI's preference is the Net Invested Funds method per SS 35).
- Beneficiary-side movements when Zakah is collected and distributed (Sources and Uses of Charity Funds for non-mandatory Zakah; separate Zakah fund for mandatory).

For Pakistani IFIs the interaction with the **Zakat and Ushr Ordinance 1980** is important — see `jurisdictional-overlay.md`.

---

## 9. FAS 40 — Financial Reporting for Islamic Finance Windows

Replaces FAS 18. Applies to conventional banks operating **Islamic Windows** (a structurally separate Islamic operation within a conventional banking licence).

The standard requires:
- **Ring-fenced reporting** of the window's assets, liabilities, income, and IAH equity.
- **Separate disclosure** of co-mingling (where the window uses parent-bank infrastructure) and the basis for cost allocation.
- **Distinct profit-distribution methodology** between the window's IAH and the parent shareholders.
- A standalone window-level Shari'ah audit (GSIFI 11 + ASIFI 6 apply).

This is highly relevant to UAE, Saudi Arabia, and Pakistan, where major conventional banks operate windows (e.g., HBL Islamic, ABL Islamic).

---

## 10. FAS 42 — Takaful Disclosures

Replaces FAS 12 and FAS 13. **Effective for periods beginning 1 January 2025.**

Key concepts:
- **Three-pool model**: Participants' Risk Fund (PRF), Participants' Investment Fund (PIF), and Shareholders' Fund (SHF).
- **Surplus distribution**: how surplus in the PRF is allocated between participants and the Takaful operator (typically via Wakala fee + Mudaraba on investment returns).
- **Qard from SHF to PRF**: the interest-free loan from shareholders to cover a participant risk deficit — recognised as a receivable in SHF and a liability in PRF.
- **Disclosure of the Takaful model** (pure Wakala, pure Mudaraba, Hybrid Wakala-Mudaraba, Waqf-based) — most GCC takafuls are hybrid; many Malaysian and Pakistani takafuls are pure Wakala.

---

## 11. FAS 43 — Diminishing Musharakah

The standard for the **Diminishing Musharakah (DM)** product — particularly common in **Pakistani Islamic mortgage** finance (e.g., Meezan Easy Home).

Key bookings:
- Joint ownership of the asset by IFI and customer at inception.
- Three streams of cash flow from the customer:
  1. **Rental** for the IFI's share of the asset (Ijarah leg) → recognised as rental income.
  2. **Unit purchase** by the customer of the IFI's share over time → derecognition of partial ownership.
  3. **Other charges** (e.g., maintenance, takaful) — pass-through.

The Ijarah and Unit Purchase contracts must be **separate** (SS 12); bundling them into one document is a recurring Shari'ah finding.

---

## 12. FAS 44 — Islamic Microfinance Institutions

Tailored standard for Islamic microfinance bodies — directly relevant to **Client-MFB (Client MFB), Akhuwat, Naymet, and similar institutions** in Pakistan.

Adapts FAS 1, 28, 30, 32 to the microfinance context:
- Simplified disclosures consistent with the scale of the institution.
- Specific recognition guidance for **Qard Hasan portfolios** (cross-reference FAS 45).
- Specific guidance on **group lending** structures common in microfinance.

For Client-MFB engagements, FAS 44 is the umbrella; FAS 28, 30, 32, 45 apply to product lines.

---

## 13. FAS 53 — Istisna-Based Development Contracts

**Approved by the AAOIFI Accounting Board at its 45th meeting (January 2026).** Likely effective date is periods beginning 1 January 2027 — verify against final issued text.

Scope:
- Istisna contracts where the IFI is engaging in **real-estate or infrastructure development** — i.e., extended-term Istisna with progressive construction milestones, not the simple manufacturing Istisna of FAS 10.
- Recognition over time using a milestone or cost-input method, with **specific guidance for "off-plan" pre-sale arrangements**.
- Treatment of **parallel Istisna** sub-contracts (the IFI subcontracts construction to a developer).

Until the final standard is published, follow FAS 10 for now and **flag this in any deliverable** as "anticipated change under FAS 53; revisit on issuance".

---

## 14. The IFRS-to-AAOIFI reconciliation cheat sheet

| Topic | IFRS treatment | AAOIFI treatment | Reconciliation gap |
|---|---|---|---|
| Murabaha receivable | IFRS 9 financial asset at amortised cost (EIR) | FAS 28 — amortised cost using effective profit rate | Same substance; disclosure naming differs |
| Sukuk investment | IFRS 9 (SPPI test → amortised cost / FVTOCI / FVTPL) | FAS 33 (Amortised / FV-through-Equity / FV-through-Income) | Largely aligned; FV-through-Equity may differ on recycling rules |
| Ijarah lessee | IFRS 16 ROU asset and lease liability | FAS 32 ROU asset and Ijarah liability | Largely aligned; FAS 32 requires Shari'ah-feature disclosure |
| ECL | IFRS 9 three-stage | FAS 30 three-stage | Aligned in mechanics; FAS 30 has IAH-share-of-loss disclosure not in IFRS |
| Zakah | Generally not recognised (capital distribution) | FAS 39 — recognised on P&L or charged against equity per jurisdictional law | Material gap — adds line items |
| IAH equity | IFRS 9 — typically liability or equity depending on terms | FAS 5/6/27 — separate "Equity of IAH" category | Material gap — adds a primary FS section |
| Charity Fund (SNCI) | Not recognised | FAS 1 Revised — Statement of Sources and Uses of Charity Funds | Material gap |
| Qard Hasan | IFRS 9 financial asset at amortised cost | FAS 45 — separate fund presentation | Disclosure-driven |
| Takaful | IFRS 17 insurance contracts | FAS 42 three-pool model | Materially different — see FAS 42 vs. IFRS 17 comparative paper from KPMG/EY for detail |

The dual-reporting IFI (e.g., a Bahraini bank under CBB or a Pakistani IFI for SBP) typically presents AAOIFI-primary with IFRS reconciliation in notes; some Malaysian IFIs go the other way under MFRS.

---

> **Closing note.** This file gets you to the point of drafting confidently. For the actual operative paragraph numbers, always read the issued standard PDF. AAOIFI standards are now free at https://aaoifi.com/e-standards/ — keep tabs on the issued vs. ED status of FAS 53 and the GSIFI 13/14 in particular.
