# SEO, Meta Tags, Open Graph, and Favicon

## What is SEO?

SEO stands for **Search Engine Optimization**.

SEO means improving a page so search engines can understand it and show it properly in search results.

HTML plays an important role in SEO because search engines read HTML structure, headings, links, meta tags, and content.

---

## Important SEO Tags

### Title Tag

The title tag appears in the browser tab and search results.

```html
<title>Storix - Secure Cloud File Storage</title>
```

Good title should be:

- Clear
- Relevant
- Not too long
- Related to the page content

---

## Meta Description

The meta description explains the page.

```html
<meta
  name="description"
  content="Storix helps users upload, preview, and manage files securely."
/>
```

Search engines may show it under the title in search results.

---

## Heading Structure

Headings help users and search engines understand page hierarchy.

```html
<h1>Secure Cloud File Storage</h1>
<h2>Upload Files</h2>
<h2>Preview Files</h2>
<h2>Manage Files</h2>
```

Important:

- Use one main `<h1>` for the main page topic.
- Use `<h2>` for main sections.
- Do not skip heading levels unnecessarily.

---

## Image Alt Text

Alt text helps search engines and screen readers understand images.

```html
<img src="dashboard.png" alt="Storix dashboard showing uploaded files" />
```

---

## Open Graph Tags

Open Graph tags control how a page appears when shared on platforms like Facebook, LinkedIn, WhatsApp, and X.

Example:

```html
<meta property="og:title" content="Storix Cloud Storage" />
<meta property="og:description" content="Securely upload and manage your files." />
<meta property="og:image" content="https://storix.com/preview.png" />
<meta property="og:url" content="https://storix.com" />
<meta property="og:type" content="website" />
```

---

## Twitter/X Card Tags

```html
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Storix Cloud Storage" />
<meta name="twitter:description" content="Securely upload and manage your files." />
<meta name="twitter:image" content="https://storix.com/preview.png" />
```

---

## Favicon

A favicon is the small icon shown in the browser tab.

```html
<link rel="icon" href="/favicon.ico" />
```

You can also use PNG or SVG:

```html
<link rel="icon" type="image/png" href="/favicon.png" />
```

---

## SEO with Semantic HTML

Semantic HTML helps SEO because it makes the page structure clear.

Example:

```html
<main>
  <article>
    <h1>How Secure Cloud Storage Works</h1>
    <p>This article explains secure file storage.</p>
  </article>
</main>
```

Search engines can better understand what the main content is.

---

## Interview Answer

HTML supports SEO through title tags, meta descriptions, heading structure, semantic HTML, links, image alt text, and metadata. Open Graph tags control how a page appears when shared on social platforms, and favicon defines the small browser tab icon. Good HTML structure helps search engines understand and rank the page better.

---

## Common Interview Questions

1. What is SEO?
2. What is the purpose of the title tag?
3. What is a meta description?
4. What are Open Graph tags?
5. Why is alt text important for SEO?
6. What is a favicon?

---

## What I Learned

- SEO helps search engines understand pages.
- Title and description are important for search results.
- Open Graph controls social sharing previews.
- Favicon is the browser tab icon.
- Semantic HTML improves SEO.
