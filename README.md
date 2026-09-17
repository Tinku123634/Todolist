# Ex03 To-Do List using JavaScript
## Date:19-9-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

Index.html

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>To-Do List</h1>

        <div class="input-section">
    <input type="text" id="taskInput" placeholder="Enter a task">
    <button onclick="addTask()">Add</button>
</div>
        <ul id="taskList"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>

```

Style.css

```
body {
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #74ebd5, #ACB6E5);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    width: 350px;
    background: white;
    padding: 25px;
    border-radius: 15px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    text-align: center;
}

h1 {
    color: #333;
    margin-bottom: 20px;
}

.input-section {
    display: flex;
    gap: 10px;
}

input {
    flex: 1;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 8px;
    outline: none;
    font-size: 15px;
}

input:focus {
    border-color: #6c63ff;
}

button {
    padding: 10px 15px;
    background: #6c63ff;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    background: #574bdb;
}

ul {
    list-style: none;
    padding: 0;
    margin-top: 20px;
}

li {
    background: #f4f4f4;
    padding: 12px;
    margin-top: 10px;
    border-radius: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: 0.3s;
}

li:hover {
    transform: scale(1.02);
}

.delete {
    background: crimson;
    padding: 6px 10px;
    border-radius: 5px;
}

.delete:hover {
    background: darkred;
}

```
script.js

```
function addTask() {

    let input = document.getElementById("taskInput");
    let task = input.value;

    if (task === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");
    li.innerHTML = task;

    let deleteBtn = document.createElement("button");
    deleteBtn.innerHTML = "Delete";
    deleteBtn.className = "delete";

    deleteBtn.onclick = function () {
        li.remove();
    };

    li.appendChild(deleteBtn);

    document.getElementById("taskList").appendChild(li);

    input.value = "";
}

```





## OUTPUT

<img width="1042" height="552" alt="image" src="https://github.com/user-attachments/assets/384368fb-6ef1-4036-ba09-10ace2c007bc" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
