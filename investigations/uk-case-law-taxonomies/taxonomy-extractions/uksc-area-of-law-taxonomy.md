# Taxonomy extraction: UK Supreme Court "Area of law" filter

Full transcription of the **flat, single-level** "Area of law" filter on the [UKSC cases page](https://www.supremecourt.uk/cases) (1,601 cases at capture). It is not a dropdown but a checkbox group in the left-hand "Filters" accordion (`#accordion-aol`); each option maps 1:1 to an `areaOfLaw` value used as a URL query parameter and stored per case. The list is hardcoded in the site's client JS bundle (Next.js chunk `/_next/static/chunks/2wz95c2z6rhmb.js`, config object `areaOfLaw:{name:"aol",title:"Area of law",type:"checkbox",items:[…]}`) — it does not come from an API. 25 areas; `text` and `value` are identical for every entry.

- Arbitration
- Business, property, wills, and trusts
- Commercial
- Constitution
- Contempt
- Court procedure
- Crime
- Devolution
- Employment
- Environment and planning
- EU law
- Extradition
- Family
- Immigration
- Insolvency
- Intellectual property
- International
- Landlord and tenant
- Negligence
- Privacy and information
- Public law and human rights
- Tax
- Tort
- Veterinary surgeons
- Mission and Pastoral Measures

Extraction method: read from the live site's JS bundle (chunk `2wz95c2z6rhmb.js`), captured 4 Nov 2026.

## Notes

- **Ordering:** items 1–23 are alphabetical A→T; "Veterinary surgeons" and "Mission and Pastoral Measures" sit at the end, out of sort order — evidence they were appended later without re-sorting (hand-maintained vocabulary).
- **Unusual entries:** *Veterinary surgeons* (professional-discipline cases, e.g. appeals from the Royal College of Veterinary Surgeons) and *Mission and Pastoral Measures* (Church of England ecclesiastical-measure cases) are case-type/jurisdiction labels rather than law subjects — the scheme mixes subject facets with matter-type facets, same pattern as the tribunal schemes in [courts-tribunals-schemes.md](../notes/courts-tribunals-schemes.md).
- **Display:** on each case listing entry the area of law is shown ALL-CAPS beside the case number (e.g. `TAX`, `PUBLIC LAW AND HUMAN RIGHTS`, `LANDLORD AND TENANT`); recently lodged permission-to-appeal applications carry an empty value.
- **Sibling facet:** the same filter panel has a separate "Jurisdiction" checkbox group (`jurisdiction:{name:"j",…}`) enumerating the UKSC's appellate jurisdictions (England & Wales, Scotland, NI plus Crown Dependencies/overseas territories/Commonwealth realms) — a source facet, not subject.
- **Relevance:** this is the only live subject vocabulary run by one of the senior courts themselves; it is close in shape to ICLR's 14 Legal Topics (see [iclr-topic-taxonomy.md](../notes/iclr-topic-taxonomy.md)) but finer-grained (25 vs 14) and splits e.g. *Negligence* out of *Tort*, *Immigration* out of *Public law*, and keeps *EU law*.
