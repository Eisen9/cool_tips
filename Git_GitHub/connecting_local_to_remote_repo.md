# Connecting a local repository to a remote repository

Scenario: I have a local git repository (was initialised with git init), I want to connect it to a new remote repository, how do I do this?

To connect your local Git repository to a new remote repository, you can follow these steps:

1. Create a new empty repository on the remote platform you want to use (e.g. GitHub, GitLab, Bitbucket, etc.).

2. In your local repository, add the URL of the remote repository as a new remote. You can use the following command, replacing "remote-name" with a name of your choice (e.g. "origin"), and "remote-url" with the URL of your remote repository:
```bash
git remote add remote-name remote-url
```

3. Verify that the new remote was added successfully by running the following command:
```bash
git remote -v
```
This command will list all the remote repositories associated with your local repository.

4. Push your local repository to the new remote repository by running the following command:
```bash 
git push -u remote-name master
```

This command will push your local repository's "master" branch to the new remote repository and set up the tracking information.

Note: If you have a different branch you want to push, replace "master" with the name of your branch.

That's it! Your local repository should now be connected to the new remote repository, and you can continue to push and pull changes between them as needed.