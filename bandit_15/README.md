---
title: Bandit Level 15
user: bung3r
description: The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.
tags:
  - bandit
  - overthewire
  - ssl
  - tls
  - openssl
  - netcat
level: 15
---
# [Bandit Level 15](https://overthewire.org/wargames/bandit/bandit15.html)

- The goal here is to submit the current level's password to port **30001** on localhost, but this time the connection must be made using **SSL/TLS encryption** (`nc` won't work).

- For SSL connections we use `openssl s_client`, which is the standard tool for connecting to SSL/TLS-enabled services from the command line.
	- The `-connect` flag specifies the host and port in `host:port` format.
	- The `-ign_eof` flag tells openssl not to close the connection when it hits EOF, giving us time to type/paste the password.

![](b15_1.png)

- Connected to the local service on port 30001 via SSL.

![](b15_2.png)

- Pasted the current level's password. The service responded with `Correct!` and returned the next password.

![](b15_3.png)

![](b15_4.png)

![](b15_5.png)

![](b15_6.png)

### Password

`BfMYroe26WYalil77FoDi9qh59eK5xNr`
