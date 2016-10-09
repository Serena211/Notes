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
2. express.router

  check this link:  http://stackoverflow.com/a/33261362/6157406
