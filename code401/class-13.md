# Bearer Authorization

- Following a signin attempt your service is able to make a boolean decision as to the success of the attempt.
- Rather than continually sending username+password over the internet, or undergoing the long OAuth process, we are able to use a secondary authentication method called “Bearer Token”
- Bearer Tokens are encoded JSON objects that “bear” or “contain” enough information for the server to assert that any client request that presents a valid token must have originated from a client that has previously authenticated themselves using either Basic or OAuth.
- Bearer Tokens are sent to the user/client after the initial signin process has completed.
- Clients must make every subsequent request to the server with that token, in the header
  - Authorization: Bearer encoded.jsonwebtoken.here
- The server opens the token, does the re-authentication, and then grants or denies access
- In express servers, this can be done in middleware, in conjunction with a user model

``` 
app.get('/somethingsecret', bearerToken, (req,res) => {
  res.status(200).send('secret sauce');
});

function bearerToken( req, res, next ) {
  let token = req.headers.authorization.split(' ').pop();
  try {
    if ( tokenIsValid(token) ) { next(); }
  }
  catch(e) { next("Invalid Token") }
}

function tokenIsValid(token) {
  let parsedToken = jwt.verify(token, SECRETKEY);
  return Users.find(parsedToken.id);
}
```

### JSON Web Tokens
- JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transmitting information between parties (servers, clients, etc) as a JSON object.
- Signed tokens can verify the integrity of the claims contained within it
- When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

#### What is JWT?
- securely transfer info between two bodies
- digitally signed: verified and trusted
- can be send via URL, post request, HTTP header
- fast transmission
- self-contained: contains info about the user
- avoid query the DB more than once

header:
```
{
  "alg": "HS256",
  "typ": "JWT"
}
```

Payload: contains claims
```
{
  "sub": "12345",
  "name": "lulu",
  "admin": "true"
}
```

signature: combine header,payload plus secret
```
HMACSHA256(
  base64UrlEncode(header) + "." + base64UrlEncode(payload), secret
)
```

- combine all with dot (.) to form JWT 

### When should you use JSON Web Tokens?
- **Authorization**: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token
- **Information Exchange**: JSON Web Tokens are a good way of securely transmitting information between parties


## Resources

[Intro to JWT](https://jwt.io/introduction/)

[Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

[npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)