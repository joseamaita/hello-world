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
