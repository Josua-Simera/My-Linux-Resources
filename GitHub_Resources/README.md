# Git commands & Workflow

**The typical git workflow goes like this:**

	-> git clone the repo from SSH key
	-> git checkout new branch for your local working directory, I call it "yourname_update_#"
	-> Edit code, files, directories
	-> git add all the relevant files/directories you would like commited
	-> git commit to create a save point on your local machine, can do this multiple times per day/week
	-> git push to move the recently commited changes to the cloud
	-> git pull on different jetson/computer that is on the same branch to update working directory with changes from the cloud


**Terminal Commands**

All _italized_ arguments should be replaced by the relevant name, all non italized arguments is part of the command.

The git checkout command is used to switch between branches in a repository
	
	git checkout main
	
Clone the main repo that is currently checked out on to your local system, this is only done once to set up local environment
	
	git clone _ssh_link_ or _http_link_

Get some information about your currently local repo
	
	git status
	
Get info about all the branches that currently exist
	
	git branch -a
	
Create new branch from the main repo that was previously cloned
	
	git checkout -b _brance_name_
	
Once changes have been made to a file/directory, they are untracked. Add an untracked file/directory so that it is also updated when the branch is commited
	
	git add directory/file

Commit the changes to the tracked files in the branch you are currently working on. Each commit is a local "save point" in time that can easily be reverted back to

	git commit -m'_some comment_'

After a commit, Push branch to remote git to update in the cloud
	
	git push origin _branch_name_
	
Pull branch from remote git when you want updates on the cloud to be downloaded to your local branch

	git pull origin _branch_name_
	
Fetch all of the origin branch names/info

	git fetch
	
Display a log of all activity on the repo	
	
	git log
	
To revert back to a previous "save point", choose a commit hash (can be copied from the "git log" output), and then

	git checkout _commit_hash_
	
If any of the commits are deprecated or broken, next step is to revert them:

	git revert _commit_hash_
	
git revert requires the id of the commit you want to remove keeping it into your history

git reset requires the commit you want to keep, and will consequentially remove anything after that from history.
	


