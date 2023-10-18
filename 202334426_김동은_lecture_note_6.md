# Open Sourse SW
Department of AI,SW / 202334426 / 김동은
**Git 1**
---

### Changes vs. Snapshot
- Changes:  accumulate and overwrite changes that have accumulated over time.
- Snapshot: recording events at a specific point in time.(git uses)
---
### Local, Centralized, Distributed.
- Local: Version control only occurs on personal computers. (Difficulty collaborating with others)

- Centralized : A central server manages the version system. (A personal computer makes a request to the central server and retrieves the required version.)

- Distributed: Personal computer holds all data from central server. (central server recovery is easy because a copy exists.)
---

### Git config
- Git configurations are stored in three levels:
1) System level: --system option.
(file:/etc/gitconfig)
2) Global (user) level: --global option.
(file:~/.config/git/config)
3) Local level: --local option.
(file:.git/gitconfig)

**Each level overrides values in the previous level: system->global->local*

```sh
$ git config --list
$ git config --list --show-origin
```
->You can see where each config is stored.

---
### Initializiong a Repository
**git init**
```sh
$git init
```
-> Initialized empty Git repository in an Existing Directory.

---
### Checking Repository Status
**git status**
```sh
$git status
On branch master

No commits yet

Untracked files:
.
.
(nothing added to commit)
```

---
### Adding a new file to be staged
**$ git add [file_name]**
```sh
$ git add README.md
$ git status
On branch master

No commits yet

Changes to be commited:
.
(Ready to commit)
Untracked files:
.
.
(nothing added to commit)
```

---
#### Adding all files to be staged
**$ git add**
```sh
$ git add
$ git status
On branch master

No commits yet

Changes to be committed:
.
.
.
(Ready to commit)
```

---
### Unstaging al file
**git re -cached [file_name]**
```sh
$git rm -cached history_command.txt
rm 'history_command.txt'

Untracked files:
    history_command.txt
```
-> Because I deleted it with rm earlier, it was added to the untracked file.

---
### Ignoring a file
```sh
$ nano .gitignore

GNU nano 4.8
history_command.txt
```
```sh
$ git add
& git status
. 
.
.
Changes to be commited:
.
.
.
(No Untracked files!)
```
---
### Commit

**$ git commit -m "commit message"**
```sh
 $ git commit -m "initial commit"
```
---
### Change branch name
```sh
$ git branch
*master
$git branch -m master main
$git branch
*main
$git status
On branch main
nothing to commit, woriking tree clean
$
```