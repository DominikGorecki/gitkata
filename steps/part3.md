# Branching
5. Oh crap! We just realized that we did all that work on the master branch! Not cool. We should probably put it into a different branch so that we can do a pull request and compartmentalize changes!

- Let's create a new branch then. You can create a new branch and check it out to be your active branch at the same time: ```git checkout -b newStudent/DominikGorecki```

- This creates and checks out the branch *newStudent/DominikGorecki*. Check what branch you are on by running: ```git branch```

- Your output should look something like this:
```
master
* newStudent/DominikGorecki
```

# Resetting Origin/Master (Undoing previous)
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
