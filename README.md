# github_practice

**Q1** - What does clone set the variable origin to represent?
The "clone" command sets the variable origin as the project's URL.

**Q2** - What does the command git push --set-upstream origin master do? What does remote tracking mean in this context?
Upstream branches define the branch tracked on the remote repository by the local remote branch. Sets the main branch as upstream.

**Research and then execute the following command: git pull origin master**

**Q3** - Explain and illustrate what's happening in the commit when this command executes.
'git pull origin master' will fetch and update the master branch under origin (the remote repository).

**Q4** Are your commits overwritten by remote master?
No, because commits are saved locally and saved in the history. However, after pushing, history can only be overwritten via 'git commit --amend', 'git rebase -i', and 'git push --force'.

**Q5** Is this a merge or a rebase?
'git pull' does a 'git fetch' and then merges the code from the tracking branch and to the local version of that branch. Basically, a 'git fetch' followed by a 'git merge'.

**Q6** Person B: checkout the local master branch. Is it updated as well, or still behind remote master?

Person B: push to your remote branch using: git push --set-upstream origin <BRANCHNAME>
    Go to the Github repository and first. Verify that your changes are uploaded. Second, opena  pull       request descibing your (fake) feature that you are asking to merge into the master development           branch.
Person A: resolve the pull request by looking over the changes requested for the merge on your own computer, and then closing the pull request.
    Delete the remote branch from Person B (the feture is merged into your product, no need to keep the     feature branch hanging about.)
Person B: checkout master, pull from master.
