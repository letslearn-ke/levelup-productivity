+++
title = "Level up Git"
date = 2020-10-12T20:06:46Z
weight = 2
pre = "<b>2. </b>"
+++

### Welcome, Lets Learn Git Together.

# Git Basic to Advanced

Version control is a system that records changes to a file or set of file over time so that you can recall specific version later.
Git was initially designed and developed by Linus Torvalds for linux Kernel development. Git is a free software distributed under the **GNU General License Version2.**

The reality you can do this with nearly any type of file on a computer.

1. Opensource books are version controlled.
2. You could also do this for your notes.
3. If you are a graphic or web designer and want to keep every version of an image or layout. You would most certainly do this with Vcs.

It is a wise thing to use since

1. it allows you to revert selected files back to a previous state
2. revert the entire project back to previous state
3. compare changes over time
4. See who last modefied something that might be cousing a problem.
5. Who introducet an issue and when, and more.

using VCS means that if you screw things up or lose files, you can easily recover with little overhead.

Git is a distributed version Control systems.

If you understand what Git is and the fundamentals of how it works, then using git effectively will be much easire for you.

Git stores and think about information in a very different way, and undertanding these differences will help you avoid becoming confused while using it.

**version control system (vcs)** is a software that helps software developers to work together and maintain a complete history of their work.

Listed below are the functions of a **VCS**

1. Allows developers to work simultaneously.
2. Does not allow everwriting each other's changes.
3. Maintains a history of every version.

Following are the types of VCS.

- Centralized version control system (CVCS)
- Distributed/Decentralized version control system.

### Snapshots, Not diffrences.

Git thinks of its data more like a series of snapshots of a miniature filesystem.With git every time you commit, or save the state of your project, git basically takes a picture of what all your files look like at that momemt and stores a references to that snapshot.

To be efficient, if the file has not changed, Git doesn't store the file again, just a link to the previous identical file it has already stored.

Git thinks about its data more like a **stream of snapshots**.

### Nearly Every Operation is Local.

- Most operation in git need only local files and resoruces to operate.
- not dependend on another computer on your network.
- You have entire history of the project right there on your local disk, most operations seem almost instantenouses.
- Git reads history directly form you local database.
- Git can look up the file a month ago adn do a local difference calculation.

- This means that there is very little you can't do if you're offline. You can commit happily and later upload you changes to the server ()

### Git Has integrity.

Everything in Git is checksummend before it is stored and is then referred to by the checksum. Means it's impossible to change the content of any file or directory without Git knowing about this funcitonality.

The mechanism that Git uses for this checksumming is called a SHA-1 hash. This is a 40-character string composed of hexadecimal character (0-9 and a-f) and calculated based on the content file or directory structrue in Git. A SHA-1 has looks something like this.

### Git Generally Only Adds Data.

When you do actions in Git, nearly all them only add data to the Git Database.
It is hard to get the system to do anything that is not undoable or to make it erase in any way.

You can lose or mess up changes you haven't committed yet, but after you commit a snapshot into git , it is very difficult to lose, especially if you reqularly push your database to another repository.

Dont worry with git we can experiment without the danger of severely screwing things up. Git store its data and how you can recover data that seem lost.

#### The Three states.

Pay attention now --- here is the main thing to rember about git if you want the rest of learning process to go smoothly.

Git has three main states that your files can reside in : Modified , staged and commited.

1. **Modified** means that you have changed the file but have not committed it to your database yet.
2. **Staged** means that you have marked a modifed file in its current version to go into your next commit snapshot.
3. **Committed** means that the data is safely stored in you local database.

This leads us to three main sections of a Git project: The working tree, the staging area, and the Git directory.

**The working tree** is a single checkout of one version of the project.
The files are pulled out of the compressed databse in the Git directory and placed on disk for you to use or modify.

**The staging area** is a file, generally contained in your Git directory, that store information about what will go into your next commit. **Technical name is index**

**The git directory** if where Git store the metadata and object database for you project. This is the most important part of git, and it is What is copied when you **clone** a repository from another computer.

The basic Git workflow goes something like this:

1. You modify files in your working tree.
2. You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area.
3. You do a a commit, which takes the files as they are in the staging area and store that snapshot permanently to your git directory.

If a particula version of a file in a **git directory** is considered **committed** it means that the file has been modified and was added to the staging area.

### The command Line.

There are a lot of different ways to use git. There are

1. Command-line tools.
2. There are many graphical user interface of varying capabilities.

For this book, we will be using Git on the Command Line. If you know how to run the command-line version, you can probably also figure out how to run the GUI version, while the opposite my not be true

#### Prerequisite

1. expect you to know how to open Terminal (linux)
2. Command Prompt or PowerShell in Windows.

### Install on Linux

In linux we use Package management tools thats comes with your distribution.

if you are on arch or manjaro.

sudo pacman -S git

if you are on ubuntu.

sudo apt install git-all

### Install on windows.

There are a few ways to install git on windows. The most official build is available for download on dhe Git website. Just go to **https://git-scm.com/download/win** and download with start automatically.

You can also use **git chocolatey package**. Not that the chocolatey packaeg is community maintained.

