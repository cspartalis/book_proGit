---
tags: book, guide, git, in_progress
type: book
title: Pro Git
author: Scott Chacon and Ben Straub
---

# Introduction
---
How git works? It is like taking **snapshots** of a filesystem and storing a reference to it. If no changes were made, it simply puts a link pointing to the prvious snapshot.

Generally, git just **adds** data. Since something has been commited, is difficult to lose it.

There are 3 basic states of a file in git process:
1.  Commited: Safely stored locally
2.  Modified: It has been changed,  but not commited yet
3.  Staged: A modified file has ben **marked** to get into the next snapshot (commit)

## First-time Git Setup

Configuration files:
1. System: `/etc/gitconfig`
2. User: `~/.gitconfig` or `~/.config/git/config`
3. Repository (project): `.git/config`

## Getting help

1. `$ git help <verb>`
2. `$ git <verb> --help`
3. `$ man git-<verb>`
