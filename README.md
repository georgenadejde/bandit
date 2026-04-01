---
title: Bandit - OverTheWire
user: h4ck47d4wn
date: 2026-03-26
description: Writeups for the Bandit wargame on OverTheWire, a beginner-friendly CTF focused on Linux command-line fundamentals and security concepts.
---
# [Bandit - OverTheWire](https://overthewire.org/wargames/bandit/)

- Bandit is a wargame on OverTheWire aimed at absolute beginners and it teaches the basics of Linux navigation, file manipulation, networking, and scripting through a series of increasingly difficult challenges.
- Each level gives you SSH credentials. The goal is always to find the password for the next level, which is stored somewhere on the system.
- The challenges introduce core tools: `find`, `grep`, `sort`, `nc`, `openssl`, `git`, `ssh`, and more.

## Levels

| Level                           | Key Concept                         |
| ------------------------------- | ----------------------------------- |
| [[bandit_8/README\|Bandit 8]]   | `sort` + `uniq`                     |
| [[bandit_9/README\|Bandit 9]]   | `strings` + `grep` on binaries      |
| [[bandit_10/README\|Bandit 10]] | Base64 decoding                     |
| [[bandit_11/README\|Bandit 11]] | ROT13 with `tr`                     |
| [[bandit_12/README\|Bandit 12]] | Layered compression + hexdump       |
| [[bandit_13/README\|Bandit 13]] | SSH private key login               |
| [[bandit_14/README\|Bandit 14]] | Netcat basics                       |
| [[bandit_15/README\|Bandit 15]] | SSL with `openssl s_client`         |
| [[bandit_16/README\|Bandit 16]] | Port scanning + SSL + RSA key       |
| [[bandit_17/README\|Bandit 17]] | `diff` between files                |
| [[bandit_18/README\|Bandit 18]] | Bypassing `.bashrc` via SSH         |
| [[bandit_19/README\|Bandit 19]] | SUID binary                         |
| [[bandit_20/README\|Bandit 20]] | SUID + netcat listener              |
| [[bandit_21/README\|Bandit 21]] | Cron job enumeration                |
| [[bandit_22/README\|Bandit 22]] | Reading + reproducing a cron script |
| [[bandit_23/README\|Bandit 23]] | Writing a cron-executed script      |
| [[bandit_24/README\|Bandit 24]] | Brute-forcing a PIN with bash       |
| [[bandit_25/README\|Bandit 25]] | Identifying a non-standard shell    |
| [[bandit_26/README\|Bandit 26]] | Escaping `more` → vim → shell       |
| [[bandit_27/README\|Bandit 27]] | `git clone`                         |
| [[bandit_28/README\|Bandit 28]] | Git commit history                  |
| [[bandit_29/README\|Bandit 29]] | Git branches                        |
| [[bandit_30/README\|Bandit 30]] | Git tags                            |
| [[bandit_31/README\|Bandit 31]] | `git push` + `.gitignore` bypass    |
| [[bandit_32/README\|Bandit 32]] | Uppercase shell escape via `$0`     |
| [[bandit_33/README\|Bandit 33]] | 🏁 Final level                      |
