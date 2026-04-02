---
title: Bandit Level 16
user: bung3r
description: The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
tags:
  - bandit
  - overthewire
  - ssl
  - tls
  - openssl
  - nmap
  - portscanning
  - ssh
  - privatekey
level: 16
---
# [Bandit Level 16](https://overthewire.org/wargames/bandit/bandit16.html)

- There are several ports open in the range **31000–32000** on localhost. 
	- The challenge is to figure out which one speaks SSL and also returns the next credentials, rather than just echoing back what you send it.

- First step is scanning the port range with `nmap` to see what's open and what services are running.
	- This quickly narrows down which ports speak SSL vs. plain TCP.

![](b16_1.png)

![](b16_2.png)

- Identified the correct SSL port from the nmap output — only one of them returns credentials instead of echoing.

![](b16_3.png)

![](b16_4.png)

- Connected using `openssl s_client -connect localhost:<port>` and submitted the current password.

![](b16_5.png)

![](b16_6.png)

![](b16_7.png)

![](b16_8.png)

- The service responded with an **RSA private key** instead of a plain password. This is the SSH key for bandit17.

![](b16_9.png)

![](b16_10.png)

- Saved the private key to a file in `/tmp`, then set the correct permissions with `chmod 400` — SSH won't accept a key file that's world-readable.

![](b16_11.png)

![](b16_12.png)

![](b16_13.png)

- Used the key to SSH into bandit17: `ssh -i /tmp/key.pem bandit17@localhost -p 2220`

### Password

`cluFn7wTiGryunymYOu4RcffSxQluehd`
