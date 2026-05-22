# AAOIFI Shari'ah Standards — Deep Dive Reference

The Shari'ah Standards (SS 1–59 issued, draft SS 60–61 under consultation) define what is **permissible (halal), prohibited (haram), and conditional (makruh / disliked)** in Islamic finance contracts. This file goes one level below `standards-catalogue.md` for the standards you will actually use in practice.

For each standard you'll find: scope, the headline rule, the practical structuring implications, the most-debated contemporary issues, and where the AAOIFI position differs from other major scholarly authorities (Malaysia's Shariah Advisory Council of BNM, IFA-OIC, individual senior scholars).

> Always quote the AAOIFI clause number when citing (e.g., **SS 8, clause 2/2/4**). Clauses are numbered hierarchically — section / subsection / sub-subsection.

## Table of contents

1. SS 5 — Guarantees (Kafala)
2. SS 8 — Murabaha
3. SS 9 — Ijarah and Ijarah Muntahia Bittamleek
4. SS 10 — Salam and Parallel Salam
5. SS 11 — Istisna'a and Parallel Istisna'a
6. SS 12 — Sharikah (Musharakah) and Modern Corporations
7. SS 13 — Mudaraba
8. SS 17 — Investment Sukuk
9. SS 23 — Agency (Wakala)
10. SS 26 — Islamic Insurance (Takaful)
11. SS 30 — Tawarruq (the most-debated)
12. SS 40 — Distribution of Profit in Mudaraba-Based Investment Accounts
13. SS 49 — Wa'd (Unilateral Promise) and Muwa'adah (Bilateral Promise)
14. SS 57 — Gold and its Trading Controls
15. SS 59 — Sale of Debt
16. The contemporary contested-structures map

---

## 1. SS 5 — Guarantees (Kafala)

**Headline rule.** Kafala (guarantee) is permissible if given gratuitously. **Charging a fee for a guarantee is prohibited** (SS 5, clause 2/1/2) — this is a foundational divergence from conventional finance.

**Practical implications.**
- IFIs cannot earn fee income on standalone guarantees. They can charge **service/administrative fees** that reflect actual processing cost, but not a risk-bearing fee.
- For **structured Wakala-based guarantee products**, the guarantee is incidental to the agency arrangement, and the agency fee is permitted.
- Sukuk credit enhancement via a **third-party guarantee** is permissible only if the guarantor is unrelated and provides the guarantee gratuitously (SS 17 cross-reference).

**Common deviation.** "Standby letters of credit" priced like conventional ones — flagged consistently by SSBs.

---

## 2. SS 8 — Murabaha

The most-used Shari'ah Standard in modern Islamic banking. Murabaha is a **cost-plus sale** — the seller discloses the cost and agreed markup to the buyer.

### Structural requirements

