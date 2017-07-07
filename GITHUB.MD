# GIT HUB NOTES

## Save Existing Project (master)
1. `git add -A` Prepacd codring to save changes made to ALL files
2. `git commit –m “description of changes` Add message to your commit, be specific about changes I made.
4. `git push origin master` Pushes changes to the cloud – saves in GitHub

## GitHub Branching
1. `git checkout -b NameofNewBranch` Create a branch, and get into branch.
2. Make changes to files, then
3. `git add -A`
4. `git commit -m "some msg"`
5. `git push origin NameofNewBranch` Push files to this branch.
6. Go to github, click green buttons.
7. `git checkout master`
8. `git pull origin master`

## Login to GitHub
- `git config --global user.name "Your Name Here"` set your user name for commits
- `git config --global user.email "your_email@youremail.com"` set email to 'log in'
- `git config --global user.email` check if I'm logged in (success is returning my email address) Note: do the same thing with 'user.name' to check it.

## Other Commands
- `git status` Shows what’s been synched
- `git remote -v` check to see if we're connected remotely
- `git clone + GitHub URL` CHECK CORRECT DIRECTORY! Add someone else's repository to my C:\
- `mongo --version` Check to see if that program is installed on this device
- `npm init` creates package.json file (press enter on all questions)
- `npm install` creates node-modules folder with packages we want to install plus their specific dependencies
- `--save` saves properties to the dependencies in package.json
- `--save-dev` saves as dev dependencies which are required to run the app, but also required to develop/build the app.
- `git clone + URL` Copy someone else's project to your hard drive. You can add a different file name after the URL ` newname` if you want to put it in a differently named directory.
- `git branch` show a dir list of all your branches

## Create a New Repository
1. Make a new repository on GitHub (copy the URL)
2. `git init` CHECK CORRECT DIRECTORY! creates a new Git repository.
3. `git add -A` Add ALL files to your repository
4. `git commit -m “first commit”` "m" stands for message
5. `git remote add origin + URL` ONLY for the first time we set up a project
6. `git push -u origin master` Push ALL files in this directory to GitHub

## Ignore node_modules
- cd into main directory, `echo node_modules/ >> .gitignore`
- (success is seeing a new blank file in directory)
- ignore .env because it stores API keys (ex.gmail/amazon - users can use their logins - need to keep them private) add ".env" to your .gitignore file

## Undo Mistakes
- `git remote rm + name-of-wrong-command` When Cody spelled "origin" wrong we need to remove it
- `git remote remove origin` When Katie saved her new repository to the wrong location.
- `git remote add origin + URL` This changes the place (URL/origin) of where to save/push.
- `git stash` put the changes you made locally in the "recycle bin" and go back to your last commit.
- `git fetch origin && git reset --hard origin/master && git clean -f -d` - turn your local repository into a mirror image of the remote master (note that this destroys any local changes in your current branch)
