# AAOIFI — Decision Frameworks

This file contains the working decision frameworks you use when applying AAOIFI standards to a live question. These are the **diagnostic flows** — when the user asks "what should I do?", you walk through one of these.

## Table of contents

1. The Shari'ah-compliance gate — generic
2. Recognition decision tree for a financing transaction
3. Sukuk classification decision tree
4. ECL stage assignment under FAS 30
5. Profit-distribution waterfall (IAH vs. shareholders)
6. IFRS-vs-AAOIFI gap-analysis methodology
7. Conversion of a conventional bank to an Islamic bank (SS 6)
8. Tawarruq alternatives decision tree
9. SNCI quantification and treatment
10. Choosing the right AAOIFI deliverable format

---

## 1. The Shari'ah-compliance gate — generic

When the user asks **"is this Shari'ah compliant?"**, walk through:

1. **Identify the contract type** — Murabaha, Ijarah, Mudaraba, Musharakah, Salam, Istisna, Wakala, Sukuk, etc. If the structure is hybrid, decompose it.
2. **Locate the governing Shari'ah Standard** — using `standards-catalogue.md` cross-reference index.
3. **Test against the standard's core requirements**:
   - Subject matter — must be permissible (e.g., not alcohol, not pork, not riba-based instruments)
   - Contract elements — offer, acceptance, capacity, consideration
   - Ownership — does the IFI take ownership and risk where the contract requires?
   - Possession — physical or constructive, where required?
   - Pricing — disclosed cost-plus where required (Murabaha), agreed in advance where required
   - Risk allocation — does it follow the contract's classical risk profile?
   - Separation of contracts — are bundled contracts in fact separable?
4. **Check for contemporary contested elements** — see `shariah-standards-deep-dive.md` section 16. Is the structure Tawarruq, Bay' al-Inah, Bilateral Wa'd? If so, flag the AAOIFI position and the alternative scholarly views.
5. **Apply the jurisdictional overlay** — does the IFI's regulator's CSB or the IFI's SSB impose additional conditions?
6. **Conclude with the AAOIFI position first**, then any divergent jurisdictional view.

---

## 2. Recognition decision tree for a financing transaction

User: *"We disbursed PKR 50M to a customer to buy a vehicle. How do we book it?"*

```
Is it a Murabaha?
├─ Yes → Did the IFI take ownership of the asset before sale?
│        ├─ Yes (physical or constructive) → FAS 28 applies; book as Murabaha (see fas-deep-dive.md §3)
│        └─ No (synthetic) → Shari'ah issue; either restructure or reclassify
│
├─ Could it be an Ijarah / IMB?
│  ├─ Yes → FAS 32 applies; book as Ijarah / Ijarah liability
│  └─ No → continue
│
├─ Could it be a Diminishing Musharakah?
│  ├─ Yes → FAS 43 applies; three-stream booking
│  └─ No → continue
│
├─ Is it a Salam / Istisna?
│  ├─ Yes → FAS 7 / FAS 10 (or FAS 53 if development) applies
│  └─ No → continue
│
├─ Is it a Qard Hasan?
│  ├─ Yes → FAS 45 applies; separate fund
│  └─ No → continue
│
└─ Likely a Wakala / Mudaraba / Musharakah investment? → consult fas-deep-dive.md
```

If none of the above fit cleanly, the structure may not be properly Shari'ah-classified — escalate to SSB.

---

## 3. Sukuk classification decision tree

User: *"We bought USD 10M of [issuer] Sukuk. Where does it go?"*

Step 1 — **Identify the Sukuk's underlying structure**:

- Ijarah Sukuk → equity-of-asset; tradable
- Mudaraba/Musharakah Sukuk → equity-of-partnership; tradable if structure compliant
- Wakala Sukuk → mixed; check tangible-asset proportion
- Murabaha Sukuk → debt-type; tradable only at par
- Hybrid Sukuk → check 51% tangible-asset rule (SS 17, SS 59)

Step 2 — **Determine intent and characteristics**:

