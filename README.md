# Git-Learn
## Repository in wich I tested Git commands

Checking the git version: ```git --version```.
Creating a git repository in the current directory: ```git init```.

Clone the repository to current directory: ```git clone <repository link>```.

Check tracked files: ```git status```.
Adding file to tracked files: ```git add <file>```, or to add all files: ```git add .```.
Removing file of tracked flies: ```git rm --cached <file>```, or to remove all files: ```git rm --cached -r .```.

Commiting changes: ```git commit -m "<Message>"```
Checking the differences between modified (not staged) files and commited changes: ```git diff```. 
Checking the differences between modified (staged) files and commited changes: ```git diff <--cached or --staged>```.

See commits history: ```git log```.
See simplified history: ```git log --oneline```.
See commit update patch: ```git log --patch``` or ```git log -p```.
See files changes: ```git log --stat```.
See short version of changed files: ```git log --shortstat```.

Change commit message: ```git commit --amend -m "<New message>"```.
Add file to commit: ```git add <file>``` then ```git commit --amend --no-edit```.

Go to commited version: ```git checkout <commit code>```.
Undo code above: ```git switch -```.
go back to newest version (master/main): ```git checkout <master or main>```