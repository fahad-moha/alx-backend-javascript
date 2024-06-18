# Running JavaScript Using Node.js

## Table of Contents
1. [Using Node.js Modules](#using-nodejs-modules)
2. [Reading Files with a Node.js Module](#reading-files-with-a-nodejs-module)
3. [Accessing Command Line Arguments and Environment Using `process`](#accessing-command-line-arguments-and-environment-using-process)
4. [Creating a Simple HTTP Server with Node.js](#creating-a-simple-http-server-with-nodejs)
5. [Creating a Simple HTTP Server with Express.js](#creating-a-simple-http-server-with-expressjs)
6. [Creating Advanced Routes with Express.js](#creating-advanced-routes-with-expressjs)
7. [Using ES6 with Node.js and Babel-node](#using-es6-with-nodejs-and-babel-node)
8. [Developing Faster with Nodemon](#developing-faster-with-nodemon)

## Using Node.js Modules

Node.js provides a built-in module system that allows you to import and use different modules in your code. You can either use the built-in modules or install third-party modules from the Node.js package manager (npm).

Here's an example of how to use a built-in Node.js module:

```javascript
const fs = require('fs');

// Use the 'fs' module to read a file
fs.readFile('example.txt', 'utf8', (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});
```

## Reading Files with a Node.js Module

The `fs` (file system) module is a built-in Node.js module that provides functions for interacting with the file system. Here's an example of how to use the `fs` module to read a file:

```javascript
const fs = require('fs');

fs.readFile('example.txt', 'utf8', (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});
```

## Accessing Command Line Arguments and Environment Using `process`

The `process` object in Node.js provides access to the current process, which includes command-line arguments and environment variables. Here's an example of how to access these values:

```javascript
// Access command-line arguments
console.log(process.argv);

// Access environment variables
console.log(process.env.NODE_ENV);
```

## Creating a Simple HTTP Server with Node.js

Node.js includes a built-in HTTP server module that allows you to create a simple HTTP server. Here's an example:

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!\n');
});

const port = 3000;
server.listen(port, () => {
  console.log(`Server running at http://localhost:${port}/`);
});
```

## Creating a Simple HTTP Server with Express.js

Express.js is a popular web application framework for Node.js that makes it easier to create HTTP servers. Here's an example of how to create a simple HTTP server with Express.js:

```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}/`);
});
```

## Creating Advanced Routes with Express.js

Express.js provides a robust routing system that allows you to create more advanced routes. Here's an example:

```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/users/:id', (req, res) => {
  const userId = req.params.id;
  res.send(`Getting user with ID: ${userId}`);
});

app.post('/users', (req, res) => {
  // Implement logic to create a new user
  res.send('User created');
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}/`);
});
```

## Using ES6 with Node.js and Babel-node

Node.js supports ES6 out of the box, but you can also use Babel to transpile your ES6 code to ES5 for better compatibility. Here's an example of how to use Babel-node:

```javascript
// Install the required dependencies:
// npm install --save-dev @babel/core @babel/cli @babel/node @babel/preset-env

// Create a .babelrc file with the following configuration:
{
  "presets": ["@babel/preset-env"]
}

// Run your ES6 code with Babel-node:
babel-node your-es6-file.js
```

## Developing Faster with Nodemon

Nodemon is a tool that automatically restarts your Node.js application when it detects changes in your files. This can make development faster and more efficient. Here's how to use Nodemon:

1. Install Nodemon globally:
   ```
   npm install -g nodemon
   ```
2. Run your Node.js application with Nodemon:
   ```
   nodemon your-app.js
   ```
   Nodemon will automatically restart your application whenever you make changes to your files.

These are the key points to remember when working with Node.js and related tools. Remember to refer to the official documentation for more detailed information and examples.