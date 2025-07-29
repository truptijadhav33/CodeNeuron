# Serving static files in Express:

- To serve static files such as images, CSS files, and JavaScript files, use the `express.static` built-in middleware function in Express.
- The default behavior of EJS is that it looks into the 'public' folder for the static files.

```js
app.use(express.static(path.join(__dirname, '/public')));
```

EXAMPLE:

`index.js`

```js
const express = require("express");
const path = require("path");
const app = express();
const port = 8080;

app.use(express.static(path.join(__dirname,"public/css")));
app.set("views" , path.join(__dirname,"/views"));
app.listen(port,(req , res)=>{
    console.log(("Request received"));
});
app.set("view engine" , "ejs");
//instagram
app.get("/ig/:username" , (req , res)=>{
    const instaData = require("./data.json");
    const {username} = req.params;
    const data = instaData[username];
    if(data){
        res.render("instagram.ejs" , {data});
    }
    else{
        res.render("error.ejs" , {username});
    }
});
```

`instagram.ejs`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram</title>
     <!-- link style.css -->
    <link rel="stylesheet" href="/style.css">
</head>
<body>
    <h1>Welcome to the  @<%= data.name %></h1>
    <p> followers: <%= data.followers %> </p><p>followings: <%= data.following %> </p>
    <%for(post of data.posts){%>
        <img src="<%= post.image %>" alt=""><br>
        <span> likes: <%= post.likes %> </span><span>comments: <%= data.comments %> </span><br><hr><br>
    <%}%>
</body>
</html>
```

`./public/css/style.css`

```css
img{
height: 300px;
width: 300px;
}
```

## Include :

- <%- %> Outputs the unescaped value into the template.

- EJS provides an include function to include other EJS templates within a main template.

- To include a template, use the syntax

 - <%- include('template_name.ejs') %> 

- where **template_name.ejs** is the path to the template file. 

- This allows you to reuse common sections of HTML across multiple pages, enhancing code modularity and maintainability.

```html
<!-- included_template.ejs -->
<div>
    <p>Parameter 1: <%= param1 %></p>
    <p>Parameter 2: <%= param2 %></p>
</div>
```

```html
<!-- main.ejs -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Main Template</title>
</head>
<body>
    <h1>Main Template</h1>
    <%- include('included_template.ejs', getParams()) %>
</body>
</html>
```