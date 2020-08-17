# HTTP and REST

### Hypertext Transfer Protocol

- Applications built using HTTP subscribe to the client-server computing model. 
- In the client-server computing model a host designed to provide a service is called a server. 
- Clients are hosts that make requests to that service.

### HTTP Requests

- A HTTP/1.1 request is formatted in text
- The first line of the request contains the METHOD, URL, and HTTP VERSION
- The following lines are the request HEADERS

| HTTP Method	| Request Has Body |	Response Has Body	| Safe	| Idempotent |	Cacheable | Function |
| ----| ----| ----| ----| ----| ----| ----| 
| GET	|No	|Yes	|Yes	|Yes	|Yes	Retrieve a resource|
|HEAD	|No	|No|	Yes|	Yes|	Yes|	Like GET but headers only|
|POST	|Yes|	Yes|	No	|No	|Yes|	Create a resource|
|PUT	|Yes|	Yes|	No|	Yes	|No|	Update a resource|
|DELETE	|No|	Yes|	No|	Yes	No|	Delete a resource|
|CONNECT|	Yes	|Yes|	No|	No|	No|	Create |TCP/IP tunnel|
|OPTIONS|	Optional|	Yes	|Yes|	Yes	|No	|Returns supported methods for a URL|
|TRACE|	No|	Yes|	Yes	|Yes|	No|	Echos retrieved request|
|PATCH|	Yes	|Yes|	No|	No|	No|	Partial modification of resource|

- Safe methods should only be used for information retrieval and should not change the server state. 
- Idempotent methods means if two identical requests are made they should get an identical response.
- Cacheable means the client should be able to cache the response.

### HTTP Response

-  The first line of the response contains the HTTP VERSION, STATUS CODE, and STATUS MESSAGE. 
- The following lines are the request headers and are formatted exactly the same way as the request headers.


### REST

- REpresentational State Transfer.
- reference, manipulate, and transfer state.
- Rest uses a common set of methods (called “verbs”) to operate on the state of a resource (“noun”

- RESTful Endpoint: http://api.server.com/api/v1/people

    - http:// - Protocol/Scheme
    - api.server.com - Domain or Server
    - /api/v1 - API Endpoint
    - /people - The resource (This identifies a collection: all people)
    - /people/12345 - A more specific resource: The person with id 12345

| REST Method	| CRUD Operation |	Function|
|----|----|----|
|GET|	READ|	Retrieve 1 or More Records|
|POST	|CREATE|	Create a new record|
|PATCH	|UPDATE	|Update a record (just the parts that changed)|
|DESTROY|	DELETE|	Remove a record|

- Generally speaking, RESTful endpoints deliver data in JSON format. The best practice is to supply a header with metadata and a collection of results

### REST Documentation

- The standard for documenting REST APIs is with a “live” documentation system: Open API (formerly “Swagger”)

