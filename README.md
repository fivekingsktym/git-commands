# Git Commands

## Basic commands

- git init -> [Initializes git in a specific folder]

- git add . -> [Adds all files to the staging area]

- git status -> [Displays the staging status of the files]

- git commit -m "first commit" -> [Commits the changes to the staging area with a message]

- git commit --amend -m "New commit message" -> [Modify the most recent commit in your Git history. It allows you to make changes to the last commit]

- git log -> [To show all commit message in the command ling]

- git remote add origin url -> [ Adds the git repository to a third-party storage like GitHub, Gitlab, Bitbucket]

- git remote -v -> [it shows the current remote directory]

- push -u origin main -> [Sends the git repository to the third-party server like GitHub]
 
 ## Branch commands

- git branch -> [showing all branch names]

- git branch new-branch-name -> [create a new branch]

- git checkout new-branch-name <or> git switch  new-branch-name -> [To switch to an existing branch]

- git checkout -b new-branch-name <or> git switch -c new-branch-name -> [create a new branch and switch to that branch in a single step]

- git branch -d branch-name -> [To delete a branch(Safe deletion), Alert: Deleting the branch is not possible when you are currently on it.]

- git branch -r -> [To see remote branches (branches in a remote repository)]


## Rebasing n number of commit messages [Editing commit messages]

```bash
git rebase -i HEAD~n

<Replace n with the number of commits you want to edit. For example: git rebase -i HEAD~3 >

<After running the command, a text editor will open with a list of commits in your default text editor (such as Vim or Nano). Each commit will be prefixed with the word "pick." To edit a commit message, change "pick" to "reword" (or just "r" for short) in front of the commit you want to edit.>

- Example: 

pick 5418ffd sample.js and test.py files added

<change to>

reword 5418ffd sample.js and test.py files added

<Save and Close the Editor: Save the changes and close the text editor. use :wq then press enter>

<Edit the Commit Message: Git will now pause at the commit you marked for editing. The text editor will open again with the existing commit message. Modify the commit message to your liking, save, and close the text editor.>

```
