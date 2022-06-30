---
id: git
title: Git
---

# Git Cheat Sheet
![Git Cheat Sheet](https://res.cloudinary.com/practicaldev/image/fetch/s--bjpVKHPe--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/8ogqpfkvqqpyfbs3w6p7.png)

## ইনস্টল (Setup)
##### গিট ইনস্টল ( ম্যাক )
```
brew install git
``` 
গিট আনইনস্টল (ম্যাক)

brew remove git
গিট ইনস্টল (উবুন্টু)

sudo apt-get install git
গিট আনইনস্টল (উবুন্টু)

sudo apt-get remove git
গিট ভার্সন চেক

git --version
গিটটি কোথায় রয়েছে তা দেখুন

which git
গিট সাহায্য

git help
## Common commands

### General

### Create repository:

```git
git init
```

Add file:

	git add <file>

Remove file:

	git rm <file>

Move or rename file:

	git mv <from> <to>

Commit changes:

	git commit

Show changes:

	git status

Show log:

	git log

Show log with tags:

	git log --decorate

Search thru commit messages:

	git log --grep="<search>"

Add remote repository:

	git remote add origin <url>

### Branches

Show branches:

	git branch

Create branch:

	git branch <branch>

Create and checkout branch:

	git checkout -b <branch>

Checkout branch:

	git checkout <branch>

Rename branch:

	git branch -m <from> <to>

Delete branch:

	git branch -d <branch>

Delete remote branch:

	git push origin :<branch>

Review branch changes:

	git diff <branch>

Merge branch into current:

	git merge <branch>

Resolve merge conflicts:

	mate <file>
	git add <file>
	git commit

Discard branch changes:

	git checkout -f master

### Tags

Show tags:

	git tag

Create tag:

	git tag -a <tag>

Create tag for specific commit:

	git tag -a <tag> <commit>

Show tag data:

	git show <tag>

Delete tag:

	git tag -d <tag>

Delete remote tag:

	git push origin :refs/tags/<tag>

### Push

Push to master:

	git push origin master

Push with tags:

	git push origin master --tags

### Pull

Fetch from remote repository:

	git fetch origin

Merge remote branch into current:

	git merge origin/master

Fetch and merge into current branch:

	git pull

### Clone

Clone repository:

	git clone <url>

Clone with submodules:

	git clone --recursive <url>

### Submodules

Add submodule to repository:

	git submodule add <url>

Update submodule:

	git submodule update

### Stash

Stash changes:

	git stash

Show stashes:

	git stash list

Restore stash:

	git stash apply

Restore stash and restage files:

	git stash apply --index

Restore specific stash:

	git stash apply <stash>

Remove stash:

	git stash drop <stash>

Restore and remove stash:

	git stash pop

Create branch from stash:

	git stash branch <branch>

## Special

Remove last commit (not pushed):

	git reset --hard HEAD~1

## Misc

Get the number of commits in the current branch:

	git log --pretty=oneline | wc -l

## Configuration

Set name:

	git config --global user.name "<name>"

Set email:

	git config --global user.email "<email>"

Set editor (e.g. TextMate):

	git config --global core.editor "mate -w"

Use colors:

	git config --global color.ui true
