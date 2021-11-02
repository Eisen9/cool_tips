### How to use Git and connect to a remote GitHub using JetBrains Products such as IntelliJ.

In this very quick tutorial, you will learn how to push and pull from your local env (IntelliJ) in this example, to a remote GitHub repo.

#### Scenario
Suppose you want are a collaborator in a GitHub repo, you want to make some pushes and pulls from/to your local machine to a remote repo. Here is how you do it:

1. Launch IntelliJ.

2. Choose the option VCS - import from VCS.

3. When prompted to type in a URL, here is what you need to do:
  a. Go to the remote repo you are interested in
  b. Go to <> code from the Navbar
  c. Click the `code` button and you will see a drop down menu
  d. Copy the code that is generated from the `HTTPS` option
  e. paste the code you copied in step *d* into IntelliJ's URL prompt.

4. optional (if there are libraries involved). For the sake of example, we will use a javaparser library here.
From IntelliJ, go to, File > Project Structure > project settings > libraries, then click the + button to add the following library  “com.github.javaparser:javaparser-symbol-solver-core:3.23.1” 
5. Click apply then ok
