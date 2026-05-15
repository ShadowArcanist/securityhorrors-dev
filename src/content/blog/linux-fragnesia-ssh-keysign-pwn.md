---
title: "Fragnesia and ssh-keysign-pwn: Two More Bones Under the Kernel"
description: "TLDR and affected system summary for Fragnesia (CVE-2026-46300) and ssh-keysign-pwn (CVE-2026-46333)."
tags:
  - linux
  - kernel
  - privilege-escalation
  - cve
  - fragnesia
  - ssh
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-14T00:01:00.000Z"
image: /assets/linux-fragnesia-ssh-keysign-pwn.jpg
category: security
isNew: false
---

---

Sources:

- [Tenable: Fragnesia CVE-2026-46300](https://www.tenable.com/blog/fragnesia-cve-2026-46300-faq-about-new-linux-kernel-xfrm-esp-in-tcp-priv-esc)
- [ssh-keysign-pwn writeup](https://needhelp.icu/blogs/ssh-keysign-pwn)
- [ssh-keysign-pwn public PoC](https://github.com/0xdeadbeefnetwork/ssh-keysign-pwn)

---

__tldr: Two more Linux kernel vulnerabilities disclosed in May 2026. Fragnesia (CVE-2026-46300) is a local privilege escalation similar to Dirty Frag, affecting the same xfrm/ESP-in-TCP kernel paths. ssh-keysign-pwn (CVE-2026-46333) is a six-year-old logic bug that lets unprivileged users read root-owned files, fixed on May 14, 2026 in commit `31e62c2ebbfd`. A public PoC exists for ssh-keysign-pwn.__

## Affected versions and systems

| CVE | Impact | Affected | Fixed |
| --- | --- | --- | --- |
| CVE-2026-46300 (Fragnesia) | Local privilege escalation | Same kernel versions as Dirty Frag; any distro without the May 13 patch | Apply the May 13 Dirty Frag patch |
| CVE-2026-46333 (ssh-keysign-pwn) | Read root-owned files as unprivileged user | Most Linux kernels built before May 14, 2026 | Kernel commit `31e62c2ebbfd` |

- Fragnesia shares the Dirty Frag attack surface. If your kernel is already patched for Dirty Frag, you are covered.
- ssh-keysign-pwn has a public PoC and has been exploitable for six years. Treat it as actively exploitable.

## What to do

- Apply the latest kernel updates from your distribution covering both CVEs.
- For Fragnesia, verify the May 13 Dirty Frag mitigation is in place; it addresses this variant.
- For ssh-keysign-pwn, prioritize patching on multi-user and multi-tenant systems where unprivileged users can run code.
- Audit systems for unauthorized reads of sensitive root-owned files.
