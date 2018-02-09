# gitkata
A Kata to practice some GIT fundamentals. Please FORK and follow the instructions. 
1. Fork this repo (FORK button in the top right)

## Clone
2. Clone your forked repository to your local machine. 
- Open your preffered your terminal window 
- Go to the root directory where you want to install this repository. (If you go to ~/code or C:/code, the repostiroy will install in ~/code/gitkata or C:/code/gitkata)
> If you haven't set up SSH with github, ensure you select the "Clone with HTTPS" button. This Kata will not go through setting up SSH because I wanted it to be applicable to Windows, Linux, and Mac users. Since Setting up SSH in Windows is more difficult (at least different) than setting it up on Linux/Mac, we stay away from it here.
```
git clone https://github.com/_____/gitkata.git
```

## Status
3. Let's check the current status of your clone local repository:
```
git status
```
- Hopefully our output is something like this, which indicates that our local repo is in sync with the origin/master branch.
```
On branch master
Your branch is up-to-date with 'origin/master'.

nothing to commit, working tree clean
```

Got to [Part 2](steps/part2.md).
## Adding 
4. Let's add a file to our repository. Inside out the nikgo folder, we will add a [github_username].md file. For example, since my github username is DominikGorecki, I have created a new file called, *DominikGorecki.md* in my favorite editor vim (but feel free to use notepad, atom, vscode, or whatever). 
- After we create the file, let's check the status again: ```git status```
- You should see something like this output that indicates that you have an untracked file in your repo:
```
On branch master
Your branch is up-to-date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.md

nothing added to commit but untracked files present (use "git add" to track)
```
- Let's also add a file called *scratch.md* in our favorite text editor
- Let's check status again: ```git status```
- You should now notice that *scratch.md* is also in the "Untracked files list"
- The scratch file is not something we want to push up to the server or even commit to our local repository. The scratch file is just a document we want to keep to ourselves to keep random notes on this project. 
- Let's "add" *[GH_Username].md* to Git. This will essentially tel Git to track this file: ```git add DominikGorecki.md```
- Let's check the status again: ```git status```
