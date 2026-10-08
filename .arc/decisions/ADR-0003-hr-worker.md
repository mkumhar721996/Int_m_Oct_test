---
id: ADR-0003
category: component
title: HR Worker
status: accepted
superseded_by: null
component_id: comp_hr_worker
responsibility: 'Handles asynchronous background work: sending email notifications/approval
  emails, leave and attendance reminders, and scheduled report generation.'
kind: worker
split_reason: Background async work (notification sending) has different latency/throughput
  characteristics than synchronous API request handling.
talks_to:
- component_id: comp_relational_database
  interaction: shared-storage
  evidence: HR Worker reads pending notification/report jobs and employee data from
    the same relational store.
evidence: "about.md 'Integrations' \u2014 Email service for notifications and approvals."
---

## Context

about.md 'Integrations' — Email service for notifications and approvals.

## Decision

Handles asynchronous background work: sending email notifications/approval emails, leave and attendance reminders, and scheduled report generation.

Kept separate because Background async work (notification sending) has different latency/throughput characteristics than synchronous API request handling..

## Talks to

- **Relational Database** (shared-storage) — HR Worker reads pending notification/report jobs and employee data from the same relational store.
