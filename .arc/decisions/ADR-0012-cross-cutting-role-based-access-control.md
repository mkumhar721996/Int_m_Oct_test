---
id: ADR-0012
category: cross_cutting
title: 'Cross-cutting: Role-based access control'
status: accepted
superseded_by: null
component_id: null
decision: Enforced centrally in HR API using roles/claims sourced from Microsoft Entra
  ID (Azure AD); access to HR data and actions is gated by role.
evidence: "Brief: Compliance and data residency \u2014 access controlled through role-based\
  \ permissions; human's decision to use Microsoft Entra ID."
---

## Context

Brief: Compliance and data residency — access controlled through role-based permissions; human's decision to use Microsoft Entra ID.

## Decision

Enforced centrally in HR API using roles/claims sourced from Microsoft Entra ID (Azure AD); access to HR data and actions is gated by role.
