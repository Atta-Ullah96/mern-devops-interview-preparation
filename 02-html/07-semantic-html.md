# Semantic HTML

## What is Semantic HTML?

Semantic HTML means using HTML tags that clearly describe the meaning and purpose of the content.

Simple meaning:

> Semantic HTML tells the browser, search engines, screen readers, and developers what each part of the page means.

---

## Non-Semantic Example

```html
<div>
  <div>Header</div>
  <div>Main Content</div>
  <div>Footer</div>
</div>
```

This works, but it does not clearly explain the purpose of each part.

---

## Semantic Example

```html
<header>
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
  </nav>
</header>

<main>
  <section>
    <h1>Welcome to Storix</h1>
    <p>Secure cloud file storage app.</p>
  </section>
</main>

<footer>
  <p>Copyright 2026 Storix</p>
</footer>
```

This is better because every section has meaning.

---

## Common Semantic Tags

### `<header>`

Represents the top section of a page or section.

```html
<header>
  <h1>Storix</h1>
</header>
```

### `<nav>`

Represents navigation links.

```html
<nav>
  <a href="/">Home</a>
  <a href="/pricing">Pricing</a>
</nav>
```

### `<main>`

Represents the main content of the page.

```html
<main>
  <h1>Dashboard</h1>
</main>
```

Usually, one page should have one main `<main>` element.

### `<section>`

Represents a section of related content.

```html
<section>
  <h2>Features</h2>
  <p>Upload and manage files securely.</p>
</section>
```

### `<article>`

Represents independent content that can stand alone.

Examples:

- Blog post
- News article
- Forum post
- Product card in some cases

```html
<article>
  <h2>How Cloud Storage Works</h2>
  <p>This article explains file storage.</p>
</article>
```

### `<aside>`

Represents side content.

Examples:

- Sidebar
- Related links
- Ads
- Extra information

```html
<aside>
  <h3>Related Articles</h3>
</aside>
```

### `<footer>`

Represents footer content.

```html
<footer>
  <p>Contact: support@storix.com</p>
</footer>
```

---

## Why is Semantic HTML Important?

Semantic HTML improves:

1. **Readability**: Developers understand the structure easily.
2. **SEO**: Search engines understand the page better.
3. **Accessibility**: Screen readers can navigate the page better.
4. **Maintainability**: Code becomes easier to update.
5. **Browser understanding**: Browser can understand the role of page sections.

---

## Semantic HTML in React

Even when using React, we should still write semantic HTML.

Bad:

```jsx
function Layout() {
  return (
    <div>
      <div>Navbar</div>
      <div>Content</div>
      <div>Footer</div>
    </div>
  );
}
```

Good:

```jsx
function Layout() {
  return (
    <>
      <header>Navbar</header>
      <main>Content</main>
      <footer>Footer</footer>
    </>
  );
}
```

---

## Interview Answer

Semantic HTML means using meaningful HTML tags like `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, and `<footer>` instead of using only `<div>` everywhere. It is important because it improves code readability, SEO, accessibility, and helps browsers and screen readers understand the structure of the page.

---

## Common Interview Questions

1. What is semantic HTML?
2. Why should we not use only `<div>` everywhere?
3. What is the difference between `<section>` and `<article>`?
4. Why is semantic HTML important for accessibility?
5. Can we use semantic HTML in React?

---

## What I Learned

- Semantic tags describe meaning.
- Semantic HTML improves SEO and accessibility.
- `<main>` is for main page content.
- `<article>` is for independent content.
- React apps should also use semantic HTML.
