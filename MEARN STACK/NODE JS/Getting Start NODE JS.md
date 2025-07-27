
##### Hello World:

```js
console.log('Hello, World!');
```

#### REPL

- REPL stands for **Read-Eval-Print-Loop**.
- It is a simple, interactive computer programming environment.

```node
$ node
> console.log('Hello, World!');
Hello, World!
undefined
>
```

#### Command Line Arguments

You can access command line arguments using `process.argv`

> **Process**: 
>    - Process is object provides info. about current Node JS process and also control over that process `i.e current work info.`
>    
>    - Returns an array containing the command-line arguments passed when the  [[NODE JS]] process was launched.


```js
let args = process.argv;
for(let i = 2 ; i< args.length;i++)
{
    console.log("Hello ",args[i]);
}
```

##### Global Objects

- Node.js global objects are global in nature and available in all modules.

```js
console.log(__dirname);
console.log(__filename);
```

#### Check out more:
[[NODE JS]] ||  [[Modules in Node JS]] || [[What is NPM]] || [[Creating Node Server]]