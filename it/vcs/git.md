# Quick learn Git

1. What is Git?
    - Git is a "version control system (VCS)". VCS is a program to track file changes. e.g. Git, SVN, mercury, helix etc
    - It was created by Linux Torvalds (creator of Linux) during linux kernel development
    - It is tool to track changes and lets you travel back and forth (v1 to v2, v2 to v1 etc)
    - without git, you will be create duplicate copies/folders for each change like v1, v2, v3 etc.
2. What are some key terms in Git?
    1. Repository: 
        - is a directory/folder that stores related files. 
        - A git repository should contain '.git' folder.
    2. Local repository: 
        - the local version of a git repository stored in your hard disk
    3. Remote repository: 
        - the online version of the same git repository, managed by a service provider like GitHub, GitLab, Bitbucket etc
        - Used for collaboration among developers and for backup
        - Users can access it via an HTTP URL and download them to local (cloning)
        - Proper permissions are needed to save to remote repository (push)
    4. `init`:
        - command to initialize a git repository.
        - i.e. covert your local folder to a git repository so that you can use git for tracking changes.
    5. `commit`: 
        - git command used to save changes in local repository
        - e.g. `git commit -a -m "your message"`, this saves all unsaved changes to local repository.
        - IMPORTANT: Git will track changes to a file only if you commit that file. Once 
    6. Working directory and staging area:
        - These are logical concept used to manage changes
        - Any change you make to a file is first available in working area.
        - staging area
    7. `push`:
        - git command used to save (or upload) changes to the remote repository
    8. `pull`:
        - Fetch changes from the remote and sync with local 
    9. `branch`:
        - a pointer for organizing and classifying your data/code
        - It allows developers to work on new features or experiments without affecting main code
        - `main` is the root branch. You can create 'n'  number of branches for a repository
        - local branches track remote branches, like repository
        - remote branches have format like `origin/<branch_name>
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
3. 