# Git Process
This document is purely a reference guide. If you have your own methods, feel free to follow them. This is more for those who want direction or are unfamiliar with Git. Much of this can also be done using GitHub Desktop GUI instead of command line if that's what you prefer. If you have any questions, feel free to ask away in the `#general` channel on Discord.

### How Do I Submit My Changes?
Klavvy controls the master repository. To submit a change, you must first push the changes from your computer to Git. Once pushed, create a Pull Request and Klavvy will review it. If accepted, it will be merged into the master repository. Please ensure to update any associated [Issue(s)]() once a feature has been added.

## Branches
Branches are a wonderful tool to keep changes organized and decoupled. You should avoid working on `main` directly. Instead, keep `main` up-to-date and create branches for each individual feature/fix.

### Keeping Main Up-To-Date
You'll want to regularly update your `main` branch so you're working with the latest code. To do this, run the following commands:
```
git checkout main       # Sets 'main' as current branch
git pull upstream main  # Sync your 'main' with Klavvy's repo
git push origin main    # Updates your forked main on GitHub
```
It's a good idea to do this every time you want to create a new branch and/or before pushing any branch for a pull request to ensure there are no merge conflicts.

### Creating New Branches
Before creating a new branch, ensure your `main` is up-to-date (see above). Once verified, checkout your main branch and run the following:
```
git checkout -b myCoolFeature   # Creates a new branch called 'myCoolFeature'
```

### Commiting Changes
Once you've made the changes you want to make, you can add and commit the changes. First, use `git status` to check which files have been modified.
```
git status
```
If you accidentally modified files that you didn't mean to modify, you can use `git restore filename.ext` to undo those changes.

Next, you'll want to stage the files in preperation to be committed.
```
git add filename.txt    # Adds the file 'filename.txt'
OR
git add *               # Adds all files in the current directory
```
If you accidentally staged a file you didn't want to, you can use `git restore filename.txt` to discard the changes.

Once all the files have been committed, you can use `git status` to see (in green) all files that will be sent. Finally, you'll want to commit these changes using:
```
git commit -m "Provide your description here"
```
*Note: Please try to be crystal clear as to what these code changes are achieving. Descriptions like "Fixed a bug" are too vague and not helpful. Aim for more details such as "Fixed the floating energy crystal bug (Issue 802)".*

### Creating A Pull Request
To create a pull request, you'll need to first push your branch to your fork.
```
git checkout main       # Sets 'main' as current branch
git pull upstream main  # Sync your 'main' with Klavvy's repo
git checkout myCoolFeature  # Sets 'myCoolFeature' as current branch
git merge main          # Merges any updates from 'main' into 'myCoolFeature'
git push origin myCoolFeature   # Pushes myCoolFeature to your fork
```
Once this has been pushed, go to your GitHub repo webpage. If already on the page, you may need to reload the page. You should now see your branch in the branch-menu. Select it, and then select "Create Pull Request". Ensure that this branch is targetting FROM `myCoolFeature` TO `main`. Review the code submission before submitting the Pull Request, and add any applicable details (such as mentioning related [Issue]() links).

---
### RETURN: [First Time Setup](FirstTimeSetup.md)