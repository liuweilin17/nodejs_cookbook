# nodejs_cookbook
Node.js is a powerful JavaScript framework that is developed on Chrome’s V8 JavaScript engine. It helps in compiling [JavaScript](https://www.edureka.co/blog/what-is-javascript/) directly into the native machine code.Node.js extends JavaScript API which enables the usual server-side functionalities as well. It is generally used for large-scale application development, especially for video streaming sites, single-page application, and other web applications. Node.js makes use of an event-driven, non-blocking I/O model which makes it a right pick for the data-intensive real-time applications.

Here are the outline:

* <a href="#architect">Architecture</a>
* <a href="#npm">NPM</a>
* <a href="#rest-api">REST API</a>
* <a href="#express">Express.js</a>
* <a href="#http">HTTP Request</a>

## <div id="architect">Architecture</div>

Generally, the server-side technologies like [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/), ASP.NET, [Ruby](https://www.edureka.co/blog/ruby-on-rails-tutorial/) & [Java](https://www.edureka.co/blog/java-tutorial/) Servers all follow a multi-threaded model. In this traditional architectural approach, each client request creates a new thread or a process.

![alt text](img/NodeJS-Architecture.png "nodejs architecture")

To avoid this, Node.js uses **Single Threaded Event Loop Model** **Architecture**. It means that all the client requests on Node.js are executed on the same thread. But this architecture is not just single-threaded, but event-driven as well. It helps Node.js in handling multiple clients concurrently. Below diagram, represents the Single Threaded Event Loop Model architecture.

![alt text](img/Single-Thread-Architecture.png "nodejs architecture")


## <div id="npm">NPM</div>

NPM stands for Node Package Manager, the default package manager of Node.js that is completely written in JavaScript.

It provides online repositories for packages/modules for Node.js which you can easily search online on their [official site](https://www.npmjs.com/).

It also provides a Command Line Interface (CLI) which helps the developers in locally interacting with their systems.

* npm version: 

  ```bash
  npm -v
  ```

* Initialize:

  ```bash
  npm init
  ```

  Node.js will ask you to enter some details to build .json file

* Install packages

  ```bash
  npm install <package-name> # locally
  npm install -g <package-name> # globally
  npm install <package_name> --save # requested module added to package.json
  npm list -g --depth 0 # check global packages
  ```

* package.json

  *Main:* Points to the entry point/file of the application

  *Scripts:* Contains the list of scripts which are required to be included in the application to execute properly

  *Dependencies:* Depicts the list of 3rd Party packages or modules installed using NPM

  *DevDependencies:* Dependencies that are used only in the development part of the app are specified here

* Some useful packages:

  *Express*: Fast, unopinionated, minimalist web framework for [Node.js](https://nodejs.org/en/)

  *nodemon*: Implicitly detect the changes and restart the server for you

## <div id="rest-api">REST API</div>

**RE**presentational **S**tate **T**ransfer. It is an architectural style as well as an approach for communications purposes that is often used in various web services development. It is an application program interface (API) that makes use of the HTTP requests to GET, PUT, POST and DELETE the data over WWW.

## <div id="express">Express.js</div>

the de facto standard server framework for Node.js.

* Example:

  ``` javascript
  //Importing express module
  const express = require('express') 
  //Creating an express module object
  const app = express() 
   
  //Creating Callback function and sending response
  app.get('/', (req, res) => res.send('Welcome to Edureka Demo!!!'))
   
  //Establish the server connection
  //PORT ENVIRONMENT VARIABLE
  const port = process.env.PORT || 8080;
  app.listen(port, () => console.log(`Listening on port ${port}..`));
  ```

* Routing methods:

  ```javascript
  app.METHOD(PATH, HANDLER)
  // app is an instance of express where you can use any variable.
  // METHOD is an HTTP request method such as get, set, put, delete.
  // PATH is the route to the server for a specific webpage.
  // HANDLER is the callback function that is executed when the matching route is found.
  ```

## <div id='http'> HTTP Request </div>
* HTTP Module
```javascript
const https = require("https");
const url = "<a href="https://my-json-server.typicode.com/edurekaDemo/noderequest/db">https://my-json-server.typicode.com/edurekaDemo/noderequest/db</a>";
https.get(url, res => {
res.setEncoding("utf8");
let body = "";
res.on("data", data => {
body += data;
});
res.on("end", () => {
body = JSON.parse(body);
console.log(body);
});
});
```

* Request Module

  ```javascript
  const request = require("request");
  const url = "<a href="https://my-json-server.typicode.com/edurekaDemo/noderequest/db">https://my-json-server.typicode.com/edurekaDemo/noderequest/db</a>";
  request.get(url, (error, response, body) => {
  let json = JSON.parse(body);
  console.log(body);
  });
  ```

* Axios Module

  It provides a single API for handling XMLHttpRequest and node’s HTTP interface, generally used when one is dealing with a complicated series of events. And since building asynchronous code can be really confusing, Promises has become one of the most prominent solutions to this problem.

  ``` javascript
  const axios = require("axios");
  const url = "<a href="https://my-json-server.typicode.com/edurekaDemo/noderequest/db">https://my-json-server.typicode.com/edurekaDemo/noderequest/db</a>";
  const getData = async url => {
    try {
      const response = await axios.get(url);
      const data = response.data;
      console.log(data);
    } catch (error) {
      console.log(error);
    }
  };
  getData(url);
  ```

  

## Reference

* [edureka blog](https://www.edureka.co/blog/node-js-npm-tutorial/)
* 