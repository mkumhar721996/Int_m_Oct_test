---
id: ADR-0001
category: component
title: Web App
status: accepted
superseded_by: null
component_id: comp_web_app
responsibility: Web interface for employees, managers, and HR staff covering employee
  management, recruitment tracking, leave requests, attendance, and HR dashboards/reporting.
kind: web_ui
split_reason: Single web client for all user roles described in the brief; one web
  UI per client is the start-small default.
talks_to:
- component_id: comp_hr_api
  interaction: sync
  evidence: "Brief: What it is \u2014 single web app for employees, managers, HR staff\
    \ calling the backend."
evidence: "about.md 'What it is' \u2014 web-based HR Management System for HR teams,\
  \ managers, and employees."
---

## Context

about.md 'What it is' — web-based HR Management System for HR teams, managers, and employees.

## Decision

Web interface for employees, managers, and HR staff covering employee management, recruitment tracking, leave requests, attendance, and HR dashboards/reporting.

Kept separate because Single web client for all user roles described in the brief; one web UI per client is the start-small default..

## Talks to

- **HR API** (sync) — Brief: What it is — single web app for employees, managers, HR staff calling the backend.
