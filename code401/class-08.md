# Express Routing & Connected API

Routes can be managed in separate modules from the main server, allowing us to extract that logic and wiring to be more topical.

## server’s role

- index.js - Entry Point
- server.js - Hub, Exported Server
- models/categories.js, etc - Data Models
- routes/categories.js, etc - Routers and Handlers

## [Express Routing](https://expressjs.com/en/guide/routing.html)

- routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. 
- routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.

## Route paths

This route path will match acd and abcd.
```
app.get('/ab?cd', function (req, res) {
  res.send('ab?cd')
})
```
This route path will match abcd, abxcd, abRANDOMcd, ab123cd, and so on.
```
app.get('/ab*cd', function (req, res) {
  res.send('ab*cd')
})
```

#### Route paths based on regular expressions:

This route path will match anything with an “a” in it.
```
app.get(/a/, function (req, res) {
  res.send('/a/')
})
```
This route path will match butterfly and dragonfly, but not butterflyman, dragonflyman, and so on.
```
app.get(/.*fly$/, function (req, res) {
  res.send('/.*fly$/')
})
```

## [ExpressJS 4.0 Router](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

### express.Router()
```
// get an instance of router
var router = express.Router();

// home page route (http://localhost:8080)
router.get('/', function(req, res) {
    res.send('im the home page!');  
});

// about page route (http://localhost:8080/about)
router.get('/about', function(req, res) {
    res.send('im the about page!'); 
});

// apply the routes to our application
app.use('/', router);
```

With Express 4.0 Router, we can: 
- Use express.Router() multiple times to define groups of routes
- Apply the express.Router() to a section of our site using app.use()
- Use route middleware to process requests
- Use route middleware to validate parameters using .param()
- Use app.route() as a shortcut to the Router to define multiple requests on a route
