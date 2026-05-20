---
title: "Nx Console: One Stolen Token, One Poisoned Marketplace"
description: "TLDR and affected version summary for the Nx Console VS Code extension compromise via a contributor's leaked GitHub PAT."
tags:
  - vscode
  - supply-chain
  - malware
  - extension
  - credentials
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-19T00:04:00.000Z"
image: /assets/nx-console-marketplace-compromise.webp
category: security
isNew: false
---

---

Source:

- [StepSecurity: Nx Console VS Code extension compromised](https://www.stepsecurity.io/blog/nx-console-vs-code-extension-compromised)

---

__tldr: A contributor's GitHub Personal Access Token was compromised, allowing attackers to publish a malicious version of the Nx Console VS Code extension (`nrwl.angular-console`) to the VS Code Marketplace. Version `18.95.0` is the affected release — all prior versions are safe, and OpenVSX was not affected.__

## Affected versions

- **Affected:** `nrwl.angular-console` version `18.95.0` on the VS Code Marketplace.
- **Safe:** All versions before `18.95.0` and OpenVSX is not affected

## What to do

- Check if you have `nrwl.angular-console` version `18.95.0` installed and remove or downgrade it immediately.
- If you installed the affected version, treat your machine as potentially compromised — audit running processes and rotate credentials.
- Review the [StepSecurity writeup](https://www.stepsecurity.io/blog/nx-console-vs-code-extension-compromised) for full details on the attack chain.

