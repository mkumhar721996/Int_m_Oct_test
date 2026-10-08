---
id: ADR-0013
category: cross_cutting
title: 'Cross-cutting: Audit logging'
status: accepted
superseded_by: null
component_id: null
decision: HR API writes an audit trail (actor, timestamp, before/after values) for
  all changes to sensitive employee records, stored in the Relational Database.
evidence: "Brief: Compliance and data residency \u2014 basic audit and security controls\
  \ should be implemented for sensitive employee data."
---

## Context

Brief: Compliance and data residency — basic audit and security controls should be implemented for sensitive employee data.

## Decision

HR API writes an audit trail (actor, timestamp, before/after values) for all changes to sensitive employee records, stored in the Relational Database.
