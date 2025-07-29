
### Basic Routing:

- Routing refers to how an application responds to client requests to specific endpoints (URIs) using different HTTP methods (GET, POST, PUT, DELETE, etc.).

- Express provides simple methods to define routes that correspond to HTTP methods:

| `app.get()`    | Handle GET requests     |
| -------------- | ----------------------- |
| `app.post()`   | Handle POST request     |
| `app.put()`    | Handle PUT request      |
| `app.delete()` | Handle DELETE requests  |
| `app.all()`    | Handle all HTTP methods |

```js
const express = require('express');  
const app = express();  
const port = 8080;  

// Start the server  
app.listen(port, () => {  
  console.log(`Example app listening at http://localhost:${port}`);  
});
// Respond to GET request on the root route  
app.get('/', (req, res) => {  
  res.send('GET request to the homepage');  
});  
  
// Respond to POST request on the root route  
app.post('/', (req, res) => {  
  res.send('POST request to the homepage');  
});  
  
// Respond to GET request on the /about route  
app.get('/about', (req, res) => {  
  res.send('About page');  
});  
  
// Catch all other routes  
app.all('*', (req, res) => {  
  res.status(404).send('404 - Page not found');  
});  
  
```

### Route Parameters

- Route parameters are named URL segments that capture values at specific positions in the URL.

- They are specified in the path with a colon `:` prefix.

- **Example:** `/users/:userId/books/:bookId`

- In this example, `userId` and `bookId` are route parameters that can be accessed via `req.params`.

```js
// Route with parameters  
app.get('/users/:userId/books/:bookId', (req, res) => {  
  // Access parameters using req.params  
  res.send(`User ID: ${req.params.userId}, Book ID: ${req.params.bookId}`);  
});
```

### Query Parameters

- Query parameters are key-value pairs that appear after the `?` in a URL.

- They are automatically parsed by Express and available in `req.query`.

- **Example URL:** `http://example.com/search?q=express&page=2`

- In this URL, `q=express` and `page=2` are query parameters that can be accessed as `req.query.q` and `req.query.page`.

```js
// Route handling query parameters  
app.get('/search', (req, res) => {  
  // Access query parameters using req.query  
  const { q, category } = req.query;  
  res.send(`Search query: ${q}, Category: ${category}`);  
});
```