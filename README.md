# PrairieCloud Status Page

[![Uptime CI](https://github.com/prairiecloud-llc/status-page/workflows/Uptime%20CI/badge.svg)](https://github.com/prairiecloud-llc/status-page/actions?query=workflow%3A%22Uptime+CI%22)
[![Response Time CI](https://github.com/prairiecloud-llc/status-page/workflows/Response%20Time%20CI/badge.svg)](https://github.com/prairiecloud-llc/status-page/actions?query=workflow%3A%22Response+Time+CI%22)

**Live at:** [status.prairiecloud.io](https://status.prairiecloud.io)

Powered by [Upptime](https://upptime.js.org).

## Current Monitors

| Service | URL |
| ------- | --- |
| API | `https://api.prairiecloud.io/health` |
| Docs | `https://docs.prairiecloud.io` |
| Dashboard | `https://dashboard.prairiecloud.io` |

Checks run every 5 minutes via GitHub Actions. Status page is hosted on GitHub Pages.

## Planned Maintenance Operations

This repo is also PrairieCloud's current public status surface for planned maintenance communications.

See:
- `docs/maintenance-workflow.md`

That workflow documents how to:
- create a maintenance thread
- publish updates during a maintenance window
- trigger a manual site refresh when needed

## Repo Notes

Configuration is in:
- `.upptimerc.yml`

Main workflows:
- `.github/workflows/uptime.yml`
- `.github/workflows/response-time.yml`
- `.github/workflows/graphs.yml`
- `.github/workflows/summary.yml`
- `.github/workflows/static-site.yml`
- `.github/workflows/maintenance-site-refresh.yml`

## DNS Required

Cloudflare should include:
- **Type:** CNAME
- **Name:** `status`
- **Target:** `prairiecloud-llc.github.io`

## GitHub Pages

GitHub Pages should publish from the `gh-pages` branch.

## License

Powered by [Upptime](https://github.com/upptime/upptime) (MIT).
