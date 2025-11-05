
JavaScript (JS) is a programming language used to make websites interactive — buttons, sliders, animations, popups, and logic.


 HTML → Structure


 CSS → Style


 JavaScript → Functionality



 How to Add JavaScript
 Inline
<button onclick="alert('Hello!')">Click Me</button>

 Internal
<script>
  alert("Welcome to JavaScript!");
</script>

 External
<script src="script.js"></script>

 Always prefer external JS for large projects.

 Basic Output Methods
console.log("Hello Console"); // Developer log
alert("This is an alert box!");
document.write("Hello Document");


 Variables in JS
let name = "Faizan";
const age = 20;
var country = "Pakistan";

console.log(name, age, country);


let → can change later


const → fixed


var → old version (avoid it)



 Data Types
let text = "Hello";       // String
let number = 42;          // Number
let isOnline = true;      // Boolean
let fruits = ["Apple", "Banana"];  // Array
let person = { name: "Faizan", age: 20 };  // Object


 Operators
let a = 10, b = 5;

console.log(a + b); // Addition
console.log(a - b); // Subtraction
console.log(a * b); // Multiplication
console.log(a / b); // Division
console.log(a % b); // Remainder


 Conditional Statements
let age = 18;

if (age >= 18) {
  console.log("You are adult");
} else {
  console.log("You are minor");
}


 Loops in JS
For Loop
for (let i = 1; i <= 5; i++) {
  console.log("Number:", i);
}

While Loop
let i = 1;
while (i <= 3) {
  console.log("Loop", i);
  i++;
}


 Functions
function greet(name) {
  console.log("Hello " + name + "!");
}

greet("Faizan");

 Use functions to reuse code easily.

 Arrays
let colors = ["Red", "Green", "Blue"];

console.log(colors[0]); // Red
colors.push("Yellow");  // Add new
colors.pop();           // Remove last

console.log(colors);


 Objects
let student = {
  name: "Faizan",
  age: 20,
  course: "Web Development"
};

console.log(student.name);
console.log(student["course"]);


 Events in JS
<button onclick="showMessage()">Click Me</button>

<script>
  function showMessage() {
    alert("Button Clicked!");
  }
</script>

 Events like onclick, onmouseover, onchange, etc., make websites interactive.

 DOM Manipulation
The Document Object Model (DOM) lets JS interact with HTML.
<h2 id="title">Hello World</h2>
<button onclick="changeText()">Change Text</button>

<script>
  function changeText() {
    document.getElementById("title").innerHTML = "Text Changed!";
  }
</script>


 Changing CSS with JS
<p id="para">This is a paragraph.</p>
<button onclick="changeColor()">Change Color</button>

<script>
  function changeColor() {
    document.getElementById("para").style.color = "blue";
  }
</script>


 Getting Input from User
<input id="name" placeholder="Enter your name">
<button onclick="greetUser()">Greet</button>

<script>
  function greetUser() {
    let user = document.getElementById("name").value;
    alert("Hello " + user + "!");
  }
</script>


 Math Object
console.log(Math.sqrt(25));  // 5
console.log(Math.pow(2, 3)); // 8
console.log(Math.random());  // Random number 0–1


 String Methods
let text = "Hello World";
console.log(text.length);
console.log(text.toUpperCase());
console.log(text.toLowerCase());
console.log(text.replace("World", "Faizan"));


 Date Object
let now = new Date();
console.log(now);
console.log(now.getFullYear());
console.log(now.getHours());


 Arrays Methods
let nums = [1, 2, 3, 4];
nums.push(5);
nums.splice(1, 1); // remove 1 element at index 1
nums.forEach(num => console.log(num));


 Arrow Functions
const add = (a, b) => a + b;
console.log(add(5, 3)); // 8


 Loops with Arrays
let students = ["Ali", "Sara", "Faizan"];

for (let s of students) {
  console.log(s);
}


 JSON (JavaScript Object Notation)
let person = { name: "Faizan", age: 20 };
let jsonData = JSON.stringify(person); // Convert to JSON
console.log(jsonData);

let parsed = JSON.parse(jsonData); // Convert back
console.log(parsed.name);


 Mini Project — Counter App
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Counter App</title>
  <style>
    body { text-align: center; font-family: Arial; padding-top: 50px; }
    button { padding: 10px 20px; margin: 5px; font-size: 18px; }
  </style>
</head>
<body>
  <h1 id="count">0</h1>
  <button onclick="increase()">+</button>
  <button onclick="decrease()">−</button>
  <button onclick="reset()">Reset</button>

  <script>
    let counter = 0;
    function increase() { counter++; document.getElementById("count").innerText = counter; }
    function decrease() { counter--; document.getElementById("count").innerText = counter; }
    function reset() { counter = 0; document.getElementById("count").innerText = counter; }
  </script>
</body>
</html>


 Mini Project — To-Do List
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do App</title>
  <style>
    body { font-family: Arial; text-align: center; padding: 30px; }
    input { padding: 10px; width: 60%; }
    button { padding: 10px; }
    ul { list-style: none; padding: 0; }
    li { margin: 10px 0; background: #eee; padding: 10px; border-radius: 5px; }
  </style>
</head>
<body>
  <h1>To-Do App</h1>
  <input id="taskInput" placeholder="Add a new task">
  <button onclick="addTask()">Add</button>
  <ul id="taskList"></ul>

  <script>
    function addTask() {
      let input = document.getElementById("taskInput");
      let li = document.createElement("li");
      li.textContent = input.value;
      document.getElementById("taskList").appendChild(li);
      input.value = "";
    }
  </script>
</body>
</html>






✨ Star this repo if you liked this JavaScript Guide!

Would you like me to make a Full Front-End Roadmap README next (HTML + CSS + JS + tools + career path) — formatted for your GitHub?
