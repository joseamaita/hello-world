# Git Cheat Sheet

## CREATE REPOSITORIES

Start a new repository or obtain one from an existing URL

### Create a new local repository

```
$ git init
```

```
$ git init [project-name.git]
```

### Clone an existing repository by using the HTTPS protocol

```
$ git clone https://domain/user/repo.git
```

```
$ git clone https://domain/user/repo.git repo.git
```

### Clone an existing repository by using the SSH protocol

```
$ git clone ssh://user@domain.com/repo.git
```

```
$ git clone ssh://user@domain.com/repo.git repo.git
```

## GETTING HELP

Review pages of the command Git manual

### Shows help on 'init' command

```
$ git init --help
```

### Shows help on 'clone' command

```
$ git clone --help
```

## MAKE CHANGES

Review edits and craft a commit transaction

### Lists all new or modified files to be committed

```
$ git status
```

### Shows file differences not yet staged

```
$ git diff
```

### Snapshots the file in preparation for versioning

```
$ git add name_of_the_file
```

### Snapshots all the files in the current folder

```
$ git add .
```

### Shows file differences between staging and the last file version

```
$ git diff --staged
```

### Unstages the file, but preserve its contents

```
$ git reset name_of_the_file
```

### Records file snapshots permanently in version history

```
$ git commit -m "this is a commit message"
```

## GROUP CHANGES

Name a series of commits and combine completed efforts

### Lists all local branches in the current repository

```
$ git branch
```

### Creates a new branch

```
$ git branch name_of_the_branch
```

### Switches to the specified branch or tag and updates the working directory

```
$ git checkout name_of_the_branch_or_tag
```

### Combines the specified branch's history into the current branch

```
$ git merge name_of_the_branch_with_the_changes
```

### Deletes the specified branch

```
$ git branch -d name_of_the_branch
```

## REFACTOR FILENAMES

Relocate and remove versioned files

### Deletes the file from the working directory and stages the deletion

```
$ git rm name_of_the_file
```

### Removes the file from version control but preserves the file locally

```
$ git rm --cached name_of_the_file
```

### Changes the file name and prepares it for commit

```
$ git mv name_of_the_file-original name_of_the_file-renamed
```

## REVIEW HISTORY

Browse and inspect the evolution of project files

### Lists version history for the current branch

```
$ git log
```

### Lists version history for a file, including renames

```
$ git log --follow name_of_the_file
```

### Shows content differences between two branches

```
$ git diff name_of_first_branch_or_tag name_of_second_branch_or_tag
```

### Outputs metadata and content changes of the specified commit

```
$ git show commit_number
```

## REDO COMMITS

Erase mistakes and craft replacement history

### Undoes all commits after the specified commit, preserving changes locally

```
$ git reset commit_number
```

### Undo last commit

```
$ git reset --soft HEAD~1
```

### Discards all history and changes back to the specified commit

```
$ git reset --hard commit_number
```
