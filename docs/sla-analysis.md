# SLA Performance Analysis Report
**Project:** IT Service Desk Process Optimisation  
**Author:** Nolwazi Hlongwane  
**Period Analysed:** January 2024 — February 2024  
**Total Incidents Analysed:** 20

---

## Executive Summary

Analysis of 20 incidents logged during January 2024 reveals that 11 out of 20 tickets (55%) breached their SLA targets. The highest breach rates occur in the Network and Access categories, with root causes pointing to inadequate escalation procedures, poor onboarding processes, and reactive rather than proactive infrastructure monitoring.

This report identifies the key failure points and recommends targeted process improvements to bring SLA compliance above 90%.

---

## SLA Performance by Priority

| Priority | Total Tickets | SLA Breached | Breach Rate | SLA Target |
|---|---|---|---|---|
| Critical | 3 | 1 | 33% | 1-2 hours |
| High | 9 | 6 | 67% | 4 hours |
| Medium | 6 | 3 | 50% | 8 hours |
| Low | 3 | 2 | 67% | 24 hours |
| **Total** | **20** | **11** | **55%** | — |

---

## SLA Performance by Category

| Category | Total Tickets | SLA Breached | Breach Rate | Avg Resolution Time (hrs) |
|---|---|---|---|---|
| Network | 6 | 4 | 67% | 18.0 |
| Access | 4 | 3 | 75% | 34.8 |
| Software | 5 | 3 | 60% | 22.8 |
| Hardware | 6 | 3 | 50% | 26.3 |

---

## Key Findings

### Finding 1 — Access Management is the highest breach category (75%)
Three out of four access-related tickets breached SLA. Root cause analysis shows these delays stem from manual onboarding processes, lack of role-based access templates, and no automated provisioning. INC-009 and INC-013 both involved users waiting over 30 hours for basic access rights.

### Finding 2 — High priority tickets have a 67% breach rate
High priority tickets carry a 4-hour SLA target yet 6 out of 9 breached it. This suggests the triage process is not correctly identifying urgency at the point of logging, leading to under-resourced responses.

### Finding 3 — Network incidents take the longest to resolve on average
Average resolution time for network incidents is 18 hours against a typical 4-hour SLA target. INC-012 took 56 hours due to reliance on ISP escalation with no internal workaround in place.

### Finding 4 — Recurring issues are not being prevented
INC-003 (Teams cache), INC-014 (Outlook add-in), and INC-018 (backup storage) are all issues that could have been prevented with proactive monitoring or a known error database. These tickets consumed Tier 1 and Tier 2 time unnecessarily.

### Finding 5 — No after-hours escalation path visible
INC-016 involved a full site outage that was resolved in 3 hours but still breached its 2-hour SLA. This suggests no on-call escalation path was triggered immediately.

---

## Recommendations

| Priority | Recommendation | Expected Impact |
|---|---|---|
| 1 | Implement automated user provisioning via AD groups and role templates | Reduce access breach rate from 75% to under 20% |
| 2 | Introduce triage quality checks — supervisor reviews priority assignments | Reduce high priority breach rate from 67% to under 30% |
| 3 | Build a Known Error Database (KEDB) for recurring software issues | Reduce repeat incident resolution time by 40% |
| 4 | Implement proactive network monitoring with automated alerts | Catch network failures before user impact |
| 5 | Define and document on-call escalation path for Critical incidents | Ensure Critical SLA target of 1-2 hours is consistently met |

---

## Conclusion

The current service desk operation is reactive, manually driven, and lacking standardised processes for access management and escalation. Implementing the five recommendations above is projected to improve overall SLA compliance from 45% to above 90% within one quarter, directly improving user productivity and reducing operational risk.
