# Intro to Express

## What is ExpressJS?

- ExpressJS is a nodejs framework that lets you build web application servers for single-paged, multi-paged and hybrid web applications.
- What ExpressJS does is allow us to create APIs really easily
- ExpressJS is unopinionated; you can designate how you put together your server free from basic requirements.
- ExpressJS will allow us to build a web server API that follows RESTful conventions and provides an API for client requests to interact with a database and provide meaningful responses back to the client.

## What is an API? What does it stand for?

- API stands for Application Programming Interface.
- APIs let your service and products communicate with other products and services.
- APIs are like waiters at a restaurant. They communicate your orders to the kitchen.
- API lets you interact with other software without letting you know how it's implemented (aka you can order steak Diane and don't have to know how to make it, the kitchen does that for you).
- API knows how to take the request, process it as data, and send the information back to you without you seeing the process.

## What/who uses API? What are the two sides to a API "conversation"?

- Request side: Client
- Response side: Server

### What is a client? What is a server?

- The client (program/web browser) requests data of the server via the API
- The server is a series of code that comprises a database with the info the client needs

### What is the relationship between client and server?

- The client and the server act independently.
- The client intiates the API conversation by sending a request for information.
- The server waits for the request and will respond accordingly.

## What is REST? What does REST stand for?

- REST stands for REpresentational State Transfer.
- REST is a system of rules/constraits. It's not a protocol nor a standard.

### What is "state" in REST?

- State refers to the literal current state of information at a given moment. It's something the application remembers (browser history, browser preferences and saved passwords are examples of state.)
- REST is stateless.

### What does REST being stateless mean?

- Each individual request contains all the information to perform the request and return a response regardless of the other requests made by the same API user

### What is an example of a request that proves the statelessness in REST?

- Example of this is you're logged out of IG (different computer/browser) and try to "like" a picture. It redirects to the login page and asks for your information. You put in your information and it logs you in. Then IG completes the request to "like" the photo by redirecting you back to the page as an authenticated user aka "logged in" user where the photo is now "liked".

## What is a resource?

- Any object that the API can provide information about.
- An example of a resource can be a username, photo, or hashtag in Instagram.
- The identifier can be a name or a number.

### What are some of the qualities of RESTful API?

- Client only make one request at a time.

## What is CRUD? What does CRUD stand for?

- CRUD stands for Create, Read, Update, and Delete.
- A model (database) should have the ability to perform these four functions in order to be complete.

### What is an example of a model?

A template for the information stored by a database. If a library was a database, some database models it might have are:

```json
"book": {
  "uid": <Integer>,
  "title": <String>,
  "author": <String>,
  "isbn": <Integer>
}
```

```json
"patron": {
  "name": <String>,
  "joinDate": <Date>,
  "accountStanding" <String[] "good" | "bad">,
  "booksOnLoan": <Integer[] Book.uid | []> // establishing the relation between books and patrons
}
```

### What are some of the specific details of each CRUD method?

- Create: the ability to add new info into the database based on some form of information model.

  - e.g. the ability to add a new patron or a new book to the database

- Read: the ability to see one, many or all of a set of requested information based on given parameters.

  - e.g. the ability to get a book with one specific uid or the ability to get all books that have a given author or the ability to get all books available in the library. Another example is read the database and retrieve all the books that a specific patron has loaned out.

- Update: the ability to modify existing database entries.

  - e.g. the ability to change the value of an author for a specific book. Another example would be changing the accountStanding of a specific patron from "good" to "bad" or vice versa. You can also add or remove books from a specific patron's booksOnLoan array.

- Delete: the ability to remove existing data from the database.

  - e.g. the ability to delete a patron entry.
