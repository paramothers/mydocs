# Web History

 1. in 1995 Web history revolutioned.
 2. Internet Explorer 1.0 and  Mosaic browser was first one.
 3. Netscape Navigator browser 2.0 was embbeded a programming in 1995 May ( Mocha -> Live Script -> JavaScript )
 4. Netscape company only publised JavaScript to ECMA standard.
 4. in 1997 javaScript become default programming language for browser
 5. in  2000 Google released AJAX when Gmail and Google map release.

**In 2000, the SHIFT, AJAX technology only transfered WebSite to Web Application**

    
 6. JQuery and Prototype framework got released
 7. In 2008 Google's V8 JavaScript engine released
 
** V8 engin's JIT ( Just In Time ) compiler**
 
 8. in 2009 Node.js enables, javascript run on server and database ( like MongoDB)
 9. AngularJS enables, make use of power of latest browser.
 
**Single language for all layer of programming**

*From best JAVA deverloper to JavaScript Developer*

#MEAN
 
  1. AngularJS as Front end framework
  2. MongoDB as DB
  3. Express as Web framework
  4. Node.js as server platform

###Modern web developement splited as below layers
 
  1. DB
  2. Server
  3. Client Logic
  4. Client UI
  
##How Node.js become effective platform

1. JavaScript's  Event-Deriven Programming
2. JavaScript's  Closure Object facility
3. Isolated JavaScript Module definition ( thanks to CommonJS )
  

##CommonJS

1. it introduce require() method - used to load module into our application
2. Exports javascript objects - it is inside of module itself and expose what code are visible to outside of module.
3. Module javascript objects - it is metadata about module and also has pointer to Exports object. 
4. Without Module concept, Node.js might have more complex 
**Every Node.js module is a implementation of CommonJS Specification**

##Node.JS

  It is implemented in C language with, wrapper for v8.<br />   
  It is a product came out from V8-engine-open-sourced-from-google.<br />   
  The current version i used is 0.10.35<br />   
  it allow two-way communication between browser and server<br />   
  V8 - engine built for client side programming<br />  
  But, Node.js extend v8 capabiltiy to server side programming<br />  
  
  **v8 - engine fit for Non-Blocking Socket I/O **<br />   
#### v8 engine based database is MongoDB, released in 2009.
###Connect module has been developed by Sencha (EXTJS company )
**Connect - is one of the middleware module**
##NPM 

 node package manager. it has local and global mode.
 When a package itself depend others, those are also resolved automatically like Maven.
 
 **package.json** is configuration file for npm, which is placed in root of a project. This file can be  created automatically by *NPM Init*
##NPM commands

####setup####
 1. npm init - to create sample package.json file
 
####Install####

 2. npm install - if we run from root of a project, it will install all the dependency specified in package.json file
 3. npm install `<package>` it will install spedified package in project specific `node_modules` folder.
 4. npm install `<package>@ <version>`
 
####update 

 5. npm udpate
 6. 