---
layout: page
title: Git
---

## Rebase

Most often, just use this:
* `git pull --rebase origin master`

Interactive rebase for the past 3 commits (to squash, delete, pick, etc.):
* `git rebase -i HEAD~3`

---

## Tagging

**Git tags are just branches that can no longer change; they behave almost the same as a branch.**
There are annotated tags and lightweight ones, annotated tags can store author name, release notes, a message, and date.

List existing tags:
* `git tag` 
* `git tag -l 'v1.8.*'`

Annotate an existing tag with a message:
* `git tag -a v1.4 -m 'my version 1.4 annotated message'`

View details for an existing tag:
* `git show v1.4`

Add a tag to existing commit:
* `git tag -a v1.2 9fceb02`

Add a tag based on the current commit:
* `git tag -a 1.4`

`git push` does **not** transfer tags to remote servers. To do so, execute the following **after** creating the tag:
* `git push <remote> <tagname>` example: `git push origin v1.4`
* `git push origin --tags`: pushes all tags up

Delete tags:
* `git tag -d v1.4.temp`

You can checkout the patchset that corresponds with a tag:
* `git checkout v1.4`

---
