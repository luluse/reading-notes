# Authentication

## User Modeling

- developers responsibility to store that information responsibly
- emails, user names, and addresses can be stored in plain text, as long as the database is password protected and/or behind a firewall
- users password, should be encrypted using a hashing algorithm before it is ever stored.

## Cryptography

- science which studies methods for encoding messages
- key: secret information required for decoding
- cryptanalysis: science of decoding encrypted messages without possessing the proper key

## Hash Algorithms

- takes a piece of data and produces a hash that is deliberately difficult to reverse
- If identical data is passed into the algorithm the same hash will always be produced
- used for checking the integrity of data
- hash password can be stored when the user signs up

## Cypher Algorithms

- takes a piece of data and a key and produces encrypted data
- Later the encrypted data can be reversed into the original data by decrypting it using the same key

## Basic Authorization

- common method used to send a username and password in an HTTP request.  
  - The username and password are joined with a ‘:’ then “base64 encoded” and placed after the string ‘Basic ‘. 
  - The resulting string is set to the value of an Authorization header.

- In browsers, we get atob and btoa to convert to/from “Base64 Encoding”

```
let encoded = window.btoa('someusername:P@55w0rD!')
// c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==

let decoded = window.atob('c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==');
// someusername:P@55w0rD!

request({
  method: 'GET',
  url: 'https://api.example.com/login',
  headers: {
    Authorization: `Basic ${encoded}`,
  },
})
.then(handleLogin)
.catch(handleLoginError)
```

In node app: 
```
let base64 = require('base-64');

let string = 'someusername:P@55w0rD!';
let encoded = base64.encode(string); // c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==
let decoded = base64.decode(encoded); // someusername:P@55w0rD!
```

## Authentication Cheat Sheet
- process of verifying that an individual, entity or website is whom it claims to be
- Make sure your usernames/user IDs are case-insensitive. Usernames should also be unique.
- Implement Proper Password Strength Controls


## Bcript

- library to help you hash passwords.


## Resources

[intro to jwt](https://jwt.io/introduction/)
[OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
[bcrypt docs](https://www.npmjs.com/package/bcrypt)