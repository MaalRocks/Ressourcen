WebDEV - General
=========

a bunch of shit you have to know to make webstuff

Table of contents
-----------------
- [req.body](#req-body)  
* [req.query](#req-query)
* [req.body](#req-body)


req.body
=========
**contains**:
  - anything in the request body

**usage**:
- POST , PUT
- use ``enctype="application/x-www-form-urlencoded" ``

**example**:
> POST to url.com with the body of {"foo":"bar"} and a header of type application/json = {foo: "bar"}



req.query(req-query)
=========
**contains**:
 - the query params of the request

**usage**:
- GET
- takes parameters in the URL

**example**:
JavaScript
`` http://localhost/users?name=Jesus app.get('/users/', (req, res) => { console.log(req.query.name === "Jesus") } ``



req.params
=========
**contains**:
  - the end part of URL as parameter

**usage**:
get URL-values

**example**:
`` http://localhost/users/1 app.get('/users/:id', (req, res) => { console.log(req.params.id === 1) } ``






req.query takes parameters in the URL (mainly GET method) example for this URL ► http://localhost/books?author=Asimov app.get('/books/', (req, res) => { console.log(req.query.author) } will return Asimov

req.params take the end part of the URL as a parameter. example for this URL ► http://localhost/books/14 app.get('/books/:id', (req, res) => { console.log(req.params.id) } will return 14
