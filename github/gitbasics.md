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

##### Installing *Git* – the easy way

> *Git* is a [free and open source](http://git-scm.com/about/free-and-open-source) distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

– The [*Git* website](http://git-scm.com/)

Choose one of the following options.
- [Instructions for *Windows*](#file-windows-md)
- [Instructions for *Mac*](#file-mac-md)
- [Instructions for *Linux*](#file-linux-md)

##### Installing *Git* on a *Windows* 
 
**Download** *Git* from [Git for Windows](https://gitforwindows.org) and **install it**. 

##### Installing *Git* on a *Mac*

[Open a terminal window](http://www.youtube.com/watch?v=zw7Nd67_aFw).

###### Step 1 – Install [*Homebrew*](http://brew.sh/)

> *H#omebrew* […] simplifies the installation of software on the Mac OS X operating system.

– [Homebrew – Wikipedia](http://en.wikipedia.org/wiki/Homebrew_%28package_management_software%29)

**Copy & paste the following** into the terminal window and **hit `Return`**.

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
brew doctor
```

You will be offered to install the *Command Line Developer Tools* from *Apple*. **Confirm by clicking *Install***. After the installation finished, continue installing *Homebrew* by **hitting `Return`** again.

##### Step 2 – Install *Git*

**Copy & paste the following** into the terminal window and **hit `Return`**.

```shell
brew install git
```

**You can use *Git* now.**

##### Installing *Git* on *Linux*

Determine on **which *Linux* distribution** your system is based on. See [List of Linux distributions – Wikipedia](http://en.wikipedia.org/wiki/List_of_Linux_distributions) for a list. **Most *Linux* systems – including *Ubuntu* – are *Debian*-based**.


##### *Debian*-based linux systems

**[Open a terminal window](https://help.ubuntu.com/community/UsingTheTerminal). Copy & paste the following** into the terminal window and **hit `Return`**. You may be prompted to enter your password.

```shell
sudo apt update
sudo apt upgrade
sudo apt install git
```

**You can use *Git* now.**


##### *Red Hat*-based linux systems

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


Generating a new SSH key

Open Git Bash.

Paste the text below, substituting in your GitHub email address.

``` $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com" ```

This creates a new ssh key, using the provided email as a label.

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

``` > Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter] ```

At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".

```shell
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again] 
```

#### Adding a new SSH key to your GitHub account

1. Copy the SSH key to your clipboard.

2. If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.

```shell
$ clip < ~/.ssh/id_rsa.pub
# Copies the contents of the id_rsa.pub file to your clipboard
```

3. In the upper-right corner of any page, click your profile photo, then click Settings.
4. In the user settings sidebar, click SSH and GPG keys.
5. Click New SSH key or Add SSH key.
6. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal System, you might call this key "Personal SystemName".
7. Paste your key into the "Key" field.
8. Click Add SSH key.
9. If prompted, confirm your GitHub password.


#### Testing your SSH connection

1. Open Git Bash.

2. Enter the following:
```shell
$ ssh -T git@github.com
# Attempts to ssh to GitHub
```

You may see a warning like this:
```shell
> The authenticity of host 'github.com (IP ADDRESS)' can't be established.
> RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
> Are you sure you want to continue connecting (yes/no)?
```
or like this:
```shell
> The authenticity of host 'github.com (IP ADDRESS)' can't be established.
> RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
> Are you sure you want to continue connecting (yes/no)?
```

3.Verify that the fingerprint in the message you see matches one of the messages in step 2, then type yes:
```shell
$ ssh -T git@github.com
Hi <<username>>! You've successfully authenticated, but GitHub does not provide shell access.
```


## Glossary

- git: an open source, distributed version-control system
- GitHub: a platform for hosting and collaborating on Git repositories
- commit: a Git object, a snapshot of your entire repository compressed into a SHA
- branch: a lightweight movable pointer to a commit
- clone: a local version of a repository, including all commits and branches
- remote: a common repository on GitHub that all team members use to exchange their changes
- fork: a copy of a repository on GitHub owned by a different user
- pull request: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more
- HEAD: representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using git checkout
- ORGANIZATIONS: Organizations allow users to share ownership and administration for a group of repositories. They help developers collaborate by providing a shared workspace to coordinate on projects, and practical permissions tools to make sure the right people have access to the right repositories.
- Outside Collaborators: You can grant access to repositories to users who are not part of an organization by making them Outside Collaborators. Each repository maintains a list of these externally approved users for easy auditing. This allows you to collaborate with any user on GitHub without giving them access to the rest of the data in your Organization.
- Staging Area: You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.
- SHA : SHA is basically an ID number for each commit. Ex. E2adf8ae3e2e4ed40add75cc44cf9d0a869afeb6

# Github Global Configure 

Configure user information for all local repositories

```shell 
$ git config --global user.name "[name]"
```

Sets the name you want attached to your commit transactions

```shell 
$ git config --global user.email "[email address]"
```

Sets the email you want attached to your commit transactions

```shell 
$ git config --global color.ui auto
```

Enables helpful colorization of command line output

# Github Organization 

ORGANIZATIONS: Organizations allow users to share ownership and administration for a group of repositories. They help developers collaborate by providing a shared workspace to coordinate on projects, and practical permissions tools to make sure the right people have access to the right repositories.


# Github Repo Types 

| Repo Type | Description | 
|----|-----|
| Public Repo | They're visible to any user on your GitHub Enterprise instance. everyone who has access to your GitHub instance has access to view and clone the repository and read all Issues and Pull Requests. With a GitHub user account, they can also open Issues, join discussions, and fork the repository, but won't be able to modify any of the files directly. Push access to repositories is granted by adding users as collaborators, or, in the case of organization members, assigning write permissions to members or teams. |
| Private Repo |  They're only available to the repository owner. You can add collaborators of your choise to share with. Private repositories are only visible to the members(users) of that users or organizations. An organization can configure a default repository permission that gets applied to all members, but users can be granted more explicit permissions through their membership in a relevant team.
 |

 Note:-  You can keep all the repositories in the your organization's GitHub Enterprise to Private by default with exception to a few repositories which contain sensitive information. This is a good way to keep reusing the code in the same organization.  If you have a repository you want made Public instead of Private you can request to your GitHub Enterprise to white-list it.

###  .gitignore file
Sometimes it may be a good idea to exclude files from being tracked with Git. This is typically done in a special file named .gitignore. You can find helpful templates for .gitignore files at github.com/github/gitignore.

# Gitlab Commands
### Getting & Creating Projects

| Command Type | Command | Description |
|------- | ------- | ----------- |
| ssh |  ``` git clone ssh://git@github.com/[username]/[repository-name].git ``` | Create a local copy of a remote repository using ssh option   |
| https | ``` git clone https://github.com/[username]/[repository-name].git ``` |  Create a local copy of remote repository using https option required user id password  |
| Git CLI | ``` gh repo clone [username]/[repository-name] ``` |  Create a local copy of remote repository using ssh  |

#### Creating Projects in the local system 
| Command | Description |
|----|-----|
| git init  | Initialize a local Git repository   |


### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently “checked out” to. Use git status to see which branch that is.

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
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

### Redo commits
| Command | Description |
| ------- | ----------- |
| `git reset [commit]` | Undoes all commits after [commit], preserving changes locally |
| `git reset --hard [commit]` | Discards all history and changes back to the specified commit |



### Git Configurations
Your `.gitconfig` file contains all your Git configurations.

#### Aliases
Aliases are helpers that let you define your own git calls. For example you could set `git a` to run `git add --all`.

To add an alias, either navigate to `~/.gitconfig` and fill it out in the following format:

```
[alias]
  co = checkout
  cm = commit
  p = push
  # Show verbose output about tags, branches or remotes
  tags = tag -l
  branches = branch -a
  remotes = remote -v
```

...or type in the command-line:

```bash
$ git config --global alias.new_alias git_function
```

For example:

```bash
$ git config --global alias.cm commit
```

For an alias with multiple functions use quotes:

```bash
$ git config --global alias.ac 'add -A . && commit'
```

Some useful aliases include:

| Alias | Command | What to Type |
| --- | --- | --- |
| `git cm` | `git commit` | `git config --global alias.cm commit` |
| `git co` | `git checkout` | `git config --global alias.co checkout` |
| `git ac` | `git add . -A` `git commit` | `git config --global alias.ac '!git add -A && git commit'` |
| `git st` | `git status -sb` | `git config --global alias.st 'status -sb'` |
| `git tags` | `git tag -l` | `git config --global alias.tags 'tag -l'` |
| `git branches` | `git branch -a` | `git config --global alias.branches 'branch -a'` |
| `git cleanup` | `git branch --merged \| grep -v '*' \| xargs git branch -d` | `git config --global alias.cleanup "!git branch --merged \| grep -v '*' \| xargs git branch -d"` |
| `git remotes` | `git remote -v` | `git config --global alias.remotes 'remote -v'` |
| `git lg` | `git log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --` | `git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --"` |

*Some Aliases are taken from [@mathiasbynens](https://github.com/mathiasbynens) dotfiles: https://github.com/mathiasbynens/dotfiles/blob/master/.gitconfig*

#### Auto-Correct
Git gives suggestions for misspelled commands and if auto-correct is enabled the command can be fixed and executed automatically. Auto-correct is enabled by specifying an integer which is the delay in tenths of a second before git will run the corrected command. Zero is the default value where no correcting will take place, and a negative value will run the corrected command with no delay.

For example, if you type `git comit` you will get this:

```bash
$ git comit -m "Message"
# git: 'comit' is not a git command. See 'git --help'.

# Did you mean this?
#   commit
```

Auto-correct can be enabled like this (with a 1.5 second delay):

```bash
$ git config --global help.autocorrect 15
```

So now the command `git comit` will be auto-corrected to `git commit` like this:

```bash
$ git comit -m "Message"
# WARNING: You called a Git command named 'comit', which does not exist.
# Continuing under the assumption that you meant 'commit'
# in 1.5 seconds automatically...
```

The delay before git will rerun the command is so the user has time to abort.

#### Color
To add more color to your Git output:

```bash
$ git config --global color.ui 1
```

[*Read more about the Git `config` command.*](http://git-scm.com/docs/git-config)

### Git Resources
| Title | Link |
| ----- | ---- |
| Official Git Site | http://git-scm.com/ |
| Official Git Video Tutorials | http://git-scm.com/videos |
| Official Git Tutorial | http://git-scm.com/docs/gittutorial |
| Everyday Git | http://git-scm.com/docs/everyday |
| Git Immersion | http://gitimmersion.com/ |
| Git for Computer Scientists | http://eagain.net/articles/git-for-computer-scientists/ |
| Git Magic | http://www-cs-students.stanford.edu/~blynn/gitmagic/ |
| Git Visualization Playground | http://onlywei.github.io/explain-git-with-d3/#freeplay |
| A collection of useful .gitignore templates | https://github.com/github/gitignore |
| Unixorn's git-extra-commands collection of git scripts | https://github.com/unixorn/git-extra-commands |

#### Git Books
| Title | Link |
| ----- | ---- |
| Pro Git | http://git-scm.com/book |
| Git Internals PluralSight | https://github.com/pluralsight/git-internals-pdf |
| Git in the Trenches | http://cbx33.github.io/gitt/ |
