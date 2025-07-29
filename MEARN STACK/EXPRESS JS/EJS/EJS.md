### Introduction:

- EJS **Embedded JavaScript Templating** is a templating engine used by Node.js. 

- Template engine helps to create an HTML template with minimal code.

- EJS is a simple templating language that is used to generate HTML markup with plain JavaScript. 

- It also helps to embed JavaScript into HTML pages.

### Installing EJS

`npm install express ejs --save`

- It install express and ejs as dependency in the node.js project.

---
### Set Up Your Node Application

`index.js`:

```js
const express = require('express');
const app = express();

// Set EJS as templating engine
app.set('view engine', 'ejs');
```

---
### Create the EJS Template

#### Views Directory:

The default behavior of EJS is that it looks into the 'views' folder for the templates to render.

`/views/home.ejs`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Home</title>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui porro modi...
    </p>
    <button>click me !</button>
  </body>
</html>
```

`index.js`

```js
const express = require("express");
const path = require("path");
const app = express();
const port = 8080;

app.set("view engine" , "ejs");
app.set("views", path.join(__dirname,"/views"));
app.listen(port,(req , res)=>{
    console.log(("Request received"));
});
//home
app.get("/",(req,res)=>{
    res.render("home.ejs");
});
```

- The render method takes the name of the HTML page to be rendered as input.

- This page should be in the views folder in the root directory.

---
#### We will embed the username ( route parameter )  to the HTML page :

```js
app.get("/ig/:username" , (req , res)=>{
    const {username} = req.params;
        res.render("instagram.ejs" , {username});
});
```

```html
<h1>Welcome to the  @<%= data.name %></h1>
```

