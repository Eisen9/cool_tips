#### Create and initialise repository from command line:

1. create a repository WITHOUT A README file
2. once you hit create, you will see the following code:

```
echo "# cool_tips" >> README.md

git init

git add README.md

git commit -m "first commit"

git branch -M main

git remote add origin https://github.com/username/repository_name.git

git push -u origin main

```
