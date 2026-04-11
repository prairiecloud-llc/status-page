# PrairieCloud Status Page Maintenance Workflow

This document describes how to use the `prairiecloud-llc/status-page` repository as PrairieCloud's **current public planned-maintenance surface**.

## Purpose

Until PrairieCloud adopts a more maintenance-aware status platform, this repo should be used to:
- publish planned maintenance notices
- publish maintenance start updates
- publish extension updates
- publish completion updates
- rebuild the status site on demand when a maintenance update should appear quickly

## Important current-state note

Upptime is strong for uptime monitoring and incident visibility, but it is not a polished first-class scheduled-maintenance system in this setup.

Because of that:
- maintenance publishing should follow a repeatable operator workflow
- the public rendering behavior should be validated with a dry run before first customer-facing use

## Recommended workflow

### 1. Create a maintenance thread
Create a GitHub issue in this repo for the maintenance event.

Recommended title format:
- `Scheduled maintenance: PrairieCloud API on 2026-04-19 08:00 CDT`

Recommended body sections:
- summary
- affected services
- maintenance window with timezone
- expected impact
- statement that updates will be posted in the same thread

### 2. Publish the initial notice
Once the issue is created:
- verify the content is correct
- use the issue URL in customer email notifications
- manually trigger a status-site refresh if faster public propagation is needed

### 3. Publish start update
At maintenance start:
- add an update comment to the same thread
- state the actual start time and impact
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
- refresh the site if needed

## Manual site refresh

Use the GitHub Actions workflow:
- `Maintenance Site Refresh`

This workflow exists so operators can rebuild/deploy the public status site without waiting for the scheduled static-site run.

## Suggested labels

Recommended issue labels for maintenance threads:
- `maintenance`
- `scheduled-maintenance`
- `customer-visible`
- `extended` (only when applicable)

## Dry run recommendation

Before the first real customer-facing maintenance event:
1. create a fake maintenance issue
2. trigger a site refresh
3. verify public rendering
4. add a start update
5. trigger another refresh
6. add a completion update
7. verify the final public result

## Operational rule

The status page is the canonical public source of truth for PrairieCloud maintenance events.
