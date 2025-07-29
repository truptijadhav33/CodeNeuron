#### Introduction:

Interpolation refers to the embedding expressions into marked up text.

EJS  uses specific tags for interpolation to embed dynamic content within HTML templates. 
### Tags:

refer: [tags](https://ejs.co/)

###### Most commonly used:

```
<% %> 'Scriptlet' tag, for control-flow, no output.

<%= %> Outputs the value into the template (HTML escaped)

<%- %> Outputs the unescaped value into the template

```



```
<%= %> - tag is used to embed JavaScript code that evaluates to a value, variables .
which is then inserted into the rendered HTML output.

`syntax:`
<p>Hello, <%= username %></p>
```

- EJS empowers developers to introduce conditional statements into their templates, providing control over the flow of the content.

##### Example:
`rolldice.ejs`

```
<body>
    <h1>Dice value : <%= diceVal %> </h1>
    <% if(diceVal==6){ %>
        <h1> nice roll dice again </h1>
    <% } %>
</body>
```

`index.js`

```js
//rolldice
app.get("/rolldice",(req,res)=>{
    const diceVal = Math.floor(Math.random() * 6)+1;
    res.render("rolldice.ejs" , {diceVal});
});
```
