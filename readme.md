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
