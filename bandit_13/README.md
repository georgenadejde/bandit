---
title: Bandit Level 13
user: bung3r
description: The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.
tags:
  - bandit
  - overthewire
  - ssh
  - privatekey
---
# [Bandit Level 13](https://overthewire.org/wargames/bandit/bandit13.html)

- There's no password to find here 
	- the home directory contains a private SSH key (`sshkey.private`) that you use to log directly into bandit14.

- `ssh -i sshkey.private bandit14@localhost -p 2220` connects using the key instead of a password.
	- The `-i` flag specifies the identity file (private key) to use for authentication.
	- Once in as bandit14, you can `cat /etc/bandit_pass/bandit14` to get the actual password for the next challenge.

### Password

`8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL`
