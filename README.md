# Table of Contents

- [Hello World! 🌏](#hello-world-)
- [Git & GitHub Workflow 📚✨🌐](#git--github-workflow-)
- [Git Commands 📖](#git-commands-)
- [Complete Guide to Git Merging and Rebasing 🔄](#complete-guide-to-git-merging-and-rebasing-)
- [Interactive Rebase 🌵](#interactive-rebase-)
- [Important Points ⚠](#important-points-)

# Hello World! 🌏

Hi there!👋, my name is **Vidyasagar Yadav** and this is the **first repository** that i have created, to embark on a journey of learning and practicing **Git** & **Github** along with it's various functions and features.

# Git & GitHub Workflow 📚✨🌐

## 1. Clone the Repository 💾✨🌍
To start working on a project, clone the repository from GitHub to your local machine.

```
git clone <repo-url>
```

## 2. Create a New Branch 🌳✨🔧
Before making changes, create a new branch to keep your work separate from the main branch.

```
git checkout -b <branch-name>  # Creates and switches to a new branch
git branch <branch-name>       # Creates a new branch
git checkout <branch-name>     # Switches to the newly created branch
```

Alternatively, you can use:

```
git branch -c <branch-name>    # Creates a new branch and copies the current branch's history
```

## 3. Work on Your Branch 📚🌿✨
Make your changes, then stage and commit them.

```
git add .                      # Stages all changes in the current directory
git commit -m "commit message" # Commits the staged changes with a descriptive message
```

Use these additional commands if needed:

```
git status                     # Shows the status of the working directory
git diff                       # Shows the differences between the working directory and the index
```

## 4. Push Your Branch to Remote Repository 🌐📢✨
Push your branch to the remote repository to share your changes.

```
git push -u origin <branch-name>  # Pushes the branch and sets the upstream reference
```

## 5. Create a Pull Request on GitHub 🔧📚🌟
Go to GitHub, navigate to your repository, and create a pull request to propose your changes for review.

## 6. Review and Merge 💡🌿🔄
After the pull request is reviewed and approved, merge it into the main branch on GitHub.

## 7. Update Your Local Repository (main branch) 🌐🔧🌿
Keep your local main branch up-to-date with the remote repository.

```
git switch main                # Switches to the main branch
git pull origin main          # Pulls the latest changes from the remote main branch
```

Alternatively, you can use:

```
git checkout main              # Switches to the main branch
git fetch origin               # Fetches changes from the remote repository
git merge origin/main         # Merges the fetched changes into the main branch
```

# Git Commands 📖
| Command | Description |
|---|---|
| **Initialization Commands** |  |
| `git init` | Initializes a new git repository by adding a `.git` folder to it. |
| `git clone <url>` | Creates a copy of an existing repository from a remote URL. Example: `git clone https://github.com/user/repo.git` |
| **Staging Commands** |  |
| `git add -A` | Adds all changes (tracked and untracked) to the staging area. |
| `git add .` | Adds new/untracked files or modified files to the staging area in the current directory. |
| `git add <file>` | Adds a specific file to the staging area. Example: `git add index.html` |
| **Commit Commands** |  |
| `git commit -m "message"` | Commits changes with a message. Example: `git commit -m "Add login feature"` |
| `git commit --amend` | Adds changes to the latest commit and allows editing the commit message. |
| `git commit --amend --no-edit` | Adds changes to the latest commit without changing the commit message. |
| `git commit -a -m "message"` | Commits all tracked files with a message, skipping the staging area. Example: `git commit -a -m "Fix typos"` |
| **Status Commands** |  |
| `git status` | Displays the status of the working directory and staging area. |
| `git status -s` | Shows a short format for the status. |
| **Push Commands** |  |
| `git push` | Pushes changes from the local repository to the remote repository's default branch. |
| `git push <remote> <branch>` | Pushes the specified branch to the specified remote repository. Example: `git push origin feature/login` |
| `git push --force` | Forces the push by overwriting the remote branch history with local history. Example: `git push --force` |
| `git push --all <remote>` | Pushes all local branches to the specified remote repository. Example: `git push --all origin` |
| `git push --tags` | Pushes all tags to the remote repository. |
| `git push --set-upstream <remote> <branch>` | Sets the remote branch as the upstream branch for the local branch and pushes to it. Example: `git push --set-upstream origin feature/login` |
| **Fetch Commands** |  |
| `git fetch` | Downloads all branches and tags from the default remote repository. |
| `git fetch <remote>` | Fetches data from a specified remote repository. Example: `git fetch origin` |
| `git fetch <remote> <branch>` | Fetches updates from a specific branch of the remote repository. Example: `git fetch origin develop` |
| `git fetch --all` | Fetches updates from all configured remotes. |
| `git fetch --prune` | Removes references to branches deleted from the remote. |
| **Pull Commands** |  |
| `git pull` | Fetches and merges changes from the default remote and branch. |
| `git pull <remote> <branch>` | Pulls changes from a specific branch of the remote repository. Example: `git pull origin main` |
| `git pull --rebase` | Fetches changes and rebases the local branch on top of the remote branch. |
| `git pull --strategy=<strategy>` | Uses a specific merge strategy when pulling changes. Example: `git pull --strategy=recursive` |
| **Checkout Commands** |  |
| `git checkout <branch>` | Switches to the specified branch. Example: `git checkout feature-xyz` |
| `git checkout -b <name>` | Creates a new branch and switches to it. Example: `git checkout -b new-feature` |
| `git checkout <hash>` | Checks out a specific commit, detaching the HEAD. Example: `git checkout abc1234` |
| `git checkout <file>` | Restores a specific file from the last commit or the index. Example: `git checkout README.md` |
| **Branch Commands** |  |
| `git branch` | Lists all local branches. |
| `git branch -c <name>` | Creates a new branch with the specified name. Example: `git branch -c feature/search` |
| `git branch -d <branch>` | Deletes the specified branch. Example: `git branch -d feature/old` |
| `git branch -m <oldname> <newname>` | Renames the specified branch. Example: `git branch -m feature/old feature/new` |
| **Configuration Commands** |  |
| `git config --global alias.<alias> "<command>"` | Creates a global alias for a git command. Example: `git config --global alias.co "checkout"` |
| `git config --global user.name "<name>"` | Sets the global username for commits. Example: `git config --global user.name "John Doe"` |
| `git config --global user.email "<email>"` | Sets the global email for commits. Example: `git config --global user.email "john@example.com"` |
| **Remote Commands** |  |
| `git remote add <name> <url>` | Adds a new remote repository. Example: `git remote add upstream https://github.com/original/repo.git` |
| `git remote remove <name>` | Removes the specified remote repository. Example: `git remote remove upstream` |
| `git remote rename <old> <new>` | Renames a remote repository. Example: `git remote rename origin upstream` |
| **Log Commands** |  |
| `git log` | Shows the commit history. |
| `git log --all --decorate --oneline --graph` | Displays a detailed log with graph view. |
| `git log -p` | Shows the commit history with the diffs of each commit. |
| **Reset Commands** |  |
| `git reset HEAD <file>` | Unstages a file without removing changes. Example: `git reset HEAD index.html` |
| `git reset --hard <commit>` | Resets to a specific commit, discarding all changes. Example: `git reset --hard HEAD~1` |
| **Stash Commands** |  |
| `git stash save "<message>"` | Stashes changes with a descriptive message. Example: `git stash save "WIP: login feature"` |
| `git stash pop` | Applies and removes the last stashed changes. |
| **Clean Commands** |  |
| `git clean -df` | Removes untracked files and directories forcefully. |
| `git clean -n` | Shows what would be removed by `git clean`. |
| **Rebase Commands** |  |
| `git rebase <branch>` | Rebases current branch on top of specified branch. Example: `git rebase main` |
| `git rebase <remote>/<branch>` | Rebases on top of a remote branch. Example: `git rebase origin/main` |
| `git rebase --onto <newbase> <oldbase> <branch>` | Rebases specified branch onto new base. Example: `git rebase --onto main feature/v1 feature/v2` |
| **Tag Commands** |  |
| `git tag <tagname>` | Creates a lightweight tag at the current commit. Example: `git tag v1.0.0` |
| `git tag -a <tagname> -m "<message>"` | Creates an annotated tag with a message. Example: `git tag -a v1.0.0 -m "Release version 1.0.0"` |
| **Diff Commands** |  |
| `git diff` | Shows unstaged changes. |
| `git diff --staged` | Shows staged changes. |
| `git diff <commit1> <commit2>` | Shows changes between two commits. Example: `git diff abc1234 def5678` |

# Complete Guide to Git Merging and Rebasing 🔄

## 1. Basic Git Merging 🧩

### What is Merging?
Merging is like combining different versions of your work into one final version. In Git, it's the process of integrating changes from one branch into another.

### Basic Merge Commands
```
# Switch to target branch (e.g., main)
git checkout main

# Merge another branch into current branch
git merge feature-branch
```

## 2. Handling Merge Conflicts ⚡

### What a Conflict Looks Like
```
<<<<<<< HEAD (Current branch)
Your changes
=======
Their changes
>>>>>>> feature-branch
```

### Steps to Resolve Conflicts
1. Check conflicted files:
```
git status
```

2. Edit conflicted files
- Remove conflict markers
- Choose desired changes
- Save files

3. Complete the merge:
```
# Add resolved files
git add fixed-file.txt

# Commit the merge
git commit -m "Resolved merge conflicts"
```

## 3. Three-Way Merge 🌟
A three-way merge occurs when Git needs to consider three different versions:
- Common ancestor (original version)
- Your branch changes
- Their branch changes

```
# Automatic three-way merge
git checkout main
git merge feature-branch
```

Git automatically performs a three-way merge when needed by comparing:
1. Last common commit between branches
2. Latest commit on main
3. Latest commit on feature-branch

## 4. Rebasing 🔄

### Basic Rebase Command
```
# Go to branch to rebase
git checkout feature-branch

# Rebase onto main
git rebase main
```

### Complete Rebase Process
1. Save current work:
```
git add .
git commit -m "Save changes"
```

2. Update main:
```
git checkout main
git pull
```

3. Perform rebase:
```
git checkout feature-branch
git rebase main
```

### Handling Rebase Conflicts
```
# After fixing conflicts
git add fixed-file.txt
git rebase --continue

# To cancel rebase
git rebase --abort
```

## 5. Merge vs. Rebase Comparison

### Merge Structure
```
Before merge:
A---B---C (main)
     \
      D---E (feature)
      
After merge:
A---B---C---F (main)
     \     /
      D---E (feature)
```

### Rebase Structure
```
Before rebase:
A---B---C (main)
     \
      D---E (feature)
      
After rebase:
A---B---C (main)
         \
          D'---E' (feature)
```

## 6. When to Use What

### Use Merge When:
- Working on shared branches
- Need to preserve exact history
- Working on long-running features

### Use Rebase When:
- Keeping feature branch updated with main
- Want a linear history
- Working on personal branches

## 7. Best Practices

### Safety Tips 🛡️
1. Always verify current branch before merging/rebasing
2. Keep work backed up
3. Seek help when uncertain
4. Take time with conflict resolution

### Golden Rules for Rebasing 👑
1. Never rebase shared branches
2. Rebase before pushing to remote
3. Default to merge if unsure

### Helpful Commands
```
# Check current branch
git branch

# View status
git status

# Abort merge
git merge --abort

# Abort rebase
git rebase --abort
```

# Interactive Rebase 🌵

Interactive Rebase is a tool for optimizing and cleaning up your commit history. It's like a swiss-army knife for git operations.
It can help peform various operations:
 - Change a commit's message.
 - Delete commits.
 - Reorder commits,
 - Squash: Combine multiple commits into one.
 - Edit/split an existing commit into mutliple new ones.

> ⚠️ **Warning:** Do NOT use Interactive Rebase on commits that you have already pushed/shared on a remote repository! Instead, use it to clean your local commit history before merging it into a shared team branch. Remember this mantra, **NEVER REBASE PUSHED COMMITS!**

## Workflow 🍃༄
### Step 1: Determine the Base Commit
1. **How far do you want to go?**
   - Decide which commit you want to start from, at least the ancestor or parent of the commit you want to change.

2. **Choose the Base Commit**:
   - Use `git log` or `git log --oneline` to find the appropriate commit hash or relative reference.
   
     ```
     git log --oneline
     ```

### Step 2: Start the Interactive Rebase
1. **Run the Command**:
   - Start the interactive rebase with one of the following commands:

     ```
     git rebase --interactive HEAD~3
     ```
     OR
     ```
     git rebase -i HEAD~3
     ```
     OR
     ```
     git rebase -i <hash>
     ```

### Step 3: Choose Actions in the Editor
1. **Editor Opens**:
   - A text editor will open, listing commits from the base commit to the HEAD.
   
2. **Determine Actions**:
   - For each commit, specify the action to perform:
     - `pick`: Use the commit as is (default).
     - `reword`: Change the commit message.
     - `edit`: Amend the commit content.
     - `squash`: Combine this commit with the previous one, merging messages.
     - `fixup`: Combine with the previous commit, discarding this commit's message.
     - `drop`: Remove the commit entirely.

3. **Example**:
   ```
   pick abc123 Commit message 1
   reword def456 Commit message 2
   edit ghi789 Commit message 3
   ```

4. **Save and Close**:
   - Save the file and close the editor to proceed.

### Step 4: Execute Actions
1. **Reword Commit Messages**:
   - If `reword` was chosen, Git will prompt you to edit the commit message. Update the message, save, and close.

2. **Edit Commit Content**:
   - If `edit` was chosen, Git will pause the rebase. Make your changes, stage them, and amend the commit:
     
     ```
     git add <file>
     git commit --amend
     ```
   - Continue the rebase:
     
     ```
     git rebase --continue
     ```

3. **Resolve Conflicts** (if any):
   - If conflicts arise, resolve them manually, then stage the resolved files:
     
     ```
     git add <file>
     ```
   - Continue the rebase:
     
     ```
     git rebase --continue
     ```
   - To abort the rebase if needed:
     
     ```
     git rebase --abort
     ```

### Step 5: Finalize and Verify
1. **Completion**:
   - Once all commits are processed, the rebase completes successfully.
     
2. **Review History**:
   - Check the updated commit history to ensure everything is as expected:
     
     ```
     git log --oneline
     ```

## Additional Tips:
- **Backup Branch**: Before rebasing, create a backup branch for safety:
  
  ```
  git branch backup-branch
  ```
  
- **Rebase Shared History**: Be cautious when rebasing commits that have been shared with others. Coordinate with your team to avoid issues.

# Important Points ⚠

1. Suppose you create a branch, say `my-branch` and you work on this and do not commit the changes and try to switch to some other branch, say `main` you may loose the changes you made on `my-branch`. Commit your changes before switching branches!
