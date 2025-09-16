# Linux & Git Command Cheat Sheet

_Built in Vim, one branch per command._

##Command -> pwd
What does it do -> Prints the current working directory

##Command -> ls

What does it do -> lists files and directories in the current directory

## Command -> mkdir

What does it do -> creates a new directory 

Flags:
# -p -> create parent directories if needed
# -v -> print a message for each directory created
# -m <mode> -> set permissions for the new directory, using chmod-style syntax

Example:
# mkdir <Sample directory>

##Command -> rm

What it does -> Removes files or directories

Flags:
# -r -> recursive (delete directories and their contents)
# -f -> force (ignore prompts/errors)

Example:
# rm -rf-old_folder

##Command -> cp

What it does -> copies files or directories

Flags:
# -r -> copy directories recursively
# -v -> verbose, show files being copied
# -i -> prompt before overwrite

Example:
#cp file.txt backup.txt

##Command -> mv

What it does -> moves or renames files and directories

Flags:
# -i -> prompt before overwrite 
# -v -> verbose, show what is happening 

Examples:
# mv old.txt new.txt

##Command -> grep

What it does -> searches for text patterns inside files

Flags:
# -i -> case-insensitive search
# -r -> recursive, search through directories 
# -n -> show line number
# --color -> highlight matches

Example: 
# grep "main" file.txt

##Command -> git status

What it does -> shows the state of the working directory and stating area

Flags:
# none

Example:
# git status


##Command -> git add

What it does -> Stages changes so they're ready to be committed

Flags:
# . -> add everyrthing in the current directory
# <file> -> add a specific file
# -p -> interactively choose hunks of changes

Example:
# git add file.txt

##Command -> git commit 

What it does -> Records stages changes into the repository history

Flags:
# -m -> add a commit message inline
# -a -> automatically stage tracked files before committing
# --amend -> change the most recent commit

Example:
# git commit -m "docs: add grep section"



##Command -> git log

What it does: Shows the commit history of the repository.

Flags:
# `--oneline` → compact one-line output per commit
# `--graph` → show ASCII graph of branches and merges
# `--decorate` → show branch and tag names
# `-p` → show the patch (changes) each commit introduced

Examples:
# git log
# git log --oneline --graph --decorate
# git log -p

##Command -> git branch

What does it do: Lists, creates, or deletes branches.

Flags:
# no flags → list branches
# -d → delete a branch
# -m → rename a branch

Examples:
# git branch
# git branch new-feature
# git branch -d old-feature
# git branch -m old-name new-name


##Command -> git switch

What does it do: Switches between branches.

Flags:
# -c → create and switch to a new branch

Examples:
# git switch main
# git switch -c feature-login

##Command -> git merge

What does it do: Combines changes from another branch into the current branch.

Flags:
# --no-ff → create a merge commit even if fast-forward is possible

Examples:
# git merge feature-branch
# git merge --no-ff feature-branch

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

