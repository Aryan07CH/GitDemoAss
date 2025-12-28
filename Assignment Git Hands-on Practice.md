
## **Assignment: Git Hands-on Practice**

### **Task 1: Configure Git**

1. Set your username and email in Git.
2. Verify the configuration.

**Expected Output:**

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/Assignment
$ git congif --global user.name "Aryan07CH"
git: 'congif' is not a git command. See 'git --help'.

The most similar command is
        config


aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/Assignment
$ git config --global user.email "aryanchogale3@gmail.com"

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/Assignment
$ git config list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
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
core.editor="C:\Users\aryan\AppData\Local\Programs\Microsoft VS Code\bin\code" --wait
user.name=Aryan07CH
user.email=aryanchogale3@gmail.com


Screenshot or command output showing configured username and email.


### **Task 2: Initialize a Local Repository**

1. Create a new folder named `git-hands-on`.
2. Initialize it as a Git repository.
3. Check the repository status.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on
$ git init
Initialized empty Git repository in C:/Users/aryan/Desktop/CDAC/SDM/git-hands-on/.git/

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt

nothing added to commit but untracked files present (use "git add" to track)

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$


### **Task 3: Create and Track Files**

1. Create a file named `documentation.txt`.
2. Add a short project description inside it.
3. Check file status.
4. Stage the file.
5. Commit the changes with an appropriate message.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ nano documentation.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt
        documentation.txt

nothing added to commit but untracked files present (use "git add" to track)

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git add documentation.txt
warning: in the working copy of 'documentation.txt', LF will be replaced by CRLF the next time Git touches it

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git add documentation.txt -A

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ nano documentation.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git commit -m "Documentation File Commited"
[master (root-commit) 10d3698] Documentation File Commited
 1 file changed, 1 insertion(+)
 create mode 100644 documentation.txt



### **Task 4: Modify and Commit Changes**

1. Edit `documentation.txt` and add one more line.
2. View the differences between working directory and staging area.
3. Stage and commit the changes.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git diff
warning: in the working copy of 'documentation.txt', LF will be replaced by CRLF the next time Git touches it
diff --git a/documentation.txt b/documentation.txt
index 486015e..5a797ee 100644
--- a/documentation.txt
+++ b/documentation.txt
@@ -1 +1,3 @@
 Update All Project Changes Here
+
+Add all dependencies in this file
\ No newline at end of file

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git commit -m "Documentation with Dependencies File Commited"
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   documentation.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt

no changes added to commit (use "git add" and/or "git commit -a")

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git add documentation.txt -A

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git commit -m "Documentation with Dependencies File Commited"
[master a448b58] Documentation with Dependencies File Commited
 1 file changed, 2 insertions(+)



### **Task 5: View Commit History**

1. View the complete commit history.
2. View commit history in one-line format.

Output:-

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git log
commit a448b580920d50aa6ec475ad27191a36a5de33e4 (HEAD -> master)
Author: Aryan07CH <aryanchogale3@gmail.com>
Date:   Sun Dec 28 16:27:05 2025 +0530

    Documentation with Dependencies File Commited

commit 10d369825f3b8c4bc5ae577d3696e5ccb152bacd
Author: Aryan07CH <aryanchogale3@gmail.com>
Date:   Sun Dec 28 16:24:41 2025 +0530

    Documentation File Commited

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git log --pretty=oneline
a448b580920d50aa6ec475ad27191a36a5de33e4 (HEAD -> master) Documentation with Dep
endencies File Commited
10d369825f3b8c4bc5ae577d3696e5ccb152bacd Documentation File Commited


### **Task 6: Create and Work with Branches**

1. Create a new branch named `feature-1`.
2. Switch to the new branch.
3. Create a new file `feature.txt`.
4. Commit the changes.
5. Switch back to the main branch.


Output:-

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git checkout -b feature-1
Switched to a new branch 'feature-1'

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (feature-1)
$ nano feature.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (feature-1)
$ git commit -m "Features File Commited"
On branch feature-1
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt
        feature.txt

nothing added to commit but untracked files present (use "git add" to track)

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (feature-1)
$ git add feature.txt -A

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (feature-1)
$ git commit -m "Features File Commited"
[feature-1 f68d47a] Features File Commited
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (feature-1)
$ git checkout master
Switched to branch 'master'


### **Task 7: Merge Branches**

1. Merge `feature-1` branch into `main`.
2. Verify the merge using commit history.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git merge feature-1
Updating a448b58..f68d47a
Fast-forward
 feature.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git log
commit f68d47ad6ee95f230b25f0d882e270553e954b4e (HEAD -> master, feature-1)
Author: Aryan07CH <aryanchogale3@gmail.com>
Date:   Sun Dec 28 16:31:08 2025 +0530

    Features File Commited

commit a448b580920d50aa6ec475ad27191a36a5de33e4
Author: Aryan07CH <aryanchogale3@gmail.com>
Date:   Sun Dec 28 16:27:05 2025 +0530

    Documentation with Dependencies File Commited

commit 10d369825f3b8c4bc5ae577d3696e5ccb152bacd
Author: Aryan07CH <aryanchogale3@gmail.com>
Date:   Sun Dec 28 16:24:41 2025 +0530

    Documentation File Commited


### **Task 8: Connect to a Remote Repository**

1. Create a new repository on GitHub.
2. Add the remote repository URL to your local repo.
3. Verify the remote connection.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git remote -v

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git remote add origin https://github.com/Aryan07CH/GitDemoAss.git

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git remote -v
origin  https://github.com/Aryan07CH/GitDemoAss.git (fetch)
origin  https://github.com/Aryan07CH/GitDemoAss.git (push)



### **Task 9: Push Code to GitHub**

1. Push the `main` branch to GitHub.
2. Verify files on GitHub.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git push origin master
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (9/9), 939 bytes | 469.00 KiB/s, done.
Total 9 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Aryan07CH/GitDemoAss.git
   15cffb8..de2e6e1  master -> master



### **Task 10: Clone a Repository**

1. Clone the same GitHub repository into a different folder.
2. Verify the cloned content.

Output:-

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/clone-gitHands-on
$ git clone https://github.com/Aryan07CH/GitDemoAss.git
Cloning into 'GitDemoAss'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 12 (delta 1), reused 9 (delta 1), pack-reused 0 (from 0)
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (1/1), done.


### **Task 11: Undo Changes**

1. Make a change in `documentation.txt` but do not commit.
2. Discard the changes.
3. Verify the file status.

Output:-
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM
$ cd git-hands-on

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ nano documentation.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   documentation.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt

no changes added to commit (use "git add" and/or "git commit -a")

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ nano documentation.txt

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   documentation.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt

no changes added to commit (use "git add" and/or "git commit -a")

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$



### **Task 12: Remove Files**9

1. Delete `feature.txt` using Git.
2. Commit the deletion.

Output:-

aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git rm --cached feature.txt
rm 'feature.txt'
aryan@ARYAN MINGW64 ~/Desktop/CDAC/SDM/git-hands-on (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    feature.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Assignment Git Hands-on Practice.txt
        feature.txt


## **Submission Guidelines**

* Submit screenshots or terminal output for each task
* Provide GitHub repository link
* Ensure commit messages are meaningful

