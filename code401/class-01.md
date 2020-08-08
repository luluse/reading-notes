# Node Ecosystem, TDD, CI/CD


**Why would you want to run JavaScript code outside of a browser?**

You want to run JavaScript outside of a browser to built back-end apps and desktop tools by using Node.js.
- [Quora](https://www.quora.com/What-exactly-does-running-JavaScript-inside-a-browser-and-outside-of-a-browser-mean#:~:text=Running%20JavaScript%20inside%20a%20browser%20means%20you%20are%20interacting%20with,to%20execute%20your%20JavaScript%20code.)
- [Stack Overflow](https://stackoverflow.com/questions/35785841/running-javascript-app-outside-of-the-browser)

**What is the difference between a module and a package?**

A package is a file or directory that is described by a package.json file. A package must contain a package.json file in order to be published to the npm registry. A package is one or more modules (libraries) grouped (or packaged) together.

A modules is a librarie for Node.js. It is any file or directory in the node_modules directory that can be loaded by the Node.js require() function. 
    
Since modules are not required to have a package.json file, not all modules are packages. Only modules that have a package.json file are also packages.

- [Docs npm](https://docs.npmjs.com/about-packages-and-modules)
- [Stack Overflow](https://stackoverflow.com/questions/20008442/difference-between-a-module-and-a-package-in-node-js#:~:text=A%20module%20is%20a%20single,has%20metadata%20about%20the%20package.&text=Now%20it's%20very%20common%20for,a%20package%20as%20a%20module.)

**What does the node package manager do?**

- An online repository for the publishing of open-source Node.js projects
- A command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

- [nodejs.org](https://nodejs.org/en/knowledge/getting-started/npm/what-is-npm/)

**Provide code snippets showing 3 different ways to export a function from a node module**

```
module.exports = function (msg) { 
    console.log(msg);
};
```


```
let msg = require('./Log.js');

msg('Hello World');
```

- [Tutorialsteacher](https://www.tutorialsteacher.com/nodejs/nodejs-module-exports)


**ecosystem** 

The Node.js Ecosystem includes the communities of any project, tool, framework, or application that depends on Node.js – and the people who work within them.
- [nodesource.com](https://nodesource.com/blog/the-age-of-node-js-and/#:~:text=something%20like%20this%3A-,The%20Node.,people%20defined%20what%20%22The%20Node.)


**Node.js**

Node.js is a free, open-sourced, cross-platform JavaScript run-time environment that lets developers write command line tools and server-side scripts outside of a browser. 
- [nodeje.dev](https://nodejs.dev/learn)

**V8 Engine**

V8 is the name of the JavaScript engine that powers Google Chrome. It's the thing that takes our JavaScript and executes it while browsing with Chrome.
- [v8.dev](https://v8.dev/)
- [nodeje.dev](https://nodejs.dev/learn/the-v8-javascript-engine)

**module**

A set of functions you want to include in your application.

A modules is a librarie for Node.js. It is any file or directory in the node_modules directory that can be loaded by the Node.js require() function.

- [w3schools](https://www.w3schools.com/nodejs/nodejs_modules.asp)
- [Docs npm](https://docs.npmjs.com/about-packages-and-modules)

**package**

A package is one or more modules (libraries) grouped (or packaged) together.
- [Stack Overflow](https://stackoverflow.com/questions/20008442/difference-between-a-module-and-a-package-in-node-js#:~:text=A%20module%20is%20a%20single,has%20metadata%20about%20the%20package.&text=Now%20it's%20very%20common%20for,a%20package%20as%20a%20module.)

**node package manager (npm)**

Node Package Manager (NPM) is a command line tool that installs, updates or uninstalls Node.js packages in your application. It is also an online repository for open-source Node.js packages. The node community around the world creates useful modules and publishes them as packages in this repository.
- [Tutorialsteacher](https://www.tutorialsteacher.com/nodejs/what-is-node-package-manager)

**server**

A server is a computer, a device or a program that is dedicated to managing network resources. They are called that because they “serve” another computer, device, or program called “client” to which they provide functionality.
- [Techopedia](https://www.techopedia.com/definition/2282/server)

**environment**

It refers to the combination of hardware and software in a computer . In this usage, the term platform is a synonym.

- [techtarget](https://whatis.techtarget.com/definition/environment)

**interpreter**

An interpreter coverts each high-level program statement, one by one, into the machine code, during program run.
- [guru99](https://www.guru99.com/difference-compiler-vs-interpreter.html)

**compiler**

A compiler is a computer program that transforms code written in a high-level programming language into the machine code. It is a program which translates the human-readable code to a language a computer processor understands (binary 1 and 0 bits). It will convert the code into machine code (create an exe) before program run.
- [guru99](https://www.guru99.com/difference-compiler-vs-interpreter.html)

