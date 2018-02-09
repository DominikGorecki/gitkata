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
6. At this point our local master branch has a commit against it that we don't want and won't push up to origin. We can either undo that 
