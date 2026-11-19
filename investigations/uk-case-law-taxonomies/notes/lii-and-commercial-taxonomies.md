# Subject classification schemes used by legal information institutes (LIIs)

*Sub-topic of "existing subject classification schemes for case law", supporting a subject taxonomy for Find Case Law (The National Archives, caselaw.nationalarchives.gov.uk). Researched 25 Oct 2026. Scope: legal information institutes (LIIs) — see `summary.md` for the wider plan; commercial publisher schemes (Westlaw UK, Lexis, Halsbury's) where referenced appear in sibling notes.*

## Overall patterns

- **Most LIIs have no subject taxonomy for case law.** BAILII, AustLII (for cases), SAFLII, NZLII, IndiaLII and the other LII-network sites organise primary law by **jurisdiction → court/tribunal → database**, with full-text search as the primary retrieval tool ([BAILII databases](https://www.bailii.org/databases.html), [Georgetown guide on SAFLII](https://guides.ll.georgetown.edu/c.php?g=362128&p=4939499)).
- **Where subject schemes do exist, they come in three moulds:**
  - **Flat practice-area lists** (~40–50 terms) auto-assigned per case and exposed as a search-results filter — the CanLII model and now the ULII "legal topics" model.
  - **Two-tier frameworks** for legislation/indexing: broad top-level areas subdivided into specific subcategories, documents mirrored under multiple subjects — the AustLII/Anstat Subject Index Framework model.
  - **Curated "leading cases by subject" collections** — small hand-picked case collections arranged under subject headings, education-oriented — the BAILII OpenLaw model.
- **Assignment is trending from manual to automated.** WorldLII's catalog and BAILII's subject collections are maintained by human editors; CanLII trained machine-learning classifiers on law-librarian digest headnotes and law-report classifications, and is **now transitioning assignment to LLMs** ([Lexum, 2025](https://lexum.com/en/blog/from-ai-summaries-to-ai-enrichments)).
- **Lay vs professional language.** All LII subject schemes use standard legal/practice terms ("Contracts", "Torts", "Administrative law", "Insolvency & Bankruptcy"). None has designed its vocabulary for non-lawyers; LIIs serve lay users instead by pairing subject tags with plain-language summaries and clickable keywords.

---

## 1. CanLII (Canada) — ~44 flat "areas of law", AI-assigned

### Structure
- **Flat (non-hierarchical) list of 44 subjects** ("approximately 40 predefined areas of law" per [Lexum's product blog](https://lexum.com/en/blog/from-ai-summaries-to-ai-enrichments); "a total of 44 possible subjects" per the [CanLII blog, Jan 2025](https://blog.canlii.org/2025/01/23/whats-new-on-canlii-winter-2024-25/)). Terms are standard practice areas — examples observable on CanLII and its companion pages: Contracts, Criminal law, Family law, Torts, Immigration, Insurance, Bankruptcy & insolvency, Employment/labour, Tax, Evidence, Civil procedure ([slaw.ca example of selecting "Contracts"](https://tips.slaw.ca/2022/research/use-canliis-subject-classification-terms-to-narrow-your-search-results/); [CanLII Connects summary listing "AREAS OF LAW: Torts; Damages…"](https://canliiconnects.org/en/summaries/54059)).
- A case can carry **one or more subjects**; each subject is accompanied by **auto-extracted representative keywords** for finer-grained indexing.
- The same subject vocabulary is also used as a filter over **commentary** (since 2019, [CanLII blog](https://blog.canlii.org/2019/03/07/%f0%9f%a5%a7-you-can-now-search-commentary-on-canlii-by-subject-%f0%9f%a5%a7/)), giving one vocabulary across primary and secondary material.

### Assignment and maintenance
- Rolled out in stages driven by **law foundation grants**: Saskatchewan (2021) — model trained on the **Law Society of Saskatchewan Legal Resources Library's digest database** ([CanLII blog](https://blog.canlii.org/2021/06/14/new-ai-generated-subject-classification-for-saskatchewan-case-law-is-live/)); Ontario (2022) — trained on **Ontario Reports** editor classifications ([CanLII blog](https://blog.canlii.org/2022/01/25/new-ai-generated-subject-classification-for-ontario-case-law-is-live/)); then (mid-2023) expanded to all Canadian jurisdictions except Quebec, tagging ~550,000 decisions with **Lexum's "Lexkey" Longformer classifier** ([CanLII blog](https://blog.canlii.org/2025/01/23/whats-new-on-canlii-winter-2024-25/)).
- So the scheme's ground truth originates from **law-librarian classification**, but per-case assignment has never been human curator work: it is automated, and since 2025 the pipeline is **migrating from the in-house model to LLMs** ([Lexum](https://lexum.com/en/blog/from-ai-summaries-to-ai-enrichments)).
- Subjects appear as tags under search results, and as an **"All subjects" dropdown filter** in the Cases tab ([Lexum, Automatic Classification Part 1](https://lexum.com/en/blog/automatic-classification-on-canlii-part-1-functionalities); [slaw.ca](https://tips.slaw.ca/2022/research/use-canliis-subject-classification-terms-to-narrow-your-search-results/)). Tags are designed to be clickable to filter.
- Human curation persists in a parallel layer: **CanLII Connects** summaries by lawyer/student curators list "AREAS OF LAW" per case ([example](https://canliiconnects.org/en/summaries/54059)).

### Audience & usefulness for Find Case Law
- **Closest direct precedent** for a national, free, public case-law service adding a subject filter: ~44 flat terms, automated assignment at scale (~550k cases), filter-first UI, vocabulary shared across cases and commentary.
- **Coverage** good for mainstream court law; limitations: judicial decisions only (administrative decisions and Quebec civil-law cases were excluded initially), flat list means no narrowing below "Torts", and assignment quality is statistical — CanLII's own framing is that subjects "contextualise" results rather than provide authoritative indexing ([Lexum Part 1](https://lexum.com/en/blog/automatic-classification-on-canlii-part-1-functionalities)).
- **Lay accessibility** comes from the surrounding AI package (concise summaries, meaningful titles, keywords) rather than from the subject vocabulary itself — a lesson for FCL: a subject filter pairs well with plain-language enrichments.

---

## 2. AustLII / WorldLII (Australia) — two-tier frameworks, dual models

### AustLII's Subject Index Framework (SIF) to Legislation
- Joint project with **Anstat Pty Ltd** (commercial legislation publisher) to index the subject matter of **principal Acts and subordinate legislation across all Australian jurisdictions**; deliberately *not targeted at any user group* ([AustLII standards page](https://www.austlii.edu.au/techlib/standards/siflegis.html)).
- **Two-tier:** top-level categories reflect broad areas of law, subdivided into more specific subcategories; legislation relevant to multiple subjects is **mirrored under each subcategory**; links are made at subcategory level to full text, highlighting jurisdiction choice. Whole-Act indexing (not part or section level); **ongoing review** as legislation changes. Reuse by others explicitly welcomed with acknowledgement ([same page](https://www.austlii.edu.au/techlib/standards/siflegis.html), harvested via search snippet — the page itself is currently Cloudflare-guarded and has no successful Internet Archive capture, so the **fetched category list is not recoverable** from primary sources at present).
- Note: this framework indexes **legislation, not case law** — but it is AustLII's proof-of-concept for a subject structure and is directly transferable as a FCL framework design.

### WorldLII "Subjects" catalog (external links catalog)
- WorldLII's World Law catalog is browsable by **Countries, Regions, Subjects, Courts & Case-Law, Legislation, etc.** — the top-level "Categories" page ([archived copy](https://web.archive.org/web/20120218050747/http://www.austlii.edu.au/catalog/270.html)).
- The **Subjects** page is an alphabetically-ordered flat list of ~95 subject headings with rich see-references (@), e.g. Administrative Law, Alternative Dispute Resolution, Aviation Law, Banking & Finance, Competition Law, Consumer Protection, Criminal Law, Elections, Employment Law, Environment, Family Law, Freedom of Information, Human Rights, Indigenous Law, Insolvency & Bankruptcy, Intellectual Property, Legal System, Maritime Law, Privacy, Refugee & Asylum, Taxation Revenue & Customs, Tort & Personal Injury, Trade Practices, Wills & Probate — full list captured at [WorldLII >> Categories >> Subjects (2011 archive)](https://web.archive.org/web/20110518062508/http://www.austlii.edu.au/catalog/272.html).
- **Origin & maintenance:** built on AustLII's "Feathers" catalog software; by 2000 it had ~50 top-level categories "organised and divided in a way that is similar to the conventional paper-based Australian legal subject indexes", maintained **manually by AustLII secondary-materials staff**, with user submissions edited/approved before publication; every category page doubles as a **search scope** ("limited scope searching" over the linked sites and their spidered full text) ([Austin, Mowbray & Chung 2002, UTSLawRw](https://www5.austlii.edu.au/au/journals/UTSLawRw/2000/12.html); [Greenleaf's World Law guided tour](https://www2.austlii.edu.au/~graham/World_Law/index-3.html)).
- It indexes **websites and secondary materials, not individual cases** — categorisation sits one level above the case text.
- **AustLII's organizing principle for case law itself remains jurisdiction/court databases**; UK/Commonwealth content on WorldLII likewise sits under Countries/Governments/Courts & Case-Law categories, not subjects ([WorldLII Countries catalog](https://web.archive.org/web/20120218050747/http://www.austlii.edu.au/catalog/270.html)).

### Usefulness for Find Case Law
- **Two-tier framework + mirroring multi-assignment + jurisdictions as a facet** is a good structural template if FCL wants controlled depth without a sprawling hierarchy.
- The **manual-curation cost of the WorldLII model is real** and it was only ever applied to site-level catalog entries — arguably why no LII extended it to every case.
- Vocabulary is generic-lawyese; the concept granularity (see-references resolving synonyms like "Labor/Labour Employment") shows the value of **term consolidation** — something a UK vocabulary would need too ("Employment law" vs "Labour law") .

---

## 3. BAILII (UK & Ireland) — court-based databases; subjects only as curated collections

### How cases are organised
- BAILII holds **no system-wide subject classification of case law**. Content is organised as **databases by jurisdiction (England & Wales, Wales, Scotland, Northern Ireland, Ireland, UK, EU, offshore/commercial courts) and then by court or tribunal**: e.g. E&W Court of Appeal (Civil/Criminal), High Court divisions, Family Court, tribunals (Upper Tribunal chambers, First-tier Tribunal jurisdictions, Employment Tribunal, etc.). Users browse or search each database by keyword, date, or A–Z title ([BAILII databases page](https://www.bailii.org/databases.html)).
- Supporting layers: **Recent Decisions lists**, "New Cases of Interest" (curated feed), A–Z case-name/legislation/other-title indexes, citation lookup, multidatabase search, and most-downloaded judgments ([BAILII homepage, Dec 2024 archive](https://web.archive.org/web/20241229203804/https://www.bailii.org/)).
- Provenance: BAILII (founded 2001, based at the Institute of Advanced Legal Studies, supported by donors including law publishers) inherited the AustLII/WorldLII software approach; its founders/content model came from the legal information community rather than a classification process — **the only "founders' classification" is court/legislation taxonomy**, not subject.

### The one subject scheme: BAILII OpenLaw — Leading Cases by Subject
- A small **curated project "supporting legal education"** identifying *significant judgments regularly referenced in legal education*, arranged into **~24 subject collections**: Civil Procedure (Scotland), Company, Conflict of Laws (Scotland), Constitutional Law, Contract, Contract (Scotland), Criminal Law, Criminal Law (Scotland), Delict (Scotland), Employment, English Legal System, Family, Family (Scotland), Human Rights (ECHR), Immigration and Asylum, Land Law (Northern Ireland), Land & Tenant (Scotland), Northern Ireland Legal System, Property, Tax, Tort, Trusts, Various (Scotland) ([BAILII OpenLaw](https://www.bailii.org/openlaw/), reproduced from the Dec 2024 archive).
- Note the **jurisdiction-specific split** (Scotland uses Delict/Contract/Property instead of Tort/Criminal Law terms; Northern Ireland gets its own strands) — a pattern FCL should mirror for Scots law outside FCL's core (FCL does host Scottish Court of Session & High Court decisions, but has so far avoided Scottish subject vocabulary problems).
- Curated, education-facing, and explicitly not open-ended ("not feasible to add many additional cases") ([OpenLaw page](https://www.bailii.org/openlaw/)).

### Usefulness for Find Case Law
- Confirms the LII default: **court-database browsing + full-text search, no subject filter** — which is also FCL's current state; the market expectation of LIIs is thus not a barrier, but BAILII's model demonstrably doesn't help lay/public browsing.
- **OpenLaw is a cheap, high-value complement**: a curated "significant cases by subject" browse doesn't require per-case classification and speaks directly to `lay users` and students/citizen-advisers — arguably a better fit for FCL's public remit than an expensive ~2m-case tagging programme.

---

## 4. Other schemes worth noting (brief)

### ULII (Uganda) — AI/automatic "legal topics" browsing
- ULII's relaunched site exposes a **"Legal topics" browse**: two-level topics with hit counts and subtopic facets — Civil procedure (procedure & case management · appeals · pleadings), Criminal law (sentencing · sexual offences · evidence), Evidence (3,440), Land law (2,962: ownership and possession · customary tenure · registration of titles), Contract law (sale of land · guarantees · remedies), Tort (1,729), Appeal law, Constitutional law (right to fair hearing · jurisdiction · personal liberty), Administrative law (judicial review · natural justice), Succession law, Human rights, Property law, Election law ([ULII topics page](https://www.ulii.org/en/judgments/topics/); [ULII judgments page](https://www.ulii.org/en/judgments/)).
- The wording of subtopics ("ownership and possession", "right to fair hearing", "Evidence and proof") is markedly **more descriptive and lay-readable** than CanLII's practice-area labels, and counts per topic are surfaced in the UI (a strong UX pattern for a public service). Assignment appears automated for the whole corpus; no public documentation of the taxonomy source was found (page fetch is Cloudflare-guarded, so this is observed from search-indexed copies).

### SAFLII, NZLII, IndiaLII
- None has an explicit published subject scheme for case law: SAFLII and the wider LII network organise by country → court database (historical by year/alphabetical), keyword search only ([Georgetown guide re SAFLII](https://guides.ll.georgetown.edu/c.php?g=362128&p=4939499)); NZLII, IndiaLII, AsianLII, PacLII appear as court-organised members of the same network ([BAILII's World Law list](https://web.archive.org/web/20241229203804/https://www.bailii.org/)). Their shared ancestor is AustLII's catalog/database model — evidence that the **subject gap is network-wide, not UK-specific**.

### CourtListener / Free Law Project (US)
- **No practice-area or subject classification for opinions.** CourtListener's search filters are court/jurisdiction, judge, citation, date, precedential status; discovery beyond search relies on citation networks and, for dockets, **PACER "nature of suit" codes** (e.g. "850 Securities/Commodities") and keyword search alerts, plus new AI-powered search ([free.law RECAP presentation](https://free.law/pdf/presentations/Leveraging.the.RECAP.Suite.to.Support.Litigation.pdf); [岀 portfolio description](https://apify.com/jungle_synthesizer/courtlistener-opinion-scraper); [Above the Law interview with Free Law Project re AI search](https://abovethelaw.com/2025/06/3-questions-for-another-court-access-crusader-part-i/)).
- Useful negative precedent: even a well-funded, API-first free law service with 8m+ opinions has **declined to build a subject taxonomy**, treating court/date filters + full-text/semantic search as sufficient for its professional users — but it has not attempted the lay-audience job that FCL must do.

### Stanford LIST (US) — machine-readable legal-issue taxonomy (not an LII, cross-ref)
- Stanford Legal Design Lab's **[LIST (Legal Issues Taxonomy)](https://www.taxonomy.legal/)** is not an LII scheme (it classifies legal *issues*, not judgments), but it is the nearest large, machine-readable lay-taxonomy precedent — 1,301 terms / 20 domains / 4 levels with definitions, `/api/terms` JSON and crosswalks. Full extraction: [stanford-list-taxonomy.md](../taxonomy-extractions/stanford-list-taxonomy.md).

### Ireland — courts.ie
- Courts Service judgment search offers **no subject facets**: filters are court/jurisdiction, neutral citation, judge, and date; retrieval is keyword search (title or text) with ~8-week "recent judgments" listings ([courts.ie Searching for Judgments guide, PDF](https://www2.courts.ie/acc/alfresco/c938c7fa-e641-4a20-8c41-e8382e50cc1f/Searching-Judgments.pdf/pdf)).

---

## Applied assessment for a Find Case Law subject taxonomy

| Scheme | Type | Size | Assignment | Lay readability | Take for FCL |
|---|---|---|---|---|---|
| CanLII areas of law | Flat filter list | 44 subjects | ML (Longformer→LLM), trained on librarian digests | Moderate (practice-area terms) | **Strongest working precedent**: national scale, free service, filter UI, counts of ~40–50 as the sweet spot |
| AustLII/Anstat SIF | Two-tier framework (legislation only) | n/a (~20–50 top-level implied by "broad areas") | Maintained by Anstat/AustLII staff | Moderate | Structural template: two tiers + multi-assignment + jurisdiction facet |
| WorldLII Subjects | Flat web-link catalog | ~95 headings, see-references | Manual editorial | Low–moderate (generic) | Caution: manual cost; good synonym consolidation example |
| BAILII OpenLaw | Curated leading-case collections | ~24 subjects | Human curation | Good (education-facing) | Low-cost complement to any taxonomy for public users |
| ULII legal topics | Hierarchical topic browse | ~13 top + subtopics | Automated (apparent) | **Highest** (descriptive subtopics, UI counts) | Suitable UX pattern & lay wording for a public taxonomy (note: built for a corpus far smaller than FCL's) |
| CourtListener/RECAP | None for cases | — | — | — | Negative precedent: search-first is enough for professionals, not for the public |

**Synthesis for FCL:**
- No existing LII scheme is ready-to-adopt wholesale; but CanLII's **~44 flat subject areas + automated assignment + filter UI** is now a proven pattern on a comparable national common-law corpus.
- A pragmatic FCL design would combine: (a) a **flat or shallow ~40-term subject layer** (CanLII/ULII pattern, automated assignment with human sampling); (b) **Scots/Northern Irish terminology sensitivity** (BAILII OpenLaw's Delict/Land strands show the trap of a single UK vocabulary); (c) a **curated "leading/significant cases by subject" browse** for the public (cheap, education-facing); and (d) **UI counts and descriptive subtopics** à la ULII to keep the taxonomy navigable for non-lawyers.

## Sources

- CanLII: [Lexum — From AI Summaries to AI Enrichments (2025)](https://lexum.com/en/blog/from-ai-summaries-to-ai-enrichments) · [Lexum — Automatic Classification Part 1 (2023)](https://lexum.com/en/blog/automatic-classification-on-canlii-part-1-functionalities) · [CanLII blog — Subject classification for (almost) all jurisdictions (Jan 2025, 44 subjects)](https://blog.canlii.org/2025/01/23/whats-new-on-canlii-winter-2024-25/) · [CanLII blog — Saskatchewan project (2021)](https://blog.canlii.org/2021/06/14/new-ai-generated-subject-classification-for-saskatchewan-case-law-is-live/) · [CanLII blog — Ontario project (2022)](https://blog.canlii.org/2022/01/25/new-ai-generated-subject-classification-for-ontario-case-law-is-live/) · [slaw.ca tips — All subjects dropdown](https://tips.slaw.ca/2022/research/use-canliis-subject-classification-terms-to-narrow-your-search-results/) · [CanLII blog — Commentary subjects (2019)](https://blog.canlii.org/2019/03/07/%f0%9f%a5%a7-you-can-now-search-commentary-on-canlii-by-subject-%f0%9f%a5%a7/) · [CanLII Connects example "AREAS OF LAW"](https://canliiconnects.org/en/summaries/54059)
- AustLII/WorldLII: [AustLII standards — Subject Index Framework to Legislation](https://www.austlii.edu.au/techlib/standards/siflegis.html) · [WorldLII Categories (archived 2012)](https://web.archive.org/web/20120218050747/http://www.austlii.edu.au/catalog/270.html) · [WorldLII Subjects catalog (archived 2011)](https://web.archive.org/web/20110518062508/http://www.austlii.edu.au/catalog/272.html) · [Austin, Mowbray & Chung, "Scalability of Web Resources For Law" (2000, UTSLawRw 12)](https://www5.austlii.edu.au/au/journals/UTSLawRw/2000/12.html) · [Greenleaf, World Law guided tour (2000)](https://www2.austlii.edu.au/~graham/World_Law/index-3.html)
- BAILII: [BAILII homepage (archived 29 Dec 2024)](https://web.archive.org/web/20241229203804/https://www.bailii.org/) · [BAILII databases page](https://www.bailii.org/databases.html) (verified via [archived copy](http://web.archive.org/web/202412/https://www.bailii.org/databases.html)) · [BAILII OpenLaw — Leading Cases by Subject](https://www.bailii.org/openlaw/)
- Others: [ULII — Legal topics](https://www.ulii.org/en/judgments/topics/) · [ULII — Judgments](https://www.ulii.org/en/judgments/) · [Georgetown guide to SAFLII](https://guides.ll.georgetown.edu/c.php?g=362128&p=4939499) · [free.law — Leveraging the RECAP Suite](https://free.law/pdf/presentations/Leveraging.the.RECAP.Suite.to.Support.Litigation.pdf) · [Above the Law — interview with Free Law Project (2025)](https://abovethelaw.com/2025/06/3-questions-for-another-court-access-crusader-part-i/) · [courts.ie — Searching for Judgments (PDF)](https://www2.courts.ie/acc/alfresco/c938c7fa-e641-4a20-8c41-e8382e50cc1f/Searching-Judgments.pdf/pdf)
- Access note: austlii.edu.au, ulii.org and bailii.org guard some/all pages behind Cloudflare/Anubis bot protection; content above was recovered via the Internet Archive (Wayback), search-indexed copies, and cited secondary pages, as noted in each bullet.
