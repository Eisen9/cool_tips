### Branches
*📢If you want the short version (commands only), scroll down to the end of this doc*.

In this file, you will find the following:

Using the command line and git:

* create a new branch
* make changes in your new branch
* merging these changes with the main branch.

#### Practical Steps for creating

* see past logs
`git log`

* create a branch
`git branch my-new-branch`

* check what branches you have
`git branch`
The asterisk in the command line, shows you which branch you are currently on.

* to switch from branch to branch  
`git checkout my-new-branch` or, `git checkout main`

* now, you can make changes to the file(s) that is/are in the master branch. However, the code in the master will not be changed. The only change (to the file(s) that you wish to change), will be in your new branch.

* while in the new branch, add files
`git add .`

* while in the new branch, commit your changes
`git commit -m "my changes" `

* at this stage, you have my-new-branch locally. If you want to have it remotly, on GitHub, you can run: `git push --set-upstream origin my-new-branch`

* see your commits:
`git log`
here, you will see what branch has been committed to.

* to see that nothing changed in the main branch, you can switch to your main `git checkout main` then view the file(s) that you had changed in the other branch. You will notice that the changes that were made in the other branch are not present in the main branch.


Now, suppose you are happy with the changes you made in the new branch and you wish to merge them with the main branch. Here is what you do:

*** Note, you have to be in the main branch to do the merging.

STEPS:
* a. switch to main. Run: `git checkout main`
* b. merge all changes with main. Run: `git merge my-new-brach`
* c. push changes. Run: `git push` or `git push main origin main -u`


#### In Short:
In short, here is what you do if you want to create a new brach, make changes in it then merge it with main:

* `git branch my-new-branch`
* `git checkout my-new-branch`
* make changes: edit / create new files
* `git add .` or `git add <file>`
* `git commit -m "my changes"`
* if you want to make your branch remote (locally as well as on GitHub). Run: `git push --set-upstream origin my-new-branch`
* If you are happy with your changes, switch to the main branch to merge from there. Run `git checkout main`
* push changes `git push`



*End*.
