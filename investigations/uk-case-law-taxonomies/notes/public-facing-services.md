# Public-facing UK legal taxonomies (for a Find Case Law subject scheme)

How UK services aimed at the public and non-lawyers organise legal topics. Based on live site inspection (Oct 2026). Find Case Law (TNA) currently has no subject taxonomy; this reviews lay-facing schemes for coverage, depth and language.

## Overall patterns

- **Convergent top level**: every lay-facing service clusters around the same ~8–12 "life problem" areas: Debt and money, Consumer, Housing, Family/children, Employment/work, Benefits, Immigration, Health/community care, Discrimination/civil rights, and a "Law and courts / going to court" area. This is the de facto UK public taxonomy of legal problems.
- **Two audiences, two schemes**: the same organisations run *two* structures — a lay "problem route" (plain English, problem-first) and a professional "legal route" (Shelter Legal, CA AdviserNet: doctrine-first, e.g. "possession and eviction" vs "I'm being evicted"). Find Case Law will need to decide which audience level to support, or both (e.g. short lay labels as display, doctrinal terms as alternate/synonym labels).
- **Language**: lay routes use outcome/verb phrasing ("Getting evicted", "Dealing with rent arrears", "Ending a private tenancy", "Challenging a rent increase") rather than legal nouns ("possession proceedings"). Citizens Advice explicitly designs content from user-researched language ([card sorting blog](https://wearecitizensadvice.org.uk/how-people-look-for-things-af8ed57d9a07)).
- **Depth**: typically 2–3 levels + page-level granularity (e.g. Housing > Deposits > "Taking your landlord to court if they haven't followed the deposit rules"). Leaf "topics" are essentially the classification granularity that would be needed unless a case tag maps to a mid-level node.
- **Weakness for case law use**: these schemes are advice/service trees, not subject indexes — no criminal, no commercial, no tax, no public/constitutional law beyond a thin "civil rights"/"human rights" slice, and court-process nodes (settlement, appeals, disclosure) which cut across subject in a way a case-law taxonomy shouldn't. Shelter Legal and LAA categories are the clearest precedents for doctrinal coverage.
- **No shared cross-sector standard exists**: there is no published UK "advice sector subject standard"; the nearest machine-relevant schemes are (a) Citizens Advice's internal 2-tier adviser issue-code taxonomy, (b) LAA "categories of law", (c) consumers' go-to court/tribunal type labels.

---

## 1. Citizens Advice (citizensadvice.org.uk)

**Audience**: general public (multi-jurisdiction: England, Scotland, Wales, NI variants).

**Top-level nav (public site)** — 9 fixed categories:
Benefits · Work · Debt and money · Consumer · Housing · Family · Law and courts · Immigration · Health

**Depth (illustrative, Housing)** — ~28 sub-indexes at level 2, each holding 1–6 pages at level 3:
Eviction · Finding somewhere to live · Homeless help · Starting to rent from a private landlord · Applying for council housing or a housing association home · Deposits · Paying rent · Repairs and housing conditions · Fire safety · Building safety · Complaints about landlords and letting agents · Renting with other people · Ending a private tenancy · Council tax · Problems with neighbours · Right to reside · Buying and selling a home · Mortgage problems · University accommodation · Lodging and subletting · Squatting · Excluded occupiers · Armed forces, etc. (~3,000+ advice pages total).

**"Law and courts" section** (closest to case law) — only 6 sub-groups:
- Legal system (7 pages: finding free legal help, small claims, going to court without a solicitor, going to court as a witness…)
- Claiming compensation for a personal injury
- Discrimination (9 pages: protected characteristics by protected characteristic, public sector equality duty, hate crime…)
- Parking tickets (5 pages)
- Civil rights (human rights; young people's rights)

→ Notably sparse and W-shaped (mixes subject with service); *not* a usable model for a case-law subject scheme. Note CA's Employment tribunals content sits under "Work", not under Law and courts — subject-typed nav beats court-typed nav.

**Internal taxonomy (not fully public but documented)**: CA classifies all casework with a **2-tier adviser issue code** (level 1 = issue area, e.g. benefits/needs; level 2 = specific issue, e.g. Universal Credit, PIP). Documented in [Content Design London's clustering writeup](https://contentdesign.london/blog/how-i-used-data-visualisation-with-citizens-advice-content). Codes like BEN2/DEB1 exist but the full code list itself is not publicly published (AdviserNet is login-only).

**Digital blog ([wearecitizensadvice.org.uk](https://wearecitizensadvice.org.uk/how-people-look-for-things-af8ed57d9a07))** insights:
- Card sorts (54 clients + advisers) found "no differences between advisers and clients" in grouping — supports a single scheme serving both audiences.
- Users want action-oriented two-step groupings ("what to do when in debt" / "managing your debt").
- [Restructuring 'Work' post](https://wearecitizensadvice.org.uk/restructuring-our-employment-advice-f3abf775f562): only use sub-indexes where topic is "clear and self-contained" (e.g. Redundancy, Employment tribunals); avoid vague catch-alls ("Problems at work") that attract every kind of issue. Matters for FCL scheme design: keep buckets few, name them in user language, make them mutually exclusive.
- CA states advisers "need quick access to case law and complicated source material" for complex cases ([blog](https://wearecitizensadvice.org.uk/people-dont-care-which-team-content-comes-from-they-care-about-whether-it-gives-them-what-they-8d94d0dc572c)) — a latent demand for a case law route linked from a subject tree.

**Usefulness for Find Case Law**: high for lay-language label vocabulary (problem-verbs) and for a top-level "life area" layer; low depth-wise in its "Law and courts" cut; adviser codes are a live internal precedent of a 2-tier scheme, but not public/reusable.

## 2. GOV.UK "Crime, justice and the law" topic

**Audience**: public; owner: GDS/Ministry of Justice content teams.

**[Top-level /browse/justice](https://www.gov.uk/browse/justice)** — 7 sub-topics (level 2), each described with plain-language "includes" bullets:
- Your rights and legal support — "includes legal aid, consumer advice, discrimination, work and residential property disputes"
- Courts, tribunals and appeals — "includes going to court, paying fines, appealing a sentence, jury service and tribunals"
- Reporting crimes · Compensation and victim support · Penalties, sentences and police · Prisons and probation · Young people and the law

**[ Courts, tribunals and appeals](https://www.gov.uk/browse/justice/courts-sentencing-tribunals)** — 7 level-3 groups: Going to court, giving evidence and jury service · Court fees and fines · Representing yourself or someone else in court · Tribunals · Appealing court and tribunal decisions · If someone owes you money / a court says you owe money · Complain about a legal professional.

**[Your rights and legal support](https://www.gov.uk/browse/justice/your-rights-legal-support)** — 6 groups: Getting legal support and advice · Consumer advice and complaints · Data protection and FOI · Discrimination and disability rights · Workplace/procedures · Residential property and neighbour disputes.

- Case-type-relevant patterns: "Tribunals" and "Appealing court and tribunal decisions" are the only court-typed navigations; employment tribunal / immigration appeal / tax tribunal links exist but sit per-proceeding, not per-subject. Most justice links are procedural/service (fees, forms, transcripts) rather than doctrinal.
- Court-type explainer only exists for criminal courts ([ /courts](https://www.gov.uk/courts): magistrates, Crown Court, youth courts — by venue, not subject).

**Usefulness**: moderate — a "process/stage" dimension (make a claim, respond, appeal, fees, representation) that Find Case Law could borrow as a secondary facet; weak as a subject classifier, and civil/family almost absent (only homelessness → housing dispute bits live elsewhere under /browse/housing-local-services).

## 3. Shelter Legal (England & Wales housing/debt law)

**Audience**: dual — lay public route (`/housing_advice`) and professional legal route (`/professional_resources/legal`), an explicit precedent for running lay and adviser taxonomies side by side on one org.

**[Housing advice (lay route)](https://england.shelter.org.uk/housing_advice)** — 9 topic branches:
Homelessness · Private renting · Eviction · Council housing · Repairs and housing conditions · Tenancy deposits · Benefits, debts and money · Mortgage repossession · Advice for students. Articles are problem-worded ("Council help if you are homeless… could be homeless in the next 8 weeks").

**[Shelter Legal (professional route)](https://england.shelter.org.uk/professional_resources/legal)** — 11 top-level areas with editorial one-liners (doctrinal, professional register):
1. **Homelessness applications** (eligibility, homelessness, priority need, intentionality, local connection, challenge decisions)
2. **Housing options** (allocations, specific needs)
3. **Renting** (tenancy types, occupation status, security of tenure)
4. **Costs of renting** (agent fees, rent in advance, deposits, rent increases)
5. **Benefits** (housing-related, benefit cap)
6. **Possession and eviction** (grounds, notice requirements, illegal eviction and harassment)
7. **Home ownership** (leaseholders, right to buy, shared ownership, mortgage arrears, compulsory purchase)
8. **Housing conditions** (disrepair, nuisance, overcrowding)
9. **Debt and money** (court enforcement, insolvency options)
10. **Relationship breakdown** (effect on tenancies/ownership)
11. **Court action and complaints** (court structure, pre-action steps, legal aid, costs/fees)

- Depth: area → guides → references/nodes (3 levels, deeper for technical topics). Content is statutory/case-law cited, and legal topics map closely to LAA Housing and Debt categories.
- Statutory references and instrument names are used freely; navigation uses short noun phrases (e.g. "Possession and eviction", not "possession proceedings").

**Usefulness**: highest quality mix — shows exactly how to bridge lay and professional vocab in one domain; 11 legal areas ≈ a feasible breadth for a FCL "Housing" branch, but only covers one subject area.

## 4. Advicenow (advicenow.org.uk)

**Audience**: public, self-help, formerly "Law for Life". Plain English, empowerment framing.

**[Get help](https://www.advicenow.org.uk/get-help)** — 9 top categories:
- **Benefits** (incl. PIP, UC, mandatory reconsideration tools, appeals)
- **Family and children** (divorce and separation, child arrangements, domestic abuse, child protection, cohabitation)
- **Employment** (grievances, tribunal)
- **Housing and homelessness** (eviction, tenancies, repairs, guarantors)
- **Going to court or tribunal** (resolving disputes, representing yourself, legal aid, small/fast-track claims, Single Justice Procedure Notices)
- **Health and social care** · **Immigration and nationality** · **Credit, loans and debts** · **Civil rights** (discrimination, human rights, protest, police powers)

**Beautiful structure and description of this**:

- Depth: 2 levels; each category holds a handful of guides + tools. Config-driven "Chosen for you" flags indicate content-type promotion rather than fixed hierarchy.
- Language: strongly material-noun + user-vocabulary ("Unfair PIP decision?", "What to do if you get a Single Justice Procedure Notice").

**Usefulness**: lean, ~9-area scheme with good lay language and tools, but limited legal-hierarchy depth; a reasonable baseline "top-9 life areas" naming source rather than a full scheme.

## 5. Support Through Court

**Audience**: litigants-in-person in **family and civil** courts (not criminal, not housing-only).

**Public navigation ([Support Through Court](https://supportthroughcourt.org/))**: service-first — Get Help (book an appointment, How we help, Locations, Remote hearings, FAQs) — *no problem-type or subject taxonomy on the site*. Their [Useful Links page](https://supportthroughcourt.org/get-help/useful-links/) is the only topical grid:
- **Information about going to court** · **Online resources for going to court** · **Family matters** (CAFCASS, mediators, OnlyMums/Dads, FNF, Women's Aid) · **General advice and support services** (Advocate, CA, Law Centres, LawWorks, Shelter) · **Legal aid and court fees** · **Government websites**

→ Organised by **court-type + process stage** ("Facing family or civil court without a lawyer"), not legal subject. Useful only as an alternative lens.

**Usefulness**: low as a taxonomy, but a good reminder that an audience "civil/family' tile + a process-stage layer is what litigants self-sort into; case law routes could support 'what stage/did this case get appealed?' style facets.

## 6. HMCTS Court and tribunal finder (find-court-tribunal.service.gov.uk)

**[Landing page](https://www.gov.uk/find-court-tribunal)** states it surfaces per-venue: address, contacts, opening times, how to get there, **"the areas of law it covers"**, disabled access — searchable by postcode or A–Z. The service itself blocks programmatic fetch (protected/JS-driven), but GOV.UK's "Explore the topic" confirms its purpose (venue-by-area-of-law/postcode rather than subject-first).

**Classified primarily by venue name and "areas of law" label** at a coarse grain; no case-type facets beyond area-of-law at venue level. If the "areas of law" list is usable, it's a natural complement to venue-typed case data in Find Case Law (venue → area mapping), but it's not publicly queryable in the fetched HTML.

**Usefulness**: supplementary — a court/venue→subject mapping coordinate system, not a taxonomy source.

## 7. Sector / professional schemes

### LawWorks (pro bono clinics)

- Groups partner clinics by **area of law** for referral (consumer, contract/small claims, employment, family, housing, immigration, wills); no public machine-taxonomy beyond clinic-filter facets. Useful only as a working list of clinic-level "areas of law" label vocabulary.

### Law Centres Network

- Site (seen live above) is entirely service/location-first ([lawcentres.org.uk](https://lawcentres.org.uk/)): navigation = About / What is a Law Centre? / Get involved / News / Get Help (List and Map of Law Centres, Other Sources of Help). No subject taxonomy.

### Legal Aid Agency "Categories of law" (LAA/MoJ)

- Statutorily enforced civil category scheme (LASPO Sch.1) with **Category Definitions annual PDFs**: 2024 [Category Definitions (May 2025)](https://assets.publishing.service.gov.uk/media/682c7d0560f66b9c23b00c8c/Category_Definitions_2024__May_2025_.pdf).
- Civil categories include: **Debt · Discrimination · Education · Family · Housing · Immigration and Asylum** (enumerated in the fetched extract), plus Community Care, Employment, Mental Health, Actions against the Police, Public Law, Welfare Benefits, Consumer, Wrongful arrest, Exceptional funding etc. (full civil category list; the [2025 Civil Legal Advice contract](https://assets.publishing.service.gov.uk/media/679a1a75fe19800263dc7b86/2_2025_Civil_Legal_Advice_Contract_Annex_1_Specification.pdf) narrows direct CLA intake to Debt, Discrimination, Education, Housing (+ Family/Immigration through specific schemes)).
- Definitions are framing/advocacy-led and interlocked (e.g. mortgage possession = Debt, other possession = Housing), defined by statute reference rather than user need ([Apply for legal aid](https://www.gov.uk/guidance/apply-for-legal-aid)).
- **Usefulness**: the only UK-wide, administratively-maintained doctrinal category list with sub-definitions; directly reusable as a professional/alternate-language layer for Find Case Law's civil cases (helpfully aligning case data with legal-aid routing).

---

## Implications for a Find Case Law public scheme

- Adopt a two-layer model mirroring Shelter/CA practice: (1) a small (~9–12) **lay "life problem area" top level** with plain-English names drawn from Citizens Advice/Housing/Shelter/Advicenow vocab; (2) a **deeper doctrinal branch** under each area, borrowing LAA category definitions and Shelter Legal's professional phrasing for professional users, with lay↔professional label pairs (e.g. "getting evicted" ↔ "possession and eviction").
- Keep the second layer mutually exclusive (CA blog's "don't keep vague catch-all headings" lesson); use topics ("employment tribunal", "small claims") only as cross-cutting facets, not as top-level buckets.
- Don't model the scheme on court-type or process-stage labels except as a separate facet; public services use courts/tribunals as routing aids, not as subject classes.
- Coverage gap to decide consciously: lay schemes omit criminal, commercial, tax, public law almost entirely; a case law taxonomy serving legal professionals needs those branches even if hidden from the lay tier.
- Check whether Citizens Advice's unpublished 2-tier issue codes and the LAA category definitions PDF (already machine-readable) can seed a draft scheme; LAA definitions are also statutory and periodically updated, so maintain via refresh.

## Source list

- [Citizens Advice homepage/nav](https://www.citizensadvice.org.uk/) · [Housing index](https://www.citizensadvice.org.uk/housing/) · [Law and courts index](https://www.citizensadvice.org.uk/law-and-courts/)
- [CA digital blog: How people look for things (card sort)](https://wearecitizensadvice.org.uk/how-people-look-for-things-af8ed57d9a07)
- [CA digital blog: Restructuring our employment advice](https://wearecitizensadvice.org.uk/restructuring-our-employment-advice-f3abf775f562)
- [CA digital blog: Building tools that meet people's needs (adviser issue codes/case law access)](https://wearecitizensadvice.org.uk/people-dont-care-which-team-content-comes-from-they-care-about-whether-it-gives-them-what-they-8d94d0dc572c)
- [Content Design London: Citizens Advice issue-code clustering](https://contentdesign.london/blog/how-i-used-data-visualisation-with-citizens-advice-content)
- [GOV.UK Crime, justice and the law](https://www.gov.uk/browse/justice) · [Courts, tribunals and appeals](https://www.gov.uk/browse/justice/courts-sentencing-tribunals) · [Your rights and legal support](https://www.gov.uk/browse/justice/your-rights-legal-support) · [Criminal courts](https://www.gov.uk/courts) · [Find a court or tribunal](https://www.gov.uk/find-court-tribunal)
- [Shelter England: Professional resources](https://england.shelter.org.uk/professional_resources) · [Shelter Legal](https://england.shelter.org.uk/professional_resources/legal) · [Housing advice (lay)](https://england.shelter.org.uk/housing_advice) · [Get help](https://england.shelter.org.uk/get_help)
- [Advicenow homepage](https://www.advicenow.org.uk/) · [Get help index](https://www.advicenow.org.uk/get-help)
- [Support Through Court](https://supportthroughcourt.org/) · [Useful links](https://supportthroughcourt.org/get-help/useful-links/)
- [Law Centres Network](https://lawcentres.org.uk/)
- [LAA Category Definitions 2024 (May 2025 update PDF)](https://assets.publishing.service.gov.uk/media/682c7d0560f66b9c23b00c8c/Category_Definitions_2024__May_2025_.pdf) · [2025 Civil Legal Advice contract Annex 1](https://assets.publishing.service.gov.uk/media/679a1a75fe19800263dc7b86/2_2025_Civil_Legal_Advice_Contract_Annex_1_Specification.pdf) · [Apply for legal aid](https://www.gov.uk/guidance/apply-for-legal-aid)
