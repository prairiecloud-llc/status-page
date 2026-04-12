# PrairieCloud Status Page Maintenance Workflow

This document explains how to use the `prairiecloud-llc/status-page` repository as PrairieCloud's public maintenance and status publication surface.

## Public-repo rule

This repository is public. Everything committed here should be treated as public-safe.

That means this repo may contain:
- public maintenance issue structure
- public update workflow guidance
- public label conventions
- public site refresh instructions

It should not contain:
- internal-only audience details
- internal recipient lists
- private approval notes
- internal escalation notes
- internal rehearsal commentary
- sensitive operational details that are not intended for customers or the public

## Purpose

The status-page repository exists to support PrairieCloud's public status publication workflow.

For maintenance events, it should be used to:
- create public maintenance threads
- publish maintenance start updates
- publish extension updates
- publish completion updates
- rebuild the public status site on demand when needed

## Current-state note

PrairieCloud currently uses an Upptime-based status page backed by GitHub Actions and GitHub Pages.

This works well as a public status surface, but it is not a fully featured scheduled-maintenance platform. Because of that, maintenance publication currently follows a small operator workflow built around GitHub issues and manual site refresh when necessary.

## Maintenance publication workflow

### 1. Create a maintenance thread

Create a GitHub issue in this repository for the maintenance event.

Recommended title format:

`Scheduled maintenance: PrairieCloud API on 2026-04-19 08:00 CDT`

Recommended body sections:
- summary
- affected services
- maintenance window with timezone
- expected impact
- statement that updates will be posted in the same thread

### 2. Publish the initial notice

Once the issue is created:
- verify the content is correct
- use the issue URL as the canonical event link
- manually trigger a status-site refresh if faster propagation is needed

### 3. Publish start update

At maintenance start:
- add an update comment to the same thread
- state the actual start time and customer impact
- manually refresh the site if needed

### 4. Publish extension update if needed

If the work exceeds the original window:
- add an update comment immediately
- include revised expected completion time
- include current impact
- manually refresh the site if needed

### 5. Publish completion update

When the work is complete:
- add a completion update comment
- state completion time
- summarize service restoration
- close the maintenance issue so it no longer appears in the active Scheduled Maintenance section
- refresh the site so the completed event is removed from the Scheduled Maintenance section

## Manual site refresh

Use the GitHub Actions workflow:
- `Maintenance Site Refresh`

This workflow exists so operators can rebuild and deploy the public status site without waiting for the scheduled static-site run.

## Suggested labels

Recommended issue labels for maintenance threads:
- `maintenance`
- `scheduled-maintenance`

If PrairieCloud later standardizes additional labels such as extension-state markers,
this document should be updated at the same time the labels are created in GitHub.

## Operational rule

The status page is PrairieCloud's canonical public source of truth for maintenance events.
