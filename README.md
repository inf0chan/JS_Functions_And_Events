# JS_Functions_And_Events

# 📚 Topics Covered

* Functions
* Function Syntax
* Parameters & Arguments
* Return Statement
* Function vs Procedure
* Pure vs Impure Functions
* Function Declaration
* Function Expression
* Arrow Functions
* Events
  
   `addEventListener()`
* Event Object
* Common Events
  
   `removeEventListener()`
* Graceful Degradation

---

#  What is a Function?

A **function** is a reusable block of code that performs a specific task.

Instead of writing the same code many times, write it once and call it whenever needed.

Example:

```javascript
function greet() {
    console.log("Hello");
}

greet();
```

---

#  Why Use Functions?

* Write less code
* Reuse code easily
* Make code easier to read
* Easier to fix bugs
* Easier to test
* Keep projects organized

---

#  Good Function Practices

* Do one task only
* Keep functions short
* Use meaningful names
* Break large functions into smaller ones

---

# Function Syntax

```javascript
function add(a, b) {
    return a + b;
}

let result = add(2, 3);
```

---

# Parameters vs Arguments

## Parameters

Parameters are **variables** written when creating a function.

```javascript
function add(a, b)
```

Here, **a** and **b** are parameters.

## Arguments

Arguments are the **actual values** passed to the function.

```javascript
add(2, 3);
```

Here, **2** and **3** are arguments.

---

# Return Statement

The `return` keyword sends a value back from a function.

```javascript
function square(num) {
    return num * num;
}
```

> After `return`, the function stops running.

---

# Function Without Return

A function can also perform an action without returning a value.

```javascript
function greet() {
    console.log("Hello");
}
```

---

# Function vs Procedure

| Function          | Procedure                 |
| ----------------- | ------------------------- |
| Takes input       | May or may not take input |
| Returns a value   | Doesn't return a value    |
| Produces a result | Performs a task           |

> In JavaScript, both are simply called **functions**.

---

# Pure vs Impure Functions

## Pure Function

* Same input gives the same output.
* Doesn't change outside data.
* Easy to test.

```javascript
function add(a, b) {
    return a + b;
}
```

---

## Impure Function

* Output can change.
* Uses or changes outside variables.

```javascript
let count = 0;

function increment() {
    count++;
}
```

---

# Ways to Create Functions

##  Function Declaration

```javascript
function greet(name) {
    return "Hi " + name;
}
```

---

## Function Expression

```javascript
const greet = function(name) {
    return "Hi " + name;
};
```

---

## Arrow Function

```javascript
const greet = (name) => {
    return "Hi " + name;
};
```

---

# Arrow Function Shortcuts

### Implicit Return

```javascript
const add = (a, b) => a + b;
```

### Single Parameter

```javascript
const square = n => n * n;
```

### Multiple Parameters

```javascript
const add = (a, b) => a + b;
```

---

# What are Events?

An **event** is something the user does on a webpage.

Examples:

* Click
* Double Click
* Mouse Move
* Key Press
* Form Submit
* Scroll

---

# `addEventListener()`

Used to listen for an event.

```javascript
button.addEventListener("click", () => {
    console.log("Button Clicked");
});
```

---

# Callback Function

A callback function is a function passed into another function.

```javascript
button.addEventListener("click", changeColor);
```

 Don't do this:

```javascript
changeColor();
```

This runs the function immediately instead of waiting for the click.

---

# Event Object

The event object stores information about the event.

```javascript
button.addEventListener("click", (event) => {
    console.log(event.target);
    console.log(event.type);
});
```

Useful properties:

* `event.target` → Which element triggered the event.
* `event.type` → Type of event (click, keydown, etc.).

---

# Common Events

| Event       | Description             |
| ----------- | ----------------------- |
| `click`     | User clicks             |
| `dblclick`  | Double click            |
| `mouseover` | Mouse enters an element |
| `mouseout`  | Mouse leaves an element |
| `mousemove` | Mouse moves             |
| `keydown`   | Key is pressed          |
| `keyup`     | Key is released         |
| `input`     | User types              |
| `change`    | Input value changes     |
| `submit`    | Form is submitted       |
| `blur`      | Element loses focus     |
| `scroll`    | User scrolls            |
| `resize`    | Window size changes     |
| `load`      | Page finishes loading   |

---

# Event Handling Pattern

### Step 1: Select the Element

```javascript
const btn = document.querySelector(".btn");
```

### Step 2: Create the Function

```javascript
function changeColor() {
    document.body.style.background = "lightblue";
}
```

### Step 3: Attach the Event

```javascript
btn.addEventListener("click", changeColor);
```

 Easy way to remember:

> **Select → Listen → Do**

---

# `removeEventListener()`

Removes an event listener.

```javascript
btn.addEventListener("click", changeColor);

btn.removeEventListener("click", changeColor);
```

### Why use it?

* Stop one-time actions
* Save memory
* Disable features when needed

> It only works with the **same named function**.

---

# Graceful Degradation

A website should still work even if JavaScript is turned off.

### Best Practices

* Build the HTML first.
* Use CSS for styling.
* Add JavaScript only for extra features.
* Don't make the whole website depend on JavaScript.

---

# Key Takeaways

* Functions are reusable blocks of code.
* Parameters are variables inside a function.
* Arguments are the values passed to a function.
* `return` sends a value back.
* Pure functions don't change outside data.
* JavaScript supports Function Declaration, Function Expression, and Arrow Functions.
* Events make websites interactive.
* `addEventListener()` is used to listen for events.
* The event object gives information about an event.
* `removeEventListener()` removes an event listener.
* A simple event flow is:

> **Select → Listen → Do**
