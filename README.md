## Basic Commands of Linux and Mac

### 1. General Commands

```
pwd
```
Prints the current working directory.

```
clear
```
Clears the terminal screen.


### 2. Listing files and directories

```
ls
```
Lists the files and directories in the current working directory.

```
ls -l
```
Lists all the files and directories including the hidden files and directories.

```
ls -a
```
Lists the files and directories in the folderName directory.

### 3. Navigation

```
cd folderName
```
Changes the current working directory to folderName.

```
cd ..
```
Changes the current working directory to the parent directory.

```
cd ~
```
Changes the current working directory to the home directory.

```
cd -
```
Changes the current working directory to the previous working directory.

```
cd path # e.g. cd /home/user/Desktop
```
Changes the current working directory to the path directory.

### 4. Creating files and directories

```
mkdir folderName
```
Creates a new directory named folderName.

```
touch fileName
```
Creates a new file named fileName.

```
touch fileName1 fileName2 fileName3
```
Creates three new files named fileName1, fileName2, and fileName3.

```
touch fileName.{html,css,js}
```
Creates three new files named fileName.html, fileName.css, and fileName.js.

### 5. Copying files and directories

```
cp fileName1 fileName2
```
Copies the contents of fileName1 to fileName2.

```
cp -r folderName1 folderName2
```
Copies the contents of folderName1 to folderName2.

### 6. Moving files and directories

```
mv fileName1 fileName2
```
Moves the contents of fileName1 to fileName2.

```
mv folderName1 folderName2
```
Moves the contents of folderName1 to folderName2.

### 7. Removing files and directories

```
rm fileName
```
Removes the fileName file if it exists.

```
rm -r folderName
```
Removes the folderName directory and its contents recursively.

```
rm -f fileName
```
Removes the fileName file without prompting for confirmation.

```
rm -rf folderName
```
Removes the folderName directory without prompting for confirmation recursively.

```
rm -rf folderName1 folderName2
```
Removes the folderName1 and folderName2 directories without prompting for confirmation recursively.

```
rmdir folderName
```
Removes the folderName directory if it is empty.

### 8. Viewing files

```
cat fileName
```
Displays the contents of fileName.

```
less fileName
```
Displays the contents of fileName one page at a time.

```
head fileName
```
Displays the first 10 lines of fileName.

```
head -n 5 fileName
```
Displays the first 5 lines of fileName.

```
tail fileName
```
Displays the last 10 lines of fileName.

```
tail -n 5 fileName
```
Displays the last 5 lines of fileName.

```
tail -f fileName
```
Displays the last 10 lines of fileName and monitors fileName for any changes.

## Basic Commands of Git

### 1. General Commands

```
git --version
```
Displays the current version of Git.

```
git config --global user.name "Your Name"
```
Sets the name you want attached to your commit transactions.

```
git config --global user.email "youremail@domain"
```
Sets the email you want attached to your commit transactions.

```
git config --global color.ui auto
```
Enables helpful colorization of command line output.

```
git config --list
```
Lists all the configuration settings you’ve ever specified.

```
git help command
```
Displays the manual for command.

```
git command --help
```
Displays the manual for command.

```
git command -h
```
Displays the manual for command.

### 2. Creating repositories

```
git init
```
Creates a new local repository with the specified name in the current directory. 

Output:
```
Initialized empty Git repository in /home/user/Desktop/.git/
```

```
git clone
```
Downloads a project and its entire version history from a remote repository.

### 3. Making changes

```
git status
```
Lists all new or modified files to be committed in the current repository and also lists all the files that are not yet staged.
git status provides a summary of the state of both the working directory and the staging area.
1. Provides the branch name.
2. Lists all the files that are not yet staged. **(Untracked files)**
3. Lists all the files that are staged. **(Changes to be committed)**


Outputs
```
On branch master
nothing to commit, working tree clean
```

```
git diff
```
Shows file differences not yet staged.

Outputs
```
diff --git a/fileName b/fileName
index 0123456..789abcde 100644
--- a/fileName
+++ b/fileName
@@ -1 +1,2 @@
-Hello World
+Hello World!
+Goodbye ...
```

```
git add .
```
Add all the files in the current directory to the staging area and prepares them for versioning.

Before adding the files to the staging area, the output of git status is:
```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        anotherTest.html
```

After adding the files to the staging area, the output of git status is:
```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   anotherTest.html
```
    
```
git add fileName
```
Adds the fileName file to the staging area and prepares it for versioning.

```
git add fileName1 fileName2 fileName3
```
Adds the fileName1, fileName2, and fileName3 files to the staging area and prepares them for versioning.

