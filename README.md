# Git-Learn


## Starting.
Checking the git version: ```git --version```.

Creating a git repository in the current directory: ```git init```.


## Setting up repository.
Clone the repository to current directory: ```git clone <repository link>```.

Checking remote connection: ```git remote -v```.

Adding remote connection: ```git remote add <repository: origin> <link>```.

Change remote connection adress: ```git remote set-url <repository: origin> <link>```.

Pull informations from server to machine: ```git pull```.


## Managing status.
Check tracked files: ```git status```.

Adding file to tracked files: ```git add <file>```, or to add all files: ```git add .```.

Removing file of tracked flies: ```git rm --cached <file>```, or to remove all files: ```git rm --cached -r .```.

Removing flie of tracked files (if a commit has been made): ```git restore --staged <file>```.

Make file not watchable: ```git update-index --skip-worktree <file>```.

Undo command above: ```git update-index --no-skip-worktree <file>```.


## Managing commmits .
Commiting changes: ```git commit -m "<Message>"```.

Checking the differences between modified (not staged) files and commited changes: ```git diff```. 

Checking the differences between modified (staged) files and commited changes: ```git diff <--cached or --staged>```.

Change commit message: ```git commit --amend -m "<New message>"```.

Add file to commit: ```git add <file>``` then ```git commit --amend --no-edit```.

Revert commit: ```git revert HEAD```, or ```git revert <commit code```.

Remove commit: ```git reset --hard HEAD~<number of commits>```.

Remove commit, but keep changes as modified: ```git reset --mixed HEAD~<number of commits>```.

Remove commit, but keep changes as added: ```git reset --soft HEAD~<number of commits>```.


## Pushing changes
Push changes to remote server: ```git push```.

(CAUTION) Forcing push changes to remote server: ```got push --force```, for when your local repository don't match the remote one, but you're sure the local repository is correct.

Forcing push changes to remote server, if no changes would be lost: ```git push --force-with-lease```.  

 
## Changes history.
See commits history: ```git log```.

See simplified history: ```git log --oneline```.

See commit update patch: ```git log --patch``` or ```git log -p```.

See files changes: ```git log --stat```.

See short version of changed files: ```git log --shortstat```.


## Managing versions.
Go to commited version: ```git checkout <commit code>```.

Undo code above: ```git switch -```.

Go back to newest version (master/main): ```git checkout <master or main>```.

Restore file to lest commited version: ```git checkout <file>``` or to retore all files ```git checkout .```.

Remove untracked files: ```git clean -f```.

Restore all tracked and unstaged changes to last commit: ```git reset --hard```.


## .gitignore.
Create ".gitignore" file (on Git Bash): ```touch .gitignore```.


## Managing branches.
See branchs: ```git branch```.

see local and remote branchs: ```git branch -a```.

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

Fecthing remote branch to local repository: ```git fetch <repository: origin> <branch name>```.


## Managing merges.
Merge current branch with other branch changes: ```git merge <name of branch with the changes>```.

List of merged branches: ```git branch --merged```.

List of not merged branches: ```git branch --no-merged```.

Abort merge: ```git merge --abort``` or ```git reset --hard```.


## Managing Tags
Create tag: ```git tag <tag name>``` or ```git tag <tag name> <commmit code>``` to tag especified commit.

Create annotaded tag: ```git tag -a -m "<massage> <tag name>```.

Show tag: ```git show <tag name>```.

List all tags: ```git tag```,  or ```git tag -n``` to show annotations of each tag . 

Push local tag to remote server: ```git push <repository: origin> <tag name>``` or ```git push --tags``` to push all local tags (CAUTION). 

Navigate to tag commit: ```git chechout <tag name```.

Compare tags: ```git diff <tag 1> <tag 2>```.

Remove local tag: ```git tag -d <tag name>```.

Remove remote tag: ```git push --delete <repository: origin> <tag name>```.


## Stash
Create stash: ```git stash```.

List all stashs: ```git stash list```.

Applying saved stash: ```git stash apply```.

Applying specific saved stash: ```git stash @stash{<stash number>}```.

Remove saved stash: ```git stash drop```, or ```git stash drop @stash{<stash number>}``` to remove specific stash.

Applying and removing stash at the same time: ```git stash pop``` or ```git stash pop @stash{<stash number>}``` for specific stash.

Create new branch and apply stash to it: ```git stash branch <branch name>```, or ```git stash branch <branch name> @stash{<stash number>}``` for specific stash.


## Rebase
Rebase branch: ```git rebase <branch name>``` to bring <branch name> changes to current branch.

Abort rebase: ```git rebase --abort```. 

Continue rebase after resolving merge problems: ```git rebase --continue```.

Pull with rebase: ```git pull --rebase```. 

Squashing through rebase: ```git rebase --interactive```, then change the commits added to "squash" and rename the commit as intended.


## Cherry-pick
Pick specific commit from other branch and apply to current branch: ```git cherry-pick <commit code>```.


## Bisect
- Start binary seach through commits: ```git bisect start```.
- Determine good commit: ```git bisect good <commit code>```.
- Determine bad commit: ```git bisect bad <commit code>```.
- End bisect: ```git bisect reset```.

## Fetch
Pull changes from remote repository without automatic merging: ```git fecth```.

## Alias
Configuring alias for git commands: ```git config --global alias.< alias command> '<command>' ```, the '' are nedded for commands with hifens or empty spaces between.

Removing alias: ```git config --global --unset alias.<saved alias command>```


## Grep (Git bash/Linux)
Search by related name (examples): ```git branch | grep <related name>```, ```git log --oneline | grep commit```