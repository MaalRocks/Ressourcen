WebDEV - General
=========

a bunch of shit you have to know to make webstuff

Table of contents
-----------------
* [req.body](#reqbody)  
* [req.query](#reqquery)
* [req.body](#reqbody)


req.body
=========
**contains**:

    anything in the request body

**usage**:

    - POST , PUT
    - use ``enctype="application/x-www-form-urlencoded" ``

**example**:

    POST to url.com with the body of {"foo":"bar"} and a header of type application/json = {foo: "bar"}



req.query
=========
**contains**:

    the query params of the request

**usage**:

    - GET
    - takes parameters in the URL

**example**:

    http://localhost/users?name=Jesus app.get('/users/', (req, res) => { console.log(req.query.name === "Jesus") }



req.params
=========
**contains**:

    the end part of URL as parameter

**usage**:

    get URL-values

**example**:
    http://localhost/users/1 app.get('/users/:id', (req, res) => { console.log(req.params.id === 1) }


