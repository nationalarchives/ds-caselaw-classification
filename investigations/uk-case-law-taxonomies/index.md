# UK case law subject taxonomies

An investigation into existing and past taxonomies/subject classification schemes for UK case law, to inform the design of a subject taxonomy for [Find Case Law](https://caselaw.nationalarchives.gov.uk/) (The National Archives).

## Summary

See [Summary](summary.md) for the plan and status; individual notes record sources per topic.

## Notes

- [UK courts and subject coverage](notes/uk-courts-and-subject-coverage.md) — court-by-court map of Find Case Law coverage, broad subject areas, linked taxonomies already extracted, and official GOV.UK/judiciary sources for potential subject lists.
- [Court and tribunal specific schemes](notes/courts-tribunals-schemes.md) — subject/topic schemes used by individual courts or tribunals to publish their decisions.
- [Public facing and advice services](notes/public-facing-services.md) — how services aimed at non-lawyers (Citizens Advice, Shelter, Advicenow, GOV.UK, courts own websites) organise legal topics.
- [Legal information institutes and commercial taxonomies](notes/lii-and-commercial-taxonomies.md) — CanLII, AustLII, BAILII, Westlaw, Halsbury's and other professional classification schemes.
- [International and standards schemes](notes/international-standards.md) — EuroVoc, Law Classification for Contents of Law Journals, Library of Congress K, ECLI metadata and related standards.
- [iclr-topic-taxonomy](notes/iclr-topic-taxonomy.md) Summary of public ICLR categories from web site exploration

### Taxonomy extractions (nested lists for review)

- [lands-chamber-taxonomy](taxonomy-extractions/lands-chamber-taxonomy.md) — Upper Tribunal (Lands Chamber) decisions site: 17 categories / 140 subcategories, from the live `PopulateSubcategory.js` data (site frozen Aug 2025).
- [eat-taxonomy](taxonomy-extractions/eat-taxonomy.md) — Employment Appeal Tribunal: flat 43-topic list including 8 explicitly marked obsolete topics (site frozen Mar 2017).
- [eat-taxonomy-govuk](taxonomy-extractions/eat-taxonomy-govuk.md) — EAT decisions on GOV.UK: **two-level** scheme, 45 categories / 192 sub-categories parsed from the content API facet schema (captured 13 Nov 2026); includes a comparison with the legacy flat list.
- [land-registration-division-taxonomy](taxonomy-extractions/land-registration-division-taxonomy.md) — FTT (Property Chamber) Land Registration Division: **two-level** scheme, 27 categories harvested with their dependent Sub Category options via form postback (208 subcategory entries; site frozen Aug 2025).
- [Sargeant 2026 case law classification](taxonomy-extractions/Sargeant%202026%20case%20law%20classification.md)
- [stanford-list-taxonomy](taxonomy-extractions/stanford-list-taxonomy.md) — Stanford LIST (Legal Issues Taxonomy): full 1,301-term hierarchy extracted from [taxonomy.legal](https://www.taxonomy.legal/) /api/terms, 20 top-level domains, 4 levels deep.
- [thesaurus-current](taxonomy-extractions/thesaurus-current.md) — the national archives' draft legislation thesaurus (CSV in `docs/thesaurus_current.csv`): 494 terms in 3 partitions (Subject — 37 policy areas, Business — NACE-based, Regions), tree view with AltLabels in parentheses.
- [lams-ccs-taxonomy](taxonomy-extractions/lams-ccs-taxonomy.md) — LAMS Content Classification Scheme v1.6 (CSV in `docs/CCS_taxonomy_narrow.csv`): 346 terms, 14 top headings, 2–3 levels deep; the 2001 advice-sector scheme behind Just Ask / Community Legal Advice search.
- [ca-ccs-taxonomy](taxonomy-extractions/ca-ccs-taxonomy.md) — Citizens Advice CCS labels (CSV in `docs/CA_CCS_taxonomy_narrow.csv`): Caitlin Wilson research project; 108 CA page labels mapped into 7 CA website areas, flat; largely complementary to LAMS CCS (only 11 exact term overlaps).
- [uksc-area-of-law-taxonomy](taxonomy-extractions/uksc-area-of-law-taxonomy.md) — UK Supreme Court cases page "Area of law" filter: flat 25-item checkbox list extracted from the site's JS bundle (captured 4 Nov 2026); includes two out-of-order appends (*Veterinary surgeons*, *Mission and Pastoral Measures*).
- [upper-tribunal-aat-taxonomy](taxonomy-extractions/upper-tribunal-aat-taxonomy.md) — GOV.UK "Administrative appeals tribunal decisions" finder (UT Administrative Appeals Chamber): **two-level** scheme, 63 categories / 486 sub-categories parsed from the server-rendered facet checkboxes and matched by `{category} - ` prefix (captured 4 Nov 2026); benefit-led, with three out-of-order `Transport - …` appends in the category list.
- [tax-and-chancery-tribunal-taxonomy](taxonomy-extractions/tax-and-chancery-tribunal-taxonomy.md) — GOV.UK "Tax and Chancery tribunal decisions" finder (UT Tax and Chancery Chamber): flat 6-category checkbox list from the server-rendered facet (captured 4 Nov 2026); first browsable subject list observed for the chamber.
- [gazette-notice-codes-taxonomy](taxonomy-extractions/gazette-notice-codes-taxonomy.md) — The Gazette notice codes: **two-level** scheme of 7 groups / 22 categories / 258 numbered notice codes, plus 40 flat Company Law Supplement codes (A1–L2), parsed from the server-rendered page (captured 4 Nov 2026); a notice-type classification rather than a case-law subject taxonomy.
- [sali-lmss-area-of-law-taxonomy](taxonomy-extractions/sali-lmss-area-of-law-taxonomy.md) — SALI LMSS ontology (viewer.sali.org): "Area of Law" subtree, 26 areas / 102 subtopics / 3 leaves walked from the public `lmss_v2.json` in the viewer's own collation order (captured 4 Nov 2026); a US-centric legal-matter classification with `CANADA:`-prefixed entries.
- [Legal subject areas](taxonomy-extractions/Legal%20subject%20areas.md) - Draft list of legal subject areas based on common areas of law from curricula \(Blackstone's Statutes and BSB Bar Qualification Manual\)

### Synthesis

- [Candidate public-facing top-level taxonomy](synthesis/candidate-public-top-level-taxonomy.md) — 17 problem-led headings synthesised primarily from Sargeant, Stanford LIST, LAMS CCS, CA CCS and ICLR, with a doctrine crosswalk and design notes.
- [Legislation thesaurus comparison](synthesis/legislation-thesaurus-comparison.md) — comparison with the draft legislation Subject partition and recommendation for a unified, legislation-led scheme.
- [Candidate public-facing top-level taxonomy (v2, legislation-aligned)](synthesis/candidate-public-top-level-taxonomy-v2.md) — 28 problem-led headings rebuilt against the updated thesaurus, each naming its corresponding legislation Subject area(s), with documented omissions and a validation plan.
- [Mapping v2 headings to example case-law schemes](synthesis/v2-heading-scheme-mapping.md) — hub page for per-scheme crosswalks of the v2 headings, with one page and Sankey diagram per scheme: [Sargeant et al. (level 2)](synthesis/v2-sargeant-mapping.md), [ICLR Legal Topics](synthesis/v2-iclr-mapping.md), [ICLR catchwords](synthesis/v2-iclr-catchwords-mapping.md), [UKSC](synthesis/v2-uksc-mapping.md), [Legal subject areas (curricula)](synthesis/v2-legal-subject-areas-mapping.md), [Smart survey search topics](synthesis/v2-smart-survey-topics-mapping.md).
