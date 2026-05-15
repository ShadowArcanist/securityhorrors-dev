---
title: "Shadow Supply: The Package That Stole Your Secrets"
description: "TLDR and affected version summary for the node-ipc npm supply-chain compromise."
tags:
  - npm
  - supply-chain
  - node-ipc
  - malware
  - credentials
author: Andras Bacsai
authorTwitter: heyandras
date: "2026-05-14T00:00:00.000Z"
image: /assets/node-ipc-shadow-supply-credential-stealer.webp
category: security
isNew: false
---

---

Source:

- [Socket: node-ipc package compromised](https://socket.dev/blog/node-ipc-package-compromised)

---

__tldr: The popular `node-ipc` npm package was compromised after a maintainer account was taken over, allowing attackers to publish malicious versions containing a credential stealer. Affected versions are `9.1.6`, `9.2.3`, and `12.0.1`.__

## Affected versions

- Affected package: `node-ipc` on npm.
- Malicious versions: `9.1.6`, `9.2.3`, `12.0.1`.
- Any version prior to the affected versions is safe.
- Downstream projects depending on affected versions may have pulled the compromised code into builds and CI pipelines.

## What to do

- Check your lockfiles for `node-ipc` versions `9.1.6`, `9.2.3`, or `12.0.1` and remove them immediately.
- Upgrade to a known clean version or pin to a version before the compromise.
- Rotate credentials and tokens on any machine or CI runner that installed an affected version.
- Audit build logs and dependency caches for signs of the credential stealer payload.
