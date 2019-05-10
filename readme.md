## Node

- Student can create an index.js file
- Student can run a javascript file using node
- Student can run a javascript file using nodemon
- Student can describe that node is the V8 javascript engine
- Student can require and use other files in node

## Servers

- Student can describe the role of servers in a client-server model
- Student can identify the parts of code that listen to external requests

## NPM

- Student can npm init
- Student can npm install
- Student can npm install --save
- Student can describe the role of a package.json file
- Student can describe the purpose of the node_modules folder
- Student can .gitignore node_modules

## Express

- Student can install and require express
- Student can start a basic express server by creating an app and listening on a port
- Student can write the handler function with the correct parameters req, res and next
- Student can access url parameters on req.params
- Student can set up an endpoint path to expect multiple params
- Student can use req.query
- Student can send data back with res.send and res.json
- Student can set a status code with res.status

---

**Node:**

the V8 Javascript engine that runs outside of the browser

**npm:**

Node package manager

**package.json**

package.json is a config file from our application, it will have instructions on dependencies to download, and how node should run your application.

https://docs.npmjs.com/files/package.json

**.gitignore**

tells git which files not to push to github
file/directories to be ignored

- node_modules
- .env (password file)
- anything you don't want on github

**server:**

computer or a device that provides a service to another machine

in general for us:
a webserver is a program that can handle incoming requests and respond accordingly.

manages access to a centralized resource

todays centralized resource: `data.json`

**params:**
typically stand for a particular resource looks like a normal path on the frontend

backend example:
params denoted with a "`:`"

```js
app.get(`/api/:id`);
```

access params

```js
req.params.id;
```

**query**

typically used to maipulate/search data being accessed

frontend example
denoted with a "`?`"

```js
"https://localhost:4000/api/students?name=ryland";
```

access querys in endpoint function handler:

```js
req.query.name;
```

**client**

a computer program that accesses a service made available by a server

server instructions:

- mkdir server
- touch index.js .gitignore
- npm init -y
- add node_modules => .gitignore
- npm i express
- require express
- declare app variable set = to express()
- declare port
- app.listen => port
- declare endpoint
- method - get
- path '/api...'
- handler => (req,res,next) => data to send
- test in browser
