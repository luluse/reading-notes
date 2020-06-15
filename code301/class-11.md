# EJS

response.render takes 3 parameters: 
- string of file name
- object of local variables 
- call back (optional)

```
app.get('/', function(request,response){
  response.render('index', {
    foo: 'bar'
  });
});
```


```
app.get('/', function(request,response){
  response.render('index', {
    people: [
      { name:'lulu' },
      { name: 'James'}
    ]
  });
});
```

[EJS documentation](https://ejs.co/)

 EJS (Embeded js) is a simple templating language that lets you generate HTML markup with plain JavaScript.

 $ npm install ejs

 ```
 let ejs = require('ejs');
let people = ['geddy', 'neil', 'alex'];
let html = ejs.render('<%= people.join(", "); %>', {people: people});
```
configure our application to use EJS and set up our routes inside of server.js:
```
// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page 
app.get('/', function(req, res) {
    res.render('pages/index');
});
```

Using Partials The syntax to use an EJS partial is: `<% include FILENAME %>`. The path to the partial is relative to the current file.

## Google Books APIs

### [Working with volumes](https://developers.google.com/books/docs/v1/using#WorkingVolumes)

`https://www.googleapis.com/books/v1/volumes?q=search+terms`
