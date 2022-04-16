## **Material 📖**

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRd8KClKsNGwNojHX7pCZTUnW-7woPMWoAmxGohaGFg65txlCcClxVrqZBV_QYLwcYWScKYtSHWjQS2/embed?start=false&loop=false&delayms=60000" frameborder="0" width="500" height="310" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


## **Ex.1 | Javascript**

### Setup 

```javascript
let ready = (callback) => {
    if (document.readyState != "loading") callback();
    else document.addEventListener("DOMContentLoaded", callback);
};

ready(() => {
    /* Do things after DOM has fully loaded */
});

```


<!-- tabs:start -->

#### **Challenges**

### Variables
- Variables are used to store values in memory
- Variables are declared with the `var` keyword
- Scoped Variables are declared with the `let` & `const` keyword
- Variables can be reassigned
- Variables can be declared with or without a value
- Variables can be declared with or without a type

>  **Create a variable called `studentArray` with no value assigned**

### Arrays
- An array can hold many values under a single name
- Arrays are declared with the `[]` symbol
- Arrays can hold any type of data
- Arrays can be declared with or without a typeå
- Arrays can access the values by referring to an index number

>  **Assign the `studentArray` variable to an array**

### Objects
- An object is a collection of key-value pairs
- Objects are declared with the `{}` symbol
- Objects can hold any type of data
- Objects can be declared with or without a type
- Objects can access the values by referring to a key

>  **Create an object with keys of name, location, email, githubUrl, linkedinUrl, resumeLink, type; then add your own values**

### Functions
- Functions are used to perform a specific task
- Functions are declared with the `function` keyword
- Functions can be declared with or without a type; 
- If no type is declared, the function will return `undefined`
- Functions can be called by using the `()` symbol
- Functions can be passed arguments
- Functions can be passed multiple arguments
- Functions can be passed a variable as an argument
- Functions can be passed an array as an argument

>  **Create a function named `loadCards` with a argunent of `studentArray`**

### Methods
- Methods are used to perform a specific task on a specific object
- Methods are declared with the `.` symbol
- Methods can be called by using the `()` symbol
- Methods can be passed arguments
- Methods can be passed multiple arguments

> **Use the `length` method on the `studentArray` variable to get the length of the array**

### Loops
- Loops are used to repeat a specific task
- Loops are declared with the `for` keyword
- Their are different types of loops, `for` loops, `while` loops, and `do while` loops.
- All loops have a condition to check
- For loop conditions can be checked with the `if` keyword
- Loops have a different incrementer or decrementer

> **Create a for loop that iterates through the `studentArray` array and prints out the name of each student**

### Document Object Model
- The DOM is a representation of the HTML document
- The DOM is used to access and manipulate the HTML document
- You can use javascript to access and manipulate the DOM using the `document` object
- The `document` object is used to access the HTML document

> **Use the `document` object to access the `cards` element of the HTML document, store that data in a variable named `cardsDiv`**

#### **Final**

```javascript
let ready = (callback) => {
    if (document.readyState != "loading") callback();
    else document.addEventListener("DOMContentLoaded", callback);
};

const studentArray = [
    {
        name: "Erik",
        location: "San Francisco",
        email: "3salaz.dev@gmail.com",
        locationImg: "https://levineleavitt.com/wp-content/uploads/2018/11/OwenGildersleeve_SanFranciscoMag-Cover-1200x1440.jpg",
        githubUrl: "",
        linkedinUrl: "",
        resumeLink: "",
        type: "instructor",
    }
]

ready(() => {
    /* Do things after DOM has fully loaded */
    // Create An Array of Objects

    // Create An oject with key value pairs, have the keys be (name, age, location)
    function loadCards(studentArray) {
        let studentList = studentArray;
        const cardDiv = document.getElementById("cards");
        console.log(studentList.length);
        // for each currentStudent in array create a card and load it up with the currentStudent information.
        for (let i = 0; i < studentList.length; i++) {
            console.log(studentList[i]);
            let currentStudent = studentList[i];
            cardDiv.innerHTML += `
            <div class="card" id="card${i}">
                <h1 id="cardName">${currentStudent.name}</h1>
                <img src="${currentStudent.locationImg}">
                <h3 id="cardLocation">${currentStudent.location}</h3>
                <a id="cardEmail" class="link" href="mailito:${currentStudent.email}">📧 Email</a>
                <section id="cardLinks">
                    <button id="cardGithubLink" class="btn1"><a class="link" href="${currentStudent.githubUrl}">Github</a></button>
                    <button id="cardResumeLink" class="btn1"><a class="link" href="${currentStudent.resumeLink}">Resume</a></button>
                </section>
                <button id="portfolio" class="btn2"><a href="">Portfolio</button>
            </div>
            `;
        }
    }

    loadCards(studentArray);
});
```

