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


# show all the versions of a npm package
npm show express versions

# update npm packages
npm update

# show packages which will be updated
npm outdated

```

```javascript
// node wraps every file in a function with 5 parameters and a return statement
// and then executes the function
function(module, exports, require, __filename, __dirname) {
  // code inside the file


  return module.exports;
}

// export a function

module.exports = function() {
  // function body
}

// Note: assigning to just export won't export the function

exports = function() {
  // this does not work as exports is a local parameter that
  // has a reference to module.exports  
}

// global variables in node is attached to global object

console.log(global.setTimeout); // [Function: ]

global.a = '12'; // global a variable


// Event emitters
const EventEmitter = require('events');

const myEvent = new EventEmitter();

myEvent.on('lala', () => {
  console.log("blah");
})

myEvent.emit('lala');

// http server using callback
const http = require('http');

// set the callback function to handle incoming requests
const server = http.createServer((req, res) => {
  // res.write('hello world');
  // res.end();
  // or in short
  res.end('hello world');
});

// start the server on port 1234
server.listen(1234, () => {
  console.log('server is running');
});

// http server using event emitters
const http = require('http');

const server = http.createServer();

// set the callback function to handle incoming requests
server.on('request', (req, res) => {
  res.end('hello world');
});

// start the server on port 1234
server.listen(1234, () => {
  console.log('server is running');
});


// creating a http server using express

const express = require('express');

// need to invoke express as it is a function
const server = express();


// set endpoints to handle different routes
app.get('/',  (req, res) => {
  req.send('hello world');
});
// start the server on port 1234
server.listen(1234, () => {
  console.log('server is runningj');
});


// the os module

const os = require('os');

console.log(os.platform());

// the fs module

const fs = require('fs');

fs.writeFile();
fs.readFile(); 

// 

```