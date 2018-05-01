# What is npm and what does it do?
>NPM is node js package manager. Packages are the building blocks of applications and are reusable parts that are available from https://www.npmjs.com/ among many other places all over the internet. These packages are added to our application to use the functionality provided by them. npm is also the command line tool that is used to install, manage and update packages. One of the most important features of npm is dependency management, this allows all proper dependencies to be installed to run all of our packages, for our app to function and for the list of dependencies to be updated in our package.json file.

# What kind of information does package.json hold?
>npm holds information about the app, metadata, and most importantly our dependencies. npm is a way to look at the application structure and see the name of the developer and app, the current version, a brief description, the entry point for the application(usually index.js or main.js), test cases, current git repo, the keywords that describe the app, and the license information. This is the file to go to for insights if you are not familiar with the application. 

# Google another Node package. Using the demo directory run npm install <theNameOfThePackage> --save. Check the contents of your package.json file to make sure that the dependencies list the name of the Node package.
```
npm install mocha --save
```