---
tags: book, guide, git, in_progress
type: book
title: Pro Git
author: Scott Chacon and Ben Straub
---

# Introduction
---
How git works? It is like taking **snapshots** of a filesystem and storing a reference to it. If no changes were made, it simply puts a link pointing to the previous snapshot.

Generally, git just **adds** data. Since something has been committed, is difficult to lose it.

There are 3 basic states of a file in git process:
1.  Committed: Safely stored locally
2.  Modified: It has been changed,  but not committed yet
3.  Staged: A modified file has been **marked** to get into the next snapshot (commit)

## First-time Git Setup

Configuration files:
1. System: `/etc/gitconfig`
2. User: `~/.gitconfig` or `~/.config/git/config`
3. Repository (project): `.git/config`

## Getting Help

1. `$ git help <verb>`
2. `$ git <verb> --help`
3. `$ man git-<verb>`

# Git Basics
---
When git says that a file is **untracked**, it means that it doesn't exist in any previous snapshot (commit).

| Basic git command | Functionality |
|---|---|
| `git reset HEAD <file>` | unstage |
| `git add <file>` | update what will be committed|
| `git checkout --<file>` | discard changes |

`git status -s` or `--short` provides a simplified output

`git diff` is more precise than `git status`

| `git diff` | Functionality |
|:---|:---|
| no args | changed but not staged yet |
| `--staged` | what have already been staged and <br> will go into the next commit |
| `--cached` | what have been staged so far <br> (not only in the last commit)

## Ignoring Files

Inside the .gitignore file:
* Blank lines or lines starting with `#` are ignored
* Patterns apply globally
* Directories are specified with `/`
* Everything starting with `!` is negated (e.g. you want to exclude all `.tex` files but to include `main.tex`, you should write `!main.tex`)
* `*` matches zero or more characters
* `?` matches  exactly one character
* `.[oae]` means `.o`, `.a` and `.e`
* `**` matches nested directories (e.g. `a/**/z` can be interpreted as `a/b/z`, `a/b/c/z` etc)

