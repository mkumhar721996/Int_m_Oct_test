---
id: ADR-0004
category: component
title: Relational Database
status: accepted
superseded_by: null
component_id: comp_relational_database
responsibility: Stores employee, recruitment, leave, attendance, and audit records
  in a relational schema; runs on Azure SQL (managed).
kind: managed_service
split_reason: Relational database explicitly required by the brief for employee and
  HR records; a backing service the project uses but doesn't build.
evidence: "Brief: Hosting constraints \u2014 relational database required; human's\
  \ decision to host on Azure with Azure SQL."
---

## Context

Brief: Hosting constraints — relational database required; human's decision to host on Azure with Azure SQL.

## Decision

Stores employee, recruitment, leave, attendance, and audit records in a relational schema; runs on Azure SQL (managed).

Kept separate because Relational database explicitly required by the brief for employee and HR records; a backing service the project uses but doesn't build..
