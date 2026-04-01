---
title: Bandit Level 24
user: bung3r
description: A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
tags:
  - bandit
  - overthewire
  - bruteforce
  - scripting
  - bash
  - netcat
---
# [Bandit Level 24](https://overthewire.org/wargames/bandit/bandit24.html)

- There's a daemon running on port **30002** that expects the current password followed by a **4-digit secret PIN** (0000–9999). 
	- There's no way to look up the PIN — we need to brute-force all 10,000 combinations.

- Wrote a bash script to generate all combinations and pipe them to `nc`.
	- Used a `for` loop from 0000 to 9999 with `printf "%04d"` to zero-pad single/double digit numbers.
	- Each line is formatted as `<password> <pin>` and echoed into a file, then the whole file is fed to `nc localhost 30002`.
	- Piped the output through `grep -v Wrong` to filter out all the failed attempts and see only the success line.

![](b24_1.png)

- Got the response `Correct!` with the next password after the correct PIN was found.

### Password

`UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ`
