# Browser Parsing HTML

## What Happens After Browser Receives HTML?

When the browser receives an HTML response from the server, it starts reading and parsing the HTML.

The browser converts HTML text into a structure it can understand.

This structure is called the DOM.

---

## Browser Rendering Flow

```text
HTML received
↓
Parse HTML
↓
Create DOM
↓
Load and parse CSS
↓
Create CSSOM
↓
Combine DOM + CSSOM
↓
Create render tree
↓
Layout
↓
Paint
↓
User sees page
```

---

## Step 1: HTML is Received

The server sends HTML to the browser in the HTTP response.

Example response body:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Storix</title>
  </head>
  <body>
    <h1>Welcome to Storix</h1>
  </body>
</html>
```

---

## Step 2: Browser Creates DOM

DOM stands for **Document Object Model**.

DOM is a tree-like representation of the HTML document.

Example HTML:

```html
<body>
  <h1>Hello</h1>
  <p>Welcome</p>
</body>
```

DOM tree:

```text
body
├── h1
└── p
```

JavaScript can access and change the DOM.

---

## Step 3: Browser Loads CSS

The browser loads CSS files or reads CSS inside the HTML.

```html
<link rel="stylesheet" href="style.css" />
```

CSS is used to style the HTML elements.

---

## Step 4: Browser Creates CSSOM

CSSOM stands for **CSS Object Model**.

It is a tree-like structure of CSS styles.

The browser uses CSSOM to know how each element should look.

---

## Step 5: Render Tree

The browser combines DOM and CSSOM to create the render tree.

The render tree contains only visible elements.

For example, elements with `display: none` are usually not included in the render tree.

---

## Step 6: Layout

Layout means calculating the size and position of each visible element.

The browser calculates:

- Width
- Height
- Position
- Spacing

---

## Step 7: Paint

Paint means drawing pixels on the screen.

The browser paints:

- Text
- Colors
- Borders
- Images
- Shadows

---

## Step 8: JavaScript Execution

JavaScript can change the DOM and CSSOM.

Example:

```js
document.querySelector("h1").textContent = "Hello Storix";
```

When JavaScript changes the DOM or styles, the browser may need to recalculate layout and repaint the page.

---

## Why This Matters for Developers

Understanding browser parsing helps with:

- Performance optimization
- Avoiding blocking scripts
- Understanding DOM
- Improving page load speed
- Debugging rendering issues

---

## Interview Answer

When the browser receives HTML, it parses the HTML and creates the DOM. Then it loads and parses CSS to create the CSSOM. The browser combines DOM and CSSOM to create the render tree. After that, it calculates layout, paints pixels on the screen, and displays the page to the user. JavaScript can also run and modify the DOM, which may cause the browser to update the page again.

---

## Common Interview Questions

1. What is the DOM?
2. What is CSSOM?
3. What is the render tree?
4. What is the difference between layout and paint?
5. How can JavaScript affect rendering?

---

## What I Learned

- Browser converts HTML into DOM.
- CSS becomes CSSOM.
- DOM and CSSOM create render tree.
- Layout calculates positions and sizes.
- Paint draws content on screen.
