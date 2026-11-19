# CJS (Criminal Justice System) coding schemes

The PNLD (Police National Legal Database) is a "national resource for criminal justice legislation, supporting police forces, law enforcement agencies and criminal justice partners across England and Wales. Comprising Acts of Parliament, Common Law, Regulations, Orders and Byelaws, Case Law summaries, and the National Standard Offence Wordings and Codes."
Source: https://www.pnld.co.uk/article/?id=57fb5b12-351f-ef11-840a-6045bd127fdf

The National Standard Offence Wordings (SOWs) and Criminal Justice System (CJS) codes are the standard classification schema for describing each criminal offence and giving it a unique identifier. They’re used through the justice systems from charge through to court and conviction.

The SOW is the human-readable legal charging text and the CJS code is the machine-readable database key.

There are 15,352 active CJS Offence Index ([June 2026 release](https://www.gov.uk/guidance/criminal-justice-system-data-standards-forum-guidance#code-lists-for-data-standards), also hosted by the [Criminal Justice Hub](https://criminaljusticehub.org.uk/offence-classifications/). Each is given a label and unique alphanumeric identifier assigned to a specific statutory or common-law provision. 

The CJS Offence Category Code classifies the type of case or proceeding. It categorises the type of case or proceeding. It covers criminal and non-criminal court proceedings. Criminal categories are CB (non-offence breach), CE (either way), CI (indictable), CM (summary motoring), CS (summary non-motoring) and CR (civil matters related to a criminal case). Enforcement categories are EF (fines), EM (home maintenance enforcement) and EX (foreign maintenance enforcement). Civil categories are VA (miscellaneous civil applications) and VP (civil proceedings).

The CJS Offence Category Code classifies the type of court case or proceeding. It categorises the type of case or proceeding. Covering both criminal and non-criminal proceedings, which are divided into three main categories: criminal, enforcement and civil.

- Criminal categories are CB (non-offence breach), CE (either way), CI (indictable), CM (summary motoring), CS (summary non-motoring) and CR (civil matters related to a criminal case).
- Enforcement categories are EF (fines), EM (maintenance enforcement of home account) and EX (maintenance enforcement of foreign account).
- Civil categories are VA (miscellaneous civil applications) and VP (civil proceedings).

The CJS Offence Index CSV extract is published on GOV.UK under the Criminal justice system: [data standards forum guidance page](https://www.gov.uk/guidance/criminal-justice-system-data-standards-forum-guidance)

The vocabularies are maintained by the PNLD but overall governance is under the Criminal Justice System: [Data Standards Forum, chaired by the MoJ](https://www.gov.uk/government/groups/criminal-justice-system-data-standards-forum)

Our understanding is that the vast majority of criminal cases are assigned the CJS codes and those are tracked through the court systems, including Magistrates and Crown Court. The codes stay attached to the case (so that changes can be correctly entered in the Police National Computer (PNC)). 

However the Appeals or Supreme Courts cases are not assigned the offence codes, as the are organized by legal issue/appeal ground rather than offence code. Although the original CJS offence code remains linked to the underlying administrative case record in HMCTS (HM Courts & Tribunals Service) systems so PNC updates can flow back if a conviction or sentence is altered.

The CJS codes are not cited in Judgments directly - so not available as metadata in Find Case Law. However, a short form (canonical offence titles) associated with the CJS codes, are used for common offences such as “attempted murder”, “robbery”, “burglary”, “assault occasioning actual bodily harm”, e.g. https://caselaw.nationalarchives.gov.uk/search?query=assault+occasioning+actual+bodily+harm

The Criminal justice system: data standards also contain data standards/vocabularies for other key aspects of criminal cases, e.g.

- [Outcomes](https://www.gov.uk/guidance/criminal-justice-system-data-standards-forum-guidance#code-lists-for-data-standards) - possible outcomes of a criminal legal process   
- [Organisational structure standards](https://www.gov.uk/guidance/criminal-justice-system-data-standards-forum-guidance#code-lists-for-organisational-structure-standards) giving each court in the country an ‘Organisation Unit (OU) Identifier’ 