---
title: "VoidStealer: Reaching Past Chrome's Encryption"
description: "TLDR and details on VoidStealer, an infostealer bypassing Chrome's App-Bound Encryption to extract credentials and session data."
tags:
  - chrome
  - malware
  - infostealer
  - credentials
  - windows
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-19T00:00:00.000Z"
image: /assets/chrome-voidstealer-abe-bypass.webp
category: security
isNew: false
---

---

Source:

- [Kaspersky: Chrome App-Bound Encryption bypass — VoidStealer](https://www.kaspersky.com/blog/chrome-application-bound-encryption-bypass-voidstealer/55735/)

---

__tldr: An infostealer called VoidStealer is targeting Chromium-based browsers on Windows, using a debugger-based technique to bypass Chrome's App-Bound Encryption (ABE). It extracts cookies, saved passwords, and session tokens directly from Chrome process memory. No confirmed patch exists at this time.__

## What is happening

- VoidStealer uses a debugger-based technique to attach to Chrome processes and read encrypted data directly from memory, bypassing App-Bound Encryption (ABE) introduced in Chrome 127+.
- It extracts cookies, saved passwords, and session tokens.
- First discovered around late 2025, it adopted a new ABE bypass technique in early May 2026 that is now being covered across multiple security blogs.
- Current reports focus on Chromium-based browsers on Windows — it is unclear whether other platforms are affected.

## Affected versions

- Affects Chromium-based browsers on Windows using App-Bound Encryption (Chrome 127+).

## What to do

- No need to panic — this is an awareness, not a zero-click exploit.
- Be cautious with software downloads and avoid running untrusted executables.
- Monitor for updates from Google on ABE hardening against debugger-based extraction.
- Consider using hardware security keys or passkeys for high-value accounts to reduce reliance on browser-stored credentials.
- Review the [Kaspersky writeup](https://www.kaspersky.com/blog/chrome-application-bound-encryption-bypass-voidstealer/55735/) for technical details and IOCs.
