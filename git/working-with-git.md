# Working with Git

Here we present some examples when working with Git on the command line.

## CREATE REPOSITORIES

### Create a new local repository

```
$ mkdir my-repo
$ cd my-repo
$ git init my-repo.git
Initialized empty Git repository in /.../my-repo/my-repo.git/.git/
```

### Clone an existing remote repository by using the HTTPS protocol

```
$ mkdir fullstackpython
$ cd fullstackpython
$ git clone https://github.com/mattmakai/fullstackpython.com.git fullstackpython.com.git
Cloning into 'fullstackpython.com.git'...
remote: Counting objects: 38616, done.
remote: Compressing objects: 100% (400/400), done.
Receiving objects:   8% (3128/38616), 11.28 MiB | 30.00 KiB/s
remote: Total 38616 (delta 230), reused 0 (delta 0), pack-reused 38208
Receiving objects: 100% (38616/38616), 53.02 MiB | 113.00 KiB/s, done.
Resolving deltas: 100% (29007/29007), done.
Checking connectivity... done.
```

### Clone an existing remote repository by using the SSH protocol

```
$ mkdir Pyro4
$ cd Pyro4
$ git clone git@github.com:irmen/Pyro4.git Pyro4.git
Cloning into 'Pyro4.git'...
remote: Counting objects: 12464, done.
remote: Compressing objects: 100% (19/19), done.
remote: Total 12464 (delta 5), reused 0 (delta 0), pack-reused 12442
Receiving objects: 100% (12464/12464), 4.50 MiB | 177.00 KiB/s, done.
Resolving deltas: 100% (7701/7701), done.
Checking connectivity... done.
```

## GETTING HELP

Review pages of the command Git manual

### Shows help on 'init' command

```
$ git init --help
GIT-INIT(1)                    Git Manual                   GIT-INIT(1)

NAME
       git-init - Create an empty Git repository or reinitialize an
       existing one

SYNOPSIS
       git init [-q | --quiet] [--bare] [--template=<template_directory>]
                 [--separate-git-dir <git dir>]
                 [--shared[=<permissions>]] [directory]

DESCRIPTION
       This command creates an empty Git repository - basically a .git
       directory with subdirectories for objects, refs/heads,
       refs/tags, and template files. An initial HEAD file that
       references the HEAD of the master branch is also created.

       If the $GIT_DIR environment variable is set then it specifies a
       path to use instead of ./.git for the base of the repository.

       If the object storage directory is specified via the
       $GIT_OBJECT_DIRECTORY environment variable then the sha1
       directories are created underneath - otherwise the default ...
```

### Shows help on 'clone' command

```
$ git clone --help
GIT-CLONE(1)                   Git Manual                  GIT-CLONE(1)

NAME
       git-clone - Clone a repository into a new directory

SYNOPSIS
       git clone [--template=<template_directory>]
                 [-l] [-s] [--no-hardlinks] [-q] [-n] [--bare] [--mirror]
                 [-o <name>] [-b <name>] [-u <upload-pack>] [--reference <repository>]
                 [--separate-git-dir <git dir>]
                 [--depth <depth>] [--[no-]single-branch]
                 [--recursive | --recurse-submodules] [--] <repository>
                 [<directory>]

DESCRIPTION
       Clones a repository into a newly created directory, creates
       remote-tracking branches for each branch in the cloned
       repository (visible using git branch -r), and creates and checks
       out an initial branch that is forked from the cloned
       repository’s currently active branch.

       After the clone, a plain git fetch without arguments will ...
```

## MAKE CHANGES

Craft a commit transaction and review edits

### Create and edit a file to be committed

```
$ cd /my-repo/my-repo.git
$ touch index.html
$ echo "<h3>INDEX - LINE #1</h3>" > index.html
```

### Lists all new or modified files to be commited

```
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	index.html

nothing added to commit but untracked files present (use "git add" to track)
```

### Snapshots the file in preparation for versioning

```
$ git add index.html
```

### Checks status again

```
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   index.html
```

### Snapshots all the files in the current folder

```
$ git add .
```

### Shows file differences between staging and the last file version

```
$ git diff --staged
diff --git a/index.html b/index.html
new file mode 100644
index 0000000..3dd7afb
--- /dev/null
+++ b/index.html
@@ -0,0 +1 @@
+<h3>INDEX - LINE #1</h3>
```

### Unstages the file, but preserve its contents

```
$ git reset index.html
```

### Checks status again

```
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	index.html

nothing added to commit but untracked files present (use "git add" to track)
```

### Records file snapshots permanently in version history

```
$ git add index.html
$ git commit -m "Initial commit"
[master (root-commit) 6d4f552] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 index.html
```
