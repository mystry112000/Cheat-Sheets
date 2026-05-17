# 🌐 HTML Cheat Sheet

> HTML is the structure of every website — like the skeleton of a webpage.

---

## 📄 Basic Page Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Website</title>
</head>
<body>

  <h1>Hello World!</h1>
  <p>This is my first paragraph.</p>

</body>
</html>
```

---

## 🏷️ Common Tags

### Text

```html
<h1>Heading 1</h1>       <!-- Biggest heading (use once per page) -->
<h2>Heading 2</h2>       <!-- Subheading -->
<h3>Heading 3</h3>       <!-- And so on... up to h6 -->
<p>This is a paragraph of text.</p>
<strong>Bold text</strong>
<em>Italic text</em>
<br>                     <!-- Line break (no closing tag needed) -->
<hr>                     <!-- Horizontal line (no closing tag needed) -->
```

### Links & Images

```html
<!-- Link to another page -->
<a href="https://google.com">Click me</a>

<!-- Link that opens in new tab -->
<a href="https://google.com" target="_blank">Open Google</a>

<!-- Link to another page on your site -->
<a href="about.html">About Us</a>

<!-- Image -->
<img src="photo.jpg" alt="Description of image">
```

### Lists

```html
<!-- Unordered list (bullet points) -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>

<!-- Ordered list (numbered) -->
<ol>
  <li>First step</li>
  <li>Second step</li>
  <li>Third step</li>
</ol>
```

### Divs & Spans (Containers)

```html
<div>Block-level container (takes full width)</div>
<span>Inline container (stays in line with text)</span>
```

---

## 📝 Forms

```html
<form action="/submit" method="POST">
  <!-- Text input -->
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Enter your name" required>

  <!-- Email input -->
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <!-- Password -->
  <label for="password">Password:</label>
  <input type="password" id="password" name="password">

  <!-- Textarea (multi-line) -->
  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4"></textarea>

  <!-- Dropdown -->
  <label for="country">Country:</label>
  <select id="country" name="country">
    <option value="">Select...</option>
    <option value="us">United States</option>
    <option value="in">India</option>
  </select>

  <!-- Radio buttons -->
  <input type="radio" id="male" name="gender" value="male">
  <label for="male">Male</label>
  <input type="radio" id="female" name="gender" value="female">
  <label for="female">Female</label>

  <!-- Checkbox -->
  <input type="checkbox" id="agree" name="agree" required>
  <label for="agree">I agree to terms</label>

  <!-- Submit button -->
  <button type="submit">Send Message</button>
</form>
```

---

## 🧱 HTML5 Semantic Tags (Better Structure)

```html
<header>   <!-- Top of page: logo, nav, title -->
<nav>      <!-- Navigation menu -->
<main>     <!-- Main content of the page -->
<section>  <!-- A section of content -->
<article>  <!-- A self-contained piece of content -->
<aside>    <!-- Sidebar, related content -->
<footer>   <!-- Bottom of page: copyright, links -->
<figure>   <!-- An image with a caption -->
```

**Why use these?** Better for SEO, accessibility, and cleaner code.

---

## 🎯 Classes & IDs

```html
<!-- class = reusable (can use on many elements) -->
<div class="card">This is a card</div>
<div class="card">This is also a card</div>

<!-- id = unique (use only once per page) -->
<div id="main-header">Main heading</div>

<!-- How to use them -->
<style>
  .card { color: blue; }        /* Target by class */
  #main-header { font-size: 2em; }  /* Target by id */
</style>
```

---

## 🌐 Useful Attributes

```html
<img src="photo.jpg" alt="Text if image doesn't load">
<a href="page.html" title="Hover text">Link</a>
<input type="text" disabled>                 <!-- Can't type in this -->
<input type="text" readonly>                 <!-- Can see but not edit -->
<button type="submit">Send</button>          <!-- Submits form -->
<div data-user-id="123">Hidden data</div>    <!-- Store custom data -->
```

---

## 💡 Pro Tips

- Always use `<!DOCTYPE html>` at the top
- Always add `alt` text to images (accessibility + SEO)
- Use semantic tags (`<header>`, `<main>`, `<footer>`) instead of `<div>` everywhere
- Make sure your `<title>` describes the page
- Validate your HTML at https://validator.w3.org
