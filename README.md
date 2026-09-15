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

## What we discovered reviewing our own build

This register was built in one pass, then stress-tested against its own stated discipline before being called finished. Two real gaps surfaced, both fixed in the workbook, not just noted.

**1. The disambiguation criterion didn't actually match how the two real cases were decided.**
Case C-004 (R. Osei) escalates a PEP match with only a 4-year date-of-birth discrepancy, despite the nationality matching. Case C-010 (J. Santos) clears a sanctions match with a much larger discrepancy across two identifiers, plus a supporting document. Both outcomes are individually defensible, but the original Review Procedures criterion, "at least one independent identifier is inconsistent," doesn't explain why one case cleared and the other didn't. Written as-is, it could be read as contradicting the C-004 decision. Fixed by rewriting the criterion to weigh both the number of inconsistent identifiers and the size of the discrepancy, and to explicitly hold a small, single discrepancy against clearing when the listed record involves a currently active high-risk role.

**2. The Ferrotech decline risked treating an unproven association as if it were confirmed wrongdoing.**
The original note for C-006 said the UBO was "linked to two other entities flagged in prior unrelated case files," and the decision log cited that linkage as a factor in declining the application. Read carefully, that's the same failure mode this whole project is built to catch, in reverse: those other cases were never confirmed, only under review, so treating the association as decisive was an overclaim in the other direction. Fixed by rewording both the evidence note and the decision rationale to state plainly that unresolved linkage is an elevated-scrutiny factor requiring disclosure, not proof of wrongdoing, and that the decline rests primarily on the independently well-evidenced operational-substance gap.

Neither of these was a factual error. Both were places where the stated standard and the actual decision didn't quite line up, the same category of gap documented in this portfolio's other GRC work, which is exactly why it's worth checking for on every build, not just the first one.

## License

Fictional case-study project, built for portfolio and methodology demonstration purposes.
