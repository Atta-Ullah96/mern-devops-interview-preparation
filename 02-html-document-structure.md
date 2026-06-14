# HTML Document Structure

## Basic HTML Page

Every HTML page has a basic structure.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My First Page</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is my first webpage.</p>
  </body>
</html>
```

---

## What is `<!DOCTYPE html>`?

`<!DOCTYPE html>` tells the browser that this document uses modern HTML5.

It helps the browser render the page in standards mode.

```html
<!DOCTYPE html>
```

Without doctype, the browser may use old rendering behavior called quirks mode.

---

## What is `<html>`?

The `<html>` element is the root element of the document.

Everything on the page is inside this element.

```html
<html lang="en">
  ...
</html>
```

The `lang="en"` attribute tells browsers and screen readers that the page language is English.

---

## What is `<head>`?

The `<head>` contains information about the page.

This information is mostly not directly visible on the page.

Common things inside `<head>`:

- Page title
- Meta description
- Charset
- Viewport settings
- CSS links
- Favicon
- Open Graph tags
- Script links

Example:

```html
<head>
  <title>Storix - Secure File Storage</title>
  <meta name="description" content="Upload and manage your files securely." />
  <link rel="icon" href="/favicon.ico" />
</head>
```

---

## What is `<body>`?

The `<body>` contains the visible content of the page.

Example:

```html
<body>
  <h1>Welcome to Storix</h1>
  <p>Upload, preview, and manage your files securely.</p>
</body>
```

Most content that users see is inside the body.

---

## Common Head Tags

### Charset

```html
<meta charset="UTF-8" />
```

It tells the browser which character encoding to use.

### Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

It helps make the page responsive on mobile devices.

### Title

```html
<title>Storix</title>
```

It appears in the browser tab and search results.

### Description

```html
<meta name="description" content="Secure cloud file storage app." />
```

It helps search engines understand the page.

---

## Interview Answer

An HTML document has a basic structure with `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`. The doctype tells the browser to use modern HTML5. The `<html>` element is the root of the page. The `<head>` contains metadata like title, meta tags, CSS links, and favicon. The `<body>` contains the visible content that users see on the webpage.

---

## Common Interview Questions

1. What is the purpose of `<!DOCTYPE html>`?
2. What is the difference between `<head>` and `<body>`?
3. Why do we use `<meta charset="UTF-8">`?
4. Why is the viewport meta tag important?
5. What is the role of the `<title>` tag?

---

## What I Learned

- HTML has a required document structure.
- The head contains metadata.
- The body contains visible content.
- The doctype helps browsers use modern rendering.
- The viewport tag is important for responsive design.
