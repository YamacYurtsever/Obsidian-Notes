- A [[Version Control System#Centralized vs Distributed VCSs | distributed]] [[Version Control System | version control system]] 

### Commands
- `git clone <url>`: Clones Remote Repository
- `git add <filename>` or `git add --all`: Adds Files to Commit
- `git commit -m "message"`: Commits Changes to the Local Repo With a Message
- `git status`: Tells the Status of the Local Repo
- `git push`: Pushes the Changes in the Local Repo to the Remote Repo
- `git pull`: Pulls the Changes in the Remote Repo to the Local Repo
- `git log`: Shows Commit History

### Branching
- `git branch`: Tells which branch you are on
- `git checkout -b <branchname>`: Switches to a branch, creates it if it doesn't exits
- `git merge <branchname>`: Merges the named branch to the current branch

### Resolving Conflicts
```python
<<<<<<<<<<<<<<< HEAD
b = 3 # Local Changes
===============
b = 1 # Remote Changes
>>>>>>>>>>>>>>> 53423464... # Hash for the conflicting other commit
```
1. Accept Local Changes
2. Accept Incoming Changes
3. Manually Combine Changes