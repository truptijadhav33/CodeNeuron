## Introduction 

- Node.js is an open-source and cross-platform [[Javascript]] runtime environment. It is a popular tool for almost any kind of project!
-  Node.js represents a "JavaScript everywhere"
- That is it executes JavaScript code outside a web browser
- Node.js lets developers use JavaScript to write command line tools and for server-side scripting.

``` js
console.log('Hello from Node.js!');
```

---
## Installation 

- download Node.js from the official website [nodejs.org](https://nodejs.org/).

- You can also install Node.js using a package manager like `apt` for Linux

```
sudo apt install nodejs
```

---
## Features of Node.js

1.  **Asynchronous and Event-Driven:**
	1. Node.js does **not wait** for tasks to finish.
	2. It starts a task and **moves on to the next one**.
	3. When the task is done, Node.js gets the result using **callbacks or promises**.
	
2. **Very Fast**:
	1. Node.js runs on **Google's V8 engine**, which is **super fast** in running JavaScript code.
    2. It handles many operations like reading files or databases **quickly**
    
3. **Single-Threaded but Highly Scalable**
	1. Node.js uses **a single main thread** to handle requests.
	2. But it's designed to **handle thousands of users at once** using non-blocking techniques.
	3. So, even with one thread, it can **manage a lot of work**.
	
4. **No Buffering**
	1. Node.js sends data in **chunks** instead of waiting to collect all of it.
	2. This means **data is sent piece by piece** without delay.
	3. e.g Like watching a video while it’s still downloading.

---
## Node.js Applications

- Web Applications
- Real-Time Chat Applications
- [[RESTful API]] Applications
- Microservices
- CRON Jobs

#### Next:
[[Node JS Architecture]]  || [[Getting Start NODE JS]] 
