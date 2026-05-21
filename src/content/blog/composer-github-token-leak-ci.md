---
title: "Composer: Tokens Spilled on the CI Stage"
description: "TLDR and affected version summary for CVE-2026-45793, a Composer vulnerability that may expose GitHub authentication tokens in CI logs."
tags:
  - composer
  - php
  - vulnerability
  - cve
  - credentials
  - ci
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-20T00:04:00.000Z"
image: /assets/composer-github-token-leak-ci.webp
category: security
isNew: false
---

---

Source:

- [Graycore: Composer GitHub token exposure in CI](https://github.com/graycoreio/github-actions-magento2/discussions/261)

---

__tldr: CVE-2026-45793 is a vulnerability in Composer that may expose GitHub authentication tokens in CI logs. Affects all Composer versions before `2.9.8`, including `2.2.x` before `2.2.28` and `1.x` before `1.10.28`. Fixed in `2.9.8`, `2.2.28`, and `1.10.28`.__

## Affected versions

| Branch | Affected | Upgrade to |
| --- | --- | --- |
| Composer `2.3.x` – `2.9.x` | `< 2.9.8` | `2.9.8` |
| Composer `2.2.x` (LTS) | `< 2.2.28` | `2.2.28` |
| Composer `1.x` | `< 1.10.28` | `1.10.28` |

## What to do

- Upgrade Composer to the patched version for your release line.
- Audit CI logs for leaked GitHub tokens — if found, rotate them immediately.
- Review any CI pipelines that run Composer with GitHub authentication and ensure tokens are not printed to logs after upgrading.
