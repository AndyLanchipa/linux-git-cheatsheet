# Linux & Git Command Cheat Sheet

_Built in Vim, one branch per command._

### `pwd`
**What it does:** Prints the current working directory.  

**Example:**
```bash
pwd

### `ls`
**What it does:** Lists files and directories in the current directory.  

**Examples:**
```bash
ls
ls -lah

### `mkdir`
**What it does:** Creates a new directory.  

**Flags:**
- `-p` → create parent directories if needed  
- `-v` → print a message for each directory created  
- `-m <mode>` → set permissions for the new directory using chmod-style syntax  

**Example:**
```bash
mkdir -p sample_directory

### `rm`
**What it does:** Removes files or directories.  

**Flags:**
- `-r` → recursive (delete directories and their contents)  
- `-f` → force (ignore prompts/errors)  

**Example:**
```bash
rm -rf old_folder

### `cp`
**What it does:** Copies files or directories.  

**Flags:**
- `-r` → copy directories recursively  
- `-v` → verbose, show files being copied  
- `-i` → prompt before overwrite  

**Example:**
```bash
cp file.txt backup.txt

### `mv`
**What it does:** Moves or renames files and directories.  

**Flags:**
- `-i` → prompt before overwrite  
- `-v` → verbose, show what is happening  

**Example:**
```bash
mv old.txt new.txt

### `grep`
**What it does:** Searches for text patterns inside files.  

**Flags:**
- `-i` → case-insensitive search  
- `-r` → recursive, search through directories  
- `-n` → show line numbers  
- `--color` → highlight matches  

**Example:**
```bash
grep "main" file.txt


### `git status`
**What it does:** Shows the state of the working directory and staging area.  

**Flags:**  
- _(none)_  

**Example:**
```bash
git status

### `git add`
**What it does:** Stages changes so they're ready to be committed.  

**Flags:**
- `.` → add everything in the current directory  
- `<file>` → add a specific file  
- `-p` → interactively choose hunks of changes  

**Example:**
```bash
git add file.txt


### `git commit`
**What it does:** Records staged changes into the repository history.  

**Flags:**
- `-m` → add a commit message inline  
- `-a` → automatically stage tracked files before committing  
- `--amend` → change the most recent commit  

**Example:**
```bash
git commit -m "docs: add grep section"


### `git log`
**What it does:** Shows the commit history of the repository.  

**Flags:**
- `--oneline` → compact one-line output per commit  
- `--graph` → show ASCII graph of branches and merges  
- `--decorate` → show branch and tag names  
- `-p` → show the patch (changes) each commit introduced  

**Examples:**
```bash
git log
git log --oneline --graph --decorate
git log -p


### `git branch`
**What it does:** Lists, creates, or deletes branches.  

**Flags:**
- _(no flags)_ → list branches  
- `-d` → delete a branch  
- `-m` → rename a branch  

**Examples:**
```bash
git branch
git branch new-feature
git branch -d old-feature
git branch -m old-name new-name

### `git switch`
**What it does:** Switches between branches.  

**Flags:**
- `-c` → create and switch to a new branch  

**Examples:**
```bash
git switch main
git switch -c feature-login

### `git merge`
**What it does:** Combines changes from another branch into the current branch.  

**Flags:**
- `--no-ff` → create a merge commit even if fast-forward is possible  

**Examples:**
```bash
git merge feature-branch
git merge --no-ff feature-branch

---

### `git clone`
**What it does:** Creates a local copy of a remote repository.  

**Flags:**
- `<url>` → clone from a remote URL (HTTPS or SSH)  
- `<directory>` → optional, specify folder name for the clone  
- `--branch <name>` → clone a specific branch  

**Examples:**
```bash
git clone git@github.com:user/repo.git
git clone https://github.com/user/repo.git my-folder
git clone --branch main git@github.com:user/repo.git

