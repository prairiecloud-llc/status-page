# PrairieCloud Status Page

[![Uptime CI](https://github.com/prairiecloud-llc/status-page/workflows/Uptime%20CI/badge.svg)](https://github.com/prairiecloud-llc/status-page/actions?query=workflow%3A%22Uptime+CI%22)
[![Response Time CI](https://github.com/prairiecloud-llc/status-page/workflows/Response%20Time%20CI/badge.svg)](https://github.com/prairiecloud-llc/status-page/actions?query=workflow%3A%22Response+Time+CI%22)

**Live at:** [status.prairiecloud.io](https://status.prairiecloud.io)

Powered by [Upptime](https://upptime.js.org). Monitors:

| Service | URL |
|---------|-----|
| API | `api.prairiecloud.io/health` |
| Documentation | `docs.prairiecloud.io` |
| Dashboard | `dashboard.prairiecloud.io` |
| Website | `prairiecloud.io` |

Checks run every 5 minutes via GitHub Actions. Status page hosted on GitHub Pages.

## Setup

This repo is fully automated by Upptime. Configuration is in `.upptime.yml`.

### DNS Required

Add a CNAME record in Cloudflare:
- **Type:** CNAME
- **Name:** status
- **Target:** prairiecloud-llc.github.io

### GitHub Pages

Enable GitHub Pages in Settings → Pages → Source: `gh-pages` branch.

## License

Powered by [Upptime](https://github.com/upptime/upptime) (MIT).
