# HTML Cheat Sheet

## Basic Structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Page Title</title>
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
</html>
```

## Text

```html
<h1>Main Heading</h1>
<h2>Section Heading</h2>
<p>Paragraph text</p>
<strong>Important</strong>
<em>Emphasis</em>
```

## Links and Images

```html
<a href="https://example.com">Visit Example</a>
<img src="image.png" alt="Image description" />
```

## Lists

```html
<ul>
  <li>Item</li>
</ul>

<ol>
  <li>First step</li>
</ol>
```

## Table

```html
<table>
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Role</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ali</td>
      <td>Developer</td>
    </tr>
  </tbody>
</table>
```

## Form

```html
<form>
  <label for="email">Email</label>
  <input id="email" name="email" type="email" required />

  <button type="submit">Submit</button>
</form>
```

## Semantic Tags

```html
<header></header>
<nav></nav>
<main></main>
<section></section>
<article></article>
<aside></aside>
<footer></footer>
```

## SEO Tags

```html
<title>Page Title</title>
<meta name="description" content="Page description" />
```

## Open Graph

```html
<meta property="og:title" content="Page Title" />
<meta property="og:description" content="Page description" />
<meta property="og:image" content="https://example.com/image.png" />
<meta property="og:url" content="https://example.com" />
```

## Favicon

```html
<link rel="icon" href="/favicon.ico" />
```

## Accessibility

```html
<label for="name">Name</label>
<input id="name" name="name" type="text" />

<img src="logo.png" alt="Company logo" />
<button aria-label="Close menu">X</button>
```

## Form Validation

```html
<input type="email" required />
<input type="password" minlength="8" required />
<input type="number" min="1" max="100" />
```

## Script Loading

```html
<script src="main.js" defer></script>
<script src="analytics.js" async></script>
```

## Quick Interview Answer

HTML is the foundation of webpages. It structures content using tags, elements, and attributes. HTML supports text, links, images, tables, forms, semantic structure, SEO, accessibility, and script loading. The browser parses HTML and creates the DOM, which is then rendered on the screen.
