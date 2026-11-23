# ICLR Topic & Catchword Taxonomy

The Incorporated Council of Law Reporting for England & Wales (ICLR) — publisher of The Law Reports, WLR, ICR, Bus LR, and PTSR — maintains a two-layer classification system for all cases on its platform (ICLR.4). This is the most directly relevant prior art for our area-of-law dimension: it is the de facto standard subject-matter index for reported English & Welsh case law going back to 1865.

## Structure overview

ICLR applies **two independent classification layers** to each case:

1. **Legal Topic** — one of 14 broad categories (the "browse" taxonomy). A single topic is assigned per case. Used for homepage display, browsing, and search filtering.
2. **Catchwords** — a three-level hierarchical subject-matter heading plus free-text summary. Multiple catchword groups can be attached to a single case (one per distinct legal issue).

Additionally, each case carries:
- **Court** (a short code, e.g. `CA`, `KBD`, `UT`)
- **Legislation considered** (statutes, SIs, EU/international instruments)
- **Series** (which law report the case appears in)

## Layer 1: The 14 Legal Topics

These are the top-level browse categories shown on the ICLR homepage and available as a search facet. Source: [ICLR homepage](https://www.iclr.co.uk/) navigation, confirmed by `<category>` / `<topic>` fields in the [RSS feeds](https://www.iclr.co.uk/products/support/how-to-use-iclrs-latest-cases-rss-feed/).

| #   | Topic               | Notes                                                                                        |
| --- | ------------------- | -------------------------------------------------------------------------------------------- |
| 1   | Civil litigation    | Procedural/civil practice matters; also a catch-all for cases not fitting other topics       |
| 2   | Commercial          | Contracts, competition, consumer protection, arbitration, conflict of laws (commercial)      |
| 3   | Costs               | Costs disputes, solicitor-client fee issues                                                  |
| 4   | Crime               | Criminal law, sentencing, prisons, criminal procedure                                        |
| 5   | Ecclesiastical      | Church/faculty jurisdiction cases (rare)                                                     |
| 6   | Employment          | Employment/industrial relations, discrimination, TUPE                                        |
| 7   | European Union      | EU law cases (increasingly rare post-Brexit; may be legacy)                                  |
| 8   | Family              | Matrimonial, children, custody, care proceedings                                             |
| 9   | IP and Media        | Patents, copyright, trade marks, media law                                                   |
| 10  | Land law            | Property, planning, land registration                                                        |
| 11  | Public law          | Judicial review, administrative law, immigration, nationality, FOI, local government, police |
| 12  | Tax                 | Revenue/taxation (VAT, income tax, corporation tax, etc.)                                    |
| 13  | Tort                | Negligence, personal injury, nuisance, defamation                                            |
| 14  | Trusts and Chancery | Trusts, insolvency, equitable remedies, partnership                                          |

## Layer 2: Catchword hierarchy (three levels + free text)

The catchwords are the detailed subject-matter index. Each case can have **multiple subject-matter groups**, one per distinct legal issue addressed. The structure is:

```
Level 1 (ALL CAPS):   Broad subject heading
Level 2:              Sub-heading
Level 3:              Further sub-heading (optional)
Free text:            Detailed catchword summary + legislation cited
```

### Examples from live data (Oct 2026 WLR(D) feed)

| Case | L1 | L2 | L3 |
|------|----|----|----|
| Meta Platforms v Gormsen [2026] WLR(D) 492 | COMPETITION | Abuse of dominant position | Damages |
| Jones v Persons Unknown [2026] WLR(D) 491 | PRACTICE | Summary judgment | Application to set aside |
| Rogers v Wills [2026] WLR(D) 486 | DAMAGES | Assessment | Quantum |
| McGivern v MBR Acres [2026] WLR(D) 484 | LEGAL AID | Costs | Appeal |
| Uber London v White [2026] WLR(D) 480 | LITIGATION | Privilege | Litigation privilege |
| ADM Industries v Inerco [2026] WLR(D) 460 | ARBITRATION | Appeal | Award |
| Soprim v Djibouti [2026] WLR(D) 475 | CONFLICT OF LAWS | Trust | Applicable law |
| CMA v Emma Matratzen [2026] WLR(D) 472 | CONSUMER PROTECTION | Advertising | Price |
| Broadfield Law v Barnes [2026] WLR(D) 383 | SOLICITOR | Costs | Contentious business agreement |
| R (Sex Matters) v DPP [2026] WLR(D) 490 | CRIME | Sexual offences | Consent |
| R v Osmani [2026] WLR(D) 488 | CRIME | Sentence | Carrying out conduct for purpose of causing child to enter into marriage |
| Cox v DPP [2026] WLR(D) 483 | CRIME | Public order | Conduct likely to cause harassment, alarm or distress |
| R (Quaye) v SoS Justice [2026] WLR(D) 477 | PRISONS | Prisoners' rights | Detention at His Majesty's pleasure |
| Merriman v 1st Staff [2026] WLR(D) 479 | DISCRIMINATION | Disability | Duty to make reasonable adjustments |
| ABC v Huntercombe [2026] WLR(D) 476 | EMPLOYMENT | Transfer of undertaking | Effect of transfer |
| In the Petition of DM [2026] WLR(D) 467 | CHILDREN | Custody rights | Abduction |
| MF v NF [2026] WLR(D) 466 | MARRIAGE | Divorce | Financial provision |
| Lufthansa Technik v Astronics [2026] WLR(D) 461 | PATENT | Infringement | Account of profits |
| Westminster CC v Gems House [2026] WLR(D) 485 | PLANNING | Planning permission | Condition |
| King Media v SoS HCLG [2026] WLR(D) 489 | PLANNING | Advertisement | Discontinuance notice |
| R (Akinyemi) v SoS HD [2026] WLR(D) 482 | NATIONALITY | British citizenship | Application |
| CLO v Bolsover DC [2026] WLR(D) 478 | SOCIAL SECURITY | Housing benefit | Eligibility |
| UKRI v Information Comr [2026] WLR(D) 473 | FREEDOM OF INFORMATION | Disclosure | Public interest |
| R (Golding) v FSCS [2026] WLR(D) 471 | FINANCIAL SERVICES | Compensation | Statutory scheme |
| R (TDB) v Haringey LBC [2026] WLR(D) 469 | LOCAL GOVERNMENT | Community care services | Assessment of needs |
| R (BB) v Commissioner of Police [2026] WLR(D) 465 | POLICE | Commissioner's guidance | Instant messaging |
| R(NXP) v SoS HD [2026] WLR(D) 463 | JUDICIAL REVIEW | Court's jurisdiction | Transfer of proceedings |
| RC Comrs v Bolt Services [2026] WLR(D) 459 | REVENUE | Value added tax | Exemption |
| In re Cross Transport [2026] WLR(D) 474 | INSOLVENCY | Administration | Moratorium |
| Abbott v MoD [2026] 4 WLR 71 | DAMAGES | Personal injuries | Noise-induced hearing loss |
| WH Holding v London Stadium [2026] 1 WLR 4269 | CONTRACT | Construction | Expert determination |
| Republic of India v CC Devas [2026] 1 WLR 4033 | ARBITRATION | Preliminary question of law | Court's jurisdiction |
| Cobden v Cobden [2026] Ch 339 | PARTNERSHIP | Dissolution | Assets |
| Orion Shipping v Great Asia [2026] Bus LR 1815 | CONTRACT | Construction | Sale of ship |
| TAQA Bratani v Fujairah Oil [2026] 1 WLR 3852 | INSOLVENCY | Transaction at undervalue | Transaction |
| Ward v Rai [2026] 4 WLR 70 | COSTS | Detailed assessment | Appeal |
| Shehabi v Kingdom of Bahrain [2026] 3 WLR 379 | INTERNATIONAL LAW | State immunity | Statutory exception |
| VTB Bank v Kuanyshev [2026] 4 WLR 65 | INJUNCTION | Freezing order | Fortification of damages |
| Servis-Terminal v Drelle [2026] 3 WLR 357 | BANKRUPTCY | Petition | Creditor's petition |
| XGY v Chief Constable of Sussex [2026] KB 365 | BARRISTER | Immunity from suit | Statement made in court |
| Aabar Holdings v Glencore [2026] 3 WLR 551 | PRACTICE | Disclosure | Legal professional privilege |
| R (Secretary of State for Justice) v Parole Board [2026] 4 WLR 68 | PRISONS | Prisoners' rights | Release on licence |
| R v Baniulyte [2026] 1 WLR 3951 | COURT OF APPEAL (CRIMINAL DIVISION) | Practice | Anonymity |
| DPP v Ó hAnnaidh [2026] 1 WLR 3939 | CRIME | Terrorism | Institution of proceedings |
| R (Simms-Davies) v Crown Court [2026] 1 WLR 3909 | CRIME | Indictment | Deferred prosecution agreement |
| R v Kalinga [2026] WLR(D) 468 | CRIME | Carrying an offensive weapon | — |
| R v Sheikh [2026] 1 WLR 3778 | CRIME | Domestic violence | Causing or allowing vulnerable adult to suffer serious physical harm |
| R v FGD [2026] WLR(D) 462 | CRIME | Sexual offence | Rape |
| McAuley v Ethigen [2026] ICR D40 | INDUSTRIAL RELATIONS | Employment tribunals | Striking out |
| Duffy v BXTR 3 [2026] ICR D38 | EMPLOYMENT | Protected disclosure | Interim relief |
| Pekacar v Islington LBC [2026] ICR D36 | INDUSTRIAL RELATIONS | Employment tribunals | Case management |
| Geeks Ltd v Watts [2026] ICR 975 | RESTRAINT OF TRADE | Employment | Training fee |
| Jeffery v Givaudan UK [2026] ICR 962 | INDUSTRIAL RELATIONS | Employment tribunals | Reasons for decision |
| Wolfe v Taka Mayfair [2026] ICR 952 | EMPLOYMENT | Disciplinary hearing | Right to be accompanied |
| DHL Services v Ignatowicz [2026] ICR 931 | EMPLOYMENT | Unfair dismissal | Reinstatement |
| Leedham v Royal Mail [2026] ICR 921 | EMPLOYMENT | Wages | Pay statement |
| Costco Wholesale v Nash [2026] ICR 905 | INDUSTRIAL RELATIONS | Employment tribunals | Response |
| Practice Statement (ET: Legal officers) [2026] ICR 903 | PRACTICE | Employment tribunals | Legal officers |
| Day v East & North Hertfordshire NHS [2026] ICR D32 | INDUSTRIAL RELATIONS | Employment tribunals | Costs |
| In re B and G (Fact-finding) [2026] 4 WLR 69 | CHILDREN | Care proceedings | Practice / Fact-finding hearing |

## Enumerated Level-1 catchword headings

### From the 30-day all-series feed (Oct 2026) — 48 headings

The following ALL-CAPS Level-1 headings were extracted from the full 30-day RSS feed (all series: WLRD, WLR, LR_AC, LR_Ch, LR_Fam, LR_QB, Bus LR, ICR, PTSR). The feed contained **102 items** (101 with populated subject-matter groups). This is a sample, not the complete list — the full set is larger (see below for additional headings observed in search results).

| # | Level-1 heading | Cases | Observed Level-2 sub-headings |
|---|----------------|-------|------------------------------|
| 1 | ADOPTION | 1 | Adoption order |
| 2 | ARBITRATION | 3 | Appeal; Award; Preliminary question of law |
| 3 | BANKRUPTCY | 1 | Petition |
| 4 | BARRISTER | 1 | Immunity from suit |
| 5 | CHILDREN | 5 | Care proceedings; Child support maintenance; Custody rights; Practice |
| 6 | COMPETITION | 2 | Abuse of dominant position; Collective proceedings |
| 7 | CONFLICT OF LAWS | 1 | Trust |
| 8 | CONSUMER PROTECTION | 1 | Advertising |
| 9 | CONTRACT | 2 | Construction |
| 10 | COSTS | 1 | Detailed assessment |
| 11 | COURT OF APPEAL (CRIMINAL DIVISION) | 1 | Practice |
| 12 | CRIME | 8 | Carrying an offensive weapon; Domestic violence; Indictment; Public order; Sentence; Sexual offence(s); Terrorism |
| 13 | DAMAGES | 2 | Assessment; Personal injuries |
| 14 | DATA PROTECTION | 1 | Personal data |
| 15 | DEVOLUTION | 1 | Northern Ireland |
| 16 | DISCRIMINATION | 1 | Disability |
| 17 | EMPLOYMENT | 7 | Disciplinary hearing; Protected disclosure; Transfer of undertaking; Unfair dismissal; Wages |
| 18 | FINANCIAL SERVICES | 1 | Compensation |
| 19 | FREEDOM OF INFORMATION | 1 | Disclosure |
| 20 | IMMIGRATION | 4 | Deportation |
| 21 | INDUSTRIAL RELATIONS | 5 | Employment tribunals |
| 22 | INJUNCTION | 2 | Freezing order; Interim injunction |
| 23 | INSOLVENCY | 2 | Administration; Transaction at undervalue |
| 24 | INTERNATIONAL LAW | 1 | State immunity |
| 25 | JUDICIAL REVIEW | 1 | Court's jurisdiction |
| 26 | LANDLORD AND TENANT | 2 | Covenant; Right to manage |
| 27 | LAND REGISTRATION | 1 | Registration |
| 28 | LEGAL AID | 1 | Costs |
| 29 | LITIGATION | 2 | Privilege |
| 30 | LOCAL GOVERNMENT | 3 | Community care services; Road traffic |
| 31 | MARRIAGE | 3 | Divorce; Financial provision |
| 32 | MORTGAGE | 1 | Possession |
| 33 | NATIONALITY | 1 | British citizenship |
| 34 | PARTNERSHIP | 1 | Dissolution |
| 35 | PATENT | 2 | Infringement; Licence |
| 36 | PLANNING | 2 | Advertisement; Planning permission |
| 37 | POLICE | 1 | Commissioner's guidance |
| 38 | PRACTICE | 8 | Claim form; Competition Appeal Tribunal; Disclosure; Employment tribunals; Group litigation; Privilege; Service; Summary judgment |
| 39 | PRISONS | 2 | Prisoners' rights |
| 40 | PUBLIC POLICY | 1 | Illegality |
| 41 | PUBLIC PROCUREMENT | 2 | Contract award procedure |
| 42 | RATING | 1 | Rateable occupation |
| 43 | REVENUE | 4 | Income tax; Value added tax |
| 44 | RESTRAINT OF TRADE | 1 | Employment |
| 45 | SOCIAL SECURITY | 2 | Housing benefit; Jobseeker's allowance |
| 46 | SOLICITOR | 2 | Costs |
| 47 | TERRORISM | 1 | Counter-terrorism |
| 48 | TORT | 1 | Cause of action |

### Additional headings observed in ICLR search results (not in the 30-day feed)

The following Level-1 headings appeared in cached/search-indexed ICLR case pages but were not present in the 30-day RSS sample:

- CONTEMPT OF COURT
- LAW REFORM
- NEGLIGENCE
- SEQUESTRATION
- TRADE UNION

This brings the confirmed minimum to **53 distinct Level-1 headings**. The true total is almost certainly higher — rare subjects (ecclesiastical, admiralty, family sub-topics, etc.) may not appear in any given 30-day window.

### Full list not publicly enumerated

The complete set of Level-1 headings is accessible via:
- **ICLR.4 Browse page** (`/browse`) — dropdown menus for drilling through subject matter levels (behind AWS WAF; requires interactive browser session)
- **Full Search page** (`/search/fullSearch`) — Catchwords field accepts ALL-CAPS heading names
- **The Consolidated Index** (print, 1951–2020) — the "Subject Matter" section lists all headings alphabetically with cross-references; now available online via ICLR.4 search

The [ICLR glossary entry for "Catchwords"](https://www.iclr.co.uk/knowledge/glossary/catchwords) confirms: *"The first, second and third level headings may then be used to slot the subject matter into a taxonomy of subject matter, eg in a printed index such as ICLR's Consolidated Index series."*

The [Anatomy of a Law Report](https://www.iclr.co.uk/knowledge/case-law/anatomy-of-a-law-report) page gives the canonical example: *"The first one (eg 'Crime' or 'Landlord and tenant') gives a very broad indication of the type of case. The second (eg 'Theft' or 'Forfeiture of lease') narrows it down a bit, and the third (eg 'Dishonest appropriation' or 'Relief from forfeiture') identifies its subject matter with still more precision."*

## Mapping: Topics → Level-1 Catchwords

The 14 topics are coarser than the catchword headings. A rough mapping based on observed data (30-day all-series feed + search results):

| Topic | Typical Level-1 catchwords |
|-------|---------------------------|
| Civil litigation | PRACTICE, LITIGATION, DAMAGES, LEGAL AID, INJUNCTION, BANKRUPTCY, BARRISTER, CONTEMPT OF COURT, SEQUESTRATION |
| Commercial | COMPETITION, CONFLICT OF LAWS, CONSUMER PROTECTION, ARBITRATION, CONTRACT, PARTNERSHIP, PUBLIC PROCUREMENT |
| Costs | COSTS, SOLICITOR |
| Crime | CRIME, PRISONS, COURT OF APPEAL (CRIMINAL DIVISION), TERRORISM |
| Ecclesiastical | (not observed — very rare) |
| Employment | EMPLOYMENT, DISCRIMINATION, INDUSTRIAL RELATIONS, RESTRAINT OF TRADE, TRADE UNION |
| European Union | (legacy; 2 ECJ cases still in feed but topic not assigned to them) |
| Family | CHILDREN, MARRIAGE, ADOPTION |
| IP and Media | PATENT, (likely COPYRIGHT, TRADE MARKS, MEDIA — not observed in sample) |
| Land law | PLANNING, LANDLORD AND TENANT, LAND REGISTRATION, MORTGAGE, RATING |
| Public law | JUDICIAL REVIEW, NATIONALITY, SOCIAL SECURITY, FREEDOM OF INFORMATION, FINANCIAL SERVICES, LOCAL GOVERNMENT, POLICE, INTERNATIONAL LAW, IMMIGRATION, DEVOLUTION, PUBLIC POLICY, DATA PROTECTION |
| Tax | REVENUE |
| Tort | TORT, DAMAGES, NEGLIGENCE (confirmed via search; not in 30-day feed) |
| Trusts and Chancery | INSOLVENCY, (likely TRUSTS, EQUITABLE REMEDIES — not observed in sample) |

Note: LAW REFORM appears as a Level-1 heading in search results but doesn't map cleanly to a single topic — it appears as a secondary/parallel subject-matter group alongside the primary heading (e.g., "INDUSTRIAL RELATIONS — Unfair dismissal" + "LAW REFORM — Whether necessary").

## Court codes (observed in RSS `<court>` field)

From the 30-day all-series feed (102 items):

| Code | Count | Court |
|------|-------|-------|
| CA | 30 | Court of Appeal |
| KBD | 24 | High Court — King's Bench Division |
| EAT | 12 | Employment Appeal Tribunal |
| SC(E) | 11 | Supreme Court (hearing English/Welsh case) |
| UT | 9 | Upper Tribunal |
| Ch D | 4 | High Court — Chancery Division |
| Fam Ct | 3 | Family Court |
| CAT | 2 | Competition Appeal Tribunal |
| ECJ | 2 | Court of Justice of the European Union (legacy) |
| Fam D | 2 | Family Division (High Court) |
| DC | 1 | Crown Court (Distinguished Counsel?) / or Deputy Court |
| SC(NI) | 1 | Supreme Court (Northern Ireland matter) |

Note: `SC(E)` and `SC(NI)` suggest ICLR uses jurisdictional suffixes to distinguish the same court hearing cases from different UK jurisdictions.

## Law report series codes (RSS `series=` parameter)

| Code | Series |
|------|--------|
| WLRD | WLR Daily (case summaries) |
| WLR | The Weekly Law Reports |
| LR_AC | The Law Reports — Appeal Cases |
| LR_Ch | The Law Reports — Chancery |
| LR_Fam | The Law Reports — Family |
| LR_QB | The Law Reports — Queen's Bench (now King's Bench) |
| Bus LR | Business Law Reports |
| ICR | Industrial Cases Reports |
| PTSR | Public & Third Sector Law Reports |

## Assessment for our thesaurus project

**Strengths:**
- **Authoritative and maintained**: ICLR is the official law reporting body for E&W; their classification is the de facto standard.
- **Two-layer design is exactly what we need**: broad topics for browsing + fine-grained catchwords for precise classification. This mirrors our "area of law" (broad) + "subject-matter keywords" (fine) dimensions.
- **Machine-readable access**: The public RSS feeds (Base and Expanded) provide structured XML with topic, court, subject-matter hierarchy, and legislation — ideal for harvesting vocabulary.
- **Legislation linked to cases**: The catchword free-text includes statute references, supporting our "statute/legal basis" dimension.
- **Court codes** give us a starting point for the "court type" dimension (though incomplete — see below).

**Limitations:**
- **E&W only**: ICLR covers England & Wales. No Scottish or NI cases (though `SC(NI)` court code appears, suggesting some cross-jurisdictional matters are indexed). We need separate sources for those jurisdictions.
- **Full Level-1 list not published**: The complete set of ALL-CAPS headings is not publicly enumerated in any static document. Our 30-day all-series sample yields **48 headings**; search results confirm at least **5** more (CONTEMPT OF COURT, LAW REFORM, NEGLIGENCE, SEQUESTRATION, TRADE UNION), giving a confirmed minimum of **53**. The true total is likely higher (rare subjects like ECCLESIASTICAL, ADMIRALTY, COPYRIGHT, TRADE MARKS etc. may not appear in any given 30-day window). The Browse page (`/browse`) has the full dropdown but is behind AWS WAF and requires an interactive session.
- **RSS feed capped at 30 days**: The `days` parameter accepts only integers 1–30. There is no way to retrieve a longer historical window via RSS. For deeper vocabulary harvesting, one would need to: (a) collect RSS feeds over time, (b) access the ICLR.4 platform interactively, or (c) use the print Consolidated Index volumes (1951–2020).
- **Level 2 and 3 are open-ended**: Unlike Level 1 (a controlled vocabulary), Levels 2 and 3 appear to be free-text sub-headings chosen by the reporter for each case. This means they won't form a stable taxonomy without significant normalisation.
- **Topic assignment is singular**: Each case gets exactly one of the 14 topics, which can feel arbitrary for multi-issue cases (e.g., a competition case with procedural issues might be "Commercial" or "Civil litigation").
- **"European Union" topic is likely legacy**: Post-Brexit, this may rarely be used. Worth monitoring.
- **No procedural posture dimension**: The classification is purely subject-matter; it doesn't capture whether a case is a first-instance decision, appeal, judicial review, etc. (though the court code implies this partially).

## Sources

- [ICLR homepage](https://www.iclr.co.uk/) — 14-topic navigation
- [Case search on ICLR.4](https://www.iclr.co.uk/products/case-search-on-iclr-4/) — catchword structure, three levels, ALL CAPS convention
- [Interpreting results](https://www.iclr.co.uk/products/interpreting-results/) — "Legal topic" facet corresponds to homepage topics
- [Exploring case information](https://www.iclr.co.uk/products/exploring-case-information/) — Case Info page: subject matter, legislation considered, words & phrases
- [RSS feed documentation](https://www.iclr.co.uk/products/support/how-to-use-iclrs-latest-cases-rss-feed/) — Base and Expanded feed structure with XML examples; confirms `days` parameter is capped at 1–30
- [Neutral citation guide](https://www.iclr.co.uk/knowledge/case-law/neutral-citations/) — court list and citation prefixes
- [Consolidated Index (Red Book)](https://www.iclr.co.uk/products/other-publications/red-book/) — print subject-matter index 1951–2020; three levels of headings + catchwords; now available online via ICLR.4
- [Finding Consolidated Index info online](https://www.iclr.co.uk/knowledge/faq/how-do-i-find-consolidated-index-information-online/) — explains Browse page dropdowns and Full Search Catchwords field as online equivalents
- [Catchwords (glossary)](https://www.iclr.co.uk/knowledge/glossary/catchwords) — defines the three-level heading structure
- [Anatomy of a Law Report](https://www.iclr.co.uk/knowledge/case-law/anatomy-of-a-law-report) — canonical example of L1/L2/L3 ("Crime" → "Theft" → "Dishonest appropriation")
- Live data: `https://www.iclr.co.uk/documents/latest/days/30/rss-email` (all series, 102 items, fetched 4 Oct 2026)
- Search result snippets from `iclr.co.uk/browse/search/...` and `iclr.co.uk/search?filter=legal-topic:...` — additional L1 headings (CONTEMPT OF COURT, LAW REFORM, NEGLIGENCE, SEQUESTRATION, TRADE UNION)
