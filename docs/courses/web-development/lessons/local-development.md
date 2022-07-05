# Local Development

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTu38fJj0X_NK5B48z6EYILuaj435BbfNPJQajeE7MDhfa1X1xk8hxZrSjikEhXpGp8APGJn7Q8AmzP/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
## 🏋🏽‍♂️ Ex1 | Create A Web Page
---
### 1a | Use linux to create a projects folder for our excercises
```bash
    mkdir projects
```
```bash
    cd projects
```
```bash
    mkdir web-development
```
```bash
    cd web-development
```
```bash
    mkdir exercises
```
```bash
    cd exercises
```
```bash
    mkdir ex1-create-a-web-page
```
```bash
    cd ex1-create-a-web-page
```
### 1b | Create a index file within your ex.1 folder with a bare bones html structure
````bash
    touch index.html
````

````index.html
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
````
### 1c | Create folders and files (within your ex.1 folder) for your styles and scripts
```bash
    mkdir styles scripts
```
```bash
    touch styles/master.css
```
```bash
    touch scripts/main.js
```
### 1d | Link your css javascript to your html page.

```index.html
    <link rel="stylesheet" href="styles/master.css">

```

````index.html
    <script src="scripts/main.js"></script>
````
### 1e | Initiate Repo on project and push to github
````bash
    git init
````
````bash
    git add .
````
````bash
    git commit -m "Initial commit"
````
````bash
    git remote add origin

````
## 🏋🏽‍♂️ Ex2 | Style and animate your page
---
### 2a | Task 
```bash
    some commands
```
### 2b | Task 
```bash
    some commands
```
### 2c | Task 
```bash
    some commands
```
---

## 🔬Lab | Dev Portfolio

*Objective: Create your first full stack web application. To be clear this is not going to be a full fledged web application. It is just a simple web application that will serve as a learning tool, and to get you started with the basics of javascript. You will be partnering with a peer to complete this lab.*

**Prerequisites:**
- Terminal
- Text Editor (VS Code)
- Git
- HTML, CSS, Javascript

Tasks:
- Clone down the `dev-portfolio` repo from github.
- Navigate to the `dev-portfolio` folder.
- Use templates to add html, css, and javascript to your project.
- Open your index.html file in your browser.
- Check Results
- Use git to add and commit your files.
- Push your files to github.
