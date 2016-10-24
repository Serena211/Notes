#[Express](https://www.tutorialspoint.com/expressjs/expressjs_routing.htm)

1. `app.get` and `app.post`:
  have multiple different methods at the same route.
  ```
  app.get('/hello', function(req, res){
  	res.send("Hello Get Method!");
  });

  app.post('/hello', function(req, res){
  	res.send("Hello Post Method");
  });

  // works for all http method
  app.all('/hello', function(req, res){
    res.send("Hello All Method");
  });
  ```

  test post method
    - use Postman
    - use `curl -X POST "http://localhost:port/hello"` on your command line

2. express.Router():

  separate out routes from our main index.js file

  check this link:  http://stackoverflow.com/a/33261362/6157406

3. Middleware:

  `next()` : It tells that more processing is	required for the current request and is in the next middleware function/route handler.
  ![middleware](https://www.tutorialspoint.com/expressjs/images/middleware_desc.jpg)
