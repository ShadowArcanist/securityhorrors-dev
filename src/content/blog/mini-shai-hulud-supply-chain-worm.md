---
title: "Mini Shai-Hulud: The Package That Crawled Through CI"
description: "TLDR and affected package summary for the Mini Shai-Hulud npm and PyPI supply-chain campaign."
tags:
  - supply-chain
  - npm
  - pypi
  - ci
  - malware
  - tokens
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-11T00:00:00.000Z"
image: /assets/mini-shai-hulud-supply-chain-worm.jpg
category: security
isNew: false
---

---

Sources:

- [Socket: TanStack npm packages compromised in ongoing Mini Shai-Hulud supply-chain attack](https://socket.dev/blog/tanstack-npm-packages-compromised-mini-shai-hulud-supply-chain-attack)
- [Socket: Mini Shai-Hulud campaign tracker](https://socket.dev/supply-chain-attacks/mini-shai-hulud)

---

__tldr: Mini Shai-Hulud is an ongoing npm and PyPI supply-chain attack reported by Socket in May 2026. Malicious package versions attempted to steal developer and CI secrets such as GitHub tokens, npm tokens, cloud credentials, Vault tokens, and Kubernetes tokens.__

## Affected packages and apps

- Around 205 npm packages were reported affected, plus a small number of PyPI packages.
- Notable affected npm package families included TanStack packages, OpenSearch packages, and `@squawk/*` packages.
- Notable affected PyPI packages included `mistralai` and `guardrails-ai`.
- Socket reported 84 compromised TanStack npm package versions in the May 11, 2026 wave.
- Check Socket’s full compromised package list and compare against your lockfiles, CI logs, and package manager cache.

## What to do

- Remove affected versions and upgrade to clean releases.
- Rotate exposed tokens and credentials.
- Audit CI runners and developer machines that installed affected packages.
- Review GitHub Actions, npm publishing tokens, cloud credentials, Vault tokens, and Kubernetes tokens.
