# Quick learn Git, for beginners.
> See reference: [Git Book](https://git-scm.com/book/en/v2)

1. What is [Git](https://git-scm.com/book/en/v2)?
    - Git is a "version control system (VCS)". VCS is a program to track file changes. e.g. Git, SVN, mercury, helix etc
    - It was created by Linux Torvalds (creator of Linux) during linux kernel development
    - It is tool to track/manage changes to files and lets you travel back and forth in time (v1 to v2, v2 to v1 etc)
2. Why use git?
   - Without git, you will be creating duplicate copies/folders for each change like v1, v2, v3 etc
   - At any point a git repository will has only 1 copy of a file. Using various git commands and concepts you can changes this file to any version of choice.
   - Read: [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [First-Time Git Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup#_first_time)
2. What are some key terms in Git?
    1. Repository: 
        - is a directory/folder that stores related files. 
        - IMPORTANT: A git repository should contain '.git' folder. Do not delete it.
    2. Local repository: 
        - the local version of a git repository stored in your hard disk
    3. [Remote repository](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes): 
        - the online version of the same git repository, managed by a service provider like GitHub, GitLab, Bitbucket etc
        - Used for collaboration among developers and for backup
        - Users can access it via an HTTP URL and download them to local (cloning)
        - Proper permissions are needed to save to remote repository (push)
    4. `init`:
        - command to initialize a git repository.
        - i.e. covert your local folder to a git repository so that you can use git for tracking changes.
        - Some developers do not use this, instead they directly create repository in online platforms like GitHub and clone it.
    5. `commit`: 
        - git command used to save(or record) changes in local repository
        - e.g. `git commit -a -m "your message"`, this saves all unsaved changes to local repository. (direct commit without stage)
        - IMPORTANT: You should always commit for git to manage that file.
        - When you commit, a history is created (commit id), which is used for time travel😉.
    6. [Working Directory and Staging area](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository):
        - These are logical concept used to manage changes
        - In Git, when you make changes to files, they go through different areas before being saved permanently(via `commit`) in the repository. The two key areas are: Working Directory and Staging Area (Index)
        - Working Directory: It is where you actively edit, create, or delete files, but changes here are not yet tracked by git
        - Staging Area:
            - The staging area is like a clipboard where you prepare changes before committing.
            - This area holds changes that will be included in the next commit.
            - Files here are tracked but not yet saved (commit) in the repository.
            - syntax: `git add file1 file2 ...` command adds files to staging area
            - `git commit -m "your message"`, commit changes from staging area (default behaviour)
            - `git commit -a -m "your message"`, commit changes from both working directory and staging area.
    7. `push`:
        - git command used to save (or upload) changes to the remote repository
        - e.g. `git push`
    8. `pull`:
        - Fetch changes from the remote and sync with local
        - e.g. `git pull` 
    9. `branch`: For details [check here](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)
        - a pointer for organizing and classifying your data/code
        - It allows developers to work on new features or experiments without affecting main code
        - `main` is the root branch. You can create 'n'  number of branches for a repository
        - local branches track remote branches, like repository
        - remote branches have format like `origin/<branch_name>
        - A very powerfull concept, that enable collaboration in git
    10. `merge`:
        - command to move changes from one branch to another.
        - e.g. you can merge changes from branch A to `main`
    11. `pull_request`:
        - it is a review functionality for `merge` command provided by online git providers like GitHub
        - It is like a request or suggestion for `merge` command, but merge will happen only if another team member approves your changes.
        - Not a standard git command. 
        - Only applies when 2 people work on same repository, so that one person can review changes made by other.
    12. `clone`:
        - command download a remote git repository to your local
        - only used ONCE. After this any changes are pulled using `pull` command
        - e.g. `git clone <url>`
3. What is the difference between Git, GitHub and "GitKraken/Sourcetree/GitHub Desktop/TortoiseGit"?
   - Git is a version control system (VCS) to track file changes. It is a shell(command-line) program.
   - GitHub is the online platform for managing and backup of git repositories.
   - GitKraken/Sourcetree/GitHub Desktop/TortoiseGit etc are UI clients for Git
4. 
