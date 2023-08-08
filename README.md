# Git-Learn
## Repository in wich I tested Git commands

### Starting.
Checking the git version: ```git --version```.

Creating a git repository in the current directory: ```git init```.


### Setting up repository.
Clone the repository to current directory: ```git clone <repository link>```.

Checking remote connection: ```git remote -v```.

Adding remote connection: ```git remote add <repository: origin> <link>```.

Change remote connection adress: ```git remote set-url <repository: origin> <link>```.

Pull informations from server to machine: ```git pull```.


### Managing status.
Check tracked files: ```git status```.

Adding file to tracked files: ```git add <file>```, or to add all files: ```git add .```.

Removing file of tracked flies: ```git rm --cached <file>```, or to remove all files: ```git rm --cached -r .```.

Removing flie of tracked files (if a commit has been made): ```git restore --staged <file>```.

Make file not watchable: ```git update-index --skip-worktree <file>```.

Undo command above: ```git update-index --no-skip-worktree <file>```.


### Commmiting.
Commiting changes: ```git commit -m "<Message>"```.

Checking the differences between modified (not staged) files and commited changes: ```git diff```. 

Checking the differences between modified (staged) files and commited changes: ```git diff <--cached or --staged>```.

Change commit message: ```git commit --amend -m "<New message>"```.

Add file to commit: ```git add <file>``` then ```git commit --amend --no-edit```.


### Changes history.
See commits history: ```git log```.

See simplified history: ```git log --oneline```.

See commit update patch: ```git log --patch``` or ```git log -p```.

See files changes: ```git log --stat```.

See short version of changed files: ```git log --shortstat```.


### Managing versions.
Go to commited version: ```git checkout <commit code>```.

Undo code above: ```git switch -```.

Go back to newest version (master/main): ```git checkout <master or main>```.

Restore file to lest commited version: ```git checkout <file>``` or to retore all files ```git checkout .```.

Remove untracked files: ```git clean -f```.

Restore all tracked and unstaged changes to last commit: ```git reset --hard```.


### .gitignore.
Create ".gitignore" file (on Git Bash): ```touch .gitignore```.


### Managing branches.
See branchs: ```git branch```.

Create branch: ```git branch <name>```.

Change branch: ```git checkout <name>```.

Create and change branch: ```git checkout -b <name>```.

Create and switch to new brand with detached HEAD: ```git switch -c <branch name>```.

Send branch to remote repository: ```git push --set-upstream origin <branch name>```.

Removing local branch: ```git branch -d <branch name>```, or ```git branch -D <branch name>``` for forced deletion.

Removing remote branch: ```git push --delete origin <branch name>```.

Reanming checkedout branch: ```git branch -m <new name>```.

Renaming branch: ```git branch -m <current name> <new name>```.

See branch commit history: ```git log <branch name> log```.


### Managing merges.
Merge current branch with other branch changes: ```git merge <name of branch with the changes>```.

List of merged branches: ```git branch --merged```.

List of not merged branches: ```git branch --no-merged```.

Abort merge: ```git merge --abort``` or ```git reset --hard```.
