# Definations
NODE.js:
its is a platform build on chrome's javascript runtime for easily buliding network applications.
example.js
var http = require('http');

http.createServer(function (request, response) {
  response.writeHead(200, {'Content-Type': 'text/plain'});
  response.end('Hello World\n');
}).listen(8124);

console.log('Server running at http://127.0.0.1:8124/');
output : Hello World

nodejs is used to build scalable network application.
scalability stand for an application which can be used even after their is a change in its size volume etc.
A Network application is any application running on one host and provides a communication to another application running on a different host, the application may use an existing application layer protocols such as: HTTP(e.g. the Browser and web server), SMTP(e.g. the email-client).
for every framework their must be few pacakage manager

npm is a node pacakge manager complety written in javascript for default nodejs.It is also package manager to grunt,gulp,browserfiy etc.It is used by javascript developers to share and reuse the code,and is very easy to update the code.
These code are called packages or modules.Every pacakge  contain package.json which contain some embedded data about the  package.node-module is a directory.
npm init is used to avoid every time usage of npm install and to download all 20 dependencies.It creates package.json file with all dependecies.Dependecies are nothing but the packages which you have installed. dependencies can be added manual by inserting them in the directory with "*", so as to download the latest version.npm outdated command gives u the list of outdated packages,with their latest version. npm update command will update the packages.
npm uninstall package name will uninstall the package from the node module, but when u use ls command it shows unmet error with the uninstall package name,which indicates that it still the package exists in package.json file and is needed for it usage. to avoid this use npm install packagename --save command.If this is done in viceversa it shows extraneous error, which mean it doesnt need that package.
when we delete node modules, we can create it again by simply using npm install, where itsearches for all packages required for a project from package.json file and create a node module directory.
