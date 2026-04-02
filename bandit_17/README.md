---
title: Bandit Level 17
user: bung3r
description: "There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new"
tags:
  - bandit
  - overthewire
  - diff
  - filecomparison
level: 17
---
# [Bandit Level 17](https://overthewire.org/wargames/bandit/bandit17.html)

- There are two files in the home directory: `passwords.old` and `passwords.new`. The password for the next level is the **one line in `passwords.new` that doesn't exist in `passwords.old`**.

- `diff passwords.old passwords.new` compares the two files line by line and outputs only what changed.
	- Lines starting with `<` are from the first file (old), lines with `>` are from the second (new).
	- Since only one line changed, the output is short and the new password is immediately visible.

![](b17_1.png)

![](b17_2.png)

### Password

*(RSA private key used to log in — see bandit16 writeup)*
`kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd`
