<div align="center">

<br />

# BULWARK

**Autonomous external pentest agent.**

*Silent. Patient. Inevitable.*

<br />

[![License: BSL](https://img.shields.io/badge/License-BSL_1.1-000000.svg?style=flat-square&logoColor=white)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Private%20Beta-000000.svg?style=flat-square)](https://getwark.com)
[![Platform](https://img.shields.io/badge/Platform-macOS%20%7C%20Linux-000000.svg?style=flat-square)](https://getwark.com)
[![LLM](https://img.shields.io/badge/LLM-Claude%20%7C%20OpenAI-000000.svg?style=flat-square)](https://getwark.com)
[![Tests](https://img.shields.io/badge/Tests-1700%2B%20passing-000000.svg?style=flat-square)](https://getwark.com)
[![Audited](https://img.shields.io/badge/Security-Audited-000000.svg?style=flat-square)](https://getwark.com)

</div>

---

<div align="center">

```
Point it at an authorized target.
Walk away.
Come back to proof.
```

</div>

---

## What it does

BULWARK is a local desktop app. You give it a scope, a budget, and an authorization PDF. It spins up a hardened sandbox, verifies your exit IP, and runs a single autonomous agent loop:

```
recon → enumerate → find vulnerabilities → confirm exploits → report
```

No cloud. No frameworks. No babysitting.

---

## Proven

| Run | Result | Steps | Cost | Scope violations |
|-----|--------|-------|------|-----------------|
| HTB Easy | `user.txt` + `root.txt` | 88 | **$0.93** | 0 |
| HTB Medium | JWT `alg=none` → SSH CA abuse → root | — | — | 0 |

> In one run, the agent marked an unconfirmed command injection as `not_exploitable`  
> instead of fake-confirming it — then found a real path on its own.

---

## Architecture

```
One ReAct loop           — not a LangGraph zoo
Markdown vault           — not a graph database  
Hardened Kali sandbox    — not a mounted Docker socket
Deterministic cascades   — not LLM calls for every exploit variation
Stealth-first            — not fast and loud
Audit-logged             — not a black box
```

---

## Safety model

BULWARK treats the LLM as part of the threat model. Six layered guardrails ensure a misbehaving or jailbroken model **cannot** leave scope, leak your IP, or exceed your budget:

```
1. SCOPE GUARD        — every command verified before execution
2. EGRESS FILTER      — network drops everything except in-scope IPs
3. HARDENED CONTAINER — read-only, non-root, disposable, no Docker socket
4. AUDIT LOG          — hash-chained, tamper-evident, optionally encrypted
5. BUDGET GUARD       — hard cap checked before every LLM call
6. IP GUARD           — engagement freezes if exit IP drifts mid-session
```

**1,700+ automated tests passing. Independently code-audited.**

---

## Status

BULWARK is currently in **private beta**.

The core agent is being prepared for public release under BSL 1.1.  
Offensive plugin packs (playbooks, exploit cascades, CVE catalog) will be available separately.

**Early access → [getwark.com](https://getwark.com)**

---

## What's coming

- [ ] Public core release (BSL 1.1)
- [ ] RECON pack — external surface mapping
- [ ] BREACH pack — confirmed exploit chains  
- [ ] FULL SPECTRUM pack — complete external engagement coverage
- [ ] Documentation

---

## Legal

BULWARK is built for **authorized penetration testing only**.  
Every engagement requires an authorization PDF. Scope guard is not optional.  
Use responsibly. Know your laws.

---

<div align="center">

**[getwark.com](https://getwark.com)** · `hello@getwark.com`

*Incorporated in Switzerland*

<br />

<sub>© 2025 BULWARK — For authorized testing only.</sub>

</div>
