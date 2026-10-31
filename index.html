# Aldenbrook Pay: KYB/KYC & Sanctions Casework Register

> **Not real data.** Aldenbrook Pay is a fictional platform built to demonstrate evidence-first KYB, KYC, and sanctions/PEP/adverse-media casework.

**Core principle:** an unresolved screening flag is not a confirmed match; "no adverse media found" is not "confirmed clean"; and missing documentation is an open gap that blocks a decision, not evidence of low risk.

---

## 1. Project map

How the web page and the workbook fit together.

```mermaid
flowchart LR
    subgraph WEB["index.html (web page)"]
        H["Hero and core principle"]
        F["Files in this workbook"]
        C["Case Register: 10 cases"]
        P["Review Procedures"]
        S["Casework Summary"]
        L["Lessons: self-review"]
    end

    subgraph XLSX["Aldenbrook_KYB_KYC_Casework_Register.xlsx"]
        T1["Case Register"]
        T2["Evidence and Screening Register"]
        T3["Review Procedures"]
        T4["Escalation and Decision Log"]
        T5["Legend and Instructions"]
        T6["Casework Summary"]
    end

    C --- T1
    C --- T2
    P --- T3
    S --- T6
    F -.-> XLSX
    T4 -. "every decision cites its evidence and criterion" .- T2

    classDef web fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    classDef sheet fill:#f4efe0,stroke:#C9A227,color:#0E1116;
    class H,F,C,P,S,L web;
    class T1,T2,T3,T4,T5,T6 sheet;
```

---

## 2. Case portfolio (10 cases)

```mermaid
pie showData title Cases by status
    "Approved" : 5
    "Escalated" : 2
    "Under Review" : 1
    "Declined" : 1
    "Resolved" : 1
```

```mermaid
pie showData title Cases by risk tier
    "Medium" : 5
    "High" : 3
    "Low" : 2
```

| Case type | Cases |
|---|---|
| Client KYB | C-001, C-002, C-006, C-009 |
| Contractor KYC | C-003, C-004, C-007, C-010 |
| Payment Investigation | C-005, C-008 |

---

## 3. Screening decision flow (sanctions / PEP)

Why C-004 was escalated and C-010 was cleared.

```mermaid
flowchart TD
    A["Screening run"] --> B{"Potential match?<br/>(including partial name match)"}
    B -- "No match as of screening date" --> PASS["Pass<br/>Record date and sources checked"]
    B -- "Yes" --> D{"Disambiguation test:<br/>multiple identifiers inconsistent,<br/>gap too large for data-entry error,<br/>at least one corroborated by a document?"}
    D -- "Yes" --> CLEAR["Clear as false positive<br/>Example: C-010 J. Santos<br/>DOB and nationality both differ,<br/>ID and proof of address support"]
    D -- "No: one identifier differs,<br/>small gap, or active high-risk role" --> ESC["Escalate<br/>Example: C-004 R. Osei<br/>nationality matches, DOB off by 4 years,<br/>secondary document requested"]

    NOTE["Never auto-cleared or auto-declined.<br/>Never cleared on name dissimilarity alone."]
    B -.-> NOTE

    classDef good fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    classDef warn fill:#fbf3d6,stroke:#C9A227,color:#0E1116;
    classDef bad fill:#f8e4e0,stroke:#C25B4A,color:#0E1116;
    class PASS,CLEAR good;
    class ESC warn;
    class NOTE bad;
```

---

## 4. KYB evidence gaps (ownership and operations)

How open gaps block or drive a decision.

```mermaid
flowchart TD
    K["Client KYB case"] --> U{"UBO declaration:<br/>all owners identified,<br/>totals 100%, all screened?"}
    U -- "Yes" --> O{"Proof of operations:<br/>verifiable history consistent<br/>with declared activity?"}
    U -- "No" --> GAP["Open gap, case stays open<br/>C-002 Vantage Digital Media FZE:<br/>40% + 40% named, 20% unattributed"]
    O -- "Yes" --> OK["Proceed to decision"]
    O -- "No" --> DEC["Declined<br/>C-006 Ferrotech Trading DMCC:<br/>registered under 2 months,<br/>no history beyond a website,<br/>2 document requests unmet"]

    LINK["UBO linked to other entities under review:<br/>elevated scrutiny, requires disclosure.<br/>Not proof of wrongdoing."]
    DEC -.-> LINK

    classDef good fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    classDef warn fill:#fbf3d6,stroke:#C9A227,color:#0E1116;
    classDef bad fill:#f8e4e0,stroke:#C25B4A,color:#0E1116;
    class OK good;
    class GAP,LINK warn;
    class DEC bad;
```

---

## 5. The four worked cases at a glance

| Case | Subject | Issue | Handling | Outcome |
|---|---|---|---|---|
| C-002 | Vantage Digital Media FZE | 20% of ownership unattributed | Recorded as an open gap, not a benign omission | Under Review |
| C-004 | R. Osei | Partial PEP match, DOB differs by 4 years | Escalated; one small discrepancy against an active high-risk role is not enough to rule out the match | Escalated |
| C-006 | Ferrotech Trading DMCC | Recent registration, no operational history | Declined mainly on the operational-substance gap; UBO linkage treated as elevated scrutiny only | Declined |
| C-010 | J. Santos | Sanctions name match | Cleared only after two identifiers plus a document contradicted the listed record | Approved |

---

## 6. Self-review: two gaps found and fixed

```mermaid
flowchart LR
    subgraph G1["Gap 1: disambiguation criterion"]
        A1["Before:<br/>at least one identifier is inconsistent"] --> B1["Problem: did not explain why<br/>C-010 cleared but C-004 did not"]
        B1 --> C1["After: weigh the number of inconsistent<br/>identifiers and the size of the discrepancy"]
    end

    subgraph G2["Gap 2: Ferrotech decline rationale"]
        A2["Before: cited UBO link to<br/>other flagged entities"] --> B2["Problem: those cases were never concluded,<br/>so an unproven association read as fact"]
        B2 --> C2["After: linkage stated as elevated scrutiny;<br/>decline rests on operational-substance gap"]
    end

    classDef before fill:#f8e4e0,stroke:#C25B4A,color:#0E1116;
    classDef problem fill:#fbf3d6,stroke:#C9A227,color:#0E1116;
    classDef after fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    class A1,A2 before;
    class B1,B2 problem;
    class C1,C2 after;
```

Neither was a factual error. Both were places where the stated standard and the actual decision did not quite line up.

---

## Suggested walkthrough order

1. **Frame it** (not real data, then the core principle)
2. **Project map** (section 1): what is on the page vs. in the workbook
3. **Portfolio** (section 2): 10 cases, status and risk mix
4. **Screening flow** (section 3): C-010 cleared vs. C-004 escalated
5. **KYB gaps** (section 4): C-002 open gap, C-006 declined
6. **Self-review** (section 6): what was caught and fixed
