Branch

To manage different versions of same code base, branch function is used.
It allows you to branch out from original code base and isolate their work from others and merge it to primary branch later.
Changes in primary branch or any other branch will not affect your branch, unless you decide to pull that changes. 

Use the branch command with a name to create a new branch with that name. Use git branch <branchname>
To switch between branches, use git checkout <branch name>.
Use the merge command to merge branches. Use git merge <branch name>.
We can delete a branch by calling the branch command and passing in the -d option, followed by the branch name. Use git branch -d <branchname>


Head is pointer to branch currently you are. It is used by git to represent the current snapshot/position of the branch.

During "merge", Git will attempt to automatically apply those history changes and merge them with the current branch. 

There are times that "merge" could fail and that can happen when there is a conflict. If two or more members make changes on the same part of a file in the two different branches (remote and local branch in this case) that are being merged, Git will not be able to automatically merge them and you will get a merge conflict.

When this happens, Git will add some standard conflict-resolution markers to the conflicting file. The markers act as an indicator to help us figure out sections in the content of the conflicting file that needs to be manually resolved.

Whenever you switch to new branch with uncommited changes, those uncommitted changes will also be carried to the new branch. If Git finds conflict between those uncommited changes and files in new branch, you can't checkout to new branch. So you have to commit or stash those uncommited changes.
Stash stores uncommited changes(modified tracked files or staged changes) temporarily on a stack so that you can reapply that at any time.

