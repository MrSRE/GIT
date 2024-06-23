## Learning Git ##
A memory map for the Git command which I use from time to time. These are most used git commands.

## Configuration ##
git config --global user.name "Your Name": Sets your name for all repositories on your computer.
git config --global user.email "you@example.com": Sets your email for all repositories on your computer.
git config --list: Lists all settings Git is using.

##  Creating and Cloning Repositories ##
git init: Initializes a new Git repository in the current directory.
git clone <repository-url>: Clones a repository from the given URL to your local machine.

## Basic Snapshotting ##
git add <file>: Adds a file to the staging area.
git add .: Adds all files in the current directory to the staging area.
git commit -m "commit message": Commits the staged files to the repository with a message.
git status: Shows the status of files in the working directory and staging area.
git diff: Shows changes between working directory and staging area.
git diff --staged: Shows changes between the staging area and the last commit.

## Branching and Merging ##
git branch: Lists all local branches in the repository.
git branch <branch-name>: Creates a new branch.
git checkout <branch-name>: Switches to the specified branch.
git checkout -b <branch-name>: Creates and switches to a new branch.
git merge <branch-name>: Merges the specified branch into the current branch.
git branch -d <branch-name>: Deletes the specified branch.

## Remote Repositories ##
git remote add <name> <url>: Adds a new remote repository.
git remote -v: Lists all remote repositories.
git fetch <remote>: Fetches changes from the remote repository but does not merge them.
git pull <remote> <branch>: Fetches and merges changes from the remote branch to your local branch.
git push <remote> <branch>: Pushes your local branch to the remote repository.

## Inspecting and Comparing
git log: Shows the commit history for the current branch.
git log --oneline: Shows the commit history in a compact form.
git show <commit>: Shows detailed information about a specific commit.
git diff <branch1> <branch2>: Shows differences between two branches.

## Undoing Changes
git reset <file>: Unstages a file.
git reset --hard: Resets the working directory and staging area to the last commit.
git reset --hard <commit>: Resets the working directory and staging area to a specific commit.
git revert <commit>: Creates a new commit that undoes changes from a specified commit.

## Stashing Changes
git stash: Stashes the current changes in the working directory.
git stash list: Lists all stashed changes.
git stash apply: Applies the most recent stash.
git stash apply stash@{n}: Applies a specific stash.
git stash drop: Deletes the most recent stash.
git stash drop stash@{n}: Deletes a specific stash.
git stash clear: Removes all stashes.
## Advanced
git rebase <branch>: Reapplies commits on top of another base tip.
git cherry-pick <commit>: Applies changes from a specific commit to the current branch.
git tag <tagname>: Creates a tag at the current commit.
git tag: Lists all tags in the repository.

## Help
git help <command>: Shows help information for a specific Git command.
git --version: Shows the version of Git installed.