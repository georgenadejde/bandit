---
title: Bandit Level 29
user: bung3r
description: There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.
tags:
  - bandit
  - overthewire
  - git
  - gitbranch
  - gitcheckout
  - gitlog
level: 29
---
# [Bandit Level 29](https://overthewire.org/wargames/bandit/bandit29.html)

- Cloned the repo again at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. 
- The `README.md` on the main branch says "no passwords in production!" 
	- so the password isn't here, but the hint tells us to look elsewhere.

- The key is to check the **other branches**
	- `git branch -a` lists all branches including remote ones.
	- Found a `dev` branch
		- checked it out with `git checkout dev`.
	- The `README.md` on that branch had the actual password.

![](b29_1.png)

![](b29_2.png)

![](b29_3.png)

![](b29_4.png)

![](b29_5.png)

![](b29_6.png)

![](b29_7.png)

![](b29_8.png)

![](b29_9.png)

![](b29_10.png)

![](b29_11.png)

![](b29_12.png)

![](b29_13.png)

![](b29_14.png)

### Password

`bbc96594b4e001778eee9975372716b2`
