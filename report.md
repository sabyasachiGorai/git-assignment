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


## **Task 3: Staging Diff and Commit Workflow**

### **Command Used**

```bash
git status
```

### **Output**

```bash
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

### **Command Used**

```bash
git diff README.md
git add README.md
```

### **Output**

```bash
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it
diff --git a/README.md b/README.md
index 61d07fd..2539537 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,3 @@
 # Git Practical
+
+# this is a new section added to test task no 3
\ No newline at end of file

```

### **Command Used**

```bash
git diff --staged
```

### **Output**

```bash
diff --git a/README.md b/README.md
index 61d07fd..2539537 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,3 @@
 # Git Practical
+
+# this is a new section added to test task no 3
\ No newline at end of file
```

### **Command Used**

```bash
git commit -m "Added new section to the README file"
```

### **Output**

```bash
[master 6335e40] Added new section to the README file
 1 file changed, 2 insertions(+)
```


## **Task 4: Branching and Marging**
### **Command Used**

```bash
touch feature.txt
git add feature.txt
git commit -m "Add feature.txt"
```

### **Output**

```bash
[feature-1 eaee2f6] Add feature.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt
```
### **Command Used**

```bash
git checkout master
 git merge feature-1
```

### **Output**

```bash
Switched to branch 'master'
Merge made by the 'ort' strategy.
 feature.txt | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt

```
### **Command Used**

```bash
git branch
git log --oneline --graph --decorate --all
```

### **Output**

```bash
feature-1
* master
*   c3b9dee (HEAD -> master) Merge branch 'feature-1' merged from feature-1 to test again.
|\
| * 8e7cbbb (feature-1) another line added for testing
* | c9dcf85 Merge branch 'feature-1'
|\|
| * eaee2f6 Add feature.txt
| * e95e7c8 Remove report.md from tracking and ignore it
* | a115afa cleared the mess
* | b778992 added gitignore file
* | d2ab734 Stop tracking report.md temporarily
|/
* 0e9b55b task 3 is done
* 6335e40 Added new section to the README file
* 4c6336c File added: report.md
* 059a325 Initial commit: add README


```

### **Command Used**

```bash
git checkout feature-1
git log --oneline --graph --decorate --all
```

### **Output**

```bash
Switched to branch 'feature-1'
*   c3b9dee (master) Merge branch 'feature-1' merged from feature-1 to test again.
|\
| * 8e7cbbb (HEAD -> feature-1) another line added for testing
* | c9dcf85 Merge branch 'feature-1'
|\|
| * eaee2f6 Add feature.txt
| * e95e7c8 Remove report.md from tracking and ignore it
* | a115afa cleared the mess
* | b778992 added gitignore file
* | d2ab734 Stop tracking report.md temporarily
|/
* 0e9b55b task 3 is done
* 6335e40 Added new section to the README file
* 4c6336c File added: report.md
* 059a325 Initial commit: add README

```


## **Task 5: Createa and Reslove a merge Conflict**
### **Command Used**

```bash
git merge conflict-branch
```

### **Output**

```bash
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.   

```

```bash
<<<<<<< HEAD
This is the MAIN version.
 version
=======
BRANCH  This is the BRANCH version.
version
>>>>>>> conflict-branch

```
### **Command Used**
```bash
A 7/git-assignment (master|MERGING)
$ git add README.md
git commit -m "Resolve merge conflict"


```

### **Output**
``bash
[master 237baad] Resolve merge conflict
```
### **Command Used**

```bash
git status
git log --oneline --graph
```

### **Output**

```bash
On branch master
nothing to commit, working tree clean


|\
| * f0ff6db (conflict-branch) Branch version
* | 0ba972d Main version
|/
* 8d5b9e1 Branch edit
* 68d8f4b Main edit
* 08d2476 Conflict branch edit
* b4fc669 master branch edit
* 3367b02 Branch change to README
* 12dafb6 Master change to README
* 62e9284 Branch change to README
* 9f6a8ad Main change to README
* 13c2b5f conflict line added
* 20a0adf Branch change to README
* 1ed7d3a Main change to README
*   c3b9dee Merge branch 'feature-1' merged from feature-1 to test again.
|\  
| * 8e7cbbb (feature-1) another line added for testing
* | c9dcf85 Merge branch 'feature-1'
|\|
| * eaee2f6 Add feature.txt
| * e95e7c8 Remove report.md from tracking and ignore it
* | a115afa cleared the mess
* | b778992 added gitignore file
* | d2ab734 Stop tracking report.md temporarily
|/
* 0e9b55b task 3 is done
* 6335e40 Added new section to the README file
* 4c6336c File added: report.md
* 059a325 Initial commit: add README
```


## **Task 6: Remots and Push/Pull**
### **Command Used**

```bash
git remote add origin https://github.com/sabyasachiGorai/git-assignment
git push -u origin master
```

### **Output**

```bash
Enumerating objects: 69, done.
Counting objects: 100% (69/69), done.
Delta compression using up to 16 threads
Compressing objects: 100% (64/64), done.
Writing objects: 100% (69/69), 8.03 KiB | 132.00 KiB/s, done.
Total 69 (delta 20), reused 0 (delta 0), pack-reused 0 (from 0)     
remote: Resolving deltas: 100% (20/20), done.
To https://github.com/sabyasachiGorai/git-assignment
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

```

### **Command Used**

```bash
git add README.md
git commit -m "Test commit for remote sync"
git push
```

### **Output**

```bash
[master b1e595b] Test commit for remote sync
 1 file changed, 5 insertions(+), 2 deletions(-)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 415 bytes | 83.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)       
remote: Resolving deltas: 100% (1/1), completed with 1 local object 
To https://github.com/sabyasachiGorai/git-assignment
   237baad..b1e595b  master -> master

```

