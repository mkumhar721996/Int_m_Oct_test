---
id: ADR-0002
category: component
title: HR API
status: accepted
superseded_by: null
component_id: comp_hr_api
responsibility: Backend implementing employee management, recruitment tracking, leave
  management, attendance tracking, and HR dashboard/reporting logic; enforces role-based
  access control against roles sourced from the corporate identity provider.
kind: api_service
split_reason: "Single backend for a single web client at this scale (100\u20131,000\
  \ employees, 100+ concurrent users) \u2014 one API per start-small guidance; no\
  \ domain split or gateway/BFF justified yet. Confirmed: Web App calls HR API directly,\
  \ no gateway."
talks_to:
- component_id: comp_relational_database
  interaction: shared-storage
  evidence: "Brief: Hosting constraints \u2014 relational database required for employee\
    \ and HR records."
- component_id: comp_hr_worker
  interaction: async
  evidence: "Brief: Integrations \u2014 email notifications/approvals are triggered\
    \ by HR API actions but sent asynchronously."
evidence: "Brief: Buy vs build \u2014 Built; Expected scale; Compliance and data residency\
  \ (RBAC). Human's decision: single API, no gateway."
---

## Context

Brief: Buy vs build — Built; Expected scale; Compliance and data residency (RBAC). Human's decision: single API, no gateway.

## Decision

Backend implementing employee management, recruitment tracking, leave management, attendance tracking, and HR dashboard/reporting logic; enforces role-based access control against roles sourced from the corporate identity provider.

Kept separate because Single backend for a single web client at this scale (100–1,000 employees, 100+ concurrent users) — one API per start-small guidance; no domain split or gateway/BFF justified yet. Confirmed: Web App calls HR API directly, no gateway..

## Talks to

- **Relational Database** (shared-storage) — Brief: Hosting constraints — relational database required for employee and HR records.
- **HR Worker** (async) — Brief: Integrations — email notifications/approvals are triggered by HR API actions but sent asynchronously.
