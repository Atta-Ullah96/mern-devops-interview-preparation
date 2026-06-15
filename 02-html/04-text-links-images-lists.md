# Text, Links, Images, and Lists

## Headings

HTML has six heading levels.

```html
<h1>Main Heading</h1>
<h2>Section Heading</h2>
<h3>Subsection Heading</h3>
<h4>Small Heading</h4>
<h5>Smaller Heading</h5>
<h6>Smallest Heading</h6>
```

Important rules:

- Use headings for structure, not only for font size.
- Usually use one main `<h1>` per page.
- Keep heading order logical.

---

## Paragraphs

Paragraphs are used for normal text.

```html
<p>Storix helps users upload, preview, and manage files securely.</p>
```

---

## Text Formatting Tags

```html
<strong>Important text</strong>
<em>Emphasized text</em>
<mark>Highlighted text</mark>
<small>Small text</small>
```

`<strong>` means important content.

`<em>` means emphasized content.

---

## Links

Links are created with the `<a>` tag.

```html
<a href="https://google.com">Visit Google</a>
```

The `href` attribute stores the destination URL.

### Internal Link

```html
<a href="/about">About Us</a>
```

### External Link

```html
<a href="https://github.com">GitHub</a>
```

### Open Link in New Tab

```html
<a href="https://github.com" target="_blank" rel="noopener noreferrer">
  Open GitHub
</a>
```

`rel="noopener noreferrer"` improves security when opening external links in a new tab.

---

## Images

Images are created with the `<img>` tag.

```html
<img src="logo.png" alt="Storix logo" />
```

Important attributes:

- `src`: image path
- `alt`: image description
- `width`: image width
- `height`: image height

Example:

```html
<img src="profile.png" alt="User profile picture" width="200" height="200" />
```

The `alt` text is important for:

- Screen readers
- SEO
- Fallback text if image fails to load

---

## Unordered List

Used when order does not matter.

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

---

## Ordered List

Used when order matters.

```html
<ol>
  <li>Create account</li>
  <li>Login</li>
  <li>Upload file</li>
</ol>
```

---

## Description List

Used for terms and descriptions.

```html
<dl>
  <dt>HTML</dt>
  <dd>Structure of a webpage.</dd>

  <dt>CSS</dt>
  <dd>Styling of a webpage.</dd>
</dl>
```

---

## Interview Answer

HTML provides tags for structuring text and media. Headings define the page structure, paragraphs show normal text, links connect one page to another, images display media using `src` and `alt`, and lists organize related items. These elements help browsers, users, search engines, and screen readers understand the content.

---

## Common Interview Questions

1. Why should headings be used in correct order?
2. What is the purpose of the `href` attribute?
3. Why is `alt` important in images?
4. What is the difference between ordered and unordered lists?
5. Why should external links use `rel="noopener noreferrer"` with `target="_blank"`?

---

## What I Learned

- Headings create page structure.
- Links connect pages.
- Images need useful alt text.
- Lists organize related content.
- External links should be handled securely.
