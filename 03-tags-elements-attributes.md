# Tags, Elements, and Attributes

## What is a Tag?

A tag is an HTML keyword written inside angle brackets.

Example:

```html
<p>
```

`<p>` is a paragraph tag.

Most tags have an opening tag and closing tag.

```html
<p>This is a paragraph.</p>
```

---

## What is an Element?

An element is the complete HTML structure including:

- Opening tag
- Content
- Closing tag

Example:

```html
<h1>Welcome to Storix</h1>
```

Here the full line is an HTML element.

---

## What is an Attribute?

An attribute gives extra information to an HTML element.

Example:

```html
<a href="https://google.com">Visit Google</a>
```

Here:

- `href` is the attribute name.
- `https://google.com` is the attribute value.

Another example:

```html
<img src="logo.png" alt="Company logo" />
```

Here:

- `src` gives the image path.
- `alt` gives image description.

---

## Opening and Closing Tags

Some elements need opening and closing tags.

```html
<p>This is a paragraph.</p>
```

Some elements are void elements. They do not need closing tags.

Examples:

```html
<img src="logo.png" alt="Logo" />
<br />
<hr />
<input type="text" />
```

---

## Common Attributes

### `id`

Unique identifier for an element.

```html
<h1 id="main-title">Storix</h1>
```

### `class`

Used to group elements for CSS or JavaScript.

```html
<p class="description">Secure file storage app.</p>
```

### `href`

Used in links.

```html
<a href="/about">About</a>
```

### `src`

Used for images, scripts, videos, and other external resources.

```html
<img src="logo.png" alt="Logo" />
```

### `alt`

Alternative text for images.

```html
<img src="user.png" alt="User profile picture" />
```

### `type`

Used for inputs and buttons.

```html
<input type="email" />
<button type="submit">Submit</button>
```

---

## Interview Answer

A tag is an HTML keyword inside angle brackets, like `<p>`. An element is the complete structure that includes the opening tag, content, and closing tag, like `<p>Hello</p>`. An attribute provides extra information to an element, like `href` in an anchor tag or `src` and `alt` in an image tag.

---

## Common Interview Questions

1. What is the difference between a tag and an element?
2. What is an HTML attribute?
3. What is the difference between `id` and `class`?
4. Why is the `alt` attribute important?
5. What are void elements?

---

## What I Learned

- Tags are HTML keywords.
- Elements are complete HTML structures.
- Attributes provide extra information.
- Some HTML elements are void elements.
- `alt` is important for accessibility and SEO.
