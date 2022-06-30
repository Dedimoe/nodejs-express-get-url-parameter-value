# nodejs-express-get-url-parameter-value
nodejs-express-get-url-parameter-value

### Express 4.x

To get a URL parameter's value, use req.params
```
app.get('/p/:tagId', function(req, res) {
  res.send("tagId is set to " + req.params.tagId);
});

// GET /p/5
// tagId is set to 5
```
If you want to get a query parameter ?tagId=5, then use req.query
```
app.get('/p', function(req, res) {
  res.send("tagId is set to " + req.query.tagId);
});

// GET /p?tagId=5
// tagId is set to 5
```

### Express 3.x

URL parameter
```
app.get('/p/:tagId', function(req, res) {
  res.send("tagId is set to " + req.param("tagId"));
});

// GET /p/5
// tagId is set to 5
```
Query parameter
```
app.get('/p', function(req, res) {
  res.send("tagId is set to " + req.query("tagId"));
});

// GET /p?tagId=5
// tagId is set to 5
```
