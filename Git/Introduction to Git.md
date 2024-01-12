# What does git do?
1. Repositories
2. Clones a project from our local machine on to the repository
3. Allows us to control and track changes(staging and committing)
4. Pull : updates the latest version of the project to the local copy
5. Push : updates the local project changes into the main project

Imagine a team of 2 people working on a project that has been initialized in a git repository.
Person A makes changes locally and PUSHES them onto the main project.
Person B cannot access A's machine for obvious reasons. He then PULLS the project files(containing the changes made by A), and then works on the project, and then pushes it onto the repository.

## Steps in Git
1. Initializing a git folder (repository)
2. Git keeps track of the changes going on in that folder
3. Any change is known as a *modification*
4. Changes can be staged. Here information regarding what will go into your next commit goes into a file called the staging area. 
5. Stages can be committed : prompts Git to store a permanent snapshot of the files
6. You can view the history of every commit, and revert back to a previous commit.
7. **Does not store a copy of every file in every commit. It keeps track of the changes made in each commit**

### Git configuration

Allows you to set values on a global or local project level.
Global : controls settings for the current logged in user and all the repositories.
Local : Controls settings only for a specific repository.

1. the `git config` command accepts arguments to specify which configuration level to operate on.
		- `local` : by default, applied to the context repository.
		- `global` : applied to an OS user. Info is stored in a file that is located in the user's home directory
		- `system` : applied across the entire machine. Lives in the root path, covers all users on the OS and all repos.
	
```bash
git config --arg user.email
```

```bash
git init //initialises an empty repository in the directory you are working on
```

```bash
git status //lets us know whether any commits have been made, and whether the file is part of our repo. 
```

Tracked : files that Git knows about and are added to the repository
Untracked :files that are in the working directory but are not added to the repository.

1. When files are first added to an empty repository, they are all untracked. You must stage them in order to track them.

`git add file_name` : adds the file to the staging environment.

`git status` : now shows the "changes to be committed" statement. This means that the file has been staged but not committed.

```bash
git rm --cached file_name //unstages
```

`git add --all` : lets you add all files in the current directory to the S.E

`git add file1 file2` : adds specified files

          
