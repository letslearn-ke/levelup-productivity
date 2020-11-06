+++
title = "Git basics"
date = 2020-10-12T20:06:46Z
weight = 4
pre = "<b>2. </b>"
+++

## Git basics.

If you want to get going with git, this is it.
This section covers vast majority of the thing you'l eventually speed your time doing with git.

### Expectations.

1. You should be able to configure and initialize a repository.
2. Begin and stop tracking files and stages and commits changes.
3. Know how to set up git to ignore files.
4. Know how to Undo mistakes quickly and Easily.
5. How to browse the history of your project and view changes between commits.
6. How to push and pull from remote repositories.

### Getting a Git repository.

Can be obtained in two ways.

1. You can take a local directory that is currently not under version control, turn it into a **git repository**.
2. You can clone an existing Git repository from eleswhere'

#### Initializing a Repository in an Existing Directory.

```

```

If you have a project directory that is currently not under version control and you want to start controlling it with Git, you firt need to go to that project's dirctory.

```
mkdir first

cd first

```

This create a new subdirectory named **.git** that contains all of your necessary repoistory files. At this point nothing in your project is tracked yet.

```
npm install --global generate-license
```

👆 The above command install a nice tool we could use to add license to our opensource project. Daah it's a good practise.

git init

This create a new subdirectory named **.git** that contains all of your necessary repository files - **a Git repoisotory skeleton**. At this point, nothing in your project is tracked yet. The contents if the **of git will be covered on Git internals**

```
git add *.c
git add LICENSE
git commit -m "initial project version"

```

### Cloning an Existing Repository.

- Git receives a full copy of nearly all data that the server has.
- Every version of every file for the history of the project is pulled down by default when **git clone is run**

You clone a repository with **git clone <url>**.

```
git clone https://github.com/libgit2/libgit2
```

### Recording changes to the repository.

You'll want to start making change and commiting snapshots to those changes into your repository each time the project reaches a state you want to record.

Remember that each file in your working directory can be in one of two states.

1. **Tracked or untracted.**

Tracked files are files that were in the last snapshot; they can be **unmodified, modified, or staged.**

- Tracked files are files that git knows about.

**Untracked files** are everything else - any files in your working directory that were not in your last snapshot and are not in your staging area.

When you first clone a repository, all your files will be tracked and umodified because Git just checked them out and you haven't edited anything.

### Checking the Status of your files.

The main tool you use to determine which files are in which state in the **git status** command. If you run this command directly after a clone , you should see something like this.

