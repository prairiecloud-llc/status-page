# PrairieCloud First Dry-Run Plan

## Proposed dry-run event
- **Title:** PrairieCloud planned maintenance dry run
- **Date:** Saturday, April 18, 2026
- **Window:** 8:00 AM to 9:00 AM CDT
- **Audience:** internal only
- **Goal:** validate the end-to-end maintenance communications and operating process

## Objectives
- validate issue-based maintenance publishing in the `status-page` repo
- validate the manual `Maintenance Site Refresh` workflow
- validate internal-only Resend maintenance emails
- validate start/update/complete operator flow
- capture screenshots and notes

## Recommended steps
1. create the maintenance issue using the Scheduled maintenance issue template
2. trigger `Maintenance Site Refresh`
3. verify the public status site rendering
4. send the internal-only reminder email
5. post the start update at the scheduled time
6. optionally simulate an extension update
7. post the completion update
8. trigger `Maintenance Site Refresh` after meaningful updates if needed
9. document what was awkward or unclear

## Success criteria
- operators can complete the flow without improvisation
- maintenance thread/update model is understandable
- emails are clear and professional
- no hidden tooling gaps remain
