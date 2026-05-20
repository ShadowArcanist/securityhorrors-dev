---
title: "Mini Shai-Hulud: 639 Packages Deep and Still Burrowing"
description: "TLDR and affected package summary for the latest wave of the Mini Shai-Hulud npm supply-chain campaign targeting antv and echarts-for-react."
tags:
  - supply-chain
  - npm
  - malware
  - tokens
  - credentials
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-19T00:08:00.000Z"
image: /assets/mini-shai-hulud-antv-wave.webp
category: security
isNew: true
---

---

Sources:

- [Socket: AntV packages compromised in Mini Shai-Hulud supply-chain attack](https://socket.dev/blog/antv-packages-compromised)

---

__tldr: The Mini Shai-Hulud supply-chain campaign is back with another wave. Around 639 npm packages are now confirmed compromised, including over 275 packages in the `antv` family and `echarts-for-react`. Same worm, bigger reach — check your lockfiles.__

## Affected packages

- Around **639 npm packages** are affected in this wave.
- Notable affected package families include **antv** (over 275 packages) and **echarts-for-react**.
- This is a continuation of the [same campaign that hit TanStack and other packages](/all/mini-shai-hulud-supply-chain-worm) earlier in May 2026.
- Socket maintains a [full list of affected packages](https://socket.dev/blog/antv-packages-compromised#Affected-Packages) for this wave.

## What to do

- Check your lockfiles and dependency trees against the [full affected package list](https://socket.dev/blog/antv-packages-compromised#Affected-Packages).
- Review Socket's [Indicators of Compromise](https://socket.dev/blog/antv-packages-compromised#Indicators-of-Compromise) to determine if your environments were hit.
- Remove affected versions and upgrade to clean releases.
- Rotate tokens and credentials on any machine or CI runner that installed an affected package.
- Audit GitHub tokens, npm publishing tokens, cloud credentials, and other secrets as in the previous wave.
