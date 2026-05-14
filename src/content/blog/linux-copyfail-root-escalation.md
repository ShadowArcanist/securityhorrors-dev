---
title: "CopyFail: Root Was Only 732 Bytes Away"
description: "TLDR and affected system summary for CVE-2026-31431, the Linux CopyFail local privilege escalation."
tags:
  - linux
  - kernel
  - privilege-escalation
  - copyfail
  - cve
  - containers
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-04-29T00:00:00.000Z"
image: /assets/linux-copyfail-root.jpg
category: security
isNew: false
---

---

Source:

- [CopyFail: CVE-2026-31431](https://copy.fail/)

---

__tldr: CopyFail, CVE-2026-31431, is a reliable Linux local privilege escalation publicly disclosed on April 29, 2026. It affects many Linux kernels since 2017 and can allow local attackers to gain root, with container escape implications.__

## Affected versions and systems

- Affected component: Linux kernel `algif_aead` / AF_ALG-related functionality, according to the CopyFail disclosure.
- Affected systems include many Linux kernels dating back to 2017.
- Impacted environments may include servers, developer machines, CI runners, containers, and multi-tenant Linux hosts.
- Major Linux distributions may be affected depending on kernel version and configuration.
- Check the CopyFail page and your Linux distribution advisories for exact kernel package versions.

## What to do

- Patch kernels to versions containing the upstream fix.
- If patching is delayed, consider disabling the affected module where safe.
- For untrusted workloads, consider blocking AF_ALG socket creation with seccomp.
- Prioritize shared hosts, CI runners, and container platforms.
