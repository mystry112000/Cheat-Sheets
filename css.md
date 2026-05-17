# 🎨 CSS Cheat Sheet

> CSS makes your HTML look good — colors, layouts, fonts, spacing, animations.

---

## 📝 Syntax

```css
/* Select which HTML element to style */
selector {
  property: value;  /* What to change and how */
}
```

**Example:**
```css
p {
  color: blue;        /* Make text blue */
  font-size: 16px;    /* Set size */
}
```

---

## 🎯 Selectors (Targeting Elements)

```css
/* Element selector */
p { color: red; }

/* Class selector (use with class="name" in HTML) */
.card { background: white; }

/* ID selector (use with id="name" in HTML) */
#header { font-size: 2em; }

/* All elements */
* { margin: 0; }

/* Multiple selectors */
h1, h2, h3 { font-weight: bold; }

/* Nested element */
div p { color: gray; }           /* p inside a div */
div > p { color: gray; }         /* p DIRECTLY inside div */

/* Attribute selector */
input[type="text"] { border: 1px solid gray; }

/* Pseudo-classes (state) */
button:hover { background: blue; }     /* When hovering */
a:visited { color: purple; }           /* Visited links */
input:focus { border-color: green; }   /* When focused */
```

---

## 🎨 Colors

```css
color: red;                    /* Color name */
color: #FF0000;                /* Hex code */
color: rgb(255, 0, 0);         /* RGB */
color: rgba(255, 0, 0, 0.5);  /* RGB with transparency */
background: linear-gradient(to right, red, blue);  /* Gradient */
```

> Find colors at: https://coolors.co or https://colorhunt.co

---

## 📐 Box Model (Every element is a box)

```
┌─────────── Margin ───────────┐
│  ┌──────── Border ─────────┐ │
│  │  ┌───── Padding ──────┐ │ │
│  │  │  ┌── Content ───┐  │ │ │
│  │  │  │   Text/Image  │  │ │ │
│  │  │  └──────────────┘  │ │ │
│  │  └────────────────────┘ │ │
│  └────────────────────────┘  │
└──────────────────────────────┘
```

```css
/* Full example */
.box {
  width: 200px;
  height: 100px;
  margin: 20px;        /* Space OUTSIDE the element */
  border: 2px solid black;  /* Border around element */
  padding: 15px;       /* Space INSIDE the element */
  background: white;
}
```

---

## 📦 Display (How elements behave)

```css
display: block;         /* Takes full width, stacks vertically (div, p, h1) */
display: inline;        /* Sits in line with text (span, a, strong) */
display: inline-block;  /* Inline but can set width/height */
display: none;          /* Hidden — completely removed from page */
```

---

## 📏 Positioning

```css
position: static;       /* Default — follows page flow */
position: relative;     /* Move from its normal position */
position: absolute;     /* Position relative to nearest positioned parent */
position: fixed;        /* Stays in place even when scrolling */
position: sticky;       /* Normal until scroll, then sticks */
```

**Example (fixed navbar):**
```css
nav {
  position: fixed;
  top: 0;
  width: 100%;
  background: white;
  z-index: 100;  /* Stays above other content */
}
```

---

## 📊 Flexbox (Best for Layout)

```css
/* Parent container */
.container {
  display: flex;           /* Turn on flexbox */
  flex-direction: row;     /* row (default) or column */
  justify-content: center; /* Horizontal: flex-start, center, flex-end, space-between */
  align-items: center;     /* Vertical: flex-start, center, flex-end, stretch */
  gap: 20px;               /* Space between items */
  flex-wrap: wrap;         /* Wrap to new line if needed */
}

/* Child items */
.item {
  flex: 1;                 /* All items equal width */
  /* Or */
  flex: 0 0 300px;         /* Fixed width 300px */
}
```

---

## 📋 CSS Grid (Another Great Layout)

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;    /* 3 equal columns */
  /* Or */
  grid-template-columns: repeat(3, 1fr);  /* Same thing */
  gap: 20px;
}

/* Span multiple columns */
.item-big {
  grid-column: span 2;    /* Takes up 2 columns */
}
```

---

## 📱 Responsive Design (Mobile-Friendly)

```css
/* Add this to your HTML head */
/* <meta name="viewport" content="width=device-width, initial-scale=1.0"> */

/* Desktop first: override for mobile */
@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;  /* Stack on mobile */
  }
  h1 {
    font-size: 24px;             /* Smaller on mobile */
  }
}

/* Mobile first: override for desktop */
@media (min-width: 768px) {
  .container {
    grid-template-columns: 1fr 1fr;
  }
}
```

---

## ✨ Common Useful Styles

```css
/* Text */
text-align: center;       /* left, center, right */
font-weight: bold;        /* 400 = normal, 700 = bold */
font-family: Arial, sans-serif;
line-height: 1.6;         /* Space between lines */
text-decoration: none;    /* Remove underline from links */
text-transform: uppercase;  /* ALL CAPS */

/* Images */
img {
  max-width: 100%;        /* Image never exceeds its container */
  border-radius: 8px;     /* Rounded corners */
}

/* Shadows */
box-shadow: 2px 2px 10px rgba(0,0,0,0.1);  /* Box shadow */
text-shadow: 1px 1px 2px rgba(0,0,0,0.5);  /* Text shadow */

/* Rounded corners */
border-radius: 8px;       /* All corners */
border-radius: 50%;       /* Circle */

/* Transitions (smooth changes) */
button {
  transition: all 0.3s ease;
}
button:hover {
  transform: scale(1.1);  /* Grow on hover */
}
```

---

## 💡 Pro Tips

- Use `* { margin: 0; padding: 0; box-sizing: border-box; }` to reset default spacing
- Use **Flexbox** for 1D layouts (rows or columns)
- Use **Grid** for 2D layouts (rows AND columns)
- Always use `max-width: 100%` on images so they don't overflow
- Use Chrome DevTools (`F12`) → Elements → Styles to test CSS live
- Keep CSS in a separate `.css` file and link it: `<link rel="stylesheet" href="style.css">`
