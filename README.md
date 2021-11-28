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

**Q7** - Run git branch. Did your local copy of your branch delete when Person A deleted the remote branch?

If not, delete the local copy of the branch using git branch -d BRANCHNAME

    'branch2' didn't delete when the local copy was deleted.
  
    **Q8** - Use git log --graph --all to view the branching structure and copy and paste the result into the README.md formatted as a code segment (see markdown cheatsheet).
    
    * commit f005bfbf77e0c557f6e0bbfd2b916b8e2c25cfce (HEAD -> Feature2, origin/Feature2)
| Author: Zion Choi <zchoi22@kentdenver.org>
| Date:   Sun Nov 28 14:35:23 2021 -0700
|
|     changed hello file
|
| *   commit 84e7e26ef5d6e06c956fa1a17cf4b32f123b47b3 (origin/main)
| |\  Merge: d52693d f1caf69
| |/  Author: HotFunyun23 <90862989+HotFunyun23@users.noreply.github.com>
|/|   Date:   Sun Nov 28 14:30:40 2021 -0700
| |
| |       Merge pull request #1 from zchoi22/master
| |
| |       Master
| |
* | commit f1caf69a8d61dd651b2f0e9a7ebeab911dd1b56c (origin/master, origin/branch2, master)
| | Author: unknown <cschaden22@kentdenver.org>
| | Date:   Tue Oct 19 11:22:32 2021 -0600
| |
| |     hello
| |
* |   commit 12eab54a800e5c4a2dcfd5749dd107077f5d1163
|\ \  Merge: 17bf5bf 33a3a5e
| | | Author: unknown <cschaden22@kentdenver.org>
| | | Date:   Tue Oct 19 11:21:54 2021 -0600
| | |
| | |     Merge branch 'master' of https://github.com/zchoi22/github_practice
| | |
| * | commit 33a3a5ef713e472111e341857aa43e4d16af93d9
| | | Author: Zion Choi <zchoi22@kentdenver.org>
| | | Date:   Tue Oct 19 10:45:43 2021 -0600
| | |
| | |     the squeakwal
| | |
| * | commit a4cb3e9e2bd84ee75c74908ff0187ae9e6b2f7c6
|  /  Author: Zion Choi <zchoi22@kentdenver.org>
| |   Date:   Tue Oct 19 08:19:42 2021 -0600
| |
| |       commiting new text file
| |
| * commit d52693d445da58124deedf3b7ce04e3d07380e09
| | Author: zchoi22 <88288951+zchoi22@users.noreply.github.com>
| | Date:   Sun Nov 28 14:30:33 2021 -0700
| |
| |     update with Q7
| |
| * commit 955fff47533c63efb9e5ac5fa9f32b237822c90b
|/  Author: zchoi22 <88288951+zchoi22@users.noreply.github.com>
|   Date:   Tue Oct 19 23:04:34 2021 -0600
:
