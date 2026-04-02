---
title: Bandit Level 11
user: bung3r
description: The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
tags:
  - bandit
  - overthewire
  - rot13
  - tr
  - encoding
level: 11
---
# [Bandit Level 11](https://overthewire.org/wargames/bandit/bandit11.html)

- `data.txt` contains the password encoded with **ROT13** 
	- each letter is shifted 13 places in the alphabet. 

- Since the alphabet has 26 letters, applying ROT13 twice gets you back to the original, which means encoding and decoding are the same operation.

- `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'` decodes it.
	- `tr` is a character translation tool
		- it swaps characters from the first set to the matching position in the second set.
	- The pattern maps `A-M` to `N-Z` and `N-Z` to `A-M` (same for lowercase), which is exactly ROT13.

### Password

`IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`
