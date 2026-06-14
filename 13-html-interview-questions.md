# HTML Interview Questions

## Beginner Questions

### 1. What is HTML?

HTML stands for HyperText Markup Language. It is used to create the structure of webpages using tags, elements, and attributes.

### 2. Is HTML a programming language?

No. HTML is not a programming language. It is a markup language because it marks content using tags.

### 3. What is the difference between a tag and an element?

A tag is the keyword inside angle brackets, like `<p>`. An element is the complete structure, like `<p>Hello</p>`.

### 4. What is an attribute?

An attribute gives extra information to an element, like `href` in an anchor tag or `src` in an image tag.

### 5. What is the difference between `<head>` and `<body>`?

The `<head>` contains metadata about the page, such as title, meta tags, CSS links, and favicon. The `<body>` contains visible content displayed to the user.

---

## Intermediate Questions

### 6. What is semantic HTML?

Semantic HTML means using meaningful tags like `<header>`, `<main>`, `<section>`, `<article>`, `<nav>`, and `<footer>` to describe page structure.

### 7. Why is semantic HTML important?

It improves readability, SEO, accessibility, and helps browsers and screen readers understand the page structure.

### 8. What is the difference between `<section>` and `<article>`?

`<section>` is used for a related section of content. `<article>` is used for independent content that can stand alone, like a blog post or news article.

### 9. What is the purpose of the `alt` attribute?

The `alt` attribute provides alternative text for images. It helps screen readers, SEO, and users when images fail to load.

### 10. What is the purpose of labels in forms?

Labels describe inputs and improve accessibility. They help screen readers and allow users to click the label to focus the input.

---

## SEO and Accessibility Questions

### 11. What is SEO in HTML?

SEO means helping search engines understand a webpage using proper title tags, meta descriptions, headings, links, semantic HTML, and alt text.

### 12. What are Open Graph tags?

Open Graph tags control how a webpage appears when shared on platforms like Facebook, LinkedIn, and WhatsApp.

### 13. What is a favicon?

A favicon is the small icon displayed in the browser tab.

### 14. What is ARIA?

ARIA stands for Accessible Rich Internet Applications. It adds extra accessibility information when normal HTML is not enough.

### 15. Should we use ARIA everywhere?

No. First prefer semantic HTML. Use ARIA only when normal HTML cannot describe the behavior properly.

---

## Advanced Questions

### 16. What is the difference between `async` and `defer`?

`defer` downloads JavaScript while HTML is parsing and runs it after HTML parsing is complete. It preserves script order. `async` downloads JavaScript while HTML is parsing but runs it as soon as it downloads, so order is not guaranteed.

### 17. What happens when the browser parses HTML?

The browser parses HTML and creates the DOM. It also loads CSS and creates CSSOM. Then it combines DOM and CSSOM into the render tree, calculates layout, paints pixels, and displays the page.

### 18. What is DOM?

DOM stands for Document Object Model. It is a tree-like representation of the HTML document that JavaScript can read and modify.

### 19. Why is the viewport meta tag important?

The viewport meta tag helps the webpage display properly on mobile devices by controlling layout width and scale.

### 20. Why should we not use tables for layout?

Tables should be used for tabular data only. Using tables for layout makes the page less semantic, harder to maintain, and worse for accessibility.

---

## Practice Task

Answer these without looking:

1. Explain HTML history in your own words.
2. Explain tag, element, and attribute with examples.
3. Explain semantic HTML with examples.
4. Explain SEO tags in HTML.
5. Explain browser parsing HTML.
