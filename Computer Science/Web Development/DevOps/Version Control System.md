- Systems that records changes to a file or a set of files over time

### Centralized vs Distributed VCSs
![[Pasted image 20231225151923.png | 300]] ![[Pasted image 20231225151940.png | 280]]

### Key Concepts:

- **Repository:**
	- A database that stores all the files, directories, and the history of changes for a project
	- *Remote Repo*: a version-controlled project that is hosted on a server, typically on the internet or a network accessible to multiple developers
	- *Local Repo*: a copy of the version-controlled project that resides on your local machine
- **Commit:**
	 - A snapshot of the project at a specific point in time
- **Branching:**
	- Allows for the creation of divergent lines of development called branches
	- Developers can work on a feature or bug fix in isolation without affecting the main codebase.
- **Merging:** ^3d24fc
	- The process of combining changes from different branches
- **Checkout:**
    - Switching between different branches or versions of the code
- **Conflict**
    - Occur when changes made in one branch cannot be automatically merged with changes in another
    - Manual intervention is required to resolve conflicts.

### Benefits of Version Control:

- **Collaboration**
	- Multiple developers can work on the same project simultaneously without interfering with each other
- **History Tracking**
	- Maintains a detailed history of changes, allowing users to track when and by whom each change was made
- **Revert to Previous States**
	- If a mistake is made or if there is a need to revert to a previous state of the project,  allows users to roll back to a specific commit
- **Branching and Experimentation**
	- Developers can create branches to experiment with new features or bug fixes without affecting the main codebase
- **Backup**
	- Serves as a backup mechanism by storing project history
	  
### VCS Hosting
- The platforms or services that provide infrastructure and tools for hosting and managing version-controlled repositories
- VCS hosting services often integrate with [[CI CD | CI/CD]] systems, automated build and test processes can be triggered whenever changes are pushed to the repository, ensuring that code changes are continuously validated
- E.g.: GitHub, GitLab, Bitbucket