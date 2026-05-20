---
title: "PostgreSQL: Eleven Stitches on a Quiet Afternoon"
description: "TLDR and affected version summary for the 11 CVEs patched in the May 14, 2026 PostgreSQL release."
tags:
  - postgresql
  - database
  - cve
  - vulnerability
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-14T00:08:00.000Z"
image: /assets/postgresql-eleven-stitches.webp
category: security
isNew: false
---

---

Sources:

- [PostgreSQL: 18.4, 17.10, 16.14, 15.18, and 14.23 released](https://www.postgresql.org/about/news/postgresql-184-1710-1614-1518-and-1423-released-3297/)
- [Christophe Pettus: Eleven CVEs walk into a release](https://thebuild.com/blog/2026/05/14/eleven-cves-walk-into-a-release/)

---

__tldr: PostgreSQL released patched versions on May 14, 2026, addressing 11 CVEs across all supported release lines. None rated critical, but four score CVSS 8.8 (High) — upgrading is strongly recommended. Fixed versions are 18.4, 17.10, 16.14, 15.18, and 14.23.__

## Affected versions

| Release line | Affected | Upgrade to |
| --- | --- | --- |
| 18.x | < 18.4 | 18.4 |
| 17.x | < 17.10 | 17.10 |
| 16.x | < 16.14 | 16.14 |
| 15.x | < 15.18 | 15.18 |
| 14.x | < 14.23 | 14.23 |

- 11 CVEs patched in total. See the [release notes](https://www.postgresql.org/about/news/postgresql-184-1710-1614-1518-and-1423-released-3297/) and [Christophe Pettus's writeup](https://thebuild.com/blog/2026/05/14/eleven-cves-walk-into-a-release/) for detailed breakdowns of each CVE.
- No critical-rated CVEs, but four score CVSS 8.8 (High) with practical exploitation paths — upgrading is strongly recommended.

## What to do

- Upgrade PostgreSQL to the patched version for your release line.
- Review the release notes for CVEs relevant to your configuration and usage patterns.
- Test upgrades in staging before applying to production, as usual with minor releases.
