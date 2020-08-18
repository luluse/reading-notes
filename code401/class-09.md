# API Server

## Express: Router Parameters

Express lets you run middleware only when certain parameters are present and expected, eliminating that choice.

```
router.param('city', function (req, res, next, id) {
  console.log('Only runs on routes that have a city param')
  next()
})


// That middleware will not run here
router.get('/places/seattle', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})

// That middleware does run here
router.get('/places/:city', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})

// But not here
router.get('/flights/to/:airport', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})
```

## [Sub documents Mongoose](https://mongoosejs.com/docs/subdocs.html)
- schema driven ORM: provide structure to our Mongo documents
- ability to take that a step further and use a schema to describe a deeper part of a data model: useful when a document contains potentially a list of other documents.

```
var childSchema = new Schema({ name: 'string' });
var house = new Schema({ address: 'string', city: 'string', state: 'string' });

var adult = new Schema({
  // Array of subdocuments
  children: [childSchema],

  // Single nested subdocuments.
  address: house
});
```

## Joining Data/Documents in Mongo

- populate() is a method we can use in Mongoose to connect 2 collections
  - Method 1: physically joining using a reference to another collection
 - Method 2: Virtual Population
    - Create a virtual field in a document pointed to a field in another one.
    - In pre('find') you do a collection “on the fly” which can be more efficient than storing the relation.
- Pre and Post hooks (middleware)
  - Mongoose allows you to inject logic at various points in the lifecycle of a data record.
    - User can perform validation, normalization

## Resources:
[Express router.param](https://expressjs.com/en/4x/api.html#router.param)

[mongoose middleware](https://mongoosejs.com/docs/middleware.html)

[Virtual Joins](https://mongoosejs.com/docs/populate.html#populate-virtuals)
