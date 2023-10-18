# Open Sourse SW
Department of AI,SW / 202334426 / 김동은
**Descriptions of Linux CLI 2**
---

### Standard Output
- **'>'** after a command : create and save the output in a file
- Command **'cat'** : displays the content of a text file.
- **'>>'** : appends output(already exists) / create and write to a new file(doesn't exist)

### Standard Input
- **'<'** : redirect input

*It is possible to mix "<" and ">" together in a single line!*

---
### Pipelines "|"
Pipeline feeds output of previous command to input of 'next' command.
*ex) command1 | command2 | command3 ....*
```sh
$ ls -lh | less
```
Press "q" : exit the screen.
```sh
$ ls | wc -l
7
$
```
**"wc - l"** : displays the number of files in the current directory.

---

### Expansion
```sh
$ echo my name is dongeun
my name is dongeun
$
```
**"echo"** : print the text after command 'echo'.
```sh
$ echo *
```
__" echo * "__ : print the files that exist in the current directory. (same function as '-ls')

*Tip : Bachslash*
bachslash: ignore line change (enter) to enter a long command in multiple lines.

---
### Permission
**Files and directories have a permission assigned differently to owner, group, ohters.**

#### -rwx rwx rwx
-> read with 3 letters at a time
-> 'rwx' means: Read, Write, and Execution

- '-': File type

    '-': indicates regular file
    'd': indicates directory
- 1st 'rwx': permissions for the file owner.
- 2nd 'rwx': permissions for the group owner of the file
- 3rd 'rwx': permissions for all other users.

---
### Changing Permissions
**Use command "chmod" to change permissions.**
```sh
[me@linuxbox me]$ chmod 600 some_file
```
"600" means
6 = 110 = rw- for owners (owners can read and write the file)
0 = 000 = - - - for group (group owner can't read, write, and execute the file.)
0 = 000 = - - - for others (all other users can't read, write, and execute the file.)

**We can grant various permissions by combining three numbers using binary numbers.**

---
### Superuser
A superuser has all system administation authority!

Put "Sudo" before the command to use superuser's authority.
```sh
[me@linuxbox me]$ sudo some_command
```
if you want use superuser's authority continuously, use "-i"
```sh
[me@linuxbox me]$ sudo -i
```

Type "exit" : get out of a superuser session.

---
### Shell Script
This is used to store commands in advance and execute them sequentially whenever necessary.
```sh
$ nano myscript.sh
```
```sh
ehco "Hello Shell Script!"
```
```sh
$ sh myscript.sh
Hello Shell Script!
$
```





