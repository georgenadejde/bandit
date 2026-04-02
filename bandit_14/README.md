---
title: Bandit Level 14
user: bung3r
description: The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
tags:
  - bandit
  - overthewire
  - netcat
  - nc
  - networking
level: 14
---
# [Bandit Level 14](https://overthewire.org/wargames/bandit/bandit14.html)

- The password for bandit15 is retrieved by submitting bandit14's password to a service running on **port 30000** of localhost.

- `echo "4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e" | nc localhost 30000` sends the password to the service.
	- `nc` (netcat) is essentially a raw TCP client which connects to a host and port and lets you send/receive data.
	- The service validates the password and responds with the next one.

### Password

`4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`
