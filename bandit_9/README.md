---
title: Bandit Level 9
user: bung3r
description: The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
tags:
  - bandit
  - overthewire
  - strings
  - grep
  - binary
  - linux
---
# [Bandit Level 9](https://overthewire.org/wargames/bandit/bandit9.html)

- `data.txt` is mostly binary garbage 
	- the password is one of the few human-readable strings inside it, and it's preceded by a bunch of `=` signs.

- `strings data.txt | grep "==="` extracts all printable character sequences from the binary file and filters for the ones containing `===`
	- `strings` scans the file and prints any sequence of 4+ printable characters 
	- `grep` then narrows it down to the line with the `=` prefix.

### Password

`UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`
