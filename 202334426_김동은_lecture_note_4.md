# Open Sourse SW
Department of AI,SW / 202334426 / 김동은
**Descriptions of Linux CLI**
### Shell command
- pwd : shows the current path in a hierarchical directory
- cd : change directory
- ls : list files and directories
- cp : copy files and directories
- mv : move files and directories or rename them
- rm : delete files and directories
- mkdir : make a new directory

#### cp and ls
**arguments:**
- .current directory
- . .upper-level directory

This is the example
```sh
$cd OSS
$pwd
/home/kimdongeun/OSS
$ls
neuralintlab transformers
$cd ..
$pwd
/home/kimdongeun/
```

**options:**
-l show detailed information(long format)
-lh same as azbove, but size in units
```sh
$ls -l
```
---
To input past commands, you can press "up arrow" key.

---
**Help command: help**
```sh
$ help cd
```

**Help command: man**
```sh
$ man cp
```
**Exiting terminal:exit**
```sh
$ exit
```



