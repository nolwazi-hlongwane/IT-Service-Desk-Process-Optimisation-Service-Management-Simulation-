# Current State Workflow — Before Optimisation

> This diagram represents the existing IT service desk process.
> Key problems are annotated inline.

## Incident Ticket Lifecycle — Current State

```mermaid
flowchart TD
    A[User Experiences Issue] --> B[User Calls Help Desk or Sends Email]
    B --> C[Tier 1 Agent Manually Logs Ticket]
    C --> D{Agent Assesses Priority}
    D -->|Often incorrect| E[Priority Assigned Manually]
    E --> F{Can Tier 1 Resolve?}
    F -->|Yes| G[Tier 1 Attempts Resolution]
    F -->|No| H[Manual Email Escalation to Tier 2]
    H -->|No SLA tracking| I[Tier 2 Picks Up When Available]
    I --> J{Can Tier 2 Resolve?}
    J -->|Yes| K[Tier 2 Resolves Issue]
    J -->|No| L[Manual Email Escalation to Tier 3]
    L -->|Delay — no visibility| M[Tier 3 Picks Up When Available]
    M --> N[Tier 3 Resolves Issue]
    G --> O[Agent Calls User to Confirm]
    K --> O
    N --> O
    O -->|Manual update| P[Agent Manually Closes Ticket]
    P -->|No documentation| Q[No Knowledge Base Updated]
    Q --> R[Same Issue Recurs Next Month]

    style D fill:#ff6b6b,color:#fff
    style H fill:#ff6b6b,color:#fff
    style L fill:#ff6b6b,color:#fff
    style Q fill:#ff6b6b,color:#fff
    style R fill:#ff6b6b,color:#fff
    style I fill:#ffa94d,color:#fff
    style M fill:#ffa94d,color:#fff
```

## Key Problems Identified

| Problem | Impact |
|---|---|
| Manual priority assignment with no standard criteria | High priority tickets misclassified — SLA breached |
| Escalation via email only — no tracking | Tickets lost or delayed between tiers |
| No SLA visibility during ticket lifecycle | Agents unaware when SLA is about to breach |
| No Known Error Database | Same issues resolved repeatedly from scratch |
| Manual ticket closure process | Tickets left open — inaccurate reporting |
| No user self-service option | All issues routed through Tier 1 regardless of complexity |
