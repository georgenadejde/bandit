Just drop Files/ from every path:
markdown---
title: Bandit - OverTheWire
user: h4ck47d4wn
date: 2026-03-26
description: Writeups for the Bandit wargame on OverTheWire — a beginner-friendly CTF focused on Linux command-line fundamentals and security concepts.
tags:
  - bandit
  - overthewire
  - ctf
  - linux
  - wargame
  - ssh
  - git
  - ssl
  - scripting
  - bruteforce
  - compression
  - encoding
---
# [Bandit - OverTheWire](https://overthewire.org/wargames/bandit/)

#bandit #overthewire #ctf #linux #wargame

- Bandit is a wargame on OverTheWire aimed at absolute beginners — it teaches the basics of Linux navigation, file manipulation, networking, and scripting through a series of increasingly tricky challenges.
- Each level gives you SSH credentials. The goal is always to find the password for the next level, which is stored somewhere on the system.
- The challenges introduce core tools: `find`, `grep`, `sort`, `nc`, `openssl`, `git`, `ssh`, and more — building up practical command-line intuition level by level.

## Levels

| Level | Key Concept |
|-------|-------------|
| [Bandit 8](bandit_8/README.md) | `sort` + `uniq` |
| [Bandit 9](bandit_9/README.md) | `strings` + `grep` on binaries |
| [Bandit 10](bandit_10/README.md) | Base64 decoding |
| [Bandit 11](bandit_11/README.md) | ROT13 with `tr` |
| [Bandit 12](bandit_12/README.md) | Layered compression + hexdump |
| [Bandit 13](bandit_13/README.md) | SSH private key login |
| [Bandit 14](bandit_14/README.md) | Netcat basics |
| [Bandit 15](bandit_15/README.md) | SSL with `openssl s_client` |
| [Bandit 16](bandit_16/README.md) | Port scanning + SSL + RSA key |
| [Bandit 17](bandit_17/README.md) | `diff` between files |
| [Bandit 18](bandit_18/README.md) | Bypassing `.bashrc` via SSH |
| [Bandit 19](bandit_19/README.md) | SUID binary |
| [Bandit 20](bandit_20/README.md) | SUID + netcat listener |
| [Bandit 21](bandit_21/README.md) | Cron job enumeration |
| [Bandit 22](bandit_22/README.md) | Reading + reproducing a cron script |
| [Bandit 23](bandit_23/README.md) | Writing a cron-executed script |
| [Bandit 24](bandit_24/README.md) | Brute-forcing a PIN with bash |
| [Bandit 25](bandit_25/README.md) | Identifying a non-standard shell |
| [Bandit 26](bandit_26/README.md) | Escaping `more` → vim → shell |
| [Bandit 27](bandit_27/README.md) | `git clone` |
| [Bandit 28](bandit_28/README.md) | Git commit history |
| [Bandit 29](bandit_29/README.md) | Git branches |
| [Bandit 30](bandit_30/README.md) | Git tags |
| [Bandit 31](bandit_31/README.md) | `git push` + `.gitignore` bypass |
| [Bandit 32](bandit_32/README.md) | Uppercase shell escape via `$0` |
| [Bandit 33](bandit_33/README.md) | 🏁 Final level |
