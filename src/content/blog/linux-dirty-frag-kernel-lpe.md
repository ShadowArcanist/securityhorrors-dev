---
title: "Dirty Frag: Two Kernel Teeth Under the Floorboards"
description: "TLDR and affected system summary for Dirty Frag, CVE-2026-43284 and CVE-2026-43500."
tags:
  - linux
  - kernel
  - privilege-escalation
  - dirty-frag
  - cve
  - ubuntu
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-07T00:00:00.000Z"
image: /assets/linux-dirty-frag.jpg
category: security
isNew: false
---

---

Source:

- [Ubuntu: Dirty Frag Linux kernel local privilege escalation vulnerability mitigations](https://ubuntu.com/blog/dirty-frag-linux-vulnerability-fixes-available)

---

__tldr: Dirty Frag refers to two Linux kernel local privilege escalation vulnerabilities, CVE-2026-43284 and CVE-2026-43500, publicly disclosed on May 7, 2026. Ubuntu published mitigation guidance on May 8, 2026.__

## Affected versions and systems

- Affected vulnerabilities: CVE-2026-43284 and CVE-2026-43500.
- Affected components include Linux kernel modules for ESP/IPsec and RxRPC/AFS support.
- Ubuntu stated that all Ubuntu releases were affected, with other major Linux distributions also impacted depending on kernel configuration.
- Impacted environments may include Linux servers, workstations, CI runners, containers, and systems running untrusted local workloads.
- Container escape risk may exist where untrusted workloads can reach the vulnerable kernel functionality.

## What to do

- Apply fixed kernel updates from your distribution.
- If patching is delayed, follow your distribution’s module-disable mitigation guidance.
- Disable both affected areas where applicable; disabling only one may leave the other exploitable.
- Prioritize multi-tenant systems, container hosts, and exposed workload platforms.
