---
title: Bandit Level 19
user: bung3r
description: To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
tags:
  - bandit
  - overthewire
  - setuid
  - suid
  - permissions
level: 19
---
# [Bandit Level 19](https://overthewire.org/wargames/bandit/bandit19.html)

- There's a setuid binary in the home directory. A **setuid** (SUID) binary runs with the **file owner's permissions** rather than the caller's — so even though we're bandit19, the binary executes as bandit20.

- Running `./bandit20-do cat /etc/bandit_pass/bandit20` lets us read the password file that would normally be off-limits.
	- The binary basically gives us a one-shot privilege escalation — we can only run commands as bandit20 through it, not get a full shell.

![](b19_1.png)

### Password

`IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x`
