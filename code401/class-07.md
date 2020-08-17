# Express

## Express Routing
### Event driven system
- app.get('/thing', (req,res) => {})

### The Request Object
- (req,..)
- :parameters
    - app.get('/api/:thing',...) = req.params.thing
- Query Strings
    - http://server/route?ball=round = req.query.ball
### The Response Object
- (..., res)
- Responsible for sending data back to the browser
- Has methods like send() and status() that Express uses to format the output to the browser properly
    - Sends Headers
        - Cookies
        - Status Codes

## Express Middleware
### use:
- A series of functions that the request “goes through”
- receives request, response and next as parameters


1. Application Middleware
  - Error Handling
  - Bringing in other routes
  -Applies Defaults
  - JSON, Body and Form Parsing
  - Runs on every request

1. Route Middleware
  - Dealing with specific things for a route
  - things many routes would participate in
    - Are you logged in?
    - What is your IP?
    - Have we seen you here before?


### advantages
- Logging
- Dynamic Model Loading
- Browser, Location, User specific content
- Consistent Data Transition/Modeling/Preparation (Pre-Render)

## Server Testing

- avoid starting the actual server for testing
- export your server as a module in a library
- use supertest to run your tests: This will hit your routes as though your server was running, without actually starting it.

## Resources

[using express middleware](https://expressjs.com/en/guide/using-middleware.html)

[express middleware](https://www.tutorialspoint.com/expressjs/expressjs_middleware.htm)

[using express routing](https://expressjs.com/en/guide/routing.html)

[supertest](https://github.com/visionmedia/supertest)

[express middleware list](https://expressjs.com/en/resources/middleware.html)

[http status codes](https://www.restapitutorial.com/httpstatuscodes.html)

