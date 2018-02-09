## Adding 
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

5. Let's now commit these staged changes to your local repository: ```git commit -m``` 
- At this point, we haven't pushed our changes up to our repository server (origin) so we go to github.com, 

Got to [Part 3](part3.md)