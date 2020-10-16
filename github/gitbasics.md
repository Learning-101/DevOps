# Source Code Management(SCM)
Source code management (SCM) is used to track modifications to a source code repository. SCM tracks a running history of changes to a code base and helps resolve conflicts when merging updates from multiple contributors. SCM is also synonymous with Version control. 

As software projects grow in lines of code and contributor head count, the costs of communication overhead and management complexity also grow. SCM is a critical tool to alleviate the organizational strain of growing development costs.

## Source Code Management best practices

- Commit often
- Ensure you're working from latest version
- Make detailed notes
- Review changes before committing
- Use Branches
- Agree on a Workflow

# Repo types

Many of us aware about the version control when it comes to work with multiple developers on a single project and collaborate with them. There is no doubt that version control make developers work more easy and fast. In most of the organization developers use either 
- Centralized Version Control System(CVCS) like Subversion(SVN) 
- Concurrent Version System(CVS) or Distributed Version Control System(DVCS) like Git (Written in C), Mercurial (Written in Python) or Bazaar (Written in Python).

### Centrailized SCM vs Distributed SCM

| Classification | Centralized Repo | Distributed Repo |
| ------- | ----------- |-------------- |
| `Copy of code repo` | Centralized version control is the simplest form of version control in which the central repository of the server provides the latest code to the client machines | Distributed version control is a form of version control where the complete codebase is mirrored on every developer’s computer | 
|`Save`|There are no local repositories | There are local repositories |
|`Speed`|Works comparatively slower | Works faster |
|`Connection`| Always require internet connectivity | Developers can work with a local repo without an internet connection |
|`Changes` | Focuses on synchronizing tracking and backing up files | Focuses on sharing changes |
|`Fail Over`| A failure in the central server terminates all the versions | A failure in the main server does not affect the development |


## Github install

#### Installing *Git* – the easy way

> *Git* is a [free and open source](http://git-scm.com/about/free-and-open-source) distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

– The [*Git* website](http://git-scm.com/)

Choose one of the following options.
- [Instructions for *Windows*](#file-windows-md)
- [Instructions for *Mac*](#file-mac-md)
- [Instructions for *Linux*](#file-linux-md)

# Installing *Git* on a *Windows* 
 
**Download** *Git* from [Git for Windows](https://gitforwindows.org) and **install it**. 

# Installing *Git* on a *Mac*

[Open a terminal window](http://www.youtube.com/watch?v=zw7Nd67_aFw).

## Step 1 – Install [*Homebrew*](http://brew.sh/)

> *Homebrew* […] simplifies the installation of software on the Mac OS X operating system.

– [Homebrew – Wikipedia](http://en.wikipedia.org/wiki/Homebrew_%28package_management_software%29)

**Copy & paste the following** into the terminal window and **hit `Return`**.

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
brew doctor
```

You will be offered to install the *Command Line Developer Tools* from *Apple*. **Confirm by clicking *Install***. After the installation finished, continue installing *Homebrew* by **hitting `Return`** again.

## Step 2 – Install *Git*

**Copy & paste the following** into the terminal window and **hit `Return`**.

```shell
brew install git
```

**You can use *Git* now.**

# Installing *Git* on *Linux*

Determine on **which *Linux* distribution** your system is based on. See [List of Linux distributions – Wikipedia](http://en.wikipedia.org/wiki/List_of_Linux_distributions) for a list. **Most *Linux* systems – including *Ubuntu* – are *Debian*-based**.


## *Debian*-based linux systems

**[Open a terminal window](https://help.ubuntu.com/community/UsingTheTerminal). Copy & paste the following** into the terminal window and **hit `Return`**. You may be prompted to enter your password.

```shell
sudo apt update
sudo apt upgrade
sudo apt install git
```

**You can use *Git* now.**


## *Red Hat*-based linux systems

**Open a terminal. Copy & paste the following** into the terminal window and **hit `Return`**. You may be prompted to enter your password.

```shell
sudo yum upgrade
sudo yum install git
```

**You can use *Git* now.** 




##### About ssh :- 
Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username or password at each visit.


##### Generating a new SSH key and adding it to the ssh-agent
[Add ssh agent ](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)













# Gitlab Commands
### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