### 4. Committing changes

```
git commit -m "Commit message"
```
Save the staged snapshot to the project history.

Before committing the files, the output of git status is:
```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   anotherTest.html
```

After committing the files, the output of git status is:
```
On branch master
nothing to commit, working tree clean
```

```
git commit -am "Commit message"
```
Stage all modified files and commit them to the repository in one command. The -a option is a shortcut that tells Git to automatically stage every file that is already tracked before doing the commit, letting you skip the git add part.

Note: ***The -a option doesn’t tell Git to add new files, so you still need to use git add the first time you want to add a new file.***

### 5. Branching

```
git branch
```
Lists all the local branches in the current repository.

Output:
```
* master
```

```
git branch branchName
```
Creates a new branch named branchName.

After creating the branch, the output of git branch is:
```
* master
  branchName
```

```
git checkout branchName or git switch branchName
```
Switches to the specified branch and updates the working directory. Checkout command is used to switch from one branch to another but it is also used to do the following tasks:
1. Create a new branch.
2. Create a new branch and switch to it.
3. Discard changes in the working directory.
4. Restore the working directory to match the last commit.

so, git switch is introduced in Git 2.23 as a more intuitive alternative to git checkout.

```
git checkout -b branchName or git switch -c branchName
```
Creates a new branch named branchName and switches to it and updates the working directory.

```
git branch -d branchName
```
Deletes the specified branch.

```
git merge branchName
```
Combines the specified branch’s history into the current branch.

### 6. Updating repositories

```
git pull
```
Fetches and merges changes on the remote server to your working directory.
```
git push remoteName branchName
```
Pushes all the modified local objects to the remote repository and advances its branches.

### 7. Inspecting a repository

```
git log
```
Lists version history for the current branch.

```
git log --follow fileName
```
Lists version history for a file, including renames.

```
git diff branchName1 branchName2
```
Shows the differences between two branches.

```
git show commitID
```
Outputs metadata and content changes of the specified commit.

### 8. Undoing changes

```
git reset commitID
```
Undoes all commits after commitID, preserving changes locally.

```
git reset --hard commitID
```
Discards all history and changes back to the specified commitID and deletes all the uncommitted changes.

```
git reset --soft commitID
```
Undoes the commit and leave all your changed files "Changes to be committed", as git status would put it.

```
git reset --mixed commitID
```
Undoes the commit and unstage all your changed files, so that git status would report nothing.

```
git reset HEAD fileName
```
Unstages the file, but preserve its contents.

```
git checkout -- fileName
```
Discards all changes to the fileName file.

```
git revert commitID
```
Creates a new commit that undoes all of the changes made in commitID, then apply it to the current branch.


## Basic Flow of Git in Project

### 1. Create a new repository

```
git init
```
Creates a new local repository with the specified name in the current directory.

### 2. Create a new file

```
touch fileName
```
Creates a new file named fileName.

### 3. Add the file to the staging area

```
git add fileName
```
Adds the fileName file to the staging area and prepares it for versioning.

### 4. Commit the file

```
git commit -m "Commit message"
```
Save the staged snapshot to the project history.

### 5. Add a remote repository

```
git remote add origin remoteRepositoryURL
```
Adds a remote repository named origin at the specified URL.

### 6. Push the changes to the remote repository

```
git push -u origin master
```
Pushes the changes in the local repository up to the remote repository.

### 7. Pull the changes from the remote repository

```
git pull origin master
```
Fetches and merges changes on the remote server to your working directory.


## Points to Remember

Q. Differentiate & Demonstrate b/w git reset Hard, soft & mixed?
A. git reset --hard commitID
   Discards all history and changes back to the specified commitID and deletes all the uncommitted changes.

   git reset --soft commitID
   Undoes the commit and leave all your changed files "Changes to be committed", as git status would put it.

   git reset --mixed commitID
   Undoes the commit and unstage all your changed files, so that git status would report nothing.

Q. how to reset the commit and force push it?
A. First, get the commit ID using git log command.
```
git log
```
Then, reset the commit using git reset command.
```
git reset --hard commitID
```
Then, do some changes in the code and commit it again.
```
git commit -am "Commit message"
```
Finally, force push the commit using git push command.
```
git push -f origin branchName
```

if you want to reset the commit and force push it in the master branch, then you can use the following command.
```
git push -f origin master
```
Here is the complete example.
```
git log
git reset --hard 0d1d7fc32
git commit -am "Commit message"
git push -f origin master
```
Here -f stands for force push. if -f is not used, then you will get the following error.
```
error: failed to push some refs to '
```



