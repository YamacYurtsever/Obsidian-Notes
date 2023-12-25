- A [[Version Control System#Centralized vs Distributed VCSs | distributed]] [[Version Control System | version control system]] 

### Commands
- `git clone <url>`: Clones Remote Repository
- `git add <filename>` or `git add --all`: Adds Files to Commit
- `git commit -m "message"`: Commits Changes to the Local Repo With a Message
- `git status`: Tells the Status of the Local Repo
- `git push`: Pushes the Changes in the Local Repo to the Remote Repo
- `git pull`: Pulls the Changes in the Remote Repo to the Local Repo
- `git log`: Shows Commit History

### Handling Conflicts
```python
<<<<<<<<<<<<<<< HEAD
b = 3 # Local Changes
===============
b = 1 # Remote Changes
>>>>>>>>>>>>>>> 53423464... # Hash for the conflicting local commit
```
