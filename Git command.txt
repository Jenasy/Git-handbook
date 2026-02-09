Git Workflow Diagram:

[WORKING DIRECTORY] --git add--> [STAGING AREA] --git commit--> [LOCAL REPOSITORY] --git push--> [REMOTE REPOSITORY]

Explain:
- WORKING DIRECTORY: direct file editing area.
- STAGING AREA	   : location where changes are marked for the next commit
- LOCAL REPOSITORY : storage for commits and version history on the local machine
- REMOTE REPOSITORY: online storage for hosting, sharing, and collaboration

Some common commands in git:

 	* IN LOCAL REPOSITORY

git init [<repo name>]				 : initialize a new Git repository.

git clone <URL> [<clone name>]			 : Copy an existing repository from a remote source.

git config [flags] [scopes] [option.name] <value>: Configure settings (e.g., username, email)
	scopes:	--system | --global | --local

git status					 : display the state of the working directory and the staging area.

git log [flags]					 : Show the commit history.

git add <filename> | . 				 : Add file changes to the staging area.

git commit -m "<comment>"			 : Record changes to the local repository with a descriptive message.

git diff					 : Show changes between commits, commit and working tree, etc

git checkout <commit hash> | <branch name>	 : Switch branches or restore working tree files.

git branch <branch name> 			 : Create a new branch.

git branch [flags]				 : List, filter or delete branches.
	git branch -d <branch name>	: Delete a local branch.
	git push origin -d <branch name>: Delete a remote branch.

git merge <branch name>				 : Join two or more development histories together.

git rebase <branch name>			 : Reapply commits on top of another base tip.
	git rebase --continue		: Restart the rebasing process after resolving a merge conflict.
	git rebase --skip		: Restart the rebasing process by skipping the current patch.
	git rebase --abort		: Cancel the rebase operation and return the branch to its original state (before rebasing started).

git reset [flags] <commit hash>			 : Reset current HEAD to the specified state.

git revert <commit hash>			 : Create a new commit that undoes the changes from a previous commit.
	git revert --continue 		: Restart the revert process after resolving merge conflicts.
	git revert --skip		: Skip the current commit and continue with the rest of the sequence.
	git revert --abort	 	: Cancel the revert operation and return to the state before the command was run.

	* INTERACT WITH REMOTE REPOSITORY

git fetch 					 : Download objects and refs from another repository without merging

git pull					 : Fetch from and ingrate with another repository or a local branch

git push					 : Update remote refs along with associated objects.

git remote add <name> <URL>			 : Connect local repository to a remote server.
	Common name: origin

git remote -v					 : Verify the remote connection (Display URL).

git remote set-url <name> <new_url>		 : Change the URL of an existing remote.

git remote remove <name>			 : Disconnect the link to the remote repository.



