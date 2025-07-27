- A module encapsulates related code into a single unit of code.
  
- A module can be included in other modules using `require()` function.
   
- Node.js has a set of **built-in modules** which you can use without any further installation.

```js
const fs = require('fs');
const http = require('http');
const url = require('url');
```

- #### Creating Modules:

You can create your own modules using `module.exports`. 
###### math.js:

```js
// math.js
module.exports.sum = (a, b) => a + b;
```

index.js:

```js
// index.js
const math = require('./math');
console.log(math.sum(1, 2));
```

- #### Exporting Multiple things:

###### math.js:

```js
function sum(a, b) {
  return a + b;
}

function sub(a, b) {
  return a - b;
}

module.exports = {
  add,
  sub,
};

```

index.js:

```js
// index.js
const math = require('./math');

console.log(math.sum(3, 2)); // 5
console.log(math.sub(5, 1)); // 4

```


- #### Exporting Multiple files:

**Inside Directory: fruits**

**./apple.js**
	
``` js
module.exports={
name : "apple",
color : "Red",
};
```

**./banana.js**
	
``` js
module.exports={
name : "banana",
color : "yellow",
};
```

**./orange.js**
	
``` js
module.exports={
name : "orange",
color : "orange",
};
```

**./index.js**
	
``` js
const apple = require("./apple");
const banana = require("./banana");
const orange = require("./orange");
const fruits = [apple,banana,orange];
module.exports=fruits;
```


##### Outside fruit Directory 

script.js

```js
const info = require("./fruits");
console.log(info);
console.log(info[0].name,"Has",info[0].color,"color");
console.log(info[1].name,"Has",info[1].color,"color");
console.log(info[2].name,"Has",info[2].color,"color");
```

#### File Structure:

```
project/
|
├── fruits.js        ← module
|	├──apple.js
|	├──banana.js
|	├──orange.js
|
└── script.js        ← Main file requiring the module
```


#### Check out more:
[[NODE JS]] || [[Getting Start NODE JS]]  || [[What is NPM]] 
