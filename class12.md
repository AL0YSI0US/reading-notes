# Code 301 Reading Notes

## Class 12

[<== Previous Lesson](class11.md) [Next Lesson ==>](class13.md)

[<== Home](README.md) 🏠

# Mongo and Mongoose

[**Getting started with Mongoose APi**](https://mongoosejs.com/docs/index.html)

install Mongoose from the command line using `npm`:

```
$ npm install mongoose --save
```

Now say we like fuzzy kittens and want to record every kitten we ever meet in MongoDB. The first thing we need to do is include mongoose in our project and open a connection to the `test` database on our locally running instance of MongoDB.

```javascript
// getting-started.js
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost/test', {useNewUrlParser: true, useUnifiedTopology: true});
```

We have a pending connection to the test database running on localhost. We now need to get notified if we connect successfully or if a connection error occurs:

```javascript
const db = mongoose.connection;
db.on('error', console.error.bind(console, 'connection error:'));
db.once('open', function() {
  // we're connected!
});
```

Once our connection opens, our callback will be called. For brevity, let's assume that all following code is within this callback.

With Mongoose, everything is derived from a [Schema](https://mongoosejs.com/docs/guide.html). Let's get a reference to it and define our kittens.

```javascript
const kittySchema = new mongoose.Schema({
  name: String
});
```

So far so good. We've got a schema with one property, `name`, which will be a `String`. The next step is compiling our schema into a [Model](https://mongoosejs.com/docs/models.html).

```javascript
const Kitten = mongoose.model('Kitten', kittySchema);
```

A model is a class with which we construct documents. In this case, each document will be a kitten with properties and behaviors as declared in our schema. Let's create a kitten document representing the little guy we just met on the sidewalk outside:

```javascript
const silence = new Kitten({ name: 'Silence' });
console.log(silence.name); // 'Silence'
```

Kittens can meow, so let's take a look at how to add "speak" functionality to our documents:

```javascript
// NOTE: methods must be added to the schema before compiling it with mongoose.model()
kittySchema.methods.speak = function () {
  const greeting = this.name
    ? "Meow name is " + this.name
    : "I don't have a name";
  console.log(greeting);
}

const Kitten = mongoose.model('Kitten', kittySchema);
```

Functions added to the `methods` property of a schema get compiled into the `Model` prototype and exposed on each document instance:

```javascript
const fluffy = new Kitten({ name: 'fluffy' });
fluffy.speak(); // "Meow name is fluffy"
```

We have talking kittens! But we still haven't saved anything to MongoDB. Each document can be saved to the database by calling its [save](https://mongoosejs.com/docs/api.html#model_Model-save) method. The first argument to the callback will be an error if any occurred.

```javascript
  fluffy.save(function (err, fluffy) {
    if (err) return console.error(err);
    fluffy.speak();
  });
```

Say time goes by and we want to display all the kittens we've seen. We can access all of the kitten documents through our Kitten [model](https://mongoosejs.com/docs/models.html).

```javascript
Kitten.find(function (err, kittens) {
  if (err) return console.error(err);
  console.log(kittens);
})
```

We just logged all of the kittens in our db to the console. If we want to filter our kittens by name, Mongoose supports MongoDBs rich [querying](https://mongoosejs.com/docs/queries.html) syntax.

```javascript
Kitten.find({ name: /^fluff/ }, callback);
```

This performs a search for all documents with a name property that begins with "fluff" and returns the result as an array of kittens to the callback.

> That's the end of our quick start. We created a schema, added a custom document method, saved and queried kittens in MongoDB using Mongoose. Head over to the [guide](https://mongoosejs.com/docs/guide.html), or [API docs](https://mongoosejs.com/docs/api.html) for more.


## Differences between SQL and NoSQL - [source](https://www.mongodb.com/nosql-explained/nosql-vs-sql)

SQL is a language : **S**tructured **Q**uery **L**anguage

> It allows you to write database queries
>
> EXAMPLE : SELECT id, name, price FROM products

The table below summarizes the main differences between SQL and NoSQL databases.


|                                | SQL Databases                                                    | NoSQL Databases                                                                                                                                                                                                                  |
| -------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Data Storage Model             | Tables with fixed rows and columns                               | Document: JSON documents, Key-value: key-value pairs, Wide-column: tables with rows and dynamic columns, Graph: nodes and edges                                                                                                  |
| Development History            | Developed in the 1970s with a focus on reducing data duplication | Developed in the late 2000s with a focus on scaling and allowing for rapid application change driven by agile and DevOps practices.                                                                                              |
| Examples                       | Oracle, MySQL, Microsoft SQL Server, and PostgreSQL              | Document: MongoDB and CouchDB, Key-value: Redis and DynamoDB, Wide-column: Cassandra and HBase, Graph: Neo4j and Amazon Neptune                                                                                                  |
| Primary Purpose                | General purpose                                                  | Document: general purpose, Key-value: large amounts of data with simple lookup queries, Wide-column: large amounts of data with predictable query patterns, Graph: analyzing and traversing relationships between connected data |
| Schemas                        | Rigid                                                            | Flexible                                                                                                                                                                                                                         |
| Scaling                        | Vertical (scale-up with a larger server)                         | Horizontal (scale-out across commodity servers)                                                                                                                                                                                  |
| Multi-Record ACID Transactions | Supported                                                        | Most do not support multi-record ACID transactions. However, some—like MongoDB—do.                                                                                                                                             |
| Joins                          | Typically required                                               | Typically not required                                                                                                                                                                                                           |
| Data to Object Mapping         | Requires ORM (object-relational mapping)                         | Many do not require ORMs. MongoDB documents map directly to data structures in most popular programming languages.                                                                                                               |

### [NoSQL Data Modelling](http://chandermani.blogspot.com/2012/03/nosql-data-modelling.html)

* [MongoDB Schema Design](http://www.mongodb.org/display/DOCS/Schema+Design) : Great resource from MongoDB. Start with this one first.
* [MongoDB Data Modeling](http://blog.fiesta.cc/post/11319522700/walkthrough-mongodb-data-modeling): A quick read but explains some important concepts related to modelling. Embedding vs Linking.
* [MongoDB Data Modeling and Rails](http://www.mongodb.org/display/DOCS/MongoDB+Data+Modeling+and+Rails): Covers an example to make things more clear.
* [NoSQL Data Modelling Techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/): A great post that explains about data modelling techniques for all NoSQL type stores.

### Reading

* [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)
* [nosql modeling techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

### Bookmark

* [mongoose api](https://mongoosejs.com/docs/api.html#Model)
* [**Getting started with Mongoose APi**](https://mongoosejs.com/docs/index.html)

### Videos

* [sql vs nosql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y) (Video)

### Additional resources

+ [NoSQL vs SQL Databases](https://www.mongodb.com/nosql-explained/nosql-vs-sql)

* [What are the Differences between SQL and NoSQL?](https://www.mongodb.com/nosql-explained/nosql-vs-sql#differences-between-sql-and-nosql)
* [What are the Benefits of NoSQL Databases?](https://www.mongodb.com/nosql-explained/nosql-vs-sql#what-are-the-benefits-of-nosql-databases)
* [What are the Drawbacks of NoSQL Databases?](https://www.mongodb.com/nosql-explained/nosql-vs-sql#what-are-the-drawbacks-of-nosql-databases)
* [Try a NoSQL Database](https://www.mongodb.com/nosql-explained/nosql-vs-sql#how-to-try-a-nosql-database)


[<== Home](README.md) 🏠
