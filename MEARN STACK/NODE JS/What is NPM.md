## Introduction 

- npm **(Node Package Manager)**  is the package manager for [[Javascript]] and the world’s largest software registry.
- **Open-source** developers use **npm** to **share** software
- npm consists of a command line client that interacts with a remote registry.
- The name **npm** stems from when npm first was created as a package manager for  [[NODE JS]]

---
### Installation of NPM

- npm comes with Node.js. You only need to install NODE JS to get npm.

### Usage :


```shell
#You can install packages using 
npm install <package-name>

# You can install packages globally using 
npm install -g <package-name>

# You can install packages as development dependencies using 
npm install --save-dev <package-name>

# You can uninstall packages using 
npm uninstall <package-name>

# You can update packages using 
npm update <package-name>

# You can search packages using 
npm search <package-name>

# You can list packages using 
npm list
```


>  The `node_modules`, `package.json`, and `package-lock.json` files in **npm** are **automatically generated** when you install packages.

---
### 1.  Node_modules

Inside this folder, npm installs:

- All the packages listed in your `package.json`
    
- Their **internal dependencies** (which may have more dependencies, forming a dependency tree)
#### Example :
Suppose your `package.json` has:

```json
"dependencies": {
  "express": "^4.18.0"
}
```

When you run `npm install`, it will:

1. Download `express`
    
2. Download all packages that `express` depends on
    
3. Place all of them in the `node_modules` directory

- Your folder structure will look like:

```shell
my-project/
├── package.json  # Project metadata and list of dependencies
├── package-lock.json # Exact versions of installed packages for consistency
└── node_modules/ # Folder where all installed packages are saved
    ├── express/
    ├── accepts/
    ├── cookie/
    └── ...
```
### 2.  package-lock.json

- Is a detailed record of the **exact versions** of every installed package and its dependencies. 
- It ensures that anyone who installs your project will get **exactly the same versions** of all packages.

```json
{
  "name": "my_newproject",
  "version": "1.0.0",
  "lockfileVersion": 3,
  "requires": true,
  "packages": {
    :
    :
 }
```

### 3.  package.json

- The `package.json` file is the heart of a Node.js project.

- It contains metadata about the project, such as the name, version, description, and dependencies.

- All **npm** packages are defined in files called **package.json**.

 - The content of package.json must be written in **JSON**.

```json
{

  "name": "my_newproject",
  "version": "1.0.0",
  "description": "My first project using node",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "TruptiJadhav",
  "license": "ISC",
  "dependencies": {
    "figlet": "^1.8.2"
  }
}
```

---
## Managing Dependencies

**npm** can manage **dependencies**.

**npm** can (in one command line) install all the dependencies of a project.

Dependencies are also defined in **package.json**.

---
### NPM Modules

See: [[Modules in Node JS]]

- **NPM Module** (also called an npm package) is a reusable package **published on the npm registry**. These are created by others or by you and installed using:

```shell
npm install <package-name>
```

##### Examples of popular npm modules:

- [[express]] – Web framework
    
- [[axios]] - HTTP client to make API requests
    
- [[mongoose]] – MongoDB ORM

---

#### Create Your Own NPM Package:**

1. **Initialize a new project**

```shell
npm init
```

2. `package.json`:

   Add `"type": "module"`

##### To publish your package:

- You can also use **npm** to publish your own modules to the npm registry so others can install and use them.

``` bash
npm login
npm publish 
```

---
### Breakdown:

| Term        | Meaning                                                                                                         |
| ----------- | --------------------------------------------------------------------------------------------------------------- |
| **Module**  | Any reusable piece of code in a file (local or npm) — can be a single function, object, class, etc.             |
| **Package** | A **complete, shareable unit** — usually a folder with a `package.json`, which may include one or more modules. |

---
##### *Reference:*
[w3schools.com](https://www.w3schools.com/whatis/whatis_npm.asp)
[npm.com](https://docs.npmjs.com/cli/v11/commands/npm)



