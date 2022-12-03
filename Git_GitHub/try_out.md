# Git Remote
*Heads-up! This doc is scenario-based.*


Scenario: you created a directory on your local machine and then, you `git init`, you made changes: created file, modified them, made branches...etc. Now you want to connect this local repo to a remote one. How to do this? See Below.

------

## Task

do the following to recap your knowledge of git and to try out new things.

1. create a directory in your local machine
2. git init inside 1
3. make some files
4. make some branches, merges and commits
5. create a GitHub repo
6. inside your directory (1), do git clone <link for GitHub repo>
7. see that the local and the remote repos are in sync.

------
## Understanding how things work

Scenario: You create a directory on your local machine, you then `git init` in that directory, create files, add them to the staging area, and commit the changes. Once you run `git push`, you get the following message:
```
╰─ git push                                       ─╯
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>

```

follow the steps in the message, then you will need to run:
`git push --set-upstream GitHub_Testing_V1 master` the set up stream to master is a suggestion from git after you run `git push <name>`.

In your GitHub page, you should see that there is a pull request waiting for you. You can do compare and pull. Note, a log of the details is provided in the Appendix.

*Important note: next time you push, you only run `git push`*.

## Appendix
As you see in the error message, there is no name and url specified. This means that your next step would be creating a repository on GitHub and then copying the link of that repository and pasting it as an argument in the `git remote add <name> <url>`. Also, you need the name of the repo.

Try it now. Adding a README file in the repo is optional, try adding one.

what happened?
I ran: `git remote add GitHub_Testing_V1 https://github.com/Eisen9/GitHub_Testing_V1.git`
then refreshed the GitHub page; no changes were present there. Presumably, the files that are on the local machine were not present in the remote repo because there was no `git push` after you have done `git remote add`
