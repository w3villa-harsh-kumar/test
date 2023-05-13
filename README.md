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

#### 1.1. git --version
Displays the current version of Git.

#### 1.2. git config --global user.name "Your Name"
Sets the name you want attached to your commit transactions.

#### 1.3. git config --global user.email "youremail@domain"
Sets the email you want attached to your commit transactions.

#### 1.4. git config --global color.ui auto
Enables helpful colorization of command line output.

#### 1.5. git config --list
Lists all the configuration settings you’ve ever specified.

#### 1.6. git help command
Displays the manual for command.

#### 1.7. git command --help
Displays the manual for command.

#### 1.8. git command -h
Displays the manual for command.

### 2. Creating repositories

#### 2.1. git init
Creates a new local repository with the specified name.

#### 2.2. git clone
Downloads a project and its entire version history.

### 3. Making changes

#### 3.1. git status
Lists all new or modified files to be committed.

#### 3.2. git diff
Shows file differences not yet staged.

#### 3.3. git add .
Snapshots all the files in preparation for versioning and adds them to the staging area.

#### 3.4. git add fileName
Snapshots the file in preparation for versioning and adds it to the staging area.

#### 3.5. git add fileName1 fileName2 fileName3
Snapshots the files in preparation for versioning and adds them to the staging area.

### 4. Committing changes

#### 4.1. git commit -m "Commit message"
Records file snapshots permanently in version history.

#### 4.2. git commit -am "Commit message"
Snapshots all the files in preparation for versioning and records file snapshots permanently in version history.

### 5. Branching

#### 5.1. git branch
Lists all the local branches in the current repository.

#### 5.2. git branch branchName
Creates a new branch named branchName.

#### 5.3. git checkout branchName or git switch branchName
Switches to the specified branch and updates the working directory.

#### 5.4. git checkout -b branchName or git switch -c branchName
Creates a new branch named branchName and switches to it.

#### 5.5. git branch -d branchName
Deletes the specified branch.

#### 5.6. git merge branchName
Combines the specified branch’s history into the current branch.

### 6. Updating repositories

#### 6.1. git pull
Fetches and merges changes on the remote server to your working directory.

#### 6.2. git push
Pushes all the modified local objects to the remote repository and advances its branches.

### 7. Inspecting a repository

#### 7.1. git log
Lists version history for the current branch.

#### 7.2. git log --follow fileName
Lists version history for a file, including renames.

#### 7.3. git diff branchName1 branchName2
Shows the differences between two branches.

#### 7.4. git show commitID
Outputs metadata and content changes of the specified commit.

### 8. Undoing changes

#### 8.1. git reset commitID
Undoes all commits after commitID, preserving changes locally.

Q. Differentiate & Demonstrate b/w git reset Hard, soft & mixed!
A. git reset --hard: This command throws away all your uncommitted changes. It resets your working directory to the state it was in right after your last commit. It also resets the index to match it.

git reset --soft: This command resets the HEAD to another commit, so index and the working directory will not be altered in any way.

git reset --mixed: This command resets the HEAD and index to another commit, but not the working directory. The changes in the files are preserved but not marked for commit.





