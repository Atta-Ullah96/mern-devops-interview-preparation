# CSS History and Why CSS Was Created

## What is CSS?

CSS stands for **Cascading Style Sheets**.

CSS is used to style HTML pages.

Simple meaning:

> HTML creates the structure of a webpage, and CSS controls the visual design of that webpage.

Example:

```html
<h1>Welcome to Storix</h1>
<p>Secure cloud file storage app.</p>
```

```css
h1 {
  color: blue;
  font-size: 40px;
}

p {
  color: gray;
}
```

## HTML vs CSS vs JavaScript

```txt
HTML       = structure/content
CSS        = design/layout
JavaScript = behavior/interactivity
```

Example:

```txt
HTML says: This is a button.
CSS says: The button should be blue and rounded.
JavaScript says: When the button is clicked, submit the form.
```

## The early web problem

In the beginning, the web was mostly used for documents. HTML was created to describe content like headings, paragraphs, lists, and links.

But when websites became more popular, developers wanted better design:

```txt
Colors
Fonts
Spacing
Layouts
Borders
Backgrounds
Alignment
```

Before CSS, developers started using HTML for styling also.

Example of old HTML styling:

```html
<font color="red" size="5">Welcome to my website</font>
```

Developers also used tables for page layout:

```html
<table>
  <tr>
    <td>Sidebar</td>
    <td>Main Content</td>
  </tr>
</table>
```

This made websites hard to maintain.

## Main problem before CSS

HTML was doing two jobs:

```txt
1. Content and structure
2. Styling and design
```

This created messy code.

Imagine you have 100 pages and every heading is styled like this:

```html
<font color="blue" size="6">Heading</font>
```

Now the client says:

> Change all headings from blue to red.

Without CSS, you would need to edit many HTML files manually.

With CSS, you can write:

```css
h1 {
  color: red;
}
```

Now all `h1` headings can update from one place.

## Why CSS was created

CSS was created to separate **content** from **presentation**.

Meaning:

```txt
HTML handles content and structure.
CSS handles design and styling.
```

## Benefits of CSS

### 1. Cleaner code

Bad:

```html
<h1 style="color: red; font-size: 40px;">Hello</h1>
```

Better:

```html
<h1>Hello</h1>
```

```css
h1 {
  color: red;
  font-size: 40px;
}
```

### 2. Reusable styles

One CSS class can be reused many times.

```css
.btn {
  background: blue;
  color: white;
  padding: 10px 16px;
}
```

```html
<button class="btn">Login</button>
<button class="btn">Signup</button>
```

### 3. Easy maintenance

If you want to change all buttons, change only the CSS file.

### 4. Better performance

External CSS files can be cached by the browser.

```txt
First visit: Browser downloads CSS.
Next visit: Browser can reuse cached CSS.
```

### 5. Better teamwork

One developer can work on HTML/React components, and another developer can work on styling.

## What does Cascading mean?

Cascading means the browser decides which CSS rule wins when multiple rules apply to the same element.

Example:

```css
p {
  color: blue;
}

p {
  color: red;
}
```

```html
<p>Hello World</p>
```

Final color will be `red` because the second rule comes later.

But cascade is not only about order. It depends on:

```txt
1. Importance
2. Specificity
3. Source order
4. Inheritance
```

## Interview answer

> CSS stands for Cascading Style Sheets. It was created to separate webpage structure from design. In the early web, developers used HTML tags like `font` and tables for styling and layout, which made websites messy and hard to maintain. CSS solved this problem by allowing developers to write styles separately and reuse them across multiple pages. CSS makes code cleaner, easier to maintain, more reusable, and better for performance.

## What I learned

- CSS is used to style HTML pages.
- HTML should handle structure, CSS should handle design.
- CSS was created because styling inside HTML became messy.
- External CSS makes code reusable and maintainable.
- Cascading means the browser decides which CSS rule wins.
