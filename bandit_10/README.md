---
title: Bandit Level 10
user: bung3r
description: The password for the next level is stored in the file data.txt, which contains base64 encoded data
tags:
  - bandit
  - overthewire
  - base64
  - encoding
level: 10
---
# [Bandit Level 10](https://overthewire.org/wargames/bandit/bandit10.html)

- `data.txt` contains a base64-encoded string. Base64 is a common encoding scheme that represents binary data as ASCII text
	- since it is not encryption, but simply encoding, it is reversible.

- `base64 -d data.txt` decodes it straight to `stdout`.

### Password

`truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`
