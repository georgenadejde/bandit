---
title: Bandit Level 20
user: bung3r
description: "There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21)."
tags:
  - bandit
  - overthewire
  - setuid
  - suid
  - nc
  - networking
level: 20
---
# [Bandit Level 20](https://overthewire.org/wargames/bandit/bandit20.html)

- There's a setuid binary called `suconnect` in the home directory. It connects to a port on localhost, reads one line of input, and if it matches the current level's password it returns the next one.

- The trick here is that **we need to be the one listening**. We set up a `nc` listener in the background that serves the current password, then run the binary pointing at our listener port.
	- `echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -lp 1234 &` starts a listener in the background (`&`) that will send the password to whoever connects.
	- Then `./suconnect 1234` connects to our listener, reads the password, validates it, and sends back the next one.

![](b20_1.png)

### Password

`GbKksEFF4yrVs6il55v6gwY5aVje5f0j`
