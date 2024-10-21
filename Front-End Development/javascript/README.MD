# JavaScript Documentation

## 1. **Introduction to JavaScript**
JavaScript is a high-level, dynamic programming language commonly used for web development. It enables developers to create interactive websites by manipulating HTML and CSS, handling user inputs, and dynamically updating content. JavaScript is versatile and supports object-oriented, functional, and procedural programming styles. It can be executed in web browsers (client-side) and on servers using Node.js (server-side).

---

## 2. **Environment Setup**
### Prerequisites
- **HTML**: Structure for web pages.
- **CSS**: Styling for web pages.
- **IDE/Editor**: Code editor like Visual Studio Code or Sublime Text.

### Initializing Project with ESLint and Prettier
1. Initialize npm:
   ```bash
   npm init -y
   ```
2. Install and configure ESLint:
   ```bash
   npm install eslint --save-dev
   npx eslint --init
   ```
3. Install and configure Prettier:
   ```bash
   npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier
   ```

---

## 3. **Adding JavaScript to HTML**
There are three ways to incorporate JavaScript into an HTML file:

### 3.1 **Inline JavaScript**
JavaScript can be written directly inside an HTML tag.
```html
<body onload="alert('Welcome to JavaScript!')">
```

### 3.2 **Internal JavaScript**
JavaScript is written within the `<script>` tags inside the HTML document.
```html
<script>
  document.write("Welcome to JavaScript!");
</script>
```

### 3.3 **External JavaScript**
JavaScript code is saved in an external file with a `.js` extension and linked to the HTML file.
```html
<script src="script.js"></script>
```

---

## 4. **JavaScript Basics**
### 4.1 Print Statements
- **alert()**: Displays a popup.
  ```javascript
  alert("Welcome to JavaScript!");
  ```
- **document.write()**: Writes directly on the HTML page.
  ```javascript
  document.write("Hello, World!");
  ```
- **console.log()**: Logs information in the developer console.
  ```javascript
  console.log("Debugging information");
  ```

### 4.2 Comments
- **Single-line comments**:
  ```javascript
  // This is a comment
  ```
- **Multi-line comments**:
  ```javascript
  /* This is a 
     multi-line comment */
  ```

### 4.3 Variables
Variables in JavaScript can be declared using `var`, `let`, or `const`.
```javascript
var name = "John";
let age = 25;
const university = "XYZ University";
```

#### Naming Rules:
- Variables must start with a letter, `_`, or `$`.
- They cannot start with numbers.
- Case sensitive and cannot use reserved keywords.

---

## 5. **Data Types and Operators**
### 5.1 Data Types
- **String**: `"Hello"`
- **Number**: `123`, `45.6`
- **Boolean**: `true`, `false`
- **Object**: 
  ```javascript
  const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30
  };
  ```
  
