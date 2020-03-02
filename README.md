# nodejs_cookbook
* Node.js is an open source server environment
* Node.js uses JavaScript on the server
* Node.js uses asynchronous programming
* Node.js can generate dynamic page content, create, open, read, write, delete, and close files on the server, collect form data, add, delete, modify data in your database

Here are the outline:

* <a href="#npm">NPM</a>



### <div id="npm">NPM</div>

NPM stands for Node Package Manager, the default package manager of Node.js that is completely written in JavaScript.

It provides online repositories for packages/modules for Node.js which you can easily search online on their [official site](https://www.npmjs.com/).

It also provides a Command Line Interface (CLI) which helps the developers in locally interacting with their systems.

* npm version: 

  ```{shell}
  npm -v
  ```

* Install packages

  ```{shell}
  npm install <package-name> # locally
  npm install -g <package-name> # globally
  npm install <package_name> --save # requested module added to package.json
  npm list -g --depth 0 # check global packages
  
  ```



## Reference

* [edureka blog](https://www.edureka.co/blog/node-js-npm-tutorial/)
* 