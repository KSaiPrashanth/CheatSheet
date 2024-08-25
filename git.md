# GIT CHEAT SHEET
This cheat sheet features the most important and commonly used Git commands for easy reference.

## Index
  - [SETUP](#setup)
  - [SETUP \& INIT](#setup--init)
  - [STAGE \& SNAPSHOT](#stage--snapshot)
  - [BRANCH \& MERGE](#branch--merge)
  - [INSPECT \& COMPARE](#inspect--compare)
  - [SHARE \& UPDATE](#share--update)
  - [TRACKING PATH CHANGES](#tracking-path-changes)
  - [REWRITE HISTORY](#rewrite-history)
  - [TEMPORARY COMMITS](#temporary-commits)
  - [IGNORING PATTERNS](#ignoring-patterns)

<br>

## SETUP
Configuring user information used across all local repositories

- **Set a name** that is identifiable for credit when review version history
  ```bash
  git config --global user.name "[UserName]"
  ```

- **Set an email address** that will be associated with each history marker
  ```bash
  git config --global user.email "[valid-email]"
  ```
    
- Set automatic command line **coloring for Git** for easy reviewing
  ```bash
  git config --global color.ui auto
  ```

<br>

## SETUP & INIT
Configuring user information, initializing and cloning repositories

- **Initialize** an existing directory as a Git repository
  ```bash
  git init
  ```

- **Retrieve** an entire repository from a hosted location via URL
  ```bash
  git clone [url]
  ```

<br>

## STAGE & SNAPSHOT
Working with snapshots and the Git staging area

### Git status
Shows modified files in working directory, staged for your next commit

```bash
git status
```

### Git add
It adds changes to staging area. This command stages the changes made to files and prepares them for the next commit.

- To add a specific file
  ```bash
  git add [fileName]
  ```

- To add all the files that are new or changed in the current directory
  ```bash
  git add .
  ```

- To add all changes in the entire working tree, from the root of the repository, regardless of where you are in the directory structure
  ```bash
  git add -A
  ```

### Git reset
It resets changes in the working directory.

```bash
git reset [file]
```

- When used with –hard HEAD, this command discards all changes made to the working directory and staging area and resets the repository to the last commit (HEAD).

```bash
git reset --hard HEAD
```

### Git diff
It shows changes between commits, commit and working tree, etc. It also compares the branches.

- Shows the difference the working directory and the last commit
  ```bash
  git diff
  ```

- Shows the difference between the last and second last commits
  ```bash
  git diff HEAD-1 HEAD
  ```

- Compares the specified branches
  ```bash
  git diff [branch-1] [branch-2]
  ```

- Shows the difference of what is staged but not yet committed
  ```bash
  git diff --staged
  ```

<br>

## BRANCH & MERGE
Isolating work in branches, changing context, and integrating changes

### Git branch
It lists, creates or deleyes branches in a repository. To delete the branch using **git checkout** and then run command to delete the branch locally


- To list branches
  ```bash
  git branch
  ```

- To create a new branch
  ```bash
  git branch [branch-name]
  ```

- To delete a branch
  ```bash
  git branch -d [branch-name]
  ```
  
### Git checkout
Switch to another branch and check it out into your working directory

```bash
git checkout [branch-name]
```

### Git merge
Merge the specified branch's history into the current one

```bash
git merge [branch]
```

<br>

## INSPECT & COMPARE
Examining logs, diffs and object information

- Show all commits in the current branch's history
  ```bash
  git log
  ```

- Show the commits on **branchA** that are not on **branchB**
  ```bash
  git log [branchB]..[branchA]
  ```

- Show the commits that changed file, even across renames
  ```bash
  git log --follow [file]
  ```

- Show the diff of what is in **branchA** that is not in **branchB**
  ```bash
  git diff [branchB]...[branchA]
  ```

- Show any object in Git in human-readable format
  ```bash
  git show [SHA]
  ```

<br>

## SHARE & UPDATE
Retrieving updates from another repository and updating local repos

- Add a git URL as an **alias**
  ```bash
  git remote add [alias] [url]
  ```

- **Fetch** down all the branches from that Git remote
  ```bash
  git fetch [alias]
  ```

- **Merge** a remote branch into your current branch to bring it up to date
  ```bash
  git merge [alias]/[branch]
  ```

- Transmit local branch commits to the remote repository branch
  ```bash
  git push [alias] [branch]
  ```

- Fetch and merge any commits from the tracking remote branch
  ```bash
  git pull
  ```

<br>

## TRACKING PATH CHANGES
Versioning file removes and path changes

- Delete the file from project and stage the removal for commit
  ```bash
  git rm [file]
  ```

- Change an existing file path and stage the move
  ```bash
  git mv [existing-path] [new-path]
  ```

- Show all **commit logs** with indication of any paths that moved
  ```bash
  git log --stat -M
  ```

<br>

## REWRITE HISTORY
Rewriting branches, updating commits and clearing history

- Apply any commits of current branch ahead of specified one
  ```bash
  git rebase [branch]
  ```

- Clear staging area, rewrite working tree from specified commit
  ```bash
  git reset --hard [commit]
  ```

<br>

## TEMPORARY COMMITS
Temporarily store modified, tracked files in order to change branches

- Save modified and staged changes
  ```bash
  git stash
  ```

- List stack-order of stashed file changes
  ```bash
  git stash list
  ```

- Write working from top of stash stack
  ```bash
  git stash pop
  ```

- Discard the changes from top of stash stack
  ```bash
  git stash drop
  ```

<br>

## IGNORING PATTERNS
Preventing unintentional staging or commiting of files

- Save a file with desired patterns as **.gitignore** with either direct string matches or wildcard globs.
  ```bash
  logs/
  *.notes
  pattern*/
  ```

- System wide ignore pattern for all local repositories
  ```bash
  git config --global core.excludesfile [file]
  ```
