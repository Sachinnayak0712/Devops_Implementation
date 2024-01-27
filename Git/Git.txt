GIT COMMAND
Repository: - DevopsFiles
USERNAME:- Sachinnayak0712
PASSWORD:- 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

***********************************************************************
Creating new repository and adding newly in to the reposiroty
***********************************************************************

1) Setup the name abd email for GIT to use when you commit
git config --global user.name “[firstname lastname]”
git config --global user.email “[valid-email]”

git config --global user.name “Sachin Nayak”
git config --global user.email “nayaksachin0712@gmail.com”

2) Create a directory

3) Initialize dir
git init

4) Create a file/ Directory(git only track file not directory if a directory has no file it will not track)

5) Inset into staging area
git add .
(Will add all the file in to staging area)
git add text.txt 
(will add that secific ile in to staging area)

6) Create Remote repository in git

7) Commit the code
 git commit -m “[descriptive message]”
Ex:
git commit -m "firstcommit"

8)Adding to repository
 git remote add origin <git httpslink>
ex:
git remote add origin https://github.com/Sachinnayak0712/CleanWork.git

9)Adding to which branch
git branch -M main

10) Push the file in to repository
git push -u origin main

<File will be present in git centralized repository>

*****************************************************************************
Make changes and add in to repository
1)Make changes
vim saturn1.txt

2) check the status
 git status

On branch main
Your branch is up to date with 'origin/main'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   saturn1.txt

no changes added to commit (use "git add" and/or "git commit -a")

3) commit the changes file
git add saturn1.txt

warning: in the working copy of 'saturn1.txt', LF will be replaced by CRLF the next time Git touches it
##############	
git status

On branch main
Your branch is up to date with 'origin/main'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   saturn1.txt

4)Complete the commit
 git commit -m "saturn1 change comit"

[main a7a54e1] saturn1 change comit
 1 file changed, 1 insertion(+)

5)Push the code to repository
git push origin main

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 281 bytes | 281.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Sachinnayak0712/Devops-Files.git
   6d3d285..a7a54e1  main -> main


*********************************************************************
Create new branch locally
git branch -c <Branch_name>
Ex:
git branch -c sprint1

Check all the branch
git branch -a

Switch from one branch to another
git checkout <Branch_name>
Ex:
git checkout sprint1
	OR
git switch <Branch_name>
Ex:
git switch sprint1

Remove some file from new branch
git rm <file_name ....>
Ex
git rm saturn7.txt saturn8.txt saturn9.txt
#######################
git status
On branch sprint1
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    saturn7.txt
        deleted:    saturn8.txt
        deleted:    saturn9.txt

If there is file which cannot be deleted or removed
Add it in to the git ignore using
vim .gitignore
with in the file enter 
*.log
and save it

Merge 