### **Command Used**

```bash
git clone https://github.com/sabyasachiGorai/git-assignment test-clone

```

### **Output**

```bash
Cloning into 'test-clone'...
remote: Enumerating objects: 72, done.
remote: Counting objects: 100% (72/72), done.
remote: Compressing objects: 100% (46/46), done.
remote: Total 72 (delta 21), reused 72 (delta 21), pack-reused 0 (from 0)
Receiving objects: 100% (72/72), 8.39 KiB | 204.00 KiB/s, done.
Resolving deltas: 100% (21/21), done.

```

### **Command Used**

```bash
git remote -v

```

### **Output**

```bash
origin  https://github.com/sabyasachiGorai/git-assignment (fetch)
origin  https://github.com/sabyasachiGorai/git-assignment (push)

```

### showing the pulling case
### **Command Used**

```bash
git commit -m "Added one line to test the pull"
```

### **Output**

```bash
[master d5172f0] Added one line to test the pull
 1 file changed, 1 insertion(+)
```

### in test clone Repo
### **Command Used**

```bash
git pull

```

### **Output**

```bash
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 369 bytes | 3.00 KiB/s, done.
From https://github.com/sabyasachiGorai/git-assignment
   b1e595b..d5172f0  master     -> origin/master
Updating b1e595b..d5172f0
Fast-forward
 README.md | 1 +
 1 file changed, 1 insertion(+)

```


## **Task 7: Amend Revert and Reset**
### **Command Used**

```bash
git commit -m "Intial commit"
```

### **Output**

```bash
[master b3cc886] Intial commit
 1 file changed, 1 insertion(+)
 create mode 100644 file.txt
```


### **Command Used**

```bash
git commit --amend -m "Initial commit"
```

### **Output**

```bash
[master 4fe6497] Initial commit
 Date: Fri Nov 14 15:19:21 2025 +0530
 1 file changed, 1 insertion(+)
 create mode 100644 file.txt
```
### **Command Used**

```bash
git log --oneline -n 3
```

### **Output**

```bash
4fe6497 (HEAD -> master) Initial commit
d5172f0 (origin/master) Added one line to test the pull
b1e595b Test commit for remote sync

```

### **Command Used**

```bash
$ echo "A" >> file.txt
git add file.txt
git commit -m "Add A"

echo "B" >> file.txt
git add file.txt
git commit -m "Add B"
```

### **Output**

```bash
warning: in the working copy of 'file.txt', LF will be replaced by CRLF the next time Git touches it
[master 48c519b] Add A
 1 file changed, 1 insertion(+)
warning: in the working copy of 'file.txt', LF will be replaced by CRLF the next time Git touches it
[master d8468f9] Add B
 1 file changed, 1 insertion(+)
```


### **Command Used**

```bash
git log --oneline -n 2
```

### **Output**

```bash
d8468f9 (HEAD -> master) Add B
48c519b Add A
```

### **Command Used**

```bash
git rebase -i HEAD~2
```

### **Output**

```bash
Stopped at d8468f9...  Add B-commmit changed
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue

```
### **Command Used**

```bash
git commit --amend
```

### **Output**

```bash
[detached HEAD 9efc88a] Add B-chages the commit
 Date: Fri Nov 14 15:22:05 2025 +0530
 1 file changed, 1 insertion(+)

```


### **Command Used**

```bash
git rebase --continue
git log --oneline -n 2
```

### **Output**

```bash
Successfully rebased and updated refs/heads/master.
9efc88a (HEAD -> master) Add B-chages the commit
48c519b Add A

```
### **Command Used**

```bash
git log --oneline -2
```

### **Output**

```bash
6456c2f (HEAD -> master) added one line to show revert
9efc88a Add B-chages the commit
```

### **Command Used**

```bash
git revert 6456c2f
git log --oneline -2
```

### **Output**

```bash
[master 77731ff] Revert "added one line to show revert"
 1 file changed, 2 deletions(-)
 77731ff (HEAD -> master) Revert "added one line to show revert"
 6456c2f added one line to show revert

```


### **Command Used**

```bash
git log --oneline -n2
```

### **Output**

```bash
4dad5c2 (HEAD -> master) added one line to test soft
77731ff Revert "added one line to show revert"
```

### **Command Used**

```bash
git reset --soft HEAD~1
git log --oneline -n2
```

### **Output**

```bash
77731ff (HEAD -> master) Revert "added one line to show revert"
6456c2f added one line to show revert
```
### Revert vs Reset ()

git revert <hash> creates a new commit that undoes the changes of the specified commit. It preserves history and is safe to use on public/shared branches.

git reset (soft/mixed/hard) rewrites history by moving HEAD. reset is fine for local/private branches but dangerous on shared/public branches because it changes commit hashes and requires force-pushing to update the remote.

### Why rewriting public history is discouraged

Rewriting public history (via git commit --amend, git rebase, or git reset and then force-pushing) changes commit hashes. Other collaborators who already pulled the old commits will get conflicts and problems when you force-push new history. Use revert for safe undoing on branches shared with others; only rewrite history on local/private branches or after coordinating with your team.


## **Task 8: Tagging and Releases**
### **Command Used**

```bash
git tag -a v1.0 -m "Release 1.0"
git push origin v1.0
git push --tags
git tag

```

### **Output**

```bash
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 16 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (17/17), 1.60 KiB | 56.00 KiB/s, done.
Total 17 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), done.
To https://github.com/sabyasachiGorai/git-assignment
 * [new tag]         v1.0 -> v1.0
 
 Everything up-to-date

v1.0
```
