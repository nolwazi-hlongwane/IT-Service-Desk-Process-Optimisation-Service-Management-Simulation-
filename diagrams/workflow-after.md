# Future State Workflow — After Optimisation

> This diagram represents the improved IT service desk process.
> Key improvements are annotated inline.

## Incident Ticket Lifecycle — Future State

```mermaid
flowchart TD
    A[User Experiences Issue] --> B{Self-Service Portal Available?}
    B -->|Simple issue| C[User Resolves via Self-Service Knowledge Base]
    B -->|Complex issue| D[User Logs Ticket via Portal with Category Template]
    D --> E[System Auto-Assigns Priority Based on Category Rules]
    E --> F[SLA Timer Starts Automatically]
    F --> G{Tier 1 Assigned Within 15 Minutes}
    G --> H[Tier 1 Checks Known Error Database KEDB]
    H -->|Known fix exists| I[Tier 1 Applies Fix — Resolves Quickly]
    H -->|Unknown issue| J{Can Tier 1 Resolve Within SLA?}
    J -->|Yes| I
    J -->|No — 50% SLA elapsed| K[Automatic Escalation Alert Triggered]
    K --> L[Tier 2 Assigned Automatically — SLA Clock Visible]
    L --> M{Can Tier 2 Resolve?}
    M -->|Yes| N[Tier 2 Resolves Issue]
    M -->|No — 75% SLA elapsed| O[Automatic Escalation to Tier 3]
    O --> P[Tier 3 Resolves Issue]
    I --> Q[Automated Resolution Notification Sent to User]
    N --> Q
    P --> Q
    Q --> R[User Confirms Resolution via Portal]
    R --> S[Ticket Auto-Closed After Confirmation]
    S --> T[Resolution Added to Knowledge Base]
    T --> U[Monthly SLA Report Auto-Generated]

    style E fill:#51cf66,color:#fff
    style F fill:#51cf66,color:#fff
    style K fill:#51cf66,color:#fff
    style L fill:#51cf66,color:#fff
    style O fill:#51cf66,color:#fff
    style T fill:#51cf66,color:#fff
    style U fill:#51cf66,color:#fff
    style C fill:#74c0fc,color:#fff
    style H fill:#74c0fc,color:#fff
```

## Key Improvements Implemented

| Improvement | Problem Solved | Expected Outcome |
|---|---|---|
| Self-service knowledge base portal | Reduces Tier 1 volume by handling simple issues | 25% reduction in ticket volume |
| Automated priority assignment via category rules | Eliminates manual misclassification | High priority breach rate drops from 67% to under 30% |
| SLA timer starts at ticket creation | No SLA visibility in current state | Agents always aware of time remaining |
| Automatic escalation at 50% SLA elapsed | Email escalation caused delays and lost tickets | Escalation time reduced from hours to minutes |
| Known Error Database integrated at Tier 1 | Recurring issues solved from scratch each time | Repeat incident resolution time reduced by 40% |
| Automated user provisioning via AD role templates | Access tickets taking 30+ hours | Access ticket resolution under 2 hours |
| Auto-generated monthly SLA reports | No reporting visibility in current state | Management has real-time performance data |
