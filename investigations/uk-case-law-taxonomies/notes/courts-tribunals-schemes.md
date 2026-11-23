# Court- and tribunal-specific decision classification schemes (UK)

Research topic 1 for: existing/past subject classification schemes for UK case law, in support of a subject taxonomy for Find Case Law (The National Archives).

## Summary

- Several HMCTS/tribunal-run decision websites built their **own bespoke subject classifications** for decision search: top examples are the Upper Tribunal (Lands Chamber) site (17 categories / ~140 subcategories), the Employment Appeal Tribunal site (a flat ~43-topic list, including now-obsolete topics), and the Land Registration Division of the First-tier Tribunal (Property Chamber) (27 categories, each with postback-populated subcategories — 208 subcategory entries; **two-level**, not flat as first thought). Full nested transcriptions: [lands-chamber-taxonomy.md](../taxonomy-extractions/lands-chamber-taxonomy.md), [eat-taxonomy.md](../taxonomy-extractions/eat-taxonomy.md), [land-registration-division-taxonomy.md](../taxonomy-extractions/land-registration-division-taxonomy.md).
- Two patterns recur: a **two-level Category → Subcategory dropdown hierarchy** built into an ASP.NET search form, and flat **"Topic" dropdowns**. In every case the taxonomy is *jurisdictional/procedural in character* (statute- and claim-types plus "Procedure" and "Costs"), not a lay-friendly subject thesaurus.
- The publisher of each scheme is the tribunal itself (HMCTS web team); the audience was primarily professionals (surveyors, tax practitioners, employment lawyers) plus litigants-in-person. Classification was applied **at publication time by tribunal staff** as a context-dependent field, plus a strong parallel convention of **ALL-CAPS headnotes** in the decision title (`(RATING - VALUATION - ...)`), which continues today and is effectively a free-text sub-classification on most UKUT (LC) decisions.
- Status: the `*.decisions.tribunals.gov.uk` sites are largely **frozen ("live but closed")** — no new decisions since 2017 (EAT), May 2022 (Tax), or 4 Aug 2025 (Lands Chamber), with successors pointing to GOV.UK / [Find Case Law](https://caselaw.nationalarchives.gov.uk/). None of the newer successors (GOV.UK specialist documents, judiciary.uk) carries a subject taxonomy; GOV.UK keeps only a per-document **"Jurisdiction code"** on employment tribunal decisions.
- These dormant sites are nonetheless **the best ready-made UK public-law subject vocabularies available** for those jurisdictions: they are curated, persisted in the UK Government Web Archive, and verified live at the Lands Chamber and EAT sites.

---

## 1. Upper Tribunal (Lands Chamber) / The Lands Tribunal decisions site ⭐ (deep dive)

**Site:** https://landschamber.decisions.tribunals.gov.uk/Aspx/Default.aspx (title in page source: "The Lands Tribunal"). **Status: still live and serving data as of Oct 2026**, with a banner: *"No new decisions are being uploaded to this website from the 4th August 2025 but they can be found on The National Archives at Find Case Law - Lands Chamber"*. Decisions cover the Lands Tribunal from Nov 1999 and the Upper Tribunal (Lands Chamber) thereafter; 2,125 decisions at last crawl. The bare root URL now serves a legacy redirect page mentioning the Tribunals Service/HMCTS 2011 merger — the `/Aspx/Default.aspx` path still serves the application. The domain was also captured 13 times across 2019–2025 in the [UK Government Web Archive](https://webarchive.nationalarchives.gov.uk/ukgwa/20200101000000*/landschamber.decisions.tribunals.gov.uk) (Wayback Machine holds the same site).

**Structure:** search form with a **mandatory two-level dropdown**: `Category` → `Subcategory` (populated by `PopulateSubcategory.js`), plus filters for date, file no. (LC-YYYY-NNN), party, judge, and neutral citation. Results table columns: Date, File No., **Category, Subcategory**. The category IDs are non-contiguous (1–10, then jumps to 16, 19, 25–29), showing that **new categories were appended as new jurisdictions arrived** (Housing came into the chamber via FTT (Property Chamber) in 2013; Land Registration, ECC, Electricity Charges and Building Safety follow the same pattern).

### Exact captured taxonomy

17 categories; subcategories numbered `C.n`:

| # | Category | Subcategories |
|---|---|---|
| 1 | COMPENSATION | 1.1 Compulsory Purchase; 1.2 Land Compensation Act 1973 Part I; 1.3 Mining subsidence; 1.4 Electricity; 1.5 Water; 1.6 Purchase notice; 1.7 Tree preservation order; 1.8 Home loss payment; 1.9 Severance; 1.10 Injurious affection; 1.11 Disturbance; 1.12 Valuation method; 1.13 Scheme; 1.14 Hope value; 1.15 Ransom value; 1.16 Comparables; 1.17 Planning permission; 1.18 Blight; 1.19 Extinghishment *(sic)*; 1.20 Dwelling house; 1.21 Unfit house; 1.22 Right of way; 1.23 Agricultural land; 1.24 Minerals; 1.25 Petrol filling station; 1.26 Shop; 1.27 Road noise; 1.28 Limitation; 1.29 Interest; 1.30 Procedure; 1.31 Costs; 1.32 Stop notice; 1.33 Demolition Order; 1.34 Preliminary issue; 1.35 Prohibition Order |
| 2 | RATING | 2.1 Valuation; 2.2 Exemption; 2.3 Alteration of rating list; 2.4 Comparables; 2.5 Hereditament; 2.6 Occupation; 2.7 Shop; 2.8 Public house; 2.9 Club; 2.10 Holiday cottage; 2.11 Procedure; 2.12 Costs; 2.13 Proposal; 2.14 College premises; 2.15 Drainage rates; 2.16 Rateable property; 2.17 Plant and Machinery |
| 3 | RESTRICTIVE COVENANTS | 3.1 Discharge; 3.2 Modification; 3.3 Obsoleteness; 3.4 Practical benefits of substantial value or advantage; 3.5 Public interest; 3.6 Consent; 3.7 Injury to objector; 3.8 Consideration; 3.9 Compensation; 3.10 House; 3.11 Flat; 3.12 Alterations to house; 3.13 Agricultural building; 3.14 Home for elderly; 3.15 Procedure; 3.16 Costs; 3.17 Jurisdiction; 3.18 Entiltlement to benefit *(sic)*; 3.19 Preliminary issue |
| 4 | LEASEHOLD ENFRANCHISEMENT | 4.1 Collective enfranchisement; 4.2 House; 4.3 Flat; 4.4 Price; 4.5 Premium; 4.6 Comparables; 4.7 Standing house value; 4.8 Site value; 4.9 Intermediate leasehold interest; 4.10 Development potential; 4.11 Ground rent; 4.12 Yield rates; 4.13 Capitalisation rate; 4.14 Deferment rate; 4.15 Marriage value; 4.16 Hope value; 4.17 Terms of transfer; 4.18 Restrictive covenant; 4.19 Garage; 4.20 Procedure; 4.21 Costs; 4.22 Right to manage; 4.23 Special purchaser; 4.24 Estate charges |
| 5 | LANDLORD AND TENANT | 5.1 Service Charges; 5.2 Insurance; 5.3 Appointment of manager; 5.4 Right to manage; 5.5 Administrative Charge; 5.6 Purchase notice; 5.7 Breach of covenant; 5.8 Acquisition by tenant of new lease; 5.9 Variation of lease; 5.10 FTT procedure; 5.11 Rent Determination; 5.12 Agricultural Holdings Act 1986 |
| 6 | BLIGHT NOTICE | 6.1 Blight notice; 6.2 Preliminary Issue |
| 7 | TAX | 7.1 Inheritance tax; 7.2 Capital gains tax; 7.3 Comparables; 7.4 House; 7.5 Hotel; 7.6 Procedure; 7.7 Costs |
| 8 | EASEMENT | 8.1 Countryside and Right of Way Act 2000 |
| 9 | ARBITRATION | 9.1 Access rights |
| 10 | COSTS | 10.1 Preliminary issues; 10.2 Preliminary issues; 10.3 Right to Manage |
| 16 | HOUSING | 16.1 Emergency remedial action; 16.2 Prohibition Notice; 16.3 Enforcement action; 16.4 House in multiple occupation; 16.5 Selective Licencing (16.6 missing); 16.7 Civil Penalty; 16.8 Rent Repayment Order; 16.9 Banning Order; 16.10 Other; 16.11 Right-to-Buy |
| 19 | PARK HOMES | 19.1 Administration Charges; 19.2 Pitch Fee Review; 19.3 Sale, assignment and succession; 19.4 Site Rules; 19.5 Procedure; 19.6 Water Charges; 19.7 Site Licencing; 19.8 Jurisdiction; 19.9 Electricity Charges |
| 25 | LAND REGISTRATION | 25.1 Unilateral notice; 25.2 Adverse possession; 25.3 Alteration and rectification; 25.4 Beneficial interests, trusts and restrictions; 25.5 Boundary disputes; 25.6 Charges and charging orders; 25.7 Contracts and options; 25.8 Costs; 25.9 Easement and profits; 25.10 Fraud, forgery, duress and undue influence; 25.11 Practice and Procedure; 25.12 Rectification or setting aside of documents; 25.13 Title to land |
| 26 | ELECTRONIC COMMUNICATIONS CODE | 26.1 Jurisdiction; 26.2 Interim Code Rights; 26.3 Code rights; 26.4 Temporary Code rights; 26.5 Consideration; 26.6 Compensation; 26.7 Other; 26.8 New agreement or modification |
| 27 | INTERIM RIGHTS | (no subcategories) |
| 28 | ELECTRICITY CHARGES | (no subcategories) |
| 29 | BUILDING SAFETY | 29.1 REMEDIATION CONTRIBUTION ORDER; 29.2 Accountable Person; 29.3 LEASEHOLDER PROTECTION |

**Observations:**
- Subject facets implied by subcategory reuse across categories: *Comparables*, *Hope value*, *Procedure*, *Costs*, *House/Flat/Shop*, *Jurisdiction*, *Preliminary issue* — i.e. the scheme mixes **true subject facets** (topic/valuation method) with **procedural status facets** (a faceted-typo tendency a Find Case Law taxonomy should separate).
- Typos and inconsistencies ("Extinghishment", "Entiltlement to benefit", duplicated "Preliminary issues", "Choose a Category first") suggest uncontrolled, hand-maintained vocabulary — a caution for naive reuse.
- Parallel headnote convention: every decision title carries an ALL-CAPS category headnote, e.g. *"Banfield v Swale Borough Council (HOUSING - CIVIL PENALTY - failure to comply with an improvement notice - reasonable excuse - mitigation)"* — visible on [BAILII mirrors](https://knyvet.bailii.org/uk/cases/UKUT/LC/toc-B.html) and continuing on decisions handed down after the Aug 2025 migration to Find Case Law. So **two vocabularies coexist**: the structured DB fields (coarse) and the headnote (fine-grained issue description).

**Sources:** live [search page](https://landschamber.decisions.tribunals.gov.uk/Aspx/Default.aspx); [UKGWA timeline](https://webarchive.nationalarchives.gov.uk/ukgwa/20200101000000*/landschamber.decisions.tribunals.gov.uk); [judiciary.uk Lands Chamber decisions page](https://www.judiciary.uk/courts-and-tribunals/tribunals/upper-tribunal/upper-tribunal-lands-chamber/upper-tribunal-lands-chamber-decisions/) ("decisions dating between November 1999 and 4 August 2025 (external link)… after 4 August 2025 (external link)" → Find Case Law); [Find Case Law UKUT (LC) page](https://caselaw.nationalarchives.gov.uk/courts-and-tribunals/ukut/lc) (1,990 documents, 2014–); [GOV.UK Upper Tribunal (Lands Chamber)](https://www.gov.uk/courts-tribunals/upper-tribunal-lands-chamber) "What we do" jurisdiction list mirrors the same subject areas (rates, compulsory purchase compensation, restrictive covenants, tree preservation orders, right to light, blight, Electronic Communication Code, etc.); [Lands Chamber Records Retention Schedule PDF](https://assets.publishing.service.gov.uk/media/632ad7a2d3bf7f75cb0f309d/upper-tribunal-lands-chamber-rrds.pdf) notes decisions 1950–1972 at TNA (LT 13) and site URL as current reference.

**Usefulness for Find Case Law taxonomy:** very high for property/land law. It is the most granular public subject vocabulary for any UK tribunal (~150 terms), professionally phrased (RICS/valuation terminology), and covers 26 years of decisions. Weaknesses: lay users won't know "hereditament" or "deferment rate"; mixed procedural/subject facets; typos; incomplete for pre-1999 Lands Tribunal history (held at TNA under LT series, classified by record type, not subject). Best used as a seed vocabulary for property/land taxonomies with plain-English synonyms added.

---

## 2. Employment Appeal Tribunal — "Topic" classification

**Site:** https://employmentappeals.decisions.tribunals.gov.uk/Public/Search.aspx (successor to the archived http://www.employmentappeals.gov.uk/ and the older employmentappeals.tribunals.gov.uk domain, which now serves the HMCTS 2011 redirect page; site versions archived from 2004 in TNA record [TR 13](https://discovery.nationalarchives.gov.uk/details/r/C17563)). **Status: live but frozen** — banner: *"Employment Appeal Tribunal judgments published after March 2017 can be found on www.gov.uk/employment-appeal-tribunal-decisions"*.

**Structure:** flat single-level `Topic` dropdown alongside EAT number, judge, parties, "Starred" (starred/benchmark judgments), and hearing-date search. Exact captured topic list (asterisk-marked topics labelled "(obsolete topic)" in the UI):

Age Discrimination; Agency Workers; Blacklisting Regulations; Central Arbitration Committee (CAC); Certification Officer; Contract of Employment; Disability Discrimination; Employment Agencies Act 1973; Employment Agencies Act 1973 *(obsolete)*; Equal Pay Act; European Material *(obsolete)*; Fixed Term Regulations; Flexible Working; Harassment; Health & Safety; Human Rights; Jurisdiction *(obsolete)*; Jurisdictional Points; Maternity Rights and Parental Leave; National Minimum Wage; National Security; Part Time Workers; Practice and Procedure; Procedural Issues *(obsolete)*; Public Interest Disclosure *(obsolete)*; Race Discrimination; Redundancy; Religion or Belief Discrimination; Reserved Forces Act *(obsolete)*; Right To Be Accompanied; Rights on Insolvency; Sex Discrimination; Sexual Orientation Discrimination/Transexualism; Statutory Discipline and Grievance Procedures; Time Limits *(obsolete)*; Time Off; Trade Union Membership; Trade Union Rights; Transfer of Undertakings; Unfair Dismissal; Unlawful Deduction from Wages; Victimisation Discrimination; Working Time Regulations.

**Observations:**
- Topic = claim type under employment statutes; organisationally flat but realistically a two-level structure (statute → claim). "Obsolete topics" were retired rather than merged — evidence of ad hoc curation over ~20 years.
- Successor publication on [GOV.UK employment-appeal-tribunal-decisions](https://www.gov.uk/employment-appeal-tribunal-decisions) has **no topic field** — the classification was lost in migration.

**Sources:** live [EAT search page](https://employmentappeals.decisions.tribunals.gov.uk/public/search.aspx); [TNA record TR 13](https://discovery.nationalarchives.gov.uk/details/r/C17563); [WhatDoTheyKnow FOI on EAT publication locations](https://www.whatdotheyknow.com/request/where_are_the_costs_orders_and_j).

**Usefulness:** high for employment law; even the obsolete-topic trail of cases is useful for browsing historical coverage. Most terms are plain-English and worker-facing ("Unfair Dismissal", "Flexible Working"), making it the friendliest lay vocabulary found. Depth: one level only; no case-issue granularity beyond topic.

---

## 3. First-tier Tribunal (Property Chamber) — Land Registration Division decisions

**Site:** https://landregistrationdivision.decisions.tribunals.gov.uk/Public/search.aspx. **Status: live** (part of the FTT Property Chamber publishing suite; decisions "searchable by the name of the Judge or by category" from 1 June 2015).

**Structure:** ~~single-level `Category` dropdown (27 categories), with sub-category dependent dropdown~~ **two-level `Category` → `Sub Category` dropdowns (27 categories).** Correction (29 Oct 2026): the dependent Sub Category dropdown (`ddlScat1`) was missed in the first capture because it is populated by an ASP.NET server postback rather than a bundled JS file; a postback simulation harvested all 27 subcategory lists — **208 subcategory entries**. The full two-level transcription is at [land-registration-division-taxonomy.md](../taxonomy-extractions/land-registration-division-taxonomy.md).

Selection policy documented on-page: pre-2015 only decisions "of general interest / deciding points of law / otherwise of general importance" were published.

Highlights of the second level: deep issue-explicit subcategories under Adverse possession (factual possession, intention to possess, successive squatters, Schedule 6 LRA 2002…), Alteration and rectification, Boundary dispute (general boundaries rule, ad medium filum…), Charges, Easements, Costs, Evidence, Practice and Procedure and Estoppel; several small categories have only "No sub category" / catch-all entries. Earlier translation of the top-level list:

Exact captured categories: 1. Adverse possession; 2. Alteration and rectification of the register; 3. Beneficial interests, trusts and restrictions; 4. Boundary dispute; 5. Charges and charging orders; 6. Contracts and options; 7. Costs; 8. Easements and profits a prendre; 9. Evidence; 10. Fraud, forgery, duress and undue influence; 11. Leases and licenses; 12. Network Access Agreements; 13. Practice and Procedure; 14. Rectification or Setting Aside of Documents; 15. Manorial Rights; 16. Other; 17. Home Rights; 18. Rentcharges; 19. Compulsory Purchase; 20. Estoppel; 21. Rivers, Waterways and Foreshore; 22. Deeds; 23. Highways and public rights of way; 24. Restrictive covenants; 25. Practice Directions; 26. Miscellaneous cases; 27. Cautions against dealings.

**Sources:** live [search page](https://landregistrationdivision.decisions.tribunals.gov.uk/Public/search.aspx); [judiciary.uk Tribunal Decisions hub](https://www.judiciary.uk/judgments/tribunal-decisions/) ("Land Registration Division decisions (external link)").

**Usefulness:** moderate-high; overlaps heavily with Lands Chamber's LAND REGISTRATION category (25.1–25.13 above, visibly the same vocabulary's ancestor/sibling). Small corpus but fine-grained, fairly plain-English.

---

## 4. Upper Tribunal (Administrative Appeals Chamber) — Commissioners' decision database

**Site:** https://adminappeals.reports.tribunals.gov.uk/ → database at http://www.osscsc.gov.uk/Aspx/default.aspx. **Status: legacy pages live; database** holds Social Security & Child Support Commissioners' decisions (pre-3 Nov 2008) and superior-court decisions on appeal from the AAC. Newer AAC decisions (from Jan 2016) publish via [tribunalsdecisions.service.gov.uk](https://tribunalsdecisions.service.gov.uk/).

**Classification approach (not a subject dropdown):**
- Reported decisions curated into **"Lists and indexes of reported decisions"**, with case numbers prefixed by benefit/jurisdiction series codes (e.g. `R(IS)`, `CIS/…`, `CHI/…`) — the **benefit type encoded in the citation prefix acts as a de facto subject taxonomy** ([adminappeals reports page](https://adminappeals.reports.tribunals.gov.uk/)).
- Ancillary classified lists: *Decisions highlighted in the last 12 months*; *Decisions of Three-Judge Panels*; *Decisions of superior courts since 2006*; *Decisions in housing benefit and council tax benefit cases since 2006*; *Decisions on appeal from the Traffic Commissioners since 2009*; plus [Administrative Appeals Chamber Reports](https://adminappeals.reports.tribunals.gov.uk/) (annual printed report series, TSO) — a traditional law-report-style subject filtering.
- Migration context: MoJ's Justice Digital built [tribunalsdecisions.service.gov.uk](https://tribunalsdecisions.service.gov.uk/) (2013+) for UTIAC first, then AAC/FTT Tax/EAT ([MoJ blog](https://mojdigital.blog.gov.uk/2013/09/17/tribunals-decisions-improving-the-search-experience/)); its filters are judge name, **country**, free text, and reported/unreported status — **no subject facet** to this day.

**Sources:** [adminappeals.reports.tribunals.gov.uk](https://adminappeals.reports.tribunals.gov.uk/); [tribunalsdecisions.service.gov.uk/utiac](https://tribunalsdecisions.service.gov.uk/utiac/); [MoJ Digital blog, 2013](https://mojdigital.blog.gov.uk/2013/09/17/tribunals-decisions-improving-the-search-experience/).

**Usefulness:** the numbering-prefix system (benefit series) is a ready-cut subject vocabulary for social entitlement law, already used implicitly by practitioners; but it is citation-embedded rather than browsable, and the modern successor dropped subject classification entirely.

---

## 5. Tax & Chancery / Tax Chamber decisions

**Status:** the older Tax Chamber decisions site (linked from [judiciary.uk "Tax and Chancery Chamber decisions (external link)"](https://www.judiciary.uk/judgments/tribunal-decisions/)) stopped taking uploads in May 2022; [GOV.UK tax-tribunal-decisions](https://www.gov.uk/tax-tribunal-decisions) now points to Find Case Law and states pre-May-2022 FTT (Tax) decisions remain on the old decisions website. Direct fetches of the `taxchancery.decisions.tribunals.gov.uk` / `taxchamber` domains were unreachable at crawl time; see the [Find Case Law Tax & Chancery page](https://caselaw.nationalarchives.gov.uk/courts-and-tribunals/ukut/tcc) for the successor coverage. **Subject classification: none observed** — tax cases are found by taxpayer name, judge, and date; the de facto subject split is "Tax" (direct tax) vs "Chancery" (UT (TCC) also hears charity, information rights and other chancery matters). Lowest-granularity of the tribunals surveyed. *(Update, 4 Nov 2026: a GOV.UK finder at [gov.uk/tax-and-chancery-tribunal-decisions](https://www.gov.uk/tax-and-chancery-tribunal-decisions) now carries a flat 6-category facet — Banking / Charity / Financial Services / Land Registration / Pensions / Tax; see [tax-and-chancery-tribunal-taxonomy.md](../taxonomy-extractions/tax-and-chancery-tribunal-taxonomy.md).)*

---

## 6. Judiciary.uk "Judgments & sentencing remarks" — the current publishing front-end

**Site:** https://www.judiciary.uk/judgments/. **Status: live, actively maintained.**

**Structure:** a filterable feed with three facets:
- **Keyword** (free text);
- **Judgment type**: Anonymity Order; Committal for Contempt of Court; Judgment; Order; Privacy Order; Sentencing Remarks; Transmission Direction Order; Transparency Order; Tribunal Decision (i.e. document-type, not subject);
- **"Subject"**: a long list that is in fact **court/tribunal/division-based with a handful of vague themes**: Administrative Court; Admiralty Court; Commercial Court; Court of Appeal (Civ/Crim); Court of Protection; Crown Court; Employment Appeal Tribunal; Employment Tribunal; Family; Financial List; High Court; Immigration and Asylum Chamber (FTT/UTT); Insolvency and Companies List; Intellectual Property List; Lands Chamber (Upper Tribunal); Magistrates' court; Media and Communications List; Patents Court; Planning Court; Property Chamber (FTT); Senior Presiding Judge; Social Entitlement Chamber; Special Immigration Appeals Commission; Tax and Chancery Chamber (UT); Tax Chamber (FTT); Technology and Construction Court; War Pensions and Armed Forces Compensation Chamber; plus cross-cutting tags *Civil, Criminal, Cross Jurisdictional, Educational, Financial, Diversity and Inclusion*, and several individual judges.
Per-decision "subject" tags are plain links to `/subjects/...` taxonomy pages, so each judgment carries a small set of court+type+subject facet tags.

**Observations:** judiciary.uk has **no legal-subject taxonomy** — the "Subject" facet is really an issuing-source facet plus a few editorial themes. This is the current-front-end reality that Find Case Law's future taxonomy would complement for tribunal decisions, which judiciary.uk links out to rather than tagging by subject ([Tribunal Decisions hub](https://www.judiciary.uk/judgments/tribunal-decisions/) simply links to the ten-odd external decision sites listed above).

**Sources:** [judgments search page](https://www.judiciary.uk/judgments/); [tribunal decisions hub](https://www.judiciary.uk/judgments/tribunal-decisions/); [Lands Chamber decisions page](https://www.judiciary.uk/courts-and-tribunals/tribunals/upper-tribunal/upper-tribunal-lands-chamber/upper-tribunal-lands-chamber-decisions/).

**Usefulness:** low as subject vocabulary; high as an **organisational naming authority** for court/tribunal facets (its `/subjects/` pages provide canonical slug-able labels).

---

## 7. GOV.UK tribunal guidance pages as de facto subject vocabularies

GOV.UK "courts-tribunals" pages each open with a "What we do" jurisdiction list that enumerates the *subject matters* a body hears — an implicit, lay-facing subject vocabulary:

- [Upper Tribunal (Lands Chamber)](https://www.gov.uk/courts-tribunals/upper-tribunal-lands-chamber): rates decisions; compensation for compulsory purchase; discharge/modification of restrictive covenants; compensation for effect of public works; tree preservation orders; mining subsidence compensation; CGT/IHT land valuation; right to light; blighted land; Electronic Communication Code (masts) disputes.
- [First-tier Tribunal (SEND)](https://www.gov.uk/courts-tribunals/first-tier-tribunal-special-educational-needs-and-disability): EHC needs-assessment refusals; EHC plan content/maintenance; disability discrimination; health & social care recommendations.
- [Employment tribunal decisions](https://www.gov.uk/employment-tribunal-decisions): each decision page carries a structured **"Jurisdiction code"** field (e.g. "Redundancy and Working Time Regulations", example [K Glover v Lloyds Rescue Ltd](https://www.gov.uk/employment-tribunal-decisions/k-glover-v-lloyds-rescue-ltd-1402961-slash-2022)) — the closest thing to a live maintained subject facet on GOV.UK; see also the [document-type spec](https://docs.publishing.service.gov.uk/document-types/employment_tribunal_decision.html) (134,956 decisions indexed).

**Usefulness:** moderate — the "What we do" lists are short (8–12 items per body) but lay-readable and officially maintained; ET "Jurisdiction code" is machine-readable at scale via the GOV.UK content API.

---

## 8. SENDIST / First-tier Tribunal (SEND) decision summaries

**Status: no public subject taxonomy.** The old SENDIST site published searchable full-text decision PDFs for 2000–2006 only ([IALS description of the closed site](https://resources.ials.sas.ac.uk/eagle-i/first-tier-tribunal-special-educational-needs-and-disability-send)); later, MoJ FOI releases categorise appeals by *type of need* (Autistic Spectrum Disorder; Behavioural, Social & Emotional; Hearing; Moderate/Severe/Profound Multiple Learning Disability; Physical Disability; Speech, Language & Communication; Specific Learning; Visual Impairment) — a useful lay need-type vocabulary, though statistical ([FOI/82891 release](https://docsbay.net/doc/581918/special-educational-needs-cases-coming-before-the-sendist-tribunal-2008-to-2012-involving)). Quarterly anonymised [National Trial decision summaries](https://www.sendpathfinder.co.uk/summary-of-national-trial-decisions/) (2018–19 SEND single route of redress) and [IPSEA's curated SEN case-law pages](https://www.ipsea.org.uk/sen-and-disability-case-law) fill the gap for practitioners. Individual UT (AAC) decisions carry a standard "Summary of Decision" block keyed to statutory sections, e.g. *"85. SPECIAL EDUCATIONAL NEEDS / 85.4 Special educational provision"* ([East Riding of Yorkshire Council v Bowers [2026] UKUT 31 (AAC)](https://bruneis.bailii.org/uk/cases/UKUT/AAC/2026/31.pdf)) — an unpublished-to-the-web but numbering-stable internal summary taxonomy worth capturing.

---

## 9. Court of Protection — published cases

**Status: no subject taxonomy; selection-based publishing.** The CoP's "classification" is effectively its [publication practice guidance (Munby, Jan 2014)](https://www.judiciary.uk/wp-content/uploads/JCO/Documents/Guidance/transparency-in-the-cop.pdf), whose **Schedule enumerates judgment categories actionable for publication**: serious medical treatment; deprivation of liberty; disputes over attorneys/deputies; residential moves; sale of P's home; property & affairs assets ≥£1m; capacity to marry or consent to sexual relations; publication restraint orders. These schedule items function as an applied tag-set for what gets published (see the [2023 Transparency Implementation Group report](https://www.judiciary.uk/wp-content/uploads/2023/02/Publication-Guidance-Subgroup-Report.pdf)); published judgments flow to BAILII, judiciary.uk, and Find Case Law ([CoP overview](https://www.judiciary.uk/courts-and-tribunals/court-of-protection/)). No browse-by-topic interface exists.

**Usefulness:** the schedule headings are a defensible lay-friendly seed taxonomy for mental-capacity case law (best-interests, capacity, deputies, deprivation of liberty, medical treatment, property & affairs).

---

## Cross-cutting observations & recommendations for Find Case Law

1. **Four HMCTS vocabularies in one family.** Lands Chamber (17 categories / ~140 subcategories), EAT (43 topics), Land Registration Division (27), and the Commissioners' benefit-series codes collectively cover property, employment, and social entitlement — the three biggest tribunal domains on Find Case Law — and several terms repeat across them (adverse possession, restrictive covenants, service charges, costs, procedure).
2. **Every scheme mixes three facet types** — subject-matter, procedural status (Procedure/Costs/Jurisdiction/Preliminary issue), and outcome/relief (Civil Penalty, Rent Repayment Order, Banning Order). A Find Case Law taxonomy should split these; the legacy schemes blur them because they served "find the case you need" search rather than principled classification.
3. **Headnote practice is the hidden treasury.** The ALL-CAPS headnotes (`(CATEGORY - SUBCATEGORY - issue description)`) on UKUT (LC), UKUT (TCC), UKUT (AAC) summaries etc. provide per-decision free-text issue classification at far finer grain than any dropdown, and are machine-parseable.
4. **Migration lost metadata.** Where an old site's decisions moved to GOV.UK or Find Case Law (EAT 2017, Tax 2022, Lands Chamber 2025), the topic/category fields did not travel — supporting the case for a first-class subject taxonomy in Find Case Law itself rather than relying on source-site metadata.
5. **Coverage gaps:** no scheme found for immigration (UTIAC search has no subject facet), or for giso/charity/GRC matters. The commissioner-series codes and the Lands Chamber scheme are the only substantial UK public-law subject vocabularies located that were purpose-built for case-law retrieval.

*Research date: 25 Oct 2026. Lands Chamber category table captured verbatim from the live `/Aspx/Default.aspx` form payload and its `PopulateSubcategory.js` data; EAT and Land Registration topic lists captured verbatim from live search pages.*
