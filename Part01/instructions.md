# Step 1: Clone
Clone your forked repository to your local machine. 
- Open your preffered your terminal window 
- Go to the root directory where you want to install this repository. (If you go to ~/code or C:/code, the repostiroy will install in ~/code/gitkata or C:/code/gitkata)
> If you haven't set up SSH with github, ensure you select the "Clone with HTTPS" button. This Kata will not go through setting up SSH because I wanted it to be applicable to Windows, Linux, and Mac users. Since Setting up SSH in Windows is more difficult (at least different) than setting it up on Linux/Mac, we stay away from it here.
```
git clone https://github.com/_____/gitkata.git
```

## Status
Let's check the current status of your clone local repository:
```
git status
```
- Hopefully our output is something like this, which indicates that our local repo is in sync with the origin/master branch.
```
On branch master
Your branch is up-to-date with 'origin/master'.

nothing to commit, working tree clean
```

# Adding 
4. Let's add a file to our repository. Inside out the nikgo folder, we will add a [github_username].md file. For example, since my github username is DominikGorecki, I have created a new file called, *DominikGorecki.md* in my favorite editor vim (but feel free to use notepad, atom, vscode, or whatever). 
- After we create the file, let's check the status again: ```git status```
- You should see something like this output that indicates that you have an untracked file in your repo:
```
On branch master
Your branch is up-to-date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	DominikGorecki.md

nothing added to commit but untracked files present (use "git add" to track)
```
- Let's also add a file called *scratch.md* in our favorite text editor
- Let's check status again: ```git status```
- You should now notice that *scratch.md* is also in the "Untracked files list"
- The scratch file is not something we want to push up to the server or even commit to our local repository. The scratch file is just a document we want to keep to ourselves to keep random notes on this project. 
- Let's "add" *[GH_Username].md* to Git. This will essentially tel Git to track this file: ```git add DominikGorecki.md```
- Let's check the status again: ```git status```
- Now you should see something that indicates that you have 1 new tracked file yet to be commmited and 1 untracked file:
```
On branch master
Your branch is up-to-date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   DominikGorecki.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	scratch.md
  ```

5. Let's now commit these staged changes to your local repository: ```git commit -m "Adding DominikGorecki.md"``` 
- At this point, we haven't pushed our changes up to our repository server (origin) so when we go to github.com you will not see your commit there. 

Got to [Part 3](part3.md)

# Branching
5. Oh crap! We just realized that we did all that work on the master branch! Not cool. We should probably put it into a different branch so that we can do a pull request and compartmentalize changes!

- Let's create a new branch then. You can create a new branch and check it out to be your active branch at the same time: ```git checkout -b newStudent/DominikGorecki```

- This creates and checks out the branch *newStudent/DominikGorecki*. Check what branch you are on by running: ```git branch```

- Your output should look something like this:
```
master
* newStudent/DominikGorecki
```

# Resetting Origin/Master
6. At this point our local master branch has a commit against it that we don't want and won't push up to origin. You have the option to revert your commits to this branch, or simply to reset your local master branch to the origin's master branch. We're going to try our hand at reverting commits later, so for now we'll try the second option: reset our local branch to that of the origin--that is, no matter what we have on this branch, we'll make it look like the same branch (master) on origin. 

- First let's switch back to the master branch (set the current active branch to be master): ```git branch master``

- Now let's ensure that this did in fact happen by running ```git branch```. Our output should look something like this, with the astericks next to master now.
```
* master
newStudent/DominikGorecki
```

- Now let's look at the the prevous commits by running ```git log --oneline``` so that our output looks like:
```
xxxxxxx Adding DominikGorecki.md
``` 

- First we run a fetch from origin to ensure we have the latest info from the origin servers: ```git fetch origin```

- Next we run the reset command: ```git reset --hard origin/master```

- Now if we run ```git log --oneline``` we will only see the original commits that occurred before you perfomred the clone