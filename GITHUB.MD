# GIT HUB NOTES

## Save Existing Project
1. `git add -A` Preparing to save changes made to ALL files
2. `git commit –m “description of changes` Add message to your commit, be specific about changes I made.
3. `git push origin master` Pushes changes to the cloud – saves in GitHub

## Other Commands
- `git status` Shows what’s been synched
- `git remote -v` check to see if we're connected remotely
- `git clone + GitHub URL` CHECK CORRECT DIRECTORY! Add someone else's repository to my C:\
- `mongo --version` Check to see if that program is installed on this device
- `git remote origin set-url + URL` Save someone else's repository to one I made on GitHub
- `npm init` creates package.json file (press enter on all questions)
- `npm install` creates node-modules folder with packages we want to install plus their specific dependencies
- `--save` saves properties to the dependencies in package.json
- `--save-dev` saves as dev dependencies which are required to run the app, but also required to develop/build the app.
- `git clone + URL` Copy someone else's project to your hard drive. You can add a different file name after the URL if you want to put it in a differently named folder.

## Create a New Repository
1. Make a new repository on GitHub (copy the URL)
2. `git init` CHECK CORRECT DIRECTORY! creates a new Git repository.
3. `git add -A` Add ALL files to your repository
4. `git commit -m “first commit”` Label the first time I send something  ( "m" stands for message)
5. `git remote add origin + http:...GitHub URL` ONLY for the first time we set up a project
6. `git push -u origin master` Push ALL files in this directory to GitHub

## Ignore node_modules
- cd into main directory, `echo node_modules/ >> .gitignore`
- (success is seeing a new blank file in directory)
- ignore .env because it stores API keys (ex.gmail/amazon - users can use their logins - need to keep them private) add ".env" to your .gitignore file

## Undo Mistakes
- `git remote rm + name-of-wrong-command` When Cody spelled "origin" wrong we need to remove it
- `git remote remove origin` When Katie Katie saved her new repository to the wrong location.
- `git remote add origin + URL` This changes the place (URL/origin) of where to save/push.

## GitHub Branching
- Create a branch and get into it. `git checkout -b articles` - note that "articles" is the name of the new branch.
- Make changes to files, then
 - `git add -A`
 - `git commit -m "some msg"`
 - `git push origin articles` -> Note you pushed to your new branch
 - `git checkout master`
 - `git merge articles` -> brings your new code into articles
 - `git push origin master` -> sync your master branch with new code
