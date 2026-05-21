---
title: "NGINX njs: One Overflow to Crash Them All"
description: "TLDR and affected version summary for CVE-2026-8711, a heap buffer overflow in NGINX JavaScript (njs) that can crash workers and may allow RCE."
tags:
  - nginx
  - njs
  - vulnerability
  - cve
  - heap-overflow
  - rce
  - dos
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-20T00:00:00.000Z"
image: /assets/nginx-njs-heap-overflow-crash.webp
category: security
isNew: false
---

---

Source:

- [F5: CVE-2026-8711 - heap buffer overflow in ngx_http_js_module](https://my.f5.com/manage/s/article/K000161307)

---

__tldr: CVE-2026-8711 is a heap buffer overflow in NGINX JavaScript (njs) via `ngx_http_js_module`. It can crash workers and cause denial of service, and in some conditions may allow remote code execution. Similar in nature to the earlier [CVE-2026-42945 (NGINX Rift)](/all/nginx-three-cracks-proxy-wall). Fixed in njs `0.9.9`.__

## Affected versions

| Component | Affected | Upgrade to |
| --- | --- | --- |
| NGINX JavaScript (njs) | `0.9.4` – `0.9.8` | `0.9.9` |

## What to do

- Upgrade NGINX JavaScript (njs) to `0.9.9`.
- Review the [F5 advisory](https://my.f5.com/manage/s/article/K000161307) for environment-specific guidance.
- If you run `ngx_http_js_module` in production, audit your configuration and monitor worker stability after upgrading.
