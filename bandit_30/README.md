---
title: Bandit Level 30
user: bung3r
description: There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.
tags:
  - bandit
  - overthewire
  - git
  - gittag
  - gitshow
---
# [Bandit Level 30](https://overthewire.org/wargames/bandit/bandit30.html)

- Cloned the repo at `ssh://bandit30-git@localhost/home/bandit30-git/repo`.
	- The README is empty and there are no interesting commits or branches this time.

- The trick here is **git tags** 
	- `git tag` lists any tags in the repo and there's one called `secret`.
	- `git show secret` reveals the contents of that tag, which is the password.
	- Tags in git are often used to mark releases or important points, but they can also be used to hide data that isn't on any branch.

![](b30_1.png)

![](b30_2.png)

### Password

`5b90576bedb2cc04c86a9e924ce42faf`
