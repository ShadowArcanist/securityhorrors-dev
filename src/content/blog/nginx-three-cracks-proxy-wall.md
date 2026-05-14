---
title: "NGINX: Three Cracks in the Proxy Wall"
description: "TLDR and affected version summary for NGINX Rift, CVE-2026-42926, and CVE-2026-42946"
tags:
  - nginx
  - vulnerability
  - cve
  - heap-overflow
  - rce
  - http2
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-13T00:00:00.000Z"
image: /assets/nginx-three-cracks-proxy-wall.webp
category: security
isNew: true
---

---

Sources:

- [F5: CVE-2026-42945 - buffer overflow in ngx_http_rewrite_module](https://my.f5.com/manage/s/article/K000161019)
- [F5: CVE-2026-42926 - HTTP/2 request injection in ngx_http_proxy_module](https://my.f5.com/manage/s/article/K000161131)
- [F5: CVE-2026-42946 - buffer overread in scgi and uwsgi modules](https://my.f5.com/manage/s/article/K000161027)

---

__tldr: Three NGINX vulnerabilities disclosed to F5 in May 2026. CVE-2026-42945, also known as NGINX Rift, is a buffer overflow in `ngx_http_rewrite_module` that may cause worker crashes, denial of service, and in some conditions remote code execution. CVE-2026-42926 is an HTTP/2 request injection in `ngx_http_proxy_module`. CVE-2026-42946 is a buffer overread in scgi and uwsgi modules with memory disclosure risk. Fixed in NGINX 1.30.1 and 1.31.0.__

## Affected versions and systems

| CVE | Impact | Affected | Upgrade to |
| --- | --- | --- | --- |
| CVE-2026-42945 (NGINX Rift) | Buffer overflow, worker crash, DoS, potential RCE | 0.6.27–1.30.0 | 1.30.1+, 1.31.0+ |
| CVE-2026-42926 | HTTP/2 request injection, incorrect backend routing | 1.29.4–1.30.0 | 1.30.1+, 1.31.0+ |
| CVE-2026-42946 | Buffer overread, memory disclosure, worker crash | 0.8.42–1.30.0 | 1.30.1+, 1.31.0+ |

## What to do

- Upgrade NGINX to 1.30.1 or 1.31.0.
- Review F5 advisories for each CVE for environment-specific guidance.
- Verify [ASLR is enabled on systems](https://www.baeldung.com/linux/toggle-aslr-memory-randomization#disable-or-enable-aslr-globally-using-kernelrandomizevaspace) running NGINX.

