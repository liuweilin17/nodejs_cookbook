# nodejs_cookbook
* Node.js is an open source server environment
* Node.js uses JavaScript on the server
* Node.js uses asynchronous programming
* Node.js can generate dynamic page content, create, open, read, write, delete, and close files on the server, collect form data, add, delete, modify data in your database

Here are the outline:

* <a href="#npm">NPM</a>
* <a href="#rest-api">REST API</a>

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



## Reference

* [edureka blog](https://www.edureka.co/blog/node-js-npm-tutorial/)
* 