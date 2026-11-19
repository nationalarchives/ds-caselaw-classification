# Mapping the v2 candidate headings to example case-law schemes

This is the hub page for crosswalking the 28 headings of the [v2 candidate public-facing top-level taxonomy](candidate-public-top-level-taxonomy-v2.md) against the top-level terms of the case-law schemes gathered in this investigation. Each scheme has its **own page with a per-scheme Sankey** — the earlier combined Sankey became less readable as schemes were added, so it was split.

## Per-scheme mapping pages

| Scheme                          | Mapped at                                         | Terms     | Per-scheme page                                                     |
| ------------------------------- | ------------------------------------------------- | --------- | ------------------------------------------------------------------- |
| Sargeant et al.                 | second level (its 6-area top level is too coarse) | 67 areas  | [Mapping to Sargeant et al.](v2-sargeant-mapping.md)                |
| ICLR                            | Legal Topics                                      | 14 topics | [Mapping to ICLR](v2-iclr-mapping.md)                               |
| ICLR                            | catchwords (Level 1)                              | 177 headings | [Mapping to ICLR catchwords](v2-iclr-catchwords-mapping.md)      |
| UKSC                            | areas of law                                      | 25 areas  | [Mapping to UKSC](v2-uksc-mapping.md)                               |
| Legal subject areas (curricula) | full list                                         | 19 areas  | [Mapping to Legal subject areas](v2-legal-subject-areas-mapping.md) |
| Smart survey search topics       | raw user vocabulary (uncontrolled)               | 172 topics (21 omitted) | [Mapping to smart survey topics](v2-smart-survey-topics-mapping.md) |

Queued for later passes: [EAT](../taxonomy-extractions/eat-taxonomy.md), [Stanford LIST](../taxonomy-extractions/stanford-list-taxonomy.md), [CA CCS](../taxonomy-extractions/ca-ccs-taxonomy.md).

## Method

- Each source term maps to **one or more** v2 headings — the mapping is deliberately many-to-many.
- Each link carries a *primary* target (bold in the per-scheme tables) where a v2 heading clearly best houses the term; secondary links reflect the multi-label assignment model of the v2 taxonomy.
- Each per-scheme page carries its crosswalk table (readable detail) and a generated Sankey diagram (whole picture). Link width encodes one term→heading mapping. The Sankeys are script-generated from a single mapping file, so adding a scheme means adding its mapping entries and regenerating.

## Overall findings

1. **Total coverage both ways.** All 474 source terms across the six schemes map to at least one v2 heading, and — once the 177 ICLR catchwords are included — **all 28 v2 headings receive at least one link** (the smart survey topics reach 27; only *Religion* is unlinked there too). The coarser schemes reach fewer headings (curricula 14, UKSC 17, ICLR Topics 18, Sargeant 25), which measures how doctrinal or venue-specific each scheme is, not gaps in the v2 list.
2. **The two legislation-biased headings are confirmed after all** — by a single catchword each, and by real user search demand. *Public and personal safety (10)* is fed by ICLR's HEALTH AND SAFETY and the survey's *Health & Safety* terms; *Food and food standards (23)* by FOOD AND DRUGS and the survey's food/cosmetics/tobacco terms. Real-volume validation (food standards appeals; product-safety enforcement) is still the deciding test.
3. **Real user vocabulary lands on the problem-led headings without forcing** ([smart survey mapping](v2-smart-survey-topics-mapping.md)): *Renters Rights* → *Home*, *Welfare Benefits* → *Benefits*, *House Sale* → *Home*. Variant spellings (*Charity / Charities / Charitable Institutions.*) confirm the alias layer of the v2 design; 21 unusable survey terms were excluded and listed rather than forced.
4. **The schemes triangulate consistently.** Where two schemes have matching terms, they map to the same v2 headings: the three case-law schemes all have a Tax term → *Tax (17)*; UKSC and ICLR both split Immigration/EU law out of Public law → *Immigration (19)* / *International affairs and treaties (28)*; UKSC's *Privacy and information* and Sargeant's *Data* both map to 25+13; the curricula's *Criminal Justice & Sentencing* splits 9/11 the same way Sargeant splits Crime from Prison law. Disagreements are informative (e.g. UKSC separates *Negligence* from *Tort*; ICLR does not).
5. **Low-volume headings kept for legislation alignment**: *Government finance and procurement (15)* is fed only by Sargeant's *Procurement* and the survey's *Procurement*; *National security, defence and emergencies (12)* only by *Military*/*Army And Defense*; *Religion (27)* by ICLR's *Ecclesiastical* and UKSC's *Mission and Pastoral Measures* — and by nothing in the survey. Validation should check whether their case volumes justify top-level status.
6. **Composite and matter-type labels stress the mapping.** UKSC's *Business, property, wills, and trusts* (three headings) and its *Veterinary surgeons* / *Mission and Pastoral Measures* (case-type labels) confirm that subject and matter-type should stay separate dimensions in the final design; the survey's *Judiciary*, *Civil Court Rules* and tribunal terms point the same way.

## First-pass results (retained for the record)

The first pass combined Sargeant (top level), ICLR and the [Lands Chamber](../taxonomy-extractions/lands-chamber-taxonomy.md) categories in a single Sankey. Key findings carried forward: Lands Chamber's 17 categories collapse 13/17 into *Home, housing and land* (expected for a land-jurisdiction tribunal — it stress-tests that heading's lower levels rather than the top level); Sargeant's "Personal and consumer matters" is a residual bucket (the reason for mapping at second level now); the headings kept separate at the user's choice (Religion, Tax, Energy) each uniquely catch source content. Lands Chamber is dropped from the per-scheme pages by design; its full scheme remains available in the [extraction](../taxonomy-extractions/lands-chamber-taxonomy.md).

## Next steps

- Extend with per-scheme pages for EAT, Stanford LIST and CA CCS.
- Weight the smart-survey Sankey by search frequency once the `COUNT` column is populated.
- Test the two thinnest headings (*Public and personal safety*, *Food and food standards*) against real judgments.
- Spot-check contentious cells with real cases (UKSC *Extradition* → 19/9; Sargeant *Construction* → 16 vs 1; *IP and Media* co-primary split).

## Related pages

- [Candidate public-facing top-level taxonomy (v2)](candidate-public-top-level-taxonomy-v2.md)
- [Candidate public-facing top-level taxonomy (v1)](candidate-public-top-level-taxonomy.md)
- [Legislation thesaurus comparison](legislation-thesaurus-comparison.md)
- [Investigation summary](../summary.md)
