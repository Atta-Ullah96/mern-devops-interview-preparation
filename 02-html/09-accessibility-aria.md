# Accessibility and ARIA Basics

## What is Accessibility?

Accessibility means making websites usable for everyone, including people with disabilities.

A website should be usable by people who:

- Use screen readers
- Use keyboard navigation
- Have low vision
- Have color blindness
- Cannot use a mouse
- Use assistive technologies

---

## Why Accessibility Matters

Accessibility improves:

- User experience
- Inclusiveness
- SEO
- Code quality
- Legal compliance in many countries

Good accessibility also makes websites easier for everyone to use.

---

## Accessibility Basics in HTML

### Use Semantic HTML

Good:

```html
<button>Submit</button>
<nav>Navigation links</nav>
<main>Main content</main>
```

Bad:

```html
<div onclick="submitForm()">Submit</div>
```

Use the correct HTML element for the job.

---

## Use Labels with Inputs

Good:

```html
<label for="email">Email</label>
<input id="email" type="email" />
```

Bad:

```html
<input type="email" placeholder="Email" />
```

Placeholder is not a replacement for label.

---

## Use Alt Text for Images

```html
<img src="logo.png" alt="Storix company logo" />
```

If the image is decorative, alt can be empty:

```html
<img src="decorative-line.png" alt="" />
```

---

## Buttons vs Links

Use button for actions.

```html
<button type="button">Open Modal</button>
```

Use link for navigation.

```html
<a href="/dashboard">Go to Dashboard</a>
```

---

## Keyboard Accessibility

Users should be able to use the website with keyboard.

Important keys:

- Tab
- Shift + Tab
- Enter
- Space
- Escape

HTML buttons and links support keyboard behavior by default.

---

## What is ARIA?

ARIA stands for **Accessible Rich Internet Applications**.

ARIA adds extra accessibility information when normal HTML is not enough.

Example:

```html
<button aria-label="Close menu">X</button>
```

Here screen readers can announce this as "Close menu" instead of just "X".

---

## Important ARIA Rule

First prefer semantic HTML.

Use ARIA only when needed.

Bad:

```html
<div role="button">Submit</div>
```

Better:

```html
<button>Submit</button>
```

---

## Common ARIA Attributes

### `aria-label`

Gives an accessible label.

```html
<button aria-label="Close modal">X</button>
```

### `aria-hidden`

Hides decorative content from screen readers.

```html
<span aria-hidden="true">★</span>
```

### `aria-expanded`

Shows whether a menu is open or closed.

```html
<button aria-expanded="false">Menu</button>
```

---

## Interview Answer

Accessibility means making a website usable for all users, including users with disabilities. In HTML, accessibility is improved by using semantic tags, proper labels for inputs, alt text for images, keyboard-friendly controls, and correct heading structure. ARIA provides extra information to assistive technologies, but semantic HTML should be preferred first.

---

## Common Interview Questions

1. What is web accessibility?
2. Why are labels important for forms?
3. What is the purpose of alt text?
4. What is ARIA?
5. Why should semantic HTML be preferred over ARIA?
6. What is the difference between a button and a link?

---

## What I Learned

- Accessibility makes websites usable for everyone.
- Semantic HTML improves accessibility.
- Labels are important for inputs.
- Alt text helps screen readers.
- ARIA should be used only when normal HTML is not enough.
