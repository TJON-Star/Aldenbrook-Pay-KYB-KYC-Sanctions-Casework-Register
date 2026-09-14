# Aldenbrook Pay - KYB/KYC & Sanctions Casework Register

[View the workbook](./Aldenbrook_KYB_KYC_Casework_Register.xlsx)

A fictional case-study platform (contractor payments / Employer of Record), built to demonstrate evidence-first KYB, KYC, and sanctions/PEP/adverse-media casework, using the same discipline as this portfolio's GoLemon GRC assessment: no client, contractor, or screening data here is real.

## Why this exists

Risk-based onboarding and compliance work (reviewing corporate documents, verifying identities, running sanctions and PEP screening, investigating payment anomalies) runs on exactly the same discipline as a formal GRC control assessment: don't overclaim what the evidence supports, don't auto-clear a flag just because a document exists, and make every decision traceable back to the specific evidence and criterion it rests on.

This project applies that discipline to compliance operations casework instead of enterprise risk assessment.

## Core discipline

An unresolved screening flag is not a confirmed match. A lack of documented adverse media is not confirmation of a clean file, it means no adverse media was found in the sources checked as of the screening date. Missing or incomplete documentation is not evidence of low risk, it is an open gap that blocks a decision until it is resolved.

## Files in this workbook

| Tab | Contents |
|---|---|
| `Case Register` | 10 representative cases across Client KYB, Contractor KYC, and Payment Investigation, with risk tier and status |
| `Evidence & Screening Register` | Full evidence trails for four cases chosen to demonstrate the discipline: an open documentation gap, an escalated PEP match, a decline built on a pattern across evidence, and a sanctions match cleared as a false positive using independent identifiers |
| `Review Procedures` | Per evidence/screening type: what's reviewed, what passes, what escalates, defined before evidence arrives |
| `Escalation & Decision Log` | Every decision, citing the specific Evidence ID(s) and Review Procedures criterion it rests on |
| `Legend & Instructions` | Status coding, screening-result coding, and the discipline behind each tab |
| `Casework Summary` | Roll-up charts of the 10 cases by status and risk tier |

## The four worked cases

- **C-002 (Vantage Digital Media FZE):** UBO declaration leaves 20% ownership unattributed. Recorded as an open gap, not a benign omission. Case stays open until resolved.
- **C-004 (R. Osei):** PEP screening returns a partial name match with a 4-year date-of-birth discrepancy. Escalated for disambiguation rather than auto-cleared on a partial mismatch or auto-declined on a partial match.
- **C-006 (Ferrotech Trading DMCC):** No sanctions or adverse media hits, but no verifiable operational substance and a UBO linked to other flagged entities. Declined on the pattern across evidence, not on the screening result, which was clean.
- **C-010 (J. Santos):** Sanctions screening returns a name match. Cleared as a false positive, but only after two independent identifiers (date of birth, nationality) and a supporting document contradicted the listed record, never on name dissimilarity alone.

## Workflow

```
Case Intake -> Evidence & Screening Request -> Evidence Review -> Screening Disambiguation (where flagged)
-> Decision -> Escalation & Decision Log -> Periodic Refresh / Retest
```

## License

Fictional case-study project, built for portfolio and methodology demonstration purposes.
