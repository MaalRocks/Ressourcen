WebDEV - General
=========

a bunch of shit you have to know to make webstuff

Table of contents
-----------------
* [req.query](#req.query)
* [req.body](#req.body)  
* [req.body](#req.body)




req.query
=========

**_contains_**:

 - the query params of the request

**usage**:
> url.com?foo=bar = {foo:"bar"}

**example**:
> url.com?foo=bar = {foo:"bar"}


---

req.body
=========
*contains*:
  - anything in the request body
>
*usage*:
  - Typically this is used on PUT and POST requests.
>
*example*:
  - POST to url.com with the body of {"foo":"bar"} and a header of type application/json = {foo: "bar"}



So to answer your question, if you were to use req.body instead of req.query, it would most likely not find anything in the body, and therefore not be able to validate the jwt.


------



req.body is mainly used with form using POST method. You've to use enctype="application/x-www-form-urlencoded" in the form properties. As POST method don't show anything in URL, you have to use body-parser middleware if the form contains an input text with name="age" then req.body.age return the value of this feld.

req.query takes parameters in the URL (mainly GET method) example for this URL ► http://localhost/books?author=Asimov app.get('/books/', (req, res) => { console.log(req.query.author) } will return Asimov

by the way, req.params take the end part of the URL as a parameter. example for this URL ► http://localhost/books/14 app.get('/books/:id', (req, res) => { console.log(req.params.id) } will return 14
