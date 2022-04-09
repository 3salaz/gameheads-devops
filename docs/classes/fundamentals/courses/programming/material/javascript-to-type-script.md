<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTJhhz2WXw1EpLA3pd40saN8D2mgRuCabN4oxkeKxVNgaeIHC_w4CBtHwlk87O-lI99p0O04Pd1jg_q/embed?start=false&loop=false&delayms=60000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---

## Ex.1 |Create a Javascript file

**Obj: For this assignment I want you to use your linux knowledge to create files, your github knowledge to save your exercies in a repository, -**

- **Get a Javascript file linked to a index.html file.**

You have to create a file called index.html and put the following code in it:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>

```

- **Use console log hello world and save file.**
> 

 ```javascript
 console.log('hello world');
 ```

- **Use VsCode To Run Index File**

Right click the Inded file and select run live browser. Check bottom right corner

- **Open Developer Tools in Chrome**

**Mac:**
Option + Command + I

- **✅ Check Results**

Check the console tag to view the results.

## Ex. 2 | Run Node Server

**Obj: We're gonna use npm node and express to create a server running on a specific port of our choosing.**

> - **Initialize a npm package**

```terminal
    npm init
```

> - **Install Packages needed**

```
npm install express --save
npm install body-parser --save
```

> - **Create a server.js file**

```
const express = require('express');
const bodyParser = require("body-parser");

const app = express();
const PORT = 3000;


app.use(bodyParser.json());

app.get('/', (req, res) => {
    res.send('Hello World!');
});

const sayHi = (req, res) => {
    res.send("Hi!");
};

app.listen(PORT, () => console.log(`Server listening on port: ${PORT}`));
````

> - **Configure Package.json**

``` json
{
  "name": "ex-1",
  "version": "1.0.0",
  "description": "",
  "main": "main.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node main.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "body-parser": "^1.20.0",
    "express": "^4.17.3"
  }
}
```

> - **Run the server**
```
    node server.js
```
---
### Resources 🔗
- [JamBoard| Diagrams](https://jamboard.google.com/d/1e1fx-KsHN7Karl-oSaTC5WdXFYRHPlx28Lc_eNmjOTI/edit?usp=sharing)




