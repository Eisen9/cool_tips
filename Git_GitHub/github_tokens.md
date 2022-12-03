### GitHub Access Tokens

Where to find GitHub Access Tokens? GitHub page > Settings > Developer Settings.

Scenario: you want to push new changes to GitHub repo but upon `git push`, you get an error message due to expired access token. What to do?

STEPS:
*Note: follow these steps if you have an error message (fatal) when pushing to remote repo.*
1. Make a new access token -- you can make it permanent or with expiry date.
2. Once you have a new access token, go back to your code and run `git push`
3. Your code editor will ask you if you want to open authentication in GitHub web, allow that.
4. From the GitHub web, follow the steps on the prompt and go back to your code editor.
5. run `git push` and the push should work fine.