### 5.2 Operators
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`
- **Relational Operators**: `>`, `<`, `>=`, `<=`, `==`, `===`
- **Logical Operators**: `&&`, `||`, `!`

---

## 6. **Control Structures**
### 6.1 Conditional Statements
- **If-Else Statement**:
  ```javascript
  if (condition) {
    // code
  } else if (anotherCondition) {
    // another code
  } else {
    // code if none are true
  }
  ```

- **Switch Statement**:
  ```javascript
  switch (expression) {
    case value1:
      // code
      break;
    case value2:
      // code
      break;
    default:
      // default code
  }
  ```

### 6.2 Loops
- **For Loop**:
  ```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }
  ```

- **While Loop**:
  ```javascript
  let i = 0;
  while (i < 5) {
    console.log(i);
    i++;
  }
  ```

- **Do-While Loop**:
  ```javascript
  let i = 0;
  do {
    console.log(i);
    i++;
  } while (i < 5);
  ```

### 6.3 Ternary Operator
```javascript
let result = (condition) ? "Value if true" : "Value if false";
```

---

## 7. **Functions and Objects**
### 7.1 Functions
- **Declaration**:
  ```javascript
  function greet() {
    return "Hello!";
  }
  ```
- **With Parameters**:
  ```javascript
  function greet(name) {
    return "Hello, " + name;
  }
  ```
- **Anonymous Functions (Function Expressions)**:
  ```javascript
  const greet = function() {
    return "Hello!";
  };
  ```

### 7.2 Objects
- **Creating an Object**:
  ```javascript
  const car = {
    make: "Toyota",
    model: "Corolla",
    year: 2020
  };
  ```

- **Accessing Object Properties**:
  ```javascript
  console.log(car.make); // Outputs: Toyota
  ```

---

## 8. **Arrays**
### 8.1 Creating Arrays
- **1D Array**:
  ```javascript
  let fruits = ["Apple", "Banana", "Mango"];
  ```
- **2D Array**:
  ```javascript
  let matrix = [[1, 2], [3, 4]];
  ```

### 8.2 Array Methods
- **push()**: Adds an element to the end of an array.
  ```javascript
  fruits.push("Orange");
  ```
- **pop()**: Removes the last element.
  ```javascript
  fruits.pop();
  ```

- **slice()**: Extracts a section of an array.
  ```javascript
  let sliced = fruits.slice(0, 2); // ["Apple", "Banana"]
  ```

---

## 9. **Date and Math Objects**
### 9.1 Date Object
```javascript
let date = new Date();
console.log(date.getFullYear()); // Get current year
```

### 9.2 Math Object
```javascript
let random = Math.random(); // Generates a random number between 0 and 1
let rounded = Math.round(4.5); // Rounds to the nearest integer
```

---

## 10. **DOM Manipulation**
### 10.1 Selecting Elements
- **By ID**:
  ```javascript
  document.getElementById("elementId").innerHTML = "New Text";
  ```

- **By Tag Name**:
  ```javascript
  document.getElementsByTagName("h1")[0].innerHTML = "Heading Text";
  ```

- **By Class Name**:
  ```javascript
  document.getElementsByClassName("className")[0].innerHTML = "Class Text";
  ```

- **Query Selector**:
  ```javascript
  document.querySelector(".className").innerHTML = "Query Selector Text";
  ```

### 10.2 Modifying DOM Elements
- **Creating Elements**:
  ```javascript
  let newElement = document.createElement("p");
  let text = document.createTextNode("New Paragraph");
  newElement.appendChild(text);
  document.body.appendChild(newElement);
  ```

- **Changing Styles**:
  ```javascript
  document.getElementById("elementId").style.color = "blue";
  ```

---

## 11. **Events**
### 11.1 Event Listeners
- **Adding an Event Listener**:
  ```javascript
  document.getElementById("button").addEventListener("click", function() {
    alert("Button clicked!");
  });
  ```

### 11.2 Event Types
- **Mouse Events**: `click`, `dblclick`, `mousedown`, `mouseup`
- **Keyboard Events**: `keypress`, `keydown`, `keyup`
- **Form Events**: `submit`, `change`, `focus`

---

## 12. **Error Handling**
- **try-catch-finally**:
  ```javascript
  try {
    // Code that may throw an error
  } catch (error) {
    console.log(error.message);
  } finally {
    console.log("Executed regardless of error");
  }
  ```

---

## 13. **ES6 and Modern JavaScript**
### 13.1 let and const
- **let**: Block-scoped variable.
- **const**: Block-scoped constant.

### 13.2 Template Literals
```javascript
let name = "John";
console.log(`Hello, ${name}!`);
```

### 13.3 Arrow Functions
```javascript
const add = (a, b) => a + b;
```

---

## 14. **API Interaction**
### Fetch API Example:
```javascript
fetch('

https://jsonplaceholder.typicode.com/posts')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log('Error:', error));
```

---

## 15. **Conclusion**
This documentation covers the basic syntax, features, and techniques for working with JavaScript. It provides a foundation to help you develop interactive web pages and dynamic applications.