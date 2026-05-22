# AAOIFI — Deliverable Templates

The structures below are what a senior partner would expect to see when this skill produces an output. Each template gives you a ready scaffold — the actual content comes from the AAOIFI analysis you've done using the other reference files.

## 1. Technical accounting memo (DOCX)

Use the `docx` skill. Standard structure:

```
[IFI Letterhead — or omit if generic]

TECHNICAL ACCOUNTING MEMO

To:        [Recipient — e.g., CFO / Head of Financial Reporting / External Auditor]
From:      [Author / Drafter — e.g., Finance Manager]
Reviewed:  [Reviewer — e.g., Head of Finance / Shariah Compliance Head]
Date:      [DD Month YYYY]
Re:        [Subject — single line, e.g., "Accounting Treatment of [Transaction] under FAS [X]"]
Standards: [Pipe-separated list — e.g., FAS 28 | FAS 30 | SS 8]

────────────────────────────────────────────────────

1. Executive Summary

   [One short paragraph — the recommended treatment and why. Lead with the answer.]

2. Background and Facts

   2.1 Counterparty and tenor
   2.2 Contract documents
   2.3 Cash flow profile
   2.4 Shari'ah classification

3. Standards Engaged

   3.1 FAS [X] — [Title]
       - Scope: [paragraph reference]
       - Recognition: [paragraph reference]
       - Measurement: [paragraph reference]
       - Presentation and disclosure: [paragraph reference]
   3.2 SS [Y] — [Title]
       - Headline rule and any contemporary debate

4. Analysis

   4.1 Recognition trigger and entries
        [Show bookings as a small table — date, Dr, Cr, amount, narrative]
   4.2 Subsequent measurement
   4.3 Presentation and disclosure
   4.4 Impairment treatment (if applicable — FAS 30)
   4.5 IFRS reconciliation (if dual reporting)

5. Recommended Accounting Treatment

   [Specific, citable, audit-ready statement of treatment.]

6. Open Questions / Items Requiring SSB or Auditor Sign-off

   - [Specific items]

7. Effective Date and Transition

   [If a new standard — effective date and transition approach]

────────────────────────────────────────────────────

Prepared by: ___________________   Reviewed by: ___________________
                Name / Date                       Name / Date

Acknowledged by SSB: ___________________
                          Chair / Date
```

## 2. Shari'ah opinion draft (DOCX)

```
[IFI Letterhead]

SHARI'AH OPINION — DRAFT

To:        Board of Directors via [Company Secretary]
From:      Shari'ah Supervisory Board, [IFI Name]
Date:      [DD Month YYYY]
Re:        [Subject — e.g., "Shari'ah Compliance of [Product] Structure"]

────────────────────────────────────────────────────

1. Question Presented

   [The Shari'ah question — phrased neutrally, not leading.]

2. Documents and Information Reviewed

   - [Term sheet]
   - [Draft contract documents]
   - [Cash-flow and ownership analysis]
   - [Comparator structures used in [jurisdiction]]

3. Shari'ah Analysis

   3.1 Identification of contracts involved
        [Decompose the structure into Shari'ah contracts.]
   3.2 Application of governing Shari'ah Standards
        - SS [X] — [headline rule, clause references]
        - SS [Y] — [headline rule, clause references]
   3.3 Specific Shari'ah issues considered
        - Ownership and possession
        - Risk allocation
        - Separation of contracts
        - Promise (Wa'd) treatment
        - Pricing and disclosure
   3.4 Treatment of contested elements
        [If applicable — Tawarruq, Bay' al-Inah, etc. — with AAOIFI vs. alternative views.]

4. Conditions and Safeguards

   [What the structure needs to comply — e.g., separate documentation, ownership steps, disclosure.]

5. Opinion

   The Shari'ah Supervisory Board is of the opinion that, subject to the conditions and safeguards set out in section 4 above, the proposed [Product] structure is in compliance with Shari'ah rules and principles as set out in AAOIFI Shari'ah Standards Nos. [X, Y, Z].

   [If qualified — state qualifications clearly.]

6. Implementation Guidance

   - Documentation that must be executed in sequence
   - Internal controls to be put in place
   - Periodic review cadence
   - Items to be reported back to the SSB

────────────────────────────────────────────────────

SSB Members:

___________________   ___________________   ___________________
Chair, [Name]            Member, [Name]           Member, [Name]
Date:                    Date:                    Date:

────────────────────────────────────────────────────

Note: This is a draft Shari'ah opinion. The binding fatwa must be issued by the IFI's appointed Shari'ah Supervisory Board after their own deliberation. This draft is prepared as a working document to facilitate that deliberation.
```

## 3. Excel — journal-entry workbook (XLSX)

Tab structure (use `xlsx` skill):

