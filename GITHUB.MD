# GIT HUB NOTES

## Work Specifics
- cd into reactMobile
- verify branch is current assignment, if not `git checkout -b NameofNewBranch`
- `git pull origin NameOfBranch`
- `npm run start-dev`
- new tab, cd into reactMobile `npm run webpack-dev-browser`
- Login at S20: http://localhost:3000/WebMobility/SearchPage
- MAKE CHANGES, THEN...
- `git add -u src` OR individual files if only a few
- `git commit -m "some msg"`
- `git push origin NameOfBranch`
- go to github and create pull request
- update Jira status

## Other Commands
- `git add "src/component/Home/Home.js"` add ONE file to push up to github
- `git add -u src` add modified files from the src directory
- `npm init` creates package.json file (press enter on all questions)
- `npm install` creates node-modules folder with packages we want to install plus their specific dependencies
- `--save` saves properties to the dependencies in package.json
- `--save-dev` saves as dev dependencies which are required to run the app, but also required to develop/build the app.
- `git clone + URL` Copy someone else's project to your hard drive. You can add a different file name after the URL ` newname` if you want to put it in a differently named directory.
- `git stash clear` remove all saved stashes from your local machine
- `git stash list` list all local stashes - success shows "stash@{0}: WIP on..."
- `git branch` list of all your branches

## Troubleshooting
- `npm cache clean` clear cache
- `git status` shows what’s been synched
- `git remote -v` check to see if we're connected remotely
- `npm outdated` list all dependencies and compare versions (show missing)
- `npm-install-missing` reinstall any missing dependencies
- `git show --oneline -s` view which commit currently checked out
- `npm list -g` list which packages you have installed globally
- `npm list -g NameofDependency`check to see if a specific package is gloally installed
- `git diff` show changes between commits (brings you into "less" prompt - type `q` to quit)
- `mongo --version` Check to see if a program (in this case mongo) is installed on this device

## Undo Mistakes
- `git reset --hard` `git pull` get rid of local changes and update files to match branch
- `git add -A` `git stash` put the changes you made locally in the "recycle bin" and go back to your last commit. (basically just trash these changes)
- `git add ...` `git commit --amend` make a change right after you committed (follow propmpts to change or keep the commit message).
- `git remote rm + name-of-wrong-command` When Cody spelled "origin" wrong we need to remove it
- `git remote remove origin` When Katie saved her new repository to the wrong location.
- `git remote add origin + URL` This changes the place (URL/origin) of where to save/push.
- `git reset --soft HEAD~`then `git reset` - Undo latest commit. Removes the latest commit from github and unstages local changes.
- `npm uninstall -g jshint` remove a global package (in this case jshint)

## Save Existing Project (master)
1. `git add -A` Prepare to save changes made to ALL files
2. `git commit –m “description of changes` Add message to your commit
4. `git push origin master` Pushes changes to the cloud – saves in GitHub

## Create a New Repository
1. Make a new repository on GitHub (copy the URL)
2. `git init` CHECK CORRECT DIRECTORY! creates a new Git repository.
3. `git add -A` Add ALL files to your repository
4. `git commit -m “first commit”` "m" stands for message
5. `git remote add origin + URL` ONLY for the first time we set up a project
6. `git push -u origin master` Push ALL files in this directory to GitHub

## GitHub Branching
- `git branch` List all branches you've ever checked out on this device?
1. `git checkout -b NameofNewBranch` Create a branch, and get into branch.
2. Make changes to files, then
3. `git pull origin master` (optional, but a good idea)
4. `git add -A` Add ALL changed files to your repository
5. `git commit -m "some msg"`
6. `git push origin NameofNewBranch` Push files to this branch.
7. Go to github, click green buttons.
8. `git checkout master` (if you want to switch branches)

## Git Ignore
- `echo node_modules/ >> .gitignore` (success is seeing a new blank file in directory)

## File Locations
- Global npm installs location (Windows 7):
C:\Users\turnerj\AppData\Roaming\npm\node_modules

## Login to GitHub
- `git config --global user.name "Your Name Here"` set your user name for commits
- `git config --global user.email "your_email@youremail.com"` set email to 'log in'
- `git config --global user.email` check if I'm logged in (success is returning my email address) Note: do the same thing with 'user.name' to check it.

## PUll a single file from a repository???
git fetch --all
git checkout origin/master -- <your_file_path>
git add <your_file_path>
git commit -m "<your_file_name> updated"

git fetch  
git checkout origin/master -- path/to/file
