# AAOIFI Subject Matter Expert — Claude Skill

An installable Claude skill that acts as a senior Subject Matter Expert on the standards and pronouncements of the **Accounting and Auditing Organization for Islamic Financial Institutions (AAOIFI)** — the Bahrain-based standard-setting body for the global Islamic finance industry.

Author: **Amir W. Ahmed** ([amir.wahmed@gmail.com](mailto:amir.wahmed@gmail.com))
Status: v1.0 — initial release, May 2026
License: Proprietary — for educational and professional use

## What this skill does

Triggers on any AAOIFI-related question and produces audit-ready output for four personas in parallel:

1. **Islamic Bank Finance Team** — bookings, FAS application, financial statements, IFRS-vs-AAOIFI reconciliation
2. **Shari'ah Auditor / Shari'ah Board** — transaction review, fatwa-aligned product opinions, internal/external Shari'ah audit
3. **Product Structurer / Islamic Capital Markets** — Sukuk, Murabaha, Ijarah, Wakala documentation and structuring
4. **Regulator-facing / Academic / Training** — board papers, curriculum design, comparative regulatory analysis

Covers all **117+ AAOIFI standards** across the five families:

| Family | Identifier | Count |
|---|---|---|
| Financial Accounting Standards | FAS 1 – FAS 53 | 33 |
| Shari'ah Standards | SS 1 – SS 61 (draft) | 59 issued |
| Auditing Standards for Islamic Financial Institutions | ASIFI 1 – ASIFI 8 | 8 |
| Governance Standards for Islamic Financial Institutions | GSIFI 1 – GSIFI 14 | 14 |
| Code of Ethics | — | 3 |

## Folder layout

```
AAOIFI/
├── README.md                              ← this file
├── LICENSE
├── .gitignore
├── aaoifi-sme/                            ← the installable skill
│   ├── SKILL.md                           ← entrypoint with YAML frontmatter
│   └── references/
│       ├── standards-catalogue.md         ← all 117+ standards, numbered
│       ├── fas-deep-dive.md               ← FAS 1, 28, 30, 32, 33, 35, 39, 40, 42, 43, 44, 53
│       ├── shariah-standards-deep-dive.md ← SS 5, 8, 9, 17, 23, 26, 30, 40, 49, 57, 59
│       ├── audit-governance-ethics.md     ← ASIFI 1–8, GSIFI 1–14, Codes of Ethics
│       ├── jurisdictional-overlay.md      ← Pakistan, GCC, Malaysia, Indonesia, UK
│       ├── decision-frameworks.md         ← Shari'ah gate, ECL stages, Sukuk classification, IFRS-vs-AAOIFI
│       └── deliverable-templates.md       ← DOCX, XLSX, PPTX, PDF templates
└── source-materials/                      ← AAOIFI Exposure Drafts and reference PDFs
    └── (populated over time)
```

## Installation

### As a user skill in Cowork / Claude.ai

Copy the `aaoifi-sme/` folder to your local skills directory:

- **Windows**: `%APPDATA%\Claude\local-agent-mode-sessions\skills-plugin\<plugin-id>\<session-id>\skills\`
- **macOS**: `~/Library/Application Support/Claude/local-agent-mode-sessions/skills-plugin/<plugin-id>/<session-id>/skills/`

Or zip the `aaoifi-sme` folder with a `.skill` extension and present it via the Cowork "Save skill" install button.

### As a packaged skill

```bash
cd AAOIFI
zip -r aaoifi-sme.skill aaoifi-sme/
```

Then drop the `.skill` file into your Claude client to install.

## Triggering examples

The skill triggers automatically on prompts like:

- "Walk me through the journal entries for a PKR 50M Murabaha on a commercial vehicle."
- "Is organised Tawarruq Shari'ah compliant under AAOIFI?"
- "Build me an ECL working under FAS 30 for our microfinance Murabaha book."
- "Draft a Shari'ah opinion on a hybrid Wakala-Murabaha Sukuk."
- "Compare FAS 42 Takaful disclosures to IFRS 17."
- "What does GSIFI 12 require on Sukuk governance during a restructuring?"
- "Set up the SSB charter for a new Islamic microfinance bank in Sindh."

It also triggers on indirect symptoms — "the auditor flagged our late-payment income", "our Ijarah lease keeps failing the IMB transfer test", "regulator wants the Format-MFB plus AAOIFI reconciliation".

## How it works

The skill uses **progressive disclosure**:

1. **Metadata** (always in context) — the YAML frontmatter routes Claude to the skill.
2. **SKILL.md body** (loaded when triggered) — the high-level routing layer with persona switching, output protocols, and pointers to references.
3. **Reference files** (loaded on demand) — deep content is loaded only when needed for a specific question.

This keeps Claude's working context lean while giving it access to the full AAOIFI corpus when relevant.

## Standards data accuracy

All standard numbers, titles, and adoption status reflect the position as of **May 2026** following the AAOIFI Accounting Board's 45th meeting (January 2026) which approved FAS 53. Cross-check against the official catalogue at https://aaoifi.com/e-standards/ before issuing client deliverables. The skill embeds the reminder *"always verify the latest paragraph reference against the issued standard text"* throughout.

## Companion skills

This skill is designed to interoperate with:

- `mfb-financial-expert` — when AAOIFI work coexists with Client MFB (Client-MFB) reporting
- `core-banking-expert` — for core-banking core-banking SQL and report extraction underpinning AAOIFI reporting
- `legal-corporate-secretary` — for Pakistani board resolutions, SSB appointments, and SECP filings
- `cip-corporate-secp`, `cip-regulatory-strategy`, `cip-ip-academic`, `cip-master-plan` — for Credit Institute of Pakistan curriculum and accreditation
- `docx`, `xlsx`, `pptx`, `pdf` — for deliverable generation

## Contributing

Open issues or pull requests at the GitHub repository. Suggested contributions:

- Verification updates as AAOIFI issues new standards (FAS 53 finalisation, GSIFI 13/14, SS 60/61)
- Additional jurisdictional overlays (Nigeria, Türkiye, South Africa)
- Worked examples for less-common products (Ju'alah, Hawala, Concession contracts)
- Comparative analyses (e.g., FAS 42 vs. IFRS 17 detailed papers)

## Disclaimer

This skill produces drafting and analytical support. **It does not issue fatwas.** Any Shari'ah opinion produced via this skill is a draft to facilitate deliberation by the institution's appointed Shari'ah Supervisory Board. The skill author and Anthropic disclaim liability for accounting or Shari'ah determinations made in reliance on this skill's outputs without independent professional verification.

---

*Built using the Claude Skill Creator framework. Designed to model the cross-functional depth of a senior partner at a Big-4 Islamic Finance Centre of Excellence.*