| Tab | Content |
|---|---|
| **README** | Purpose, version, author, change log, AAOIFI standards engaged |
| **Inputs** | All input parameters — amounts, dates, rates, contract terms — in named ranges |
| **Schedule** | The cash-flow schedule (e.g., Murabaha amortisation table) |
| **JE_Day1** | Initial-recognition journal entries with narratives |
| **JE_Period** | Periodic profit-recognition entries (one row per period or aggregated) |
| **JE_Maturity** | Final-period and derecognition entries |
| **Disclosures** | Required disclosures per FAS — table extract for the FS notes |
| **IFRS_Reconciliation** | If dual reporting — IFRS equivalent and reconciliation |
| **Standards** | Citation index — every line linked to FAS / SS clause |

## 4. Excel — ECL working under FAS 30 (XLSX)

Required columns:

| Column | Notes |
|---|---|
| Customer ID | Or facility ID |
| Product | Murabaha / Ijarah / Salam / Istisna / Sukuk-AC |
| Original Disbursement Date | |
| Maturity Date | |
| Outstanding Gross Carrying Amount | EAD basis |
| Days Past Due | For Stage 2 / 3 backstops |
| Stage | 1, 2, or 3 |
| Stage rationale | Free text — SICR test, qualitative override |
| PD (12-month or lifetime) | As applicable to stage |
| LGD | Adjusted for Shari'ah-compliant collateral (Rahn) |
| EAD | For undrawn — apply CCF |
| Discount Rate | Effective profit rate |
| 12-month ECL | For Stage 1 |
| Lifetime ECL | For Stage 2/3 |
| Applicable ECL | Selected per stage |
| IAH Share of ECL | Per FAS 5/FAS 35 IAH allocation |
| Shareholders' Share of ECL | The complement |
| Period Movement | Increase/decrease vs. last period |
| Comments | Watchlist flag, restructuring history, etc. |

Plus separate tabs for: Macroeconomic scenarios, Sensitivity, Movement reconciliation by stage.

## 5. Excel — profit-distribution waterfall (XLSX)

Tab structure:

| Tab | Content |
|---|---|
| **Inputs** | Pool sizes (IAH funds by tier, shareholder funds), gross income, PSR, costs |
| **Allocation** | Gross income → pool → less provisions → less PER → distributable income |
| **IAH_Distribution** | IAH share × funding ratio, less IRR, by tier, gross-to-net by tier |
| **Shareholder_Distribution** | Mudarib fee + return on own funds |
| **Hibah** | Voluntary top-up (if any), source from shareholders, allocation |
| **Reserves_Movement** | PER and IRR opening, transfers in, distributions out, closing |
| **Disclosures** | The narrative + table for the FS notes (FAS 5, FAS 27, FAS 35, SS 40) |

## 6. PowerPoint — board paper / SSB pre-read (PPTX)

Slide structure (use `pptx` skill):

1. **Title slide** — Subject, date, recipient (Board / SSB), classification
2. **Executive summary** — 5 bullets, max
3. **Background and context**
4. **Standards engaged** — AAOIFI standards involved
5. **The question(s) before the board / SSB**
6. **Options and trade-offs** — typically 3 options with pros/cons
7. **Risk assessment** — Shari'ah, regulatory, accounting, reputational
8. **Recommendation** — single recommended path with rationale
9. **Implementation plan** — timeline, milestones, accountabilities
10. **Decisions requested** — explicit ask for the body
11. **Appendix** — detailed standards citations, contract excerpts, comparator analysis

For SSB pre-reads specifically, replace slide 7's "Risk assessment" with a dedicated "Shari'ah considerations" slide and de-emphasise regulatory/reputational angles unless directly Shari'ah-relevant.

## 7. Training deck (PPTX)

For curriculum delivery (e.g., CIP Certified Credit Professional, NIBAF, IBA-CEIF, Karachi University Islamic banking certificate):

1. **Welcome / learning objectives**
2. **Why this matters** — practitioner stories, regulatory drivers
3. **Concept introduction** — definitions, history, classical sources
4. **Standard walkthrough** — paragraph-by-paragraph for the chosen AAOIFI standard
5. **Worked example** — concrete numbers, complete bookings
6. **Common pitfalls** — what auditors find
7. **Contemporary debates** — divergent views, where the market is going
8. **Jurisdictional overlay** — particularly for Pakistani audiences
9. **Hands-on exercise** — class works through a case study
10. **Self-assessment questions** — for the workbook
11. **Further reading** — AAOIFI website, key papers, ISRA / IFA-OIC publications

Pair the training deck with a participant workbook (DOCX) and an instructor guide (DOCX).

## 8. PDF — regulator submission pack

For SBP / SECP / CBB / HSA / SAMA submissions, assemble (use `pdf` skill):

1. Cover letter from CEO / CFO
2. Executive summary
3. Technical accounting memo (per template 1 above)
4. SSB opinion (per template 2 above) — if relevant
5. Excel workbook exhibits — convert to PDF tables for inclusion
6. Standards index — list of AAOIFI standards cited
7. Regulatory references — SBP/CBB/etc. circulars cited
8. Signature page

All citations consistent across the pack; page numbers continuous.

---

> **Style closing note.** When producing deliverables in any format, the test is the same: would a senior partner at a Big-4 Islamic Finance Centre of Excellence sign this? If not, tighten the citations, sharpen the recommendation, and check the format. AAOIFI work rewards precision.
