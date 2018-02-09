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