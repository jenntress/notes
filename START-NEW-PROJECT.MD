## USING EXPRESS "bootstrap the backend"
- cd into directory
- express nameOfApp `express blog` (note that we already installed express globally on this computer)
- Delete any unnecessary things the generator created (views, public, routes)
- documentation: https://expressjs.com/en/starter/generator.html

## BOOTSTRAP
- cd into client, `npm install --save bootstrap`
- require it in the main index.js (the file that is the react brains - probably in src)
- `require('bootstrap/dist/css/bootstrap.css');`
- If that didn't work, add this to public/index.html  `<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">`
- ALSO!!!! Add MY CSS `require('./App.css');` to the main index.js after bootstrap.

## IGNORE NODE MODULES
- cd into main directory, `echo node_modules/ >> .gitignore`
- (success is seeing a new blank file in directory)
- ignore .env because it stores API keys (ex.gmail/amazon - users can use their logins - need to keep them private) add ".env" to your .gitignore file

## REACT ICONS
- `npm install --save react-icons` - Then grab the file path of the icon you want and import it: `import GitHubIcon from 'react-icons/lib/fa/github-square'` Then use it as a normal icon `<GitHubIcon />`

## HEROKU
- kill all terminal windows (including mongodb) SLEEPING WIT DA FISHIES
- download and install Heroku CLI
- open terminal and `heroku --version` "will show current installed version"
- Documentation: https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up
- `heroku login` - sign in with email & password (success is loggin in as...)
- `heroku create + newname of oneline project`

## FAKER "seed the database"
Adds generic data to our database. Note that we don't want this script to run every time we start our server. We'll add an envrioment variable that will tell us if we want to seed our data or not. Documentation: https://github.com/Marak/faker.js
1. add database-seeder.js to the root config folder (using the .env file)
2. `npm install --save-dev faker` (only use for development)
3. Make sure faker is working. Test by model.exports and let title - faker.random.words(); then console log this title. Once we know faker is working...
4. Add a remove function to get rid of all entries in the database and replace them with 20 new ones with an 'if' statement.
5. Turn .env to false - because now we gots some content in our database!
6. Now DELETE or COMMENT OUT the 'if' statement in the app.js before commiting to github.

## MONGOOSE
- We need to install mongoose for each project (no point in installing globally)
- `npm install --save mongoose`

## FAVICON
- just replace the one in public folder with a new one. SO EASY!

## react-scripts-custom
- ```create-react-app client --scripts-version react-scripts-custom```
- cd into the new client directory and ```npm install```
- can do ```npm start``` at this point
- documentation: https://www.npmjs.com/package/react-scripts-custom
- If the above didn't work, do this instead: ```create-react-app client``` instead.
- Test to see if it's working: cd into client, ```npm run start``` YAY!
- Kill server, then ```npm run eject```, are you sure? Y (this dislocates it from its origin so that we can customize its webpack)
- configure our build so we can use modulus css: client/config/webpack.config.dev.js

## FOLDER ROUTING
- to go up one whole folder use ..

## GENERAL NOTES
- Everything in client is a "React Application" that is completely separate thing from our code.
- We can start our react codebase by changing our directory to client. We cd into there and run npm start.
- Everything outside of client is our node specific application. This only manages our database and our API endpoints. We can start up this project by just running nodemon server or node server.
- Each app has its own node modules and package.json
- This doesn't work yet: ...We're gonna create a command that starts both of our apps at the same time and blends them together a little bit so that it seems like it's only one app running - but remember it's two! To start both apps at once run 'npm run dev' (this command has been created in our node package.json)...
