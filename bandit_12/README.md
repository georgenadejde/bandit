---
title: Bandit Level 12
user: bung3r
description: The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)
tags:
  - bandit
  - overthewire
  - xxd
  - hexdump
  - gzip
  - bzip2
  - tar
level: 12
---
# [Bandit Level 12](https://overthewire.org/wargames/bandit/bandit12.html)

- `data.txt` is a **hexdump** = a text representation of binary data. 
	- Underneath it is a file that has been compressed multiple times with different tools, layered one on top of another.

- First step is reversing the hexdump back to binary with `xxd -r data.txt > /tmp/data`.
	- `xxd -r` reverses a hexdump back into the original binary
	- Then use `file` on the result to identify what kind of compression is on the outermost layer

- From there it's a loop: identify the compression type with `file`, rename the file to the correct extension (e.g. `.gz`, `.bz2`, `.tar`), and decompress with the right tool (`gzip -d`, `bzip2 -d`, `tar xf`).
	- Repeat until `file` reports the result is ASCII text

### Password

`5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu`