```
Intent — hold to maturity, and the Sukuk has SPPI-equivalent cash flows?
├─ Yes → Investments at Amortised Cost (FAS 33)
│
Intent — hold long-term, may sell?
├─ Yes → Investments at Fair Value through Equity (FAS 33)
│
Intent — trading or short-term disposal?
├─ Yes → Investments at Fair Value through Income Statement (FAS 33)
```

Step 3 — **Apply the impairment model**:

- Amortised Cost → FAS 30 ECL (three-stage)
- FV-through-Equity equity-type → significant/prolonged decline test
- FV-through-Income → no separate impairment (mark-to-market)

Step 4 — **Disclose both**:
- The Shari'ah classification (Ijarah, Mudaraba, Wakala, Hybrid…)
- The accounting classification (Amortised / FVTOCI / FVTPL)

---

## 4. ECL stage assignment under FAS 30

For each financing receivable:

```
Is it credit-impaired (default, 90+ DPD, evidence of impairment)?
├─ Yes → Stage 3 → Lifetime ECL, profit on net carrying amount
│
Has there been a significant increase in credit risk (SICR) since initial recognition?
│  Tests — quantitative (lifetime PD vs origination) + qualitative (watchlist, restructure, sector stress) + backstop (30+ DPD)
├─ Yes → Stage 2 → Lifetime ECL, profit on gross carrying amount
│
Otherwise → Stage 1 → 12-month ECL, profit on gross carrying amount
```

For new originations, default is Stage 1 (unless credit-impaired at origination — "POCI", purchased-or-originated-credit-impaired, treated specially).

When the user asks for an ECL working under FAS 30 — produce as Excel using the `xlsx` skill with these columns:
- Customer ID, Product, Outstanding, Stage, PD, LGD, EAD, 12-month ECL, Lifetime ECL, Applicable ECL, Stage rationale

---

## 5. Profit-distribution waterfall (IAH vs. shareholders)

The classic IFI profit-distribution mechanism:

```
Gross income from invested funds (after direct costs)
│
├─ Allocate to Mudaraba pool (IAH-funded + shareholder-funded)
│
├─ Less: Provisions for losses on assets in the pool
│
├─ Less: PER (Profit Equalisation Reserve) transfer (FAS 35)
│
= Distributable income from Mudaraba pool
│
├─ IAH share (Rabb-al-Mal, e.g., 80%) × IAH funding ratio
│  │
│  └─ Less: IRR transfer (Investment Risk Reserve, FAS 35)
│  │
│  └─ IAH net return — distributed per tier (FAS 5, FAS 27, SS 40)
│
└─ IFI share (Mudarib + own funds)
   │
   └─ IFI's Mudarib fee + return on shareholder funds
```

The key controls and disclosures:
- **PER and IRR movements** must be approved by SSB (FAS 35, GSIFI 2)
- **Hibah** (voluntary top-up by IFI to IAH) must be disclosed and must not be guaranteed (SS 40)
- **IAH funding ratio** must be disclosed (FAS 5)
- **Profit-sharing ratio (PSR)** must be set at the start of each profit period (SS 13, SS 40)

---

## 6. IFRS-vs-AAOIFI gap-analysis methodology

When asked to compare IFRS and AAOIFI for an IFI:

1. **Determine the reporting framework hierarchy**:
   - Primary basis (AAOIFI or IFRS)?
   - Reconciliation pack required?
   - Group reporting needs (e.g., consolidated under IFRS, subsidiary under AAOIFI)?

2. **Map each material balance and line item** to the relevant standard pair:
   - Use the table in `fas-deep-dive.md` section 14 as your starting point.
   - Identify line items where AAOIFI requires additional statements (Charity Fund, IAH Equity, Qard Hasan Fund, Zakah).
   - Identify line items where measurement differs (Takaful = FAS 42 vs IFRS 17).

3. **Quantify the gaps**:
   - For each line item with measurement difference, compute the GAAP-conversion adjustment.
   - For each presentation difference, identify the disclosure note that captures it.

4. **Produce the reconciliation pack** — usually an Excel workbook with three views: AAOIFI-as-reported, IFRS-equivalent, Reconciliation.

---

## 7. Conversion of a conventional bank to an Islamic bank (SS 6)

