# Pseudo Classes in CSS

## Simple Explanation

Pseudo classes are used to style an element based on its state, position, or condition.

A normal class selects an element by class name:

```css
.button {
  background-color: blue;
}
```

A pseudo class selects an element when it is in a special state:

```css
.button:hover {
  background-color: black;
}
```

Here `:hover` applies only when the user moves the mouse over the button.

## Why Pseudo Classes Are Important

Pseudo classes help us create interactive UI without JavaScript.

They are commonly used for:

- Button hover effects
- Input focus states
- Active links
- Disabled buttons
- First or last child styling
- Table row styling
- Form validation states

## Common Pseudo Classes

### `:hover`

Used when user moves mouse over an element.

```css
.card:hover {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
}
```

### `:focus`

Used when an input, button, or link is focused.

```css
input:focus {
  border-color: #2563eb;
  outline: none;
}
```

This is very important for forms and accessibility.

### `:active`

Used while the user is clicking an element.

```css
button:active {
  transform: scale(0.97);
}
```

### `:disabled`

Used for disabled buttons or inputs.

```css
button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
```

### `:first-child`

Selects the first child element.

```css
li:first-child {
  font-weight: bold;
}
```

### `:last-child`

Selects the last child element.

```css
li:last-child {
  color: red;
}
```

### `:nth-child()`

Selects elements based on their position.

```css
li:nth-child(2) {
  color: blue;
}
```

Select even table rows:

```css
tr:nth-child(even) {
  background-color: #f9fafb;
}
```

Select odd table rows:

```css
tr:nth-child(odd) {
  background-color: white;
}
```

## Real Project Example

```css
.button {
  background-color: #2563eb;
  color: white;
  padding: 12px 18px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

.button:hover {
  background-color: #1d4ed8;
}

.button:active {
  transform: scale(0.97);
}

.button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
```

## Interview Answer

Pseudo classes are used to style elements based on state or position. Examples include `:hover`, `:focus`, `:active`, `:disabled`, `:first-child`, `:last-child`, and `:nth-child`. They help create interactive UI without JavaScript.

## Common Interview Questions

1. What are pseudo classes?
2. What is the difference between `:hover` and `:focus`?
3. What is `:nth-child()` used for?
4. Why is `:focus` important for accessibility?
5. Can pseudo classes create interactivity without JavaScript?
