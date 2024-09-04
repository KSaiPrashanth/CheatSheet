
![header](/images/JavaScript%20Cheat%20Sheet.webp)

---

<h2>Table of Contents</h2>

- [**JavaScript Cheat Sheet**](#javascript-cheat-sheet)
  - [**1. Variables**](#1-variables)
  - [**2. Data Types**](#2-data-types)
  - [**3. Operators**](#3-operators)
  - [**4. Functions**](#4-functions)
  - [**5. Control Structures**](#5-control-structures)
  - [**6. Arrays**](#6-arrays)
  - [**7. Objects**](#7-objects)
  - [**8. DOM Manipulation**](#8-dom-manipulation)
  - [**9. Events**](#9-events)
  - [**10. Promises**](#10-promises)
  - [**11. Fetch API**](#11-fetch-api)
  - [**12. Async/Await**](#12-asyncawait)
  - [**13. Error Handling**](#13-error-handling)
  - [**14. ES6+ Features**](#14-es6-features)

## JavaScript Cheat Sheet

### **1. Variables**
- **Declare variables:**
  ```javascript
  let x = 10;     // Block-scoped variable
  const y = 20;   // Block-scoped, constant variable
  var z = 30;     // Function-scoped variable
  ```

### **2. Data Types**
- **Primitive Types:** `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`
- **Example:**
  ```javascript
  let name = "John";      // string
  let age = 25;           // number
  let isActive = true;    // boolean
  let unknown = null;     // null
  let notDefined;         // undefined
  ```

### **3. Operators**
- **Arithmetic:** `+`, `-`, `*`, `/`, `%`, `++`, `--`
- **Comparison:** `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
- **Logical:** `&&`, `||`, `!`
- **Assignment:** `=`, `+=`, `-=`, `*=`, `/=`

### **4. Functions**
- **Function Declaration:**
  ```javascript
  function sum(a, b) {
    return a + b;
  }
  ```
- **Function Expression:**
  ```javascript
  const multiply = function(a, b) {
    return a * b;
  };
  ```
- **Arrow Function:**
  ```javascript
  const divide = (a, b) => a / b;
  ```

### **5. Control Structures**
- **If-Else:**
  ```javascript
  if (condition) {
    // code to execute if condition is true
  } else if (anotherCondition) {
    // code to execute if anotherCondition is true
  } else {
    // code to execute if all conditions are false
  }
  ```
- **Switch:**
  ```javascript
  switch (expression) {
    case value1:
      // code to execute if expression === value1
      break;
    case value2:
      // code to execute if expression === value2
      break;
    default:
      // code to execute if no cases match
  }
  ```
- **Loops:**
  - **For Loop:**
    ```javascript
    for (let i = 0; i < 5; i++) {
      // code to execute in each iteration
    }
    ```
  - **While Loop:**
    ```javascript
    let i = 0;
    while (i < 5) {
      // code to execute as long as condition is true
      i++;
    }
    ```
  - **Do-While Loop:**
    ```javascript
    let i = 0;
    do {
      // code to execute at least once and then continue if condition is true
      i++;
    } while (i < 5);
    ```

### **6. Arrays**
- **Create Array:**
  ```javascript
  let numbers = [1, 2, 3, 4, 5];
  ```
- **Array Methods:**
  - **`push()`**: Adds elements to the end.
  - **`pop()`**: Removes the last element.
  - **`shift()`**: Removes the first element.
  - **`unshift()`**: Adds elements to the beginning.
  - **`slice()`**: Returns a portion of an array.
  - **`splice()`**: Adds/removes elements at a specific index.
  - **`forEach()`**: Calls a function for each array element.
  - **`map()`**: Creates a new array with the results of calling a function on every element.
  - **`filter()`**: Creates a new array with all elements that pass the test implemented by the provided function.

### **7. Objects**
- **Create Object:**
  ```javascript
  let person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    greet: function() {
      console.log("Hello!");
    }
  };
  ```
- **Access Properties:**
  ```javascript
  console.log(person.firstName);  // Dot notation
  console.log(person['lastName']);  // Bracket notation
  ```
- **Object Methods:**
  - **`Object.keys(obj)`**: Returns an array of the object's keys.
  - **`Object.values(obj)`**: Returns an array of the object's values.
  - **`Object.entries(obj)`**: Returns an array of the object's key-value pairs.

### **8. DOM Manipulation**
- **Select Elements:**
  ```javascript
  const element = document.getElementById("id");
  const elements = document.getElementsByClassName("class");
  const elements = document.querySelectorAll("selector");
  ```
- **Manipulate Elements:**
  ```javascript
  element.textContent = "New Text";
  element.innerHTML = "<strong>Bold Text</strong>";
  element.style.color = "blue";
  ```

### **9. Events**
- **Add Event Listener:**
  ```javascript
  element.addEventListener("click", function() {
    // code to execute on click
  });
  ```
- **Common Events:**
  - **`click`**: User clicks an element.
  - **`mouseover`**: User hovers over an element.
  - **`keydown`**: User presses a key.

### **10. Promises**
- **Create a Promise:**
  ```javascript
  let promise = new Promise(function(resolve, reject) {
    // asynchronous code
    if (success) {
      resolve(result);
    } else {
      reject(error);
    }
  });
  ```
- **Handle a Promise:**
  ```javascript
  promise
    .then(function(result) {
      // handle success
    })
    .catch(function(error) {
      // handle error
    });
  ```

### **11. Fetch API**
- **Get Data:**
  ```javascript
  fetch("https://api.example.com/data")
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error));
  ```
  
### **12. Async/Await**
- **Async Function:**
  ```javascript
  async function fetchData() {
    try {
      let response = await fetch("https://api.example.com/data");
      let data = await response.json();
      console.log(data);
    } catch (error) {
      console.error(error);
    }
  }
  ```

### **13. Error Handling**
- **Try-Catch:**
  ```javascript
  try {
    // code that may throw an error
  } catch (error) {
    console.error(error);
  } finally {
    // code that runs regardless of an error
  }
  ```

### **14. ES6+ Features**
- **Template Literals:**
  ```javascript
  let greeting = `Hello, ${name}!`;
  ```
- **Destructuring:**
  ```javascript
  let {firstName, lastName} = person;
  let [first, second] = numbers;
  ```
- **Spread Operator:**
  ```javascript
  let newArray = [...numbers, 6, 7];
  let newObject = {...person, city: "New York"};
  ```

---