When the user is exploring conversion (relevant under the FSC 2022 judgment for Pakistan):

Steps per SS 6:
1. **Cessation of riba-bearing operations** — stop new conventional financing.
2. **Wind-down of existing conventional book** — either Shari'ah-compliant restructure, novation, or run-off.
3. **Conversion of investment book** — divest non-compliant equities, restructure or sell conventional bonds.
4. **Conversion of deposits** — replace interest with PLS (Mudaraba) IAH structure.
5. **SSB appointment and approval of entire framework** before re-licensing as IFI.
6. **Treatment of legacy income** — interest accrued but not yet earned at conversion goes to charity fund (SNCI treatment).

For Pakistan-specific conversion planning, also cross-reference SBP IBD Circular on conversion guidelines and SECP for any non-banking subsidiaries.

---

## 8. Tawarruq alternatives decision tree

When the user proposes Tawarruq for treasury liquidity / customer cash financing, walk through alternatives **before** approving Tawarruq:

```
Need is short-tenor interbank liquidity (≤ 30 days)?
├─ Yes → Try Wakala bil Istithmar (SS 23, SS 46) first
│        Mudaraba interbank as second choice
│
Need is medium-tenor customer cash financing?
├─ Yes → Can the customer use the cash for a specific asset purchase?
│        ├─ Yes → Use Murabaha on the actual asset (SS 8)
│        └─ No (true cash need) → consider Salam on customer's future commodity output
│
Need is large syndicated finance?
├─ Yes → Try Wakala-managed pool, Mudaraba Sukuk, or Murabaha syndication on real assets
│
Only after these alternatives are exhausted → consider Tawarruq with explicit SSB approval
```

Document the alternatives considered — this is what an external Shari'ah auditor will want to see (ASIFI 4 / ASIFI 6).

---

## 9. SNCI quantification and treatment

When the IFI identifies Shari'ah non-compliance income (SNCI):

Step 1 — **Identify the source**:
- Late-payment charges on Murabaha receivables
- Interest on statutory reserves at the conventional central bank
- Dividends from screened equities that crossed thresholds (e.g., > 5% revenue from non-permitted activities)
- Interest on Nostro accounts at conventional correspondents

Step 2 — **Quantify**:
- Period income from each source.
- Cumulative balance if previously not segregated.

Step 3 — **Segregate** — reclassify from P&L to a balance-sheet liability "Income to be donated to charity".

Step 4 — **Distribute** — under SSB oversight, donate to charitable causes that are documented (recipients, amounts, dates). This forms the Sources and Uses of Charity Funds statement.

Step 5 — **Disclose** — annually, in financial statements and SSB report.

Step 6 — **Prevent** — analyse the root cause and propose structural fixes (e.g., negotiate non-interest-bearing correspondent accounts, restructure screened equity holdings).

---

## 10. Choosing the right AAOIFI deliverable format

| User need | Deliverable | Format |
|---|---|---|
| Quick technical question | Inline cited answer | Chat response |
| Accounting position memo | Memo with bottom line, standards, reasoning, signature lines | DOCX (use `docx` skill) |
| Shari'ah opinion draft | Memo addressed to/from SSB, with cited clauses | DOCX |
| Journal-entry workbook | Multi-tab Excel — JE schedule, supporting calcs, references | XLSX (use `xlsx` skill) |
| ECL working | Excel with the 9-column standard format | XLSX |
| Profit-distribution working | Excel waterfall with PER/IRR/Hibah lines | XLSX |
| Sukuk classification + amortisation | Excel — categorisation, amortisation schedule, accrual table | XLSX |
| FS template (annual / interim) | Excel template with all required AAOIFI statements (FAS 1, FAS 41) | XLSX |
| Board paper / SSB pre-read | PowerPoint with executive summary, options, recommendation | PPTX (use `pptx` skill) |
| Training deck (e.g., for CIP) | PowerPoint with curriculum-style structure | PPTX |
| Regulator submission pack | PDF — bundled memo + workbook + exhibits | PDF (use `pdf` skill to assemble) |

See `deliverable-templates.md` for the actual template structures.