<!-- tabs:end -->

> [!Attention]
> **✅ Final Objective:**
>For every object in the array, create a card with the data from the object.
## **Ex.2 | Node & NPM**

<!-- tabs:start -->


#### **Challenge**

### Node
- Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser
- Node is used to create a server
- Node is used to create a command line interface
- Node is used to create a package manager
- Node is used to create a package

>  **Run node in the terminal**

### NPM
- Npm is a package manager for Node.js
- Npm is used to install packages
- NPM is initalized with the command `npm init`
- NPM stores packages in the `node_modules` folder
- NPM creates a package.json file
- NPM manages dependencies
>  **Install [Nodemon](https://www.npmjs.com/package/nodemon) with NPM**


1. Create a new js file and name it `index.js`
2. Initialize a node project with `npm -y`
3. Install the `express` & `nodemon` package using npm
4. Require the `express` package in your `index.js` file and save it to a variable called express.
5. Execute the `express` package and save it to a variable called `app`
6. Look at documentation in [Express](https://expressjs.com/en/api.html) to see how to use the `app` variable to set the static directory.
#### **Final**
```javascript
const express = require('express');
const app = express();
const port = process.env.PORT || 3001;

app.use(express.json());
app.use(express.static('public'))

app.listen(port, () => console.log(`Listening on port ${port}`));


````
<!-- tabs:end -->

> [!Attention]
> **✅ Final Objective:**
> Run your node server and have it display the contents of your pulic folder at the given URL you set at local host.


## **Lab 🔬**
 ### Full Stack Web Dev
> Objective: Create your first full stack web application. To be clear this is not going to be a full fledged web application. It is just a simple web application that will serve as a learning tool, and to get you started with the basics of javascript. You will be partnering with a peer to complete this lab.

> Prerequisites:
- JavaScript Basics
- Web Development Basics
- Git & Github Basics
- Terminal Basics
- Development Environment

Tasks:
- Create a new project and name it `lab-full-stack-web-dev`
- Partner up with someone and create a google chat between you guys so that you can discuss the lab.
- Decide who is going to create the repositoy and push the code to github.
- Create a firebase project @ https://firebase.google.com/
- Install the firebase cli @ https://firebase.google.com/docs/cli
- Use the firebase cdn to use firebase in your project files
- Initialize a firebase project
- Use the existing project you created
- Replace the public generated by firebase to your own public folder
- Use the firebase documentation to learn how to deploy your application with firebase.
- Send me the link to a live site.
## Resources 🧰

- [Javscript Documentations]('https://developer.mozilla.org/en-US/docs/Web/JavaScript')
- [Node Documentation]('https://nodejs.org/en/docs/')

<div id="previousWeeks">

<details>
    <summary>Previous Weeks</summary>
    Something small enough to escape casual notice.
    <div class="grid">
        <div class="grid-item">
        <h3 class="item-header">Programming Pt1 | Week 4</h3>
    <h6>
    <p class="item-text">
        Learn the fundamentals of programming. So what does that mean? Well, it means that you will be able to write programs that can be used to solve problems. You'll set up your development environment, select a programming language, and start writing code that can be stored and collaborated in the cloud.
    </p>
    <div class="item-links">
        <a class="btn" href="">Material</a>
        <a class="btn" href="">Assignments</a>
    </div>
</div>
<div class="grid-item">
    <h3 class="item-header">Github | Week 3</h3>
    <p class="item-text">
        Learn the fundamentals of programming. So what does that mean? Well, it means that you will be able to write programs that can be used to solve problems. You'll set up your development environment, select a programming language, and start writing code that can be stored and collaborated in the cloud.
    </p>
    <div class="item-links">
        <a class="btn" href="">Material</a>
        <a class="btn" href="">Assignments</a>
    </div>
</div>
<div class="grid-item">
    <h3 class="item-header">Operating Systems | Week 2</h3>
    <p class="item-text">
        Learn the fundamentals of programming. So what does that mean? Well, it means that you will be able to write programs that can be used to solve problems. You'll set up your development environment, select a programming language, and start writing code that can be stored and collaborated in the cloud.
    </p>
    <div class="item-links">
        <a class="btn" href="">Material</a>
        <a class="btn" href="">Assignments</a>
    </div>
</div>
<div class="grid-item">
    <h3 class="item-header">Welcome | Week 1</h3>
    <p class="item-text">
        Learn the fundamentals of programming. So what does that mean? Well, it means that you will be able to write programs that can be used to solve problems. You'll set up your development environment, select a programming language, and start writing code that can be stored and collaborated in the cloud.
    </p>
    <div class="item-links">
        <a class="btn" href="">Material</a>
        <a class="btn" href="">Assignments</a>
    </div>
</div>

</div>

</details>

</div>