<h1 align="center"> Resetting & Revert </h1>

Images used in this file are downloaded from internet. These are used only for learning purpose.

### Resetting & Revert

When we had commited certain changes and actually we din't want to commit, In that case we can do the changes in two ways

+ Revert - In this method the command will create a new commit, which literally reverse all changes that we have specified. <br />
These chages are useful when we are doing undo the changes and keep those changes in Git history.
	* git revert <COMMIT ID> : this command creates the new commit, which reverse all changes were made in <COMMIT ID>

+ Reset - In this method still there are two types.
	* soft method - This git reset command can be used to retain changes that were made on target commit after the reset operation.
		- git reset --soft HEAD~<No.of COMMITS> : to keep all the changes that were made on no.of commits after reset operation, Where no.of commits are the latest commits. 
	
	* hard method - This git reset command can be used to drop changes that were made on target commit after the reset operation.
		- git reset --hard HEAD~<No.of COMMITS> : to lose all the changes that were made on no.of commits after reset operation, Where no.of commits is number of latest commits.

### Stashing

If we want to make any changes on already commited file while working on working area file. <br />
we can do this by pushing the files from working area to temporary location before rebasing commited file. This operation can be done by using stash

+  git stash : to clear the files in working area and moving the file in temporary location.
+ git stash pop : to retrieve the files from tempoary location which already stashed.
+ git stash list : to list out the no.of stash file in temporarylocation
+ git stash show <STASH No.> : to show the content of file for specific stash
+ git stash pop <STASH No.> : to retrieve the specific stash file.

### Reflog

+ git refolg : to show the all actions have taken on repository (merge, resets, reverts or any alternation.)

### Labs

1. Reseting and Revert - Method of Resetting and Revert commits.
2. Stash - to clear the working area file to tempoarary file using stash , to retrive file from tempoary file using stash pop, stash list etc.
