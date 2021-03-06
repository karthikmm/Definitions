# Definitions

##NODE.js
Its is a platform build on chrome's javascript runtime for easily buliding network applications.
```javascript
example.js
var http = require('http');

http.createServer(function (request, response) {
  response.writeHead(200, {'Content-Type': 'text/plain'});
  response.end('Hello World\n');
}).listen(8124);

console.log('Server running at http://127.0.0.1:8124/');
```
#####output : Hello World

Nodejs is used to build scalable network application.

Scalability stand for an application which can be used even after their is a change in its size volume etc.

A Network application is any application running on one host and provides a communication to another application running on a different host, the application may use an existing application layer protocols such as: **HTTP(e.g. the Browser and web server), SMTP(e.g. the email-client)**.

For every framework their must be few pacakage managers.

###NPM
--------------------------------
npm is a node pacakge manager complety written in javascript for default nodejs.It is also package manager to grunt,gulp,browserfiy etc.It is used by javascript developers to share and reuse the code,and is very easy to update the code.

These code are called packages or modules.Every pacakge  contain package.json which contain some embedded data about the  package.node-module is a directory.

npm init is used to avoid every time usage of npm install and to download all 20 dependencies.It creates package.json file with all dependecies.

Dependencies are nothing but the packages which you have installed. Dependencies can be added manual by inserting them in the directory with "*", so as to download the latest version.
```sh
$ npm outdated 
```
command gives u the list of outdated packages,with their latest version.
```sh
$ npm update 
```
command will update the packages.
```sh
$ npm uninstall <package name>
```
will uninstall the package from the node module, but when u use ls command it shows unmet error with the uninstall package name,which indicates that it still the package exists in package.json file and is needed for it usage. To avoid this use 
```sh
$ npm install packagename --save 
```
If this is done in viceversa it shows extraneous error, which mean it doesnt need that package.
when we delete node modules, we can create it again by simply using 
```sh
$ npm install
```
where itsearches for all packages required for a project from package.json file and create a node module directory.


###GRUNT:
------------------
It is used to perform repitative task like compiling,minification etc.Simply used for automation.

It is created using
```sh
$ npm install -g grunt-cli
```
(command line interface)
```sh
$ npm install grunt --save-dev 
```
Is used to create grunt as a dependency in package.json file.

plugins are used which are generated from npm module
```
database.grunt-contrib-uglify
grunt-contrib-qunit
grunt-contrib-concat
grunt-contrib-jshint
grunt-contrib-watch
```
These are few offical plugins.
It contains mainly two files **gruntfile and package.json file**. 
Gruntfile consist of 
The "wrapper" function, 
Example :
``` 
module.exports = function(grunt) {
}
```
Project and task configuration, example: 
```javascript
grunt.initConfig({
  pkg: grunt.file.readJSON('package.json'),
  uglify: {
    options: {
      banner: '/*! <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> */\n'
    },
    build: {
      src: 'src/<%= pkg.name %>.js',
      dest: 'build/<%= pkg.name %>.min.js'
    }
  }
});
```
Loading Grunt plugins and tasks 
Example:
```
grunt.loadNpmTasks('grunt-contrib-uglify');
```
Custom tasks,
Example:
```
grunt.registerTask('default', ['uglify']); 
```
default task

###GULP:
--------------------
It is similar as Grunt, it has also many plugins defined.
Gulp does essentially the same thing as Grunt but with a more modern interface.

###WebPack:
----------------------
It is a **module Bundler**. Webpack takes modules with dependencies and generates static assets representing those modulues.it is mainly used for codespliting.
There are two versions in webpack ,static and beta. -beta is used toinstall it which may contain experimental features.


###yoeman:
-----------------
It consists of three tools
**yo, bower , grunt or gulp**.

**yo** is a scaffolding tool that offers an ecosystem of framework-specific scaffolds, called generators, that can be used to perform some of the tedious tasks mentioned earlier.
*Yeoman* also works with other tools for improving your productivity:

**Grunt** is used to build, preview, and test your project, thanks to help from tasks curated by the Yeoman team and grunt-contrib.

**Gulp** is an alternative to GruntJS that favors code over configuration.

bower is used for dependency management, so that you no longer have to manually download your front-end libraries.
