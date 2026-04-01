---
title: Bandit Level 8
user: bung3r
description: The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
tags:
  - bandit
  - overthewire
  - sort
  - uniq
---
# [Bandit Level 8](https://overthewire.org/wargames/bandit/bandit8.html)

- The password is the only line in `data.txt` that appears exactly once
	- all the other lines are duplicates.

- `sort data.txt | uniq -u` does this in one command.
	- `sort` groups identical lines together, because `uniq` only compares adjacent lines
		- thus, it needs the file sorted first.
	- `uniq -u` then prints only the lines that are **unique**.

### Password

`cvX2JJa4CFALtqS87jk27qwqGhBM9plV`
