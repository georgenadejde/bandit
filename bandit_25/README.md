---
title: Bandit Level 25
user: bung3r
description: Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.
tags:
  - bandit
  - overthewire
  - ssh
  - privatekey
  - shell
  - etcpasswd
---
# [Bandit Level 25](https://overthewire.org/wargames/bandit/bandit25.html)

- The home directory contains an SSH key for bandit26. 
	-  SSHing in with it drops you right back out

- You can look at `/etc/passwd` to see what shell bandit26 is assigned: `grep bandit26 /etc/passwd`.
	- This reveals the non-standard shell binary it uses.
	- Reading that binary shows it runs `more` on a text file and then exits 
		- which is what you need to know going into level 26.

### Password

`uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG`
