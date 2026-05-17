# 🔧 JavaScript Cheat Sheet

> JavaScript makes websites interactive — buttons that do things, animations, forms that check your input, and much more.

---

## 🚀 Running JavaScript

```html
<!-- In an HTML file (put before closing </body>) -->
<script>
  console.log("Hello!");
</script>

<!-- Or link a .js file -->
<script src="script.js"></script>
```

Open browser console: `F12` → Console tab (see your `console.log` output)

---

## 📦 Variables

```javascript
// Old way (avoid using)
var name = "Adhithya";

// New way (use these)
let age = 21;           // Can change later
const birthday = "May 1";  // Cannot change (constant)

// Data types
let name = "Adhithya";        // String
let age = 21;                 // Number
let isGamer = true;           // Boolean
let hobbies = ["code", "game"];  // Array (list)
let person = { name: "AJ", age: 21 };  // Object
```

---

## 🎯 Functions

```javascript
// Old way
function greet(name) {
  return "Hello, " + name + "!";
}

// New way (arrow function — modern)
const greet = (name) => {
  return `Hello, ${name}!`;   // Template literal (use backticks)
};

// Even shorter
const greet = name => `Hello, ${name}!`;

// Call it
console.log(greet("Adhithya"));  // Hello, Adhithya!
```

---

## 🔄 If/Else

```javascript
let age = 18;

if (age >= 18) {
  console.log("Adult");
} else if (age >= 13) {
  console.log("Teen");
} else {
  console.log("Child");
}

// Ternary (shorthand if/else)
let status = age >= 18 ? "Adult" : "Minor";
```

---

## 🔁 Loops

```javascript
// For loop
for (let i = 0; i < 5; i++) {
  console.log(i);        // 0, 1, 2, 3, 4
}

// For...of (loop through array)
const games = ["Valorant", "GTA", "Minecraft"];
for (let game of games) {
  console.log(game);
}

// ForEach (modern way)
games.forEach(game => console.log(game));

// While loop
let count = 0;
while (count < 5) {
  console.log(count);
  count++;
}
```

---

## 🧩 Arrays (Lists)

```javascript
let items = ["a", "b", "c"];

items[0]             // "a" (index starts at 0)
items.push("d")      // Add to end: ["a", "b", "c", "d"]
items.pop()          // Remove from end: ["a", "b", "c"]
items.unshift("z")   // Add to start: ["z", "a", "b", "c"]
items.shift()        // Remove from start: ["a", "b", "c"]
items.length         // 3 (how many items)
items.indexOf("b")   // 1 (position of item)
items.includes("a")  // true (check if exists)

// Array methods (very useful)
const numbers = [1, 2, 3, 4, 5];
numbers.map(n => n * 2)       // [2, 4, 6, 8, 10] (transform each)
numbers.filter(n => n > 2)    // [3, 4, 5] (keep matching)
numbers.find(n => n > 3)      // 4 (first match)
numbers.reduce((a, b) => a + b)  // 15 (add all together)
```

---

## 🔧 DOM (Changing HTML with JavaScript)

```javascript
// Get elements
document.getElementById("myId")          // By ID
document.querySelector(".myClass")       // By CSS selector (first match)
document.querySelectorAll("p")           // All matching elements

// Change content
document.querySelector("h1").textContent = "New Title";
document.querySelector("h1").innerHTML = "<span>New</span> Title";

// Change styles
document.querySelector("p").style.color = "red";
document.querySelector("p").classList.add("highlight");
document.querySelector("p").classList.remove("hidden");
document.querySelector("p").classList.toggle("active");  // On/Off switch

// Create elements
const div = document.createElement("div");
div.textContent = "Hello!";
document.body.appendChild(div);
```

---

## 🖱️ Events (Reacting to User)

```javascript
// Click
button.addEventListener("click", () => {
  alert("You clicked me!");
});

// Form submit
form.addEventListener("submit", (e) => {
  e.preventDefault();           // Stop page reload
  console.log("Form submitted");
});

// Input (while typing)
input.addEventListener("input", (e) => {
  console.log(e.target.value);  // Current text in input
});

// Hover
element.addEventListener("mouseover", () => {
  element.style.background = "blue";
});
element.addEventListener("mouseout", () => {
  element.style.background = "";
});
```

---

## ⏳ Async (Waiting for things)

```javascript
// Fetch data from an API (e.g., get data from a server)
fetch("https://api.example.com/data")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log("Error:", error));

// Modern way (async/await — cleaner)
async function getData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.log("Error:", error);
  }
}

// Wait some time
setTimeout(() => {
  console.log("2 seconds later...");
}, 2000);

// Run every X seconds
setInterval(() => {
  console.log("Every 3 seconds");
}, 3000);
```

---

## 🚨 Common Beginner Mistakes

```javascript
// Wrong (undefined)
console.log(myVar);    // Error! Not defined yet

// Right
let myVar = "hello";
console.log(myVar);

// Wrong (modifying const)
const name = "Adhithya";
name = "John";         // Error! Can't reassign const

// Right — const is fine for objects/arrays
const person = { name: "Adhithya" };
person.name = "John";  // This IS allowed (modifying property, not reassigning)

// Wrong (== vs ===)
if (5 == "5")   // true (checks value only — bad)
if (5 === "5")  // false (checks type AND value — good)
```

---

## 💡 Pro Tips

- Use `console.log()` everywhere to debug — best tool
- Always use `const` by default, `let` only when you need to reassign
- Put your `<script>` tag at the end of `<body>` (or use `defer`)
- Use backticks `` ` `` for template literals: `` `Hello ${name}` ``
- VS Code + Chrome DevTools (F12) = best development setup
- When in doubt, check the console for error messages
