### Make changes to existing file:

suppose you have a file named tip1.txt and it is already on your GitHub repository and you need to change its file extension as well as some contents. So here is what you need to do:

1. open command line.
2. navigate to the folder where tip1.txt (desired file) is located.
We assume that git is initialised in that folder. In case you want to check, run: `git init`.
3. make the desired changes (whether contents or file extension).
4. suppose you changed the extension of the file to *.md* run `git add tip1.md`
5. `git commit -m "change file extension and some contents" `
6. `git push`

Now, check your GitHub repository and you will see the change.