1. **IFI must own and possess the asset** before selling to the customer (SS 8, clause 2/2/4). Constructive possession (e.g., warehouse receipt in the IFI's name) is sufficient, but the IFI must bear the **ownership risk** for some time.
2. **The promise (Wa'd) from the customer to buy is unilateral and not a sale contract** (SS 8, clause 2/2/2). It binds the customer but is not the transfer of ownership.
3. **The Murabaha sale contract is separate** from the Wa'd, executed after possession.
4. **Cost and markup must be disclosed** to the customer.
5. **No penalty for late payment can be retained by the IFI** — any such amounts go to charity (SS 3 cross-reference).

### Contemporary debates

- **Murabaha to the Purchase Orderer (MPO)** — i.e., where the customer specifies the asset and "orders" it from the IFI — is permitted by AAOIFI provided steps 1–3 above are respected. Some scholars (notably Justice Mufti Taqi Usmani) caution against **"synthetic Murabaha"** where IFI ownership is a fiction.
- **Commodity Murabaha (London-Metals-Exchange-based)** — used widely for treasury and interbank liquidity, is permitted with strict conditions (SS 30 cross-reference for the Tawarruq variant).
- **"Murabaha by sub-Wakala"** — where the IFI appoints the customer as its agent to buy the asset on the IFI's behalf — is a permitted shortcut but **must not collapse the ownership step** (SS 8, clause 3/1/3).

---

## 3. SS 9 — Ijarah and Ijarah Muntahia Bittamleek

The Shari'ah lease standard. Two products live here: **operating Ijarah** and **Ijarah Muntahia Bittamleek (IMB)** — lease ending in ownership.

### Structural requirements

1. **The leased asset must be identifiable, usable, and have a permitted use** (SS 9, clause 3/1).
2. **The lessor (IFI) bears ownership risks** — major maintenance, insurance, and casualty risk — for the duration of the lease (SS 9, clause 5/1/7). The lessee bears only operational maintenance.
3. **Variable rent linked to a benchmark** (e.g., KIBOR/LIBOR + spread) is permitted with caveats — there must be a cap, and the variability must reflect a documented economic basis (SS 9, clause 5/2/3).
4. **IMB transfer mechanism** must be **separate** from the lease — by sale at nominal price, sale at market value, or gift (Hibah). An "automatic transfer at end of term" is not permitted (SS 9, clause 8/2).

### Common audit findings

- Insurance (Takaful) on the leased asset paid by lessee with no rebate to lessor → ownership-risk shift; structuring fix.
- Ijarah rentals capitalised into asset cost on lessee's books → presentation error and possibly Shari'ah issue.
- IMB with bundled transfer-cum-lease document → Shari'ah finding, easily remedied with separate documentation.

---

## 4. SS 10 — Salam and Parallel Salam

**Salam** is a forward sale: the buyer pays today, the seller delivers a fungible commodity later. The classical use case is agricultural (the farmer is paid in advance, delivers crop later).

### Structural requirements

- **Full price payment at contract inception** (SS 10, clause 3/1/1).
- **Goods specified by genus, quality, quantity, and delivery date** (SS 10, clause 3/2).
- **Delivery must be at a future date**, not on the spot.

### Parallel Salam

The IFI, having bought goods via Salam, sells the same quantity and quality forward via a **second, independent Salam contract** (SS 10, clause 5). The two contracts must not be conditional on each other.

### Use cases today

- **Agricultural microfinance** — direct fit; Client-MFB-relevant.
- **Commodity-backed treasury structures** — Salam Sukuk (SS 17 cross-reference).
- **Sovereign Sukuk** — Bahrain Salam Sukuk historically.

---

## 5. SS 11 — Istisna'a and Parallel Istisna'a

**Istisna'a** is a manufacturing contract: the buyer commissions a manufacturer to produce a specified asset. Payment may be deferred. The seller's *parallel Istisna'a* (where it sub-contracts production) is permitted.

### Structural requirements

- **Specifications of the manufactured good** must be sufficient to remove material ignorance (SS 11, clause 3/1/2).
- **Both immediate and deferred payment** are permitted.
- **Pre-payment (full or partial) is permitted** — unlike Salam which requires full pre-payment.
- **Penalty clauses for late delivery** are permitted if they accrue to the *buyer* (SS 11, clause 6/4).

### Practical uses

- Project finance — construction, manufacturing.
- Sukuk al-Istisna'a — common in infrastructure projects.
- **FAS 53 (new)** — Istisna-Based Development Contracts — extends application to real estate / infrastructure development. See `fas-deep-dive.md` section 13.

---

## 6. SS 12 — Sharikah (Musharakah) and Modern Corporations

The partnership standard. Covers both **Sharikah al-Aqd (contractual partnership)** and **Sharikah al-Milk (joint ownership)**.

### Key rules

- Capital contributions can be cash or in-kind (in-kind valued at fair value).
- Profit-sharing ratios are agreed in advance — they need not match capital ratios.
- **Loss-sharing must be pro-rata to capital** (SS 12, clause 3/1/4/3) — this is non-negotiable Shari'ah, no different from a fundamental Mudaraba rule.
- Modern joint-stock corporations are permitted as a form of Sharikah, with extensions for limited liability and tradable shares (SS 12, section 4).

### Diminishing Musharakah (cross-reference FAS 43)

A modern variant where the IFI's share is progressively bought out by the customer. Three contracts together (joint ownership + lease + unit purchase). Each must be separate.

---

## 7. SS 13 — Mudaraba

The trust-investment partnership. **Rabb-al-Mal** (capital provider) bears all financial loss; **Mudarib** (manager) bears only the loss of effort, unless negligence or breach of trust is proven.

### Key rules

- Capital is provided in cash or fungible assets (SS 13, clause 3/3).
- Profit-sharing ratio is fixed at inception; absolute amounts cannot be guaranteed.
- **A guarantee of capital or profit by the Mudarib is void** (SS 13, clause 8/1) — fundamental.
- Two-tier Mudaraba (IAH→IFI→assets) is the operating model for Islamic banks.

### Practical implications for IFIs

- IAH funds cannot be guaranteed by the IFI directly.
- PER and IRR (FAS 35) exist precisely to smooth IAH returns without breaching this rule.
- Profit-distribution methodology must be disclosed (SS 40, FAS 5).

---

## 8. SS 17 — Investment Sukuk

The foundational Sukuk standard. Defines **14 types of Sukuk** by underlying structure:

| Type | Underlying |
|---|---|
| Ijarah Sukuk | Lease of identifiable asset |
| Mudaraba Sukuk | Mudaraba partnership |
| Musharakah Sukuk | Musharakah partnership |
| Wakala Sukuk | Wakala (agency) arrangement |
| Salam Sukuk | Salam (forward purchase) |
| Istisna'a Sukuk | Istisna'a (manufacturing) |
| Murabaha Sukuk | Murabaha (cost-plus sale) — restricted secondary tradability |
| Hybrid Sukuk | Mix — typically Ijarah-Murabaha-Wakala |
| ... and more specific types |

### The 2008 declaration

In 2008, Justice Mufti Taqi Usmani (then Chair of the AAOIFI Shari'ah Board) issued the famous declaration that **85% of Sukuk in the market did not comply with Shari'ah principles** — driving major structural reforms. The current SS 17 incorporates those reforms.

### Key contemporary rules

- **Mudaraba and Musharakah Sukuk** — the issuer's purchase undertaking to buy back at face value is **prohibited** (it converts the Sukuk into a guaranteed-capital instrument). Purchase at fair market value or net asset value is acceptable (SS 17, clause 5/1/8/2).
- **Murabaha Sukuk** are **not tradable at premium/discount on the secondary market** because they represent debt (SS 59 — Sale of Debt). They can only be transferred at face value.
- **Asset-backed vs. asset-based** — AAOIFI prefers asset-backed (true sale) over asset-based (formal sale, beneficial ownership stays with originator). The market has historically preferred asset-based for legal-enforceability reasons.

### Sukuk governance (cross-reference GSIFI 12)

Issuer, trustee/SPV, and Sukuk-holder governance is now codified in GSIFI 12 — see `audit-governance-ethics.md`.

---

## 9. SS 23 — Agency (Wakala)

The agency standard. The agent (Wakil) acts on behalf of the principal (Muwakkil).

### Key rules

- **A fixed fee or percentage of capital is permitted** for the agent (SS 23, clause 4/1).
- **A performance fee tied to outperformance of a hurdle** is permitted with conditions (SS 23, clause 4/3) — typically structured as **fee + sharing in incentive above hurdle**.
- The Wakala does not bear capital risk; it is a fiduciary arrangement.

### Variants

- **Wakala bil Istithmar** — investment agency. The IFI invests on behalf of clients for a fee. Cross-reference SS 46 (Investment Agency) and FAS 31.
- **Wakala-Mudaraba hybrid** — common in modern interbank treasury, where the agent earns a fee plus shares in excess profit.

---

## 10. SS 26 — Islamic Insurance (Takaful)

The Takaful standard. Takaful operates on **mutual assistance (Ta'awun)** principles — participants contribute to a pool to cover specified risks.

### Operating models

- **Pure Wakala** — operator earns an agency fee on contributions; participants own the surplus.
- **Pure Mudaraba** — operator earns a share of investment profits but charges no agency fee.
- **Hybrid Wakala-Mudaraba** — operator earns agency fee on contributions + Mudaraba share of investment returns. Dominant in GCC.
- **Waqf-based** — common in South Asia; participants donate to a Waqf which then operates the Takaful pool. Pakistani regulators (SECP) have been progressive on Waqf model recognition.

Cross-reference FAS 42 for accounting.

---

## 11. SS 30 — Tawarruq (the most-debated)

Tawarruq is the **multi-leg commodity-trade structure** that delivers cash to the customer:

1. IFI buys commodity from Broker A for cash.
2. IFI sells commodity to customer at cost-plus-markup, deferred payment.
3. Customer (via agent or directly) sells commodity to Broker B for cash spot.
4. Customer ends up with cash today, owes the IFI the deferred Murabaha price.

### Two camps

- **Classical Tawarruq (rare today)** — the customer actually takes the commodity and sells it independently. **Permitted with conditions** by AAOIFI (SS 30, section 4).
- **Organised Tawarruq (the modern dominant variant)** — pre-arranged commodity brokers, customer never sees the commodity, settlement is purely cash. **Prohibited by AAOIFI** (SS 30, clause 4/5) — but **permitted by the Shariah Advisory Council of BNM (Malaysia)** under conditions.

### Practical reality

- **Malaysia and Indonesia** — organised Tawarruq is widely used (Bursa Suq Al-Sila' is the main Malaysian platform).
- **GCC** — increasingly restricted, especially Saudi Arabia, Bahrain.
- **Pakistan** — SBP has historically been cautious; product approval required from the bank's SSB. The Federal Shariat Court 2022 judgment further constrained.

### Structuring advice when challenged

If a client wants Tawarruq for treasury liquidity or syndicated finance and the SSB hesitates, **alternatives to consider**:
- **Wakala-based interbank** (SS 23, SS 46) — preferred for short-tenor liquidity.
- **Mudaraba Sukuk with proper market-value redemption** (SS 17).
- **Murabaha syndication on real assets** rather than commodities.

---

## 12. SS 40 — Distribution of Profit in Mudaraba-Based Investment Accounts

The standard governing **how IFIs split profit between IAH and shareholders**.

### Key rules

- A pre-agreed **profit-sharing ratio** (PSR) between IAH and Mudarib (IFI) is fixed at the start of each period (SS 40, clause 4/2).
- The PSR can vary between **different IAH tiers** (e.g., high-balance vs. low-balance) — permitted (SS 40, clause 4/4).
- **Hibah (gift) by the IFI to IAH** to boost the return above the contractual entitlement is permitted but must not be a guaranteed feature (SS 40, clause 5).
- **PER (Profit Equalisation Reserve)** is permitted to smooth returns (SS 40, clause 4/9) — cross-reference FAS 35.

### Common audit observations

- IAH disclosure does not show **basis of profit allocation** (FAS 5 + SS 40 jointly require this).
- Hibah practiced as a guaranteed top-up to the IFI's PLS return → effectively a guaranteed return → Shari'ah issue.

---

## 13. SS 49 — Wa'd (Unilateral Promise) and Muwa'adah (Bilateral Promise)

The standard governing **promises** — increasingly important for modern structures (FX hedging, Sukuk redemption, Diminishing Musharakah).

### Key rules

- **Unilateral promise (Wa'd) is binding** under Maliki and modern majority view, including AAOIFI (SS 49, clause 3/2).
- **Bilateral binding promises (Muwa'adah)** — where both parties are bound — is **not permitted** because it amounts to a forward contract (SS 49, clause 5).
- The exception: Muwa'adah on currency exchange for **hedging an existing exposure** (not speculation) is permitted with caveats (SS 1 + SS 49 cross-reference).

### Practical implication

- **Islamic FX forwards** (the Wa'd-based structure) — permitted unilaterally per AAOIFI; the Malaysian Shariah Advisory Council permits Muwa'adah more broadly. This is one of the clearest AAOIFI-vs-Malaysian divergences.
- **Sukuk redemption undertakings** — must be unilateral, not bilateral.

---

## 14. SS 57 — Gold and its Trading Controls

The foundational gold-finance standard, jointly developed with the **World Gold Council**.

### Key rules

- Gold-for-gold trade requires **spot delivery and like-for-like exchange** (SS 57, clause 2/1) — classic riba al-fadl rule.
- Gold-for-cash (or gold-for-non-gold currency) requires **spot exchange** (SS 57, clause 3) — riba al-nasi'ah rule.
- **Allocated** physical gold can be the underlying for Shari'ah-compliant ETFs and gold-backed Sukuk; **unallocated** gold is more contentious.
- **Gold forward and futures contracts** in the conventional sense are not permitted because they involve deferred delivery of both legs.

### Practical implication

- **Shari'ah-compliant gold ETFs** must hold allocated physical gold (e.g., Wahed Gold, HSBC Islamic Gold).
- **Gold-backed financing** (Client-MFB's gold loan portfolio, for example) operates under a different structure — typically Rahn (pledge) of gold against a Murabaha financing, not a sale of gold itself.

---

## 15. SS 59 — Sale of Debt

**The most consequential standard for Sukuk tradability.** The classical position: **debt cannot be sold at premium or discount**; it can only be transferred at face value (par).

### Practical impact on Sukuk

- **Murabaha Sukuk** — these represent debt from the originator → **not tradable** below or above par. They must be held to maturity or transferred at face value.
- **Ijarah Sukuk** — represent ownership of a leased asset → **tradable** at market price.
- **Mudaraba and Musharakah Sukuk** — represent equity-in-a-partnership → **tradable**, provided the partnership has converted contributions into real assets/projects (not still in cash form).
- **Hybrid Sukuk** — tradability depends on the **percentage of debt vs. asset components**. AAOIFI's rule of thumb (SS 17 + SS 59): Sukuk can be traded if the **tangible-asset portion is at least 51%** (some scholars say 33%, the Malaysian Shariah Advisory Council is more permissive).

### Practical implication

The **51% asset rule** is the single most cited rule in Sukuk structuring. Every Sukuk prospectus must address it. Some innovative structures (Wakala-Murabaha hybrid) tune the proportion at issuance and maintain the ratio through the life of the Sukuk via Wakala-driven asset management.

---

## 16. The contemporary contested-structures map

| Structure | AAOIFI position | Malaysian SAC | Practical |
|---|---|---|---|
| Organised Tawarruq | Prohibited | Permitted with conditions | Used widely in Malaysia; restricted in GCC |
| Bay' al-Inah | Prohibited | Permitted with conditions | Used in Malaysia historically; phased out in many products |
| Bilateral Wa'd / Muwa'adah | Prohibited | Permitted for hedging | Different IFRS / risk-management positions |
| Sukuk purchase undertaking at face value (Mudaraba/Musharakah) | Prohibited | Tolerated historically | Market increasingly moved to NAV / fair-value undertakings |
| Synthetic FX swaps | Generally rejected | Permitted under specific structures | Treasury / corporate hedging issue |
| Sale of debt at non-par | Prohibited | More permissive | Sukuk-tradability driver |

When advising in a multi-jurisdictional context, **always name which Shari'ah authority's view you are reflecting**. Do not collapse them into "Shari'ah says…".

---

> **Closing note.** Memorise the headline rule for SS 8, 9, 17, 30, 49, 57, 59 — those eight standards underpin 80% of contemporary Islamic finance structuring. The deep dives in this file are intended to support drafting, but the **actual fatwa must come from the institution's appointed Shari'ah scholars**.
