# Node JS
(Website)[https://ayonshafiul.github.io/nodejsref]


```sh
# initiale project with default options set to yes
npm init -y
# without default options
npm init


# update npm
npm install -g npm


# install local packages 
npm install packageName

# install global packages
npm install -g packageName

# install as a developer dependency
npm install -D packagename

# list packages
npm list

# npm publish packages
npm login
# then enter credentials and publish
npm publish

# npm run scripts
# scripts are defined in the package.json file as a property of the scritps object
# to run a script just use npm run
npm run start
npm run test
# start and test are used frequently so there is a shortcut
npm start
npm test

# npx is short for npm execute
# npx <packageName> runs locally installed packages
npx eslint
npx jest

# there are pre and post prefixes for every script in package.json
# scripts beginning with pre wil run before running the actual script
# scripts beginning with post will run after running the actual script
# so executing
npm run test 
# will run pretest script then test script and finally posttest


```

```javascript
// export a function

module.exports = function() {
  // function body
}

// Note: assigning to just export won't export the function

exports = function() {
  // this does not work as exports is a local parameter that
  // has a reference to module.exports  
}
