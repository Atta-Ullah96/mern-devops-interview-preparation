# CSS Selectors

## What are CSS selectors?

CSS selectors are used to select HTML elements and apply styles to them.

Example:

```css
p {
  color: red;
}
```

Here `p` is the selector.

It means:

> Select all `<p>` elements and make their text red.

## 1. Element selector

Element selector selects HTML elements by tag name.

```css
h1 {
  color: blue;
}

p {
  font-size: 18px;
}
```

HTML:

```html
<h1>Title</h1>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
```

Both paragraphs will get `font-size: 18px`.

## 2. Class selector

Class selector uses dot `.`.

```css
.card {
  border: 1px solid gray;
  padding: 20px;
}
```

HTML:

```html
<div class="card">This is a card</div>
```

Class selectors are reusable.

```html
<div class="card">Card 1</div>
<div class="card">Card 2</div>
<div class="card">Card 3</div>
```

Most real projects use class selectors heavily.

## 3. ID selector

ID selector uses `#`.

```css
#main-title {
  color: purple;
}
```

HTML:

```html
<h1 id="main-title">Welcome</h1>
```

ID should usually be unique on a page.

In modern CSS, avoid using ID selectors too much for styling because ID has high specificity and can make CSS harder to override.

## 4. Universal selector

Universal selector selects all elements.

```css
* {
  box-sizing: border-box;
}
```

Common CSS reset:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

## 5. Group selector

Group selector applies the same style to multiple selectors.

```css
h1,
h2,
h3 {
  font-family: Arial, sans-serif;
}
```

## 6. Descendant selector

Descendant selector selects elements inside another element.

```css
.card p {
  color: gray;
}
```

HTML:

```html
<div class="card">
  <p>This paragraph is inside card.</p>
</div>

<p>This paragraph is outside card.</p>
```

Only the paragraph inside `.card` becomes gray.

## 7. Child selector

Child selector selects direct child elements only.

```css
.menu > li {
  color: blue;
}
```

HTML:

```html
<ul class="menu">
  <li>Home</li>
  <li>
    Services
    <ul>
      <li>Web Development</li>
    </ul>
  </li>
</ul>
```

Only direct `li` children of `.menu` are selected.

## 8. Attribute selector

Attribute selector selects elements based on an attribute.

```css
input[type="email"] {
  border: 1px solid blue;
}
```

HTML:

```html
<input type="email" />
<input type="password" />
```

Only the email input gets the blue border.

## 9. Pseudo-class selector

Pseudo-class selects a special state.

Example:

```css
button:hover {
  background-color: black;
  color: white;
}
```

More examples:

```css
input:focus {
  border-color: blue;
}

li:first-child {
  font-weight: bold;
}

li:last-child {
  color: red;
}
```

## 10. Pseudo-element selector

Pseudo-element styles a specific part of an element.

Example:

```css
p::first-letter {
  font-size: 40px;
}
```

Example:

```css
.card::before {
  content: "New";
}
```

Common pseudo-elements:

```txt
::before
::after
::first-letter
::first-line
::placeholder
```

## Interview answer

> CSS selectors are used to select HTML elements and apply styles to them. Common selectors include element selectors like `p`, class selectors like `.card`, ID selectors like `#main-title`, universal selectors, group selectors, descendant selectors, child selectors, attribute selectors, pseudo-classes like `:hover`, and pseudo-elements like `::before`.

## What I learned

- Selectors tell CSS which elements to style.
- Element selector selects by tag name.
- Class selector uses `.` and is reusable.
- ID selector uses `#` and should usually be unique.
- Pseudo-classes select states like hover and focus.
- Pseudo-elements style parts of elements.
