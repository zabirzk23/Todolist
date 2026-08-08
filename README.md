# Ex03 To-Do List using JavaScript
# Name: Mohamed Zabir Khan A
# Register Number:212224230162
## Date: 08-08-2026

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
todo.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="todo.css">
</head>
<body>
  <div class="todo-container">
    <h1>My To-Do List</h1>
    <input type="text" id="task-input" placeholder="Add a new task...">
    <button id="add-task">Add</button>
    <ul id="task-list"></ul>
  </div>
  <script src="todo.js"></script>
</body>
</html>

```
todo.css
```
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: linear-gradient(135deg, #89f7fe 0%, #66a6ff 100%);
  height: 100vh;
}

.todo-container {
  background: #fff;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0px 4px 15px rgba(0,0,0,0.2);
  width: 350px;
  text-align: center;

  /* Position at top center */
  position: absolute;
  top: 50px;
  left: 50%;
  transform: translateX(-50%);
}

h1 {
  margin-bottom: 20px;
  color: #333;
}

#task-input {
  padding: 10px;
  width: 70%;
  border: 1px solid #ccc;
  border-radius: 5px;
}

#add-task {
  padding: 10px 15px;
  border: none;
  background-color: #5c6bc0;
  color: white;
  border-radius: 5px;
  cursor: pointer;
}

#add-task:hover {
  background-color: #3f51b5;
}

ul {
  list-style-type: none;
  padding: 0;
  margin-top: 20px;
}

li {
  padding: 10px;
  background: #f1f1f1;
  margin-bottom: 10px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li button {
  background: red;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
}

li button:hover {
  background: darkred;
}
li.completed {
  text-decoration: line-through;
  color: gray;
}

li .done-btn {
  background: green;
  margin-right: 10px;
}

li .done-btn:hover {
  background: darkgreen;
}

```
todo.js
```
const input = document.getElementById("task-input");
const addButton = document.getElementById("add-task");
const taskList = document.getElementById("task-list");


function addTask() {
  const taskText = input.value.trim();
  if (taskText === "") return;


  const li = document.createElement("li");

  
  const doneBtn = document.createElement("button");
  doneBtn.textContent = "✓"; 
  doneBtn.className = "done-btn";
  doneBtn.onclick = () => li.classList.toggle("completed");


  const deleteBtn = document.createElement("button");
  deleteBtn.textContent = "Delete";
  deleteBtn.onclick = () => li.remove();

  li.textContent = taskText;
  li.prepend(doneBtn); 
  li.appendChild(deleteBtn);

  taskList.appendChild(li);

  input.value = "";
}


addButton.addEventListener("click", addTask);
input.addEventListener("keypress", (e) => {
  if (e.key === "Enter") addTask();
});

```
## OUTPUT
<img width="1917" height="1087" alt="image" src="https://github.com/user-attachments/assets/b5b522ec-8f58-4bd6-8e75-2ed93a6aa389" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
