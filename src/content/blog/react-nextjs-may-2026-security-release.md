---
title: "React and Next.js: Thirteen Doors Left Open"
description: "TLDR and affected version summary for the May 2026 React and Next.js security advisories."
tags:
  - react
  - nextjs
  - vercel
  - vulnerability
  - ssrf
  - xss
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-07T00:01:00.000Z"
image: /assets/react-nextjs-thirteen-doors.jpg
category: security
isNew: false
---

---

Sources:

- [Vercel: Next.js May 2026 security release](https://vercel.com/changelog/next-js-may-2026-security-release)
- [React advisory GHSA-rv78-f8rc-xrxh](https://github.com/facebook/react/security/advisories/GHSA-rv78-f8rc-xrxh)

---

__tldr: On May 7, 2026, Vercel released patched Next.js versions for 13 security advisories. Issues included denial of service, middleware and proxy bypass, SSRF, cache poisoning, and XSS. One related upstream React Server Components DoS advisory was published on May 6, 2026.__

## Affected versions and apps

| Package | Affected | Upgrade to |
| --- | --- | --- |
| Next.js `13.x`, `14.x` | All versions | `15.5.18` or `16.2.6` |
| Next.js `15.x` | `<= 15.5.17` | `15.5.18` |
| Next.js `16.x` | `<= 16.2.5` | `16.2.6` |
| `react-server-dom-*` `19.0.x` | `<= 19.0.5` | `19.0.6` |
| `react-server-dom-*` `19.1.x` | `<= 19.1.6` | `19.1.7` |
| `react-server-dom-*` `19.2.x` | `<= 19.2.5` | `19.2.6` |

- Risk areas include apps relying on middleware/proxy behavior for access control, server-side fetch behavior, caching, and React Server Components.
- Check your installed `next`, `react`, and `react-server-dom-*` versions against the official advisories.

## What to do

- Upgrade Next.js to the patched version for your release line.
- Upgrade affected React Server Components packages.
- Review middleware/proxy authorization assumptions.
- Re-test SSRF protections, cache behavior, and XSS-sensitive rendering paths.
