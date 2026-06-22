# Pseudo Elements in CSS

## Simple Explanation

Pseudo elements are used to style a specific part of an element or create extra visual content using CSS.

Pseudo classes usually use one colon:

```css
button:hover {
  background-color: black;
}
```

Pseudo elements usually use double colon:

```css
.title::after {
  content: "";
}
```

## Why Pseudo Elements Are Important

Pseudo elements are useful for:

- Adding decorative icons
- Creating underline effects
- Styling placeholders
- Styling first letters or first lines
- Adding badges without extra HTML
- Creating UI effects with less markup

## Common Pseudo Elements

### `::before`

Adds content before an element's content.

```css
.badge::before {
  content: "★ ";
  color: gold;
}
```

### `::after`

Adds content after an element's content.

```css
.badge::after {
  content: " New";
  color: red;
}
```

### `::first-letter`

Styles the first letter of text.

```css
p::first-letter {
  font-size: 40px;
  font-weight: bold;
}
```

### `::first-line`

Styles the first line of text.

```css
p::first-line {
  color: blue;
}
```

### `::placeholder`

Styles input placeholder text.

```css
input::placeholder {
  color: #9ca3af;
}
```

## Practical Example: Link Underline Animation

```css
.nav-link {
  position: relative;
  color: #111827;
  text-decoration: none;
}

.nav-link::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -4px;
  width: 0;
  height: 2px;
  background-color: #2563eb;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}
```

## Difference Between Pseudo Classes and Pseudo Elements

| Pseudo Class | Pseudo Element |
|---|---|
| Styles element state or position | Styles part of an element |
| Uses `:` | Usually uses `::` |
| Example: `:hover` | Example: `::before` |
| Example: `:focus` | Example: `::after` |

## Interview Answer

Pseudo elements are used to style specific parts of an element or insert visual content through CSS. Common pseudo elements are `::before`, `::after`, `::first-letter`, `::first-line`, and `::placeholder`.
