# Aldenbrook Pay: KYB/KYC & Sanctions Casework Register

> **Not real data.** Aldenbrook Pay is a fictional platform built to demonstrate evidence-first KYB, KYC, and sanctions/PEP/adverse-media casework.

## Primary artifact: HTML dashboard

The standalone **`index.html` file is the primary project artifact**. It contains the complete dashboard, case register, review procedures, casework summary, visual walkthroughs, and lessons learned. GitHub Pages publishes this HTML file as the live dashboard. The Excel workbook is a supporting, downloadable companion, not the primary presentation.

[![Aldenbrook Pay HTML dashboard preview](./Screenshot_Overview.png)](https://tjon-star.github.io/Aldenbrook-Pay-KYB-KYC-Sanctions-Casework-Register/)

**[Open the live HTML dashboard](https://tjon-star.github.io/Aldenbrook-Pay-KYB-KYC-Sanctions-Casework-Register/)**

[View the `index.html` source](./index.html) · [Download the supporting Excel workbook](./Aldenbrook_KYB_KYC_Casework_Register..xlsx)

**Core principle:** an unresolved screening flag is not a confirmed match; "no adverse media found" is not "confirmed clean"; and missing documentation is an open gap, not evidence of low risk.

---

## 1. Project map

The HTML dashboard is the primary presentation layer. The Excel workbook is the supporting detailed register.

```mermaid
flowchart TB
    WEB["PRIMARY: index.html<br/>HTML dashboard"]
    XLSX["SUPPORTING: Excel workbook<br/>detailed register"]
    WEB -.->|"optional download"| XLSX

    WEB --> C["Case Register section<br/>10 cases, 4 worked in detail"]
    WEB --> P["Review Procedures section"]
    WEB --> S["Casework Summary section"]

    C --> T1["Tab: Case Register"]
    C --> T2["Tab: Evidence and Screening Register"]
    P --> T3["Tab: Review Procedures"]
    S --> T6["Tab: Casework Summary"]
    T2 --> T4["Tab: Escalation and Decision Log"]

    XLSX --> T5["Tab: Legend and Instructions"]

    classDef root fill:#1f2933,stroke:#9CA0AC,color:#EDEAE2;
    classDef web fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    classDef sheet fill:#f4efe0,stroke:#C9A227,color:#0E1116;
    class WEB,XLSX root;
    class C,P,S web;
    class T1,T2,T3,T4,T5,T6 sheet;
```

---

## 2. Case portfolio (10 cases)

```mermaid
%%{init: {"theme": "base", "themeVariables": {"pie1": "#3F9C82", "pie2": "#C9A227", "pie3": "#6C8EBF", "pie4": "#C25B4A", "pie5": "#8E6FB5", "pieStrokeColor": "#0E1116", "pieOuterStrokeColor": "#0E1116"}}}%%
pie showData title Cases by status
    "Approved" : 5
    "Escalated" : 2
    "Under Review" : 1
    "Declined" : 1
    "Resolved" : 1
```

```mermaid
%%{init: {"theme": "base", "themeVariables": {"pie1": "#C9A227", "pie2": "#C25B4A", "pie3": "#3F9C82", "pieStrokeColor": "#0E1116", "pieOuterStrokeColor": "#0E1116"}}}%%
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
    A["Screening run"] --> B{"Potential match?"}
    B -- "No match as of screening date" --> PASS["Pass<br/>record date and sources"]
    B -- "Yes, including partial name match" --> D{"Disambiguation<br/>test passed?"}
    D -- "Yes" --> CLEAR["Clear as false positive<br/>C-010 J. Santos"]
    D -- "No" --> ESC["Escalate<br/>C-004 R. Osei"]

    CRIT["Test passes only if:<br/>multiple identifiers inconsistent,<br/>gap too large for data-entry error,<br/>at least one corroborated by a document"]
    RULE["Never auto-cleared or auto-declined.<br/>Never cleared on name dissimilarity alone."]
    D -.-> CRIT
    B -.-> RULE

    classDef good fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    classDef warn fill:#fbf3d6,stroke:#C9A227,color:#0E1116;
    classDef bad fill:#f8e4e0,stroke:#C25B4A,color:#0E1116;
    class PASS,CLEAR good;
    class ESC,CRIT warn;
    class RULE bad;
```

---

## 4. KYB evidence gaps (ownership and operations)

How open gaps block or drive a decision.

```mermaid
flowchart TD
    K["Client KYB case"] --> U{"UBO declaration complete?<br/>all owners identified,<br/>totals 100%, all screened"}
    U -- "No" --> GAP["Open gap, case stays open<br/>C-002 Vantage Digital Media FZE<br/>20% unattributed"]
    U -- "Yes" --> O{"Proof of operations<br/>verifiable?"}
    O -- "Yes" --> OK["Proceed to decision"]
    O -- "No" --> DEC["Declined<br/>C-006 Ferrotech Trading DMCC<br/>no operational history,<br/>2 document requests unmet"]
    DEC -.-> LINK["UBO linkage to other entities under review:<br/>elevated scrutiny, not proof of wrongdoing"]

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

### Gap 1: disambiguation criterion

```mermaid
flowchart LR
    A1["Before<br/>at least one identifier is inconsistent"] --> B1["Problem<br/>did not explain why C-010 cleared<br/>but C-004 did not"] --> C1["After<br/>weigh number of inconsistent identifiers<br/>and size of the discrepancy"]

    classDef before fill:#f8e4e0,stroke:#C25B4A,color:#0E1116;
    classDef problem fill:#fbf3d6,stroke:#C9A227,color:#0E1116;
    classDef after fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    class A1 before;
    class B1 problem;
    class C1 after;
```

### Gap 2: Ferrotech decline rationale

```mermaid
flowchart LR
    A2["Before<br/>cited UBO link to other flagged entities"] --> B2["Problem<br/>those cases were never concluded,<br/>so an unproven association read as fact"] --> C2["After<br/>linkage stated as elevated scrutiny;<br/>decline rests on operational-substance gap"]

    classDef before fill:#f8e4e0,stroke:#C25B4A,color:#0E1116;
    classDef problem fill:#fbf3d6,stroke:#C9A227,color:#0E1116;
    classDef after fill:#e8f4f0,stroke:#3F9C82,color:#0E1116;
    class A2 before;
    class B2 problem;
    class C2 after;
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
