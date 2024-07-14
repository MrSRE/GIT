# Git Commands and Concepts

## Setting Up Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your@example.com"

Initializing a Local Repository
bash
Copy code
git init
Adding a Remote Repository
bash
Copy code
git remote add origin https://github.com/yourusername/your-repo-name.git
Staging and Committing Changes
bash
Copy code
git add .
git commit -m "Initial commit"
Pushing to a Remote Repository
bash
Copy code
git push -u origin master
Git Areas Overview
Working Area: Where you modify files.
Staging Area: Where you place files you want to commit.
Local Repository: Where committed files reside.
Commands:
bash
Copy code
# Move files to staging area
git add .
git add *
git add file1 file3

# Commit files from staging area to local repository
git commit -m "first commit"
Git Status
bash
Copy code
git status  # Shows the status of files in different areas
Remote Repositories
bash
Copy code
git remote add <aliasName> <RepoUrl>
git remote add df https://github.com/deflow/web-app.git 
git remote -v  # Shows mapped repositories
git push <aliasName> <BranchName>
git push df master
Viewing Commit History
bash
Copy code
git log  # See all commits
git log -2  # See the latest two commits
Viewing Commit Details
bash
Copy code
git show <commitID>  # See files and changes in a commit
git show --pretty="" --name-only <commitID>  # See only files in a commit
Resetting Changes
bash
Copy code
# Revert files from staging area to working area
git reset
git reset <fileName>

# Revert changes made in a specific commit
git revert <commitID>
Ignoring Files
Use .gitignore to ignore files that are not required.
Branching
bash
Copy code
git branch  # List branches
git branch <BranchName>  # Create a new branch
git checkout <BranchName>  # Switch to a branch
git checkout -b <BranchName>  # Create and switch to a new branch
git diff <BranchName>  # Show differences between branches
git merge <BranchName>  # Merge a branch with the current branch
Listing Branches
bash
Copy code
git branch  # Local branches
git branch -r  # Remote branches
git branch -r -a  # All branches (local and remote)
Deleting Branches
bash
Copy code
git branch -d <branchName>  # Delete a local branch
Tags
Branch: Mutable, for ongoing developments.
Tag: Immutable, for production deployment.
Tagging Commands
bash
Copy code
git tag <tagName>  # Create a tag
git push <aliasName> tag <tagName>  # Push a tag
git tag -d <tagName>  # Delete a tag
git tag -l -n3  # List tags (3 tags per page)
git tag --list  # List all tags
Stashing
Temporarily save changes in a branch without committing.
Stashing Commands
bash
Copy code
git stash --list  # List stashes
git stash apply  # Apply the latest stash
git stash apply stash@{2}  # Apply a specific stash
git stash drop stash@{2}  # Delete a specific stash
git stash pop  # Apply and delete the latest stash
Cherry-picking
Apply a specific commit from one branch to another.
Cherry-picking Commands
bash
Copy code
git cherry-pick <commitID>
Cloning and Pulling
bash
Copy code
git clone <url>  # Clone an existing repository
git pull <alias> <branch>  # Fetch and merge changes from a remote branch
git fetch <alias> <branch>  # Fetch changes from a remote branch to local
Merging and Rebasing
bash
Copy code
git merge <branch>  # Merge a branch into the current branch
git rebase <branch>  # Rebase current branch onto another branch
Branching Strategy
Prod_Retail
Staging_Retail
Pilot_Retail
Amending Commits
To fix a broken commit:
bash
Copy code
git commit --amend  # Combine staged changes with the previous commit