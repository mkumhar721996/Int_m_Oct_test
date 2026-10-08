---
id: ADR-0008
category: nfr
title: "NFR: security (HR API) \u2014 Every create/update/delete on sensitive employee\
  \ data produces an audit record\u2026"
status: accepted
superseded_by: null
dimension: security
metric: audit coverage for sensitive data changes
threshold: Every create/update/delete on sensitive employee data produces an audit
  record capturing actor, timestamp, and changed fields.
component_id: comp_hr_api
needs_dedicated_tracking: true
evidence: "Brief: Compliance and data residency \u2014 basic audit and security controls\
  \ for sensitive employee data."
---

## Context

Brief: Compliance and data residency — basic audit and security controls for sensitive employee data.

## Decision

audit coverage for sensitive data changes: Every create/update/delete on sensitive employee data produces an audit record capturing actor, timestamp, and changed fields.

Applies to HR API.
