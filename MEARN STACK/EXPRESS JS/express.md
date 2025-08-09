## What is Express.js?

- Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.

- Express provides a thin layer of fundamental web application features, without obscuring Node.js features.

---
### Installation of Express:

You can install Express using 

```shell
npm install express
```

---
### Hello World with Express

- You can create a simple Express application.

```js
const express = require('express');
const app = express();
let port = 3000;

app.listen(port,()=>{
        console.log(`app listining on ${port}`);
        });        
app.get('/', (req, res) => {
    res.send('Hello, World!');
});

```

---

1. **`const express = require('express');` :**

- This line imports the **Express** module.

2. **`const app = express();`**

- Here,  creating an instance of the Express application by calling the `express()` function.

- The `app` object is now used to configure your web server and define routes.

3. **`let port = 3000;`**

- This defines the port number your server will run on.
    
- You can access the server in your browser at `http://localhost:3000`.

```
app.listen(port, () => {
    console.log(app listening on ${port});
});

```

- This line **starts** the Express server and begins listening for incoming requests on port `3000`.
    
- When the server starts successfully, it prints: `app listening on 3000`

```
app.get('/', (req, res) => {
    res.send('Hello, World!');
});
```

- This defines a **GET route** for the **root path** `/`.

- When a user visits `http://localhost:3000/` in a browser:

   - The server receives a **GET request**.
   
  - It responds with the text: **"Hello, World!"**

#### Check out more:

[[Routing]] || [[RESTful API]] || [[EJS]]
