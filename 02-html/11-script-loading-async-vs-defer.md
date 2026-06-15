# Script Loading: async vs defer

## Why Script Loading Matters

JavaScript can block HTML parsing.

If the browser finds a normal script tag, it may stop parsing HTML, download the JavaScript file, execute it, and then continue parsing.

This can slow down page loading.

---

## Normal Script

```html
<script src="app.js"></script>
```

Behavior:

1. Browser parses HTML.
2. Browser finds script.
3. Browser pauses HTML parsing.
4. Browser downloads script.
5. Browser executes script.
6. Browser continues parsing HTML.

This can block rendering.

---

## defer

```html
<script src="app.js" defer></script>
```

Behavior:

1. Browser downloads script while HTML is still parsing.
2. Browser does not block HTML parsing.
3. Script runs after HTML parsing is complete.
4. Deferred scripts execute in order.

Use `defer` for scripts that need the DOM.

Example:

```html
<script src="main.js" defer></script>
```

---

## async

```html
<script src="analytics.js" async></script>
```

Behavior:

1. Browser downloads script while HTML is parsing.
2. Browser runs script as soon as it is downloaded.
3. HTML parsing may pause when script executes.
4. Execution order is not guaranteed.

Use `async` for independent scripts.

Examples:

- Analytics scripts
- Ads scripts
- Tracking scripts
- Third-party widgets

---

## Difference Between async and defer

| Feature | defer | async |
|---|---|---|
| Downloads while parsing HTML | Yes | Yes |
| Blocks HTML parsing while downloading | No | No |
| Executes after HTML parsing | Yes | Not always |
| Execution order guaranteed | Yes | No |
| Best for | Main app scripts | Independent scripts |

---

## Simple Rule

Use `defer` for your main JavaScript files.

Use `async` for scripts that do not depend on your HTML or other scripts.

---

## Example

```html
<head>
  <script src="main.js" defer></script>
  <script src="analytics.js" async></script>
</head>
```

Here:

- `main.js` runs after HTML parsing.
- `analytics.js` runs whenever it finishes downloading.

---

## Interview Answer

Normal script loading can block HTML parsing. The `defer` attribute downloads JavaScript in parallel while HTML is parsing and executes it after the HTML document is fully parsed. Deferred scripts execute in order. The `async` attribute also downloads JavaScript in parallel, but executes the script as soon as it downloads, so execution order is not guaranteed. `defer` is usually better for main app scripts, while `async` is useful for independent scripts like analytics.

---

## Common Interview Questions

1. Why can JavaScript block page loading?
2. What does `defer` do?
3. What does `async` do?
4. What is the main difference between `async` and `defer`?
5. Which one should we use for analytics scripts?

---

## What I Learned

- Normal scripts can block HTML parsing.
- `defer` runs after HTML parsing.
- `async` runs as soon as it downloads.
- `defer` preserves order.
- `async` does not guarantee order.
