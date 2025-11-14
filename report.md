# 📄 **Git Practical Report Assignment - 7**

**Name:** Sabyasachi Gorai
**Course:** MCA
**Subject:** Software Tools & Technologies
**Date:** *14/11/2025*

---

## **Task 1: Installation and Setup**

### **Command Used**

```bash
git --version
which git
```

### **Output**

```bash
git version 2.49.0.windows.1
/mingw64/bin/git
```

### **Command Used**

```bash
git config --global user.name
git config --global user.email
git config --global color.ui
```

### **Output**

```bash
sabyasachiGorai
12082****+sabyasachiGorai@users.noreply.github.com
auto
```

### **Command Used**

```bash
git config --list
```

### **Output**

```bash
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=schannel
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=sabyasachiGorai
user.email=12082****+sabyasachiGorai@users.noreply.github.com
color.ui=auto
```


## **Task 2: Initialize Repository and First Commit**

### **Command Used**

```bash
pwd
git init
```

### **Output**

```bash
/i/My Drive/MCA/SEC_101_STT/Software Tools A 7/git-assignment

Initialized empty Git repository in I:/My Drive/MCA/SEC_101_STT/Software Tools A 7/git-assignment/.git/
```

### **Command Used**

```bash
 git log
```

### **Output**

```bash
commit 059a3254d84b8ef79b0468491b8ba2dcb5e0ca29 (HEAD -> master)
Author: sabyasachiGorai <120822558+sabyasachiGorai@users.noreply.github.com>
Date:   Fri Nov 14 12:49:47 2025 +0530

    Initial commit: add README
```

```bash
 git log --oneline
```

### **Output**

```bash
059a325 (HEAD -> master) Initial commit: add README
```