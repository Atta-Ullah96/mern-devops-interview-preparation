# Inline CSS, Internal CSS, and External CSS

There are three main ways to add CSS to an HTML page:

```txt
1. Inline CSS
2. Internal CSS
3. External CSS
```

## 1. Inline CSS

Inline CSS is written directly inside an HTML element using the `style` attribute.

Example:

```html
<h1 style="color: red; font-size: 40px;">Welcome to Storix</h1>
```

This style applies only to this specific `h1` element.

## When inline CSS is used

Inline CSS can be used for:

```txt
Quick testing
Email templates
Dynamic styles in React
One-time styles
```

Example in React:

```jsx
function Heading() {
  return <h1 style={{ color: "red", fontSize: "40px" }}>Welcome</h1>;
}
```

## Problems with inline CSS

Inline CSS is not recommended for large projects because:

```txt
It is not reusable.
It makes HTML messy.
It is hard to maintain.
It is hard to override.
It does not support pseudo-classes like :hover.
```

Bad example:

```html
<button style="background: blue; color: white; padding: 10px;">Login</button>
<button style="background: blue; color: white; padding: 10px;">Signup</button>
```

Better:

```css
.btn {
  background: blue;
  color: white;
  padding: 10px;
}
```

```html
<button class="btn">Login</button>
<button class="btn">Signup</button>
```

## 2. Internal CSS

Internal CSS is written inside a `<style>` tag, usually inside the `<head>`.

Example:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 {
        color: blue;
      }

      p {
        color: gray;
      }
    </style>
  </head>

  <body>
    <h1>Hello</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

## When internal CSS is used

Internal CSS can be used for:

```txt
Small pages
Practice examples
Single-page demos
Quick testing
```

## Problems with internal CSS

Internal CSS is not best for large websites because it is only available inside one HTML file.

Example problem:

```txt
index.html has same CSS
about.html has same CSS
contact.html has same CSS
```

If you want to update the style, you must edit every file.

## 3. External CSS

External CSS is written in a separate `.css` file and connected to HTML using the `<link>` tag.

Example file structure:

```txt
index.html
style.css
```

HTML:

```html
<link rel="stylesheet" href="style.css" />
```

CSS:

```css
h1 {
  color: green;
}

p {
  color: gray;
}
```

## Why external CSS is preferred

External CSS is best for real projects because:

```txt
It is reusable.
It keeps HTML clean.
It is easier to maintain.
It can be cached by the browser.
It is better for large projects.
It is better for teamwork.
```

## Real project example

In a real MERN or React project, we usually avoid inline CSS for normal styling.

Common approaches:

```txt
External CSS files
CSS Modules
Tailwind CSS
Styled Components
SCSS
Component libraries
```

## Interview answer

> Inline CSS is written inside an element using the `style` attribute and affects only that element. Internal CSS is written inside a `<style>` tag in the HTML file and affects that page. External CSS is written in a separate `.css` file and linked using the `<link>` tag. In real projects, external CSS is preferred because it is reusable, maintainable, cleaner, and cacheable by the browser.

## What I learned

- Inline CSS is specific to one element.
- Internal CSS is written inside the HTML file.
- External CSS is written in a separate CSS file.
- External CSS is best for real projects.
