## GitHub & Git Practical Tutorial

#### Make sure you have git installed on your machine.

mac: https://git-scm.com/download/mac
windows: https://git-scm.com/download/windows

check that the install was successful:
* go to command line (terminal on Mac, Git bash or equivalent on Windows)
* run: `git --version`


#### Add your name and email address to git. To do this:

* go to command line
* run: `git config --global user.name 'your name' `
* run: `git config --global user.email 'you email' `
**very important: the email you add in the line above is the email you use for GitHub**.

##### In case you want to change existing git credentials:
Run the following command and follow the instructions in your editor to edit your configuration file:

    `git config --global --edit`

After doing this, you may fix the identity used for this commit with:

    `git commit --amend --reset-author`


### Collaborating on a GitHub project

**Please note: if you are added as a collaborator to a project and want to make changes graphically, you can do so by going to the GitHub repository (where you are a collaborator) and make changes without the need for GIT. However, as your project grows, you will need to use GIT language (from the command line) so you can work efficiently**.


#### STEPS for Collaboration using GIT:

1. make sure you are added as a collaborator to the desired group project.


If you are NOT added as a collaborator (**which is not the case in this tutorial**), you can `fork` the desired repository then create a `pull request`, make changes, then your changes will be reviewed by the owner who can either accept or reject your collaboration.

2. create a folder in your desired location **give it a name of the repository you are going to clone**.

3. Go to the repository you want to clone, select **<> code** from navigation bar, copy code with *HTTPS*. Then, using the command line, navigate to your directory that you have created in step 2 then run: `git clone https://github.com/username/repository_name.git`

Example: https://github.com/Eisen9/cool_tips.git
   where *Eisen9* is the username and
   *cool_tips* is the repository name.

4. make sure that repository is up-to-date on your machine by running: `git pull` .

5. make changes to repository. Example: Suppose you want to add a file to this repository, then here is what you do:

*using the command line*
  *  a. run: `touch myfile.txt`.

  *  b. add some texts to this file.

  *  c. add file to staging area, run: `git add myfile.txt`.

  *  d. commit changes, run: `git commit -m "my changes" `.
    *Note: "my changes" is a string only. You can add a better description but try to keep it short*.

  *  e. push changes from your local machine to remote repository (the repository on the internet that you are collaborating with). Run: `git push`

  Now, go to GitHub and see your changes displayed there :-)


### How to edit new files in a new session?

Okay, suppose you have shut down your computer and now you want to add new files (using GIT) to the repository (that you are collaborating on). How to do this?

#### STEPS:

1. using the command line, navigate to the folder where this repository is locally saved.
2. run: `git log` to see new logs, either by your or by other users.
3. run: `git pull` to make sure that your local files are up-to-date with remote repository.
4. suppose you want to add a new file named *new_file.txt*:
    * a. run: `touch new_file.txt`
    * b. edit new_file.text
    * c. run: `git add new_file.txt`
    * d. run: `git commit -m "add new file" `
    * e. run: `git push`. Your file is now added to the remote    repository.
