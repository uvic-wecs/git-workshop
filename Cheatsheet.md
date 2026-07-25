# Command Line & Git Cheatsheet
This file contains some common commands for using a command line or Git.

## Common commands for bash

### Change directory
```bash
cd new-directory # to move to a folder called new-directory
cd .. # to move into the parent folder
```

### List
```bash
ls # list files in current directory
ls my_folder # list files in a specific directory (called my_folder)
ls -a # show all files, including hidden ones
ls -l # list files with more information
```

### Copy
```bash
cp <current path to file> <new path where file should be copied>
cp ../file1 ./file_copies/file1 # for example, using relative file paths
```

### Move
```bash
mv <current location> <new location>
mv <current name> <new name> # This also works for renaming files
```

### Concatenate
```bash
cat filename # Prints contents of the file to the terminal
cat file1 file2 # Prints concatenated file contents
```

### Echo
```bash
echo "A string to print" # Prints a string
echo $VAR # Prints the value of a variable
```

### Touch
```bash
touch file # Create a new file named "file" if it doesn't already exist
```

### Remove
```bash
rm file # PERMANENTLY deletes a file
rm -r folder-name # Recursively deletes a folder and its contents
```

### Pipelines
```bash
cat some-file > output.txt # Pipe output of cat into a file using >
```

## Common Git commands

`git clone <url>`: Make a copy of a repository

`git init`: Make a new repository or add Git tracking to an existing directory

`git branch`: View all branches in your repository
`git branch <name>`: Create a new branch

`git checkout`: Change branches
`git checkout -b <name>`: Change to a new branch

`git switch`: Change branches cleverly (Git will do some extra work, like set that branch to track an upstream one)

`git status`: Check the status of your repo and current changes

`git diff <file>`: See the difference between your working copy of a file and the last committed version, or between different commits

`git add <path>`: Stage changes in your repo

`git commit`: Commit all staged changes, you will be prompted for a message to describe the commit
`git commit -m <message>`: Include your commit message in the command

`git push`: Push changes from your local repo to the remote one
`git push -u <remote> <branch>`: Push a local branch to the remote, you must specify which remote and the branch name (which must match the local branch)

`git pull`: Pull changes from the remote into your local branch, pull changes from a different branch by specifying the remote and branch name

`git revert`: Undo a commit by making exactly opposite changes

`git restore`: Undo changes which aren’t staged/committed, or use with --staged to unstage changes you’ve added

`git stash`: Save current untracked changes, but remove them from the working directory. The changes are pushed to a stack, and can be added back with `git stash apply`

`git log`: View the commit history

`git rebase`: Edit the commit history. Include the --interactive flag to manually edit the history, and specify the remote and branch name or commit to rebase on a specific commit.
