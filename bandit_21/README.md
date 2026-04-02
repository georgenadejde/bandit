---
title: Bandit Level 21
user: bung3r
description: A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed
tags:
  - bandit
  - overthewire
  - cron
  - cronjob
  - bash
  - scripting
level: 21
---
# [Bandit Level 21](https://overthewire.org/wargames/bandit/bandit21.html)

- There's a cron job that runs periodically as **bandit22**. Cron job configs live in `/etc/cron.d/` 
	- checking that directory reveals which script is being run.

- Read the script at the path shown in `/etc/cron.d/cronjob_bandit22`.
	- The script writes the bandit22 password to a file in `/tmp` with a predictable filename.
	- `cat` that file directly to get the password.

### Password

`gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr`
